
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>𝙏𝙧𝙖𝙣𝙨𝙡𝙖𝙩𝙚 𝙏𝙝𝙚𝙣 𝘽𝙚 𝙈𝙮 𝙇𝙤𝙫𝙚𝙧</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: radial-gradient(circle, #ff9eb5, #ff86a0, #ffc1cc);
            font-family: 'Poppins', sans-serif;
            height: 90%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #fff;
            text-align: center;
            position: relative;
            padding-top: 40px;
        }

        .container {
            text-align: center;
            width: 80%;
            padding: 20px;
            border-radius: 30px;
            background: rgba(255, 255, 255, 0.1);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
        }

        h1 {
            font-size: 40px;
            color: #ff557a;
            text-transform: uppercase;
            margin-bottom: 30px;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
        }

        .btn {
            text-decoration: none;
            display: inline-block;
            padding: 15px 30px;
            background: #ff557a;
            color: white;
            font-size: 20px;
            font-weight: bold;
            border-radius: 50px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
            transition: transform 0.1s, box-shadow 0.1s;
            cursor: pointer;
        }

        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            justify-content: center;
            align-items: center;
            animation: fadeIn 0.5s ease-out;
        }

        .modal-content {
            background: #fff;
            padding: 20px;
            border-radius: 15px;
            width: 350px;
            text-align: center;
            color: #333;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }

        .modal-content img {
            display: block;
            width: 100%;
            height: auto;
            border-radius: 10px;
            margin-bottom: 20px;
        }

        .modal-content h2 {
            margin-bottom: 15px;
            color: #ff557a;
            font-size: 38px;
        }

        .modal-content p {
            font-size: 8px;
            line-height: 2.6;
            color: #4a4a4a;
        }

        .close-btn {
            background-color: #ff557a;
            padding: 12px 25px;
            color: white;
            font-size: 18px;
            border: none;
            border-radius: 20px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .close-btn:hover {
            background-color: #ff3366;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Cậu Gì Ơi Bấm Nút Bên Dưới Đi ❤</h1>
        <button class="btn" onclick="openModal()">Bấm Vô Đây Nè 😮</button>
    </div>

    <div class="modal" id="modal">
        <div class="modal-content">
            <img src="https://i.imgur.com/Iuel994.jpeg" alt="Gà Nhỏ 😮">
            <h2>𝙂𝙖 𝘾𝙤𝙣 🐤</h2>
            <p>𝙄 𝙡𝙤𝙫𝙚 𝙮𝙤𝙪 𝙫𝙚𝙧𝙮 𝙢𝙪𝙘𝙝</p>
            <button class="close-btn" onclick="closeModal()">𝙇𝙊𝙑𝙀 𝙔𝙊𝙐 ❤</button>
        </div>
    </div>

    <iframe 
        id="youtube-player" 
        width="0" 
        height="0" 
        src="https://www.youtube.com/embed/AxmH62TfXFw?autoplay=1&loop=1&playlist=AxmH62TfXFw" 
        frameborder="0" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>

    <script>
        function openModal() {
            const modal = document.getElementById('modal');
            modal.style.display = 'flex';
        }

        function closeModal() {
            const modal = document.getElementById('modal');
            modal.style.display = 'none';
        }

        document.body.addEventListener('click', function() {
            const player = document.getElementById('youtube-player');
            player.contentWindow.postMessage('{"event":"command","func":"playVideo","args":""}', '*');
        });
    </script>
</body>
</html>
