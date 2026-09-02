<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Anita</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #1a1c29 0%, #36122d 50%, #52183c 100%);
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
            color: #fff;
        }

        .stars {
            position: absolute;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, rgba(255,182,193,0.1) 10%, transparent 10.01%);
            background-size: 20px 20px;
            z-index: 1;
        }

        .card {
            position: relative;
            z-index: 2;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            padding: 40px 30px;
            border-radius: 24px;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5), 0 0 30px rgba(230, 57, 70, 0.3);
            max-width: 500px;
            width: 90%;
            text-align: center;
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            letter-spacing: 3px;
            text-transform: uppercase;
            background: linear-gradient(45deg, #ff758c, #ff7eb3);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 20px rgba(255, 117, 140, 0.4);
        }

        p {
            font-size: 1.2rem;
            font-weight: 500;
            margin: 15px 0;
            line-height: 1.6;
            color: #f1f1f1;
        }

        .heart {
            font-size: 60px;
            color: #ff4b5c;
            display: inline-block;
            animation: pulse 1.2s infinite;
            filter: drop-shadow(0 0 15px rgba(255, 75, 92, 0.8));
        }

        .btn-container {
            margin-top: 30px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        button {
            padding: 14px 32px;
            font-size: 1.1rem;
            font-weight: 700;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }

        .yes-btn {
            background: linear-gradient(45deg, #11998e, #38ef7d);
            color: white;
        }

        .yes-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 0 20px rgba(56, 239, 125, 0.6);
        }

        .no-btn {
            background: linear-gradient(45deg, #ff416c, #ff4b2b);
            color: white;
        }

        .no-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 0 20px rgba(255, 65, 108, 0.6);
        }

        .details-box {
            background: rgba(0, 0, 0, 0.3);
            padding: 20px;
            border-radius: 12px;
            margin-top: 20px;
            text-align: left;
            font-size: 0.95rem;
            border-left: 4px solid #ff758c;
            line-height: 1.6;
        }

        .details-box ul {
            list-style: none;
        }

        .details-box li {
            margin-bottom: 10px;
        }

        #next-page {
            display: none;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.25); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>

    <div class="stars"></div>

    <!-- Romantic Background Music -->
    <audio id="romantic-music" loop>
        <source src="https://cdn.pixabay.com/download/audio/2022/05/27/audio_1808fbf07a.mp3?filename=romantic-piano-112199.mp3" type="audio/mpeg">
    </audio>

    <!-- Main Page -->
    <div class="card" id="main-page">
        <div class="heart">&hearts;</div>
        <h1>ANITA</h1>
        <p>I love you Anita, can you make my GF?</p>
        
        <div class="btn-container">
            <button class="yes-btn" onclick="goToNextPage()">Yes</button>
            <button class="no-btn" onclick="handleNo()">No</button>
        </div>
    </div>

    <!-- Thank You Page -->
    <div class="card" id="next-page">
        <div class="heart">&#128150;</div>
        <h1>THANK YOU!</h1>
        <p>Thank you for making my gf! I like girls who play games and coding, and I really like you Anita.</p>
        
        <div class="details-box">
            <ul>
                <li>🎂 <strong>Birthday:</strong> May 24, 2011</li>
                <li>🎈 <strong>Age:</strong> 14 years old</li>
                <li>🎮 <strong>Hobbies:</strong> Coding & Playing Blox Fruits</li>
                <li>📖 <strong>Message:</strong> I believe in focusing on education and goals to build a great future together!</li>
            </ul>
        </div>
    </div>

    <script>
        function playAudio() {
            var audio = document.getElementById("romantic-music");
            audio.play().catch(function(error) {
                console.log("Audio play blocked by browser settings.");
            });
        }

        function goToNextPage() {
            playAudio();
            document.getElementById('main-page').style.display = 'none';
            document.getElementById('next-page').style.display = 'block';
        }

        function handleNo() {
            playAudio();
            alert("That's okay! Education and focusing on your goals come first. We can still be great friends! 😊");
        }
    </script>

</body>
</html>
