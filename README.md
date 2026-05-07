<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>Abdul & Syahrillah</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    background:#0b141a;
    font-family:'Poppins',sans-serif;
    display:flex;
    justify-content:center;
    align-items:center;
    min-height:100vh;
    overflow:hidden;
}

.phone{
    width:390px;
    height:800px;
    background:#111b21;
    overflow:hidden;
    position:relative;
}

.header{
    height:72px;
    background:#202c33;
    display:flex;
    align-items:center;
    padding:15px;
    color:white;
    position:sticky;
    top:0;
}

.profile{
    width:45px;
    height:45px;
    border-radius:50%;
    background:#2a3942;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:22px;
    margin-right:12px;
}

.name{
    font-size:16px;
    font-weight:600;
}

.status{
    font-size:12px;
    color:#8696a0;
}

.chat-area{
    height:calc(100% - 72px);
    padding:20px 12px 100px;
    overflow-y:auto;
    background-image:url('https://i.imgur.com/6Iej2c3.png');
    background-size:cover;
}

.message{
    max-width:75%;
    padding:10px 14px;
    border-radius:12px;
    margin-bottom:12px;
    line-height:1.4;
    font-size:14px;
    display:none;
    animation:fadeIn .3s ease;
}

.sent{
    background:#005c4b;
    color:white;
    margin-left:auto;
    border-top-right-radius:4px;
}

.received{
    background:#202c33;
    color:white;
    border-top-left-radius:4px;
}

.typing{
    width:70px;
    background:#202c33;
    padding:12px;
    border-radius:12px;
    display:none;
    margin-bottom:12px;
}

.dot{
    width:8px;
    height:8px;
    background:#8696a0;
    border-radius:50%;
    display:inline-block;
    animation:blink 1.2s infinite;
}

.dot:nth-child(2){
    animation-delay:.2s;
}

.dot:nth-child(3){
    animation-delay:.4s;
}

.invitation{
    display:none;
    background:white;
    color:#111;
    padding:25px;
    border-radius:20px;
    margin-top:30px;
    text-align:center;
    line-height:1.8;
    animation:fadeIn 1s ease;
}

.invitation h1{
    margin-bottom:10px;
    font-size:28px;
}

.heart{
    font-size:30px;
    margin-bottom:15px;
}

@keyframes blink{
    0%{opacity:.2}
    20%{opacity:1}
    100%{opacity:.2}
}

@keyframes fadeIn{
    from{
        opacity:0;
        transform:translateY(10px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

</style>
</head>

<body>

<div class="phone">

    <div class="header">
        <div class="profile">💍</div>

        <div>
            <div class="name">Syahrillah ❤️</div>
            <div class="status">online</div>
        </div>
    </div>

    <div class="chat-area" id="chatArea">

        <div class="message sent">kamu tidur?</div>

        <div class="typing" id="typing1">
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
        </div>

        <div class="message received">belum hehe, kenapa?</div>

        <div class="message sent">aku lagi mikir sesuatu</div>

        <div class="typing" id="typing2">
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
        </div>

        <div class="message received">serius amat 😭</div>

        <div class="message sent">kita udah lama ya ternyata</div>

        <div class="message received">iyaa 🥺</div>

        <div class="message sent">makasih udah selalu ada</div>

        <div class="typing" id="typing3">
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
        </div>

        <div class="message received">jadi terharu :(</div>

        <div class="message sent">jadi...</div>

        <div class="message sent">lanjut hidup bareng yuk</div>

        <div class="typing" id="typing4">
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
        </div>

        <div class="message received">ke pelaminan?</div>

        <div class="message sent">iya 🤍</div>

        <div class="invitation" id="invite">

            <div class="heart">🤍</div>

            <h1>Abdul & Syahrillah</h1>

            Dengan penuh kebahagiaan,<br>
            kami mengundang Anda untuk hadir<br>
            di hari pernikahan kami.

            <br><br>

            <strong>Selasa, 20 Juli 2027</strong><br>
            15.00 WIB

            <br><br>

            📍 Kediaman Mempelai Wanita (Sonosari, Pakisaji, Malang)

            <br><br>

            “And suddenly,<br>
            all the love songs were about you.”
        </div>

    </div>

</div>

<script>

const messages = document.querySelectorAll('.message');
const typings = document.querySelectorAll('.typing');
const invite = document.getElementById('invite');
const chatArea = document.getElementById('chatArea');

let delay = 1000;

messages.forEach((msg, index) => {

    setTimeout(() => {
        msg.style.display = 'block';
        chatArea.scrollTop = chatArea.scrollHeight;
    }, delay);

    delay += 1800;

    if(typings[index]){
        setTimeout(() => {
            typings[index].style.display = 'block';
            chatArea.scrollTop = chatArea.scrollHeight;
        }, delay - 900);

        setTimeout(() => {
            typings[index].style.display = 'none';
        }, delay);
    }

});

setTimeout(() => {
    invite.style.display = 'block';
    chatArea.scrollTop = chatArea.scrollHeight;
}, delay + 1000);

</script>

</body>
</html>
