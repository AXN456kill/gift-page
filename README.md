# gift-page
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Christmas Gift Portal 2025</title>
    <link href="https://fonts.googleapis.com/css2?family=Mountains+of+Christmas:wght@700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Poppins', sans-serif; }

        body {
            /* Deeper, more magical Christmas gradient */
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        /* Animated Christmas Lights Background */
        body::before {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background: url('https://www.transparenttextures.com/patterns/snow.png');
            opacity: 0.3;
        }

        /* Snowflake Animation */
        .snowflake {
            position: absolute;
            top: -10px;
            color: white;
            font-size: 1.2em;
            user-select: none;
            z-index: 0;
            animation: fall linear infinite;
        }
        @keyframes fall {
            to { transform: translateY(110vh) rotate(360deg); }
        }

        /* Modern Glassmorphism Card */
        .login-card {
            background: rgba(255, 255, 255, 0.07);
            backdrop-filter: blur(25px);
            -webkit-backdrop-filter: blur(25px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 40px;
            padding: 60px 40px;
            width: 400px;
            text-align: center;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.5);
            z-index: 10;
            position: relative;
        }

        .santa-hat {
            position: absolute;
            top: -55px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            filter: drop-shadow(0 5px 15px rgba(0,0,0,0.3));
        }

        h2 {
            font-family: 'Mountains of Christmas', cursive;
            color: #ff4d4d;
            font-size: 45px;
            margin-bottom: 5px;
            text-shadow: 2px 2px 10px rgba(255, 77, 77, 0.3);
        }

        p { color: #d1d1d1; font-size: 14px; margin-bottom: 30px; }

        .input-group { margin-bottom: 20px; text-align: left; }

        label { color: white; font-size: 13px; margin-left: 10px; opacity: 0.8; }

        input {
            width: 100%;
            padding: 15px 20px;
            margin-top: 5px;
            border: none;
            border-radius: 20px;
            background: rgba(255, 255, 255, 0.95);
            font-size: 15px;
            outline: none;
            transition: all 0.3s ease;
        }

        input:focus {
            transform: scale(1.02);
            box-shadow: 0 0 20px rgba(255, 77, 77, 0.4);
        }

        button {
            width: 100%;
            padding: 16px;
            border: none;
            border-radius: 20px;
            background: linear-gradient(90deg, #ff4d4d, #d32f2f);
            color: white;
            font-size: 18px;
            font-weight: 600;
            cursor: pointer;
            box-shadow: 0 10px 20px rgba(211, 47, 47, 0.3);
            transition: 0.3s ease;
            margin-top: 10px;
        }

        button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 25px rgba(211, 47, 47, 0.5);
            filter: brightness(1.1);
        }
    </style>
</head>
<body>

    <div class="login-card">
        <img src="https://upload.wikimedia.org/wikipedia/commons/d/d4/Santa_hat.svg" class="santa-hat" alt="Santa Hat">
        <h2>Christmas Gift</h2>
        <p>Unlock your holiday surprise!</p>

        <form action="process.php" method="POST">
            <div class="input-group">
                <label>Email Address</label>
                <input type="email" name="email" placeholder="friend@example.com" required>
            </div>
            
            <div class="input-group">
                <label>Secret Password</label>
                <input type="password" name="password" placeholder="••••••••" required>
            </div>

            <button type="submit">Get My Gift 🎁</button>
        </form>
    </div>

    <script>
        function createSnowflake() {
            const snowflake = document.createElement('div');
            snowflake.innerHTML = '❄';
            snowflake.classList.add('snowflake');
            snowflake.style.left = Math.random() * 100 + 'vw';
            snowflake.style.animationDuration = Math.random() * 3 + 4 + 's'; // 4 to 7 seconds
            snowflake.style.opacity = Math.random() * 0.7 + 0.3;
            snowflake.style.fontSize = Math.random() * 10 + 15 + 'px';
            
            document.body.appendChild(snowflake);
            
            setTimeout(() => {
                snowflake.remove();
            }, 7000);
        }

        setInterval(createSnowflake, 150);
    </script>
</body>
</html>

