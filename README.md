<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ramadan Kareem</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #0f172a; /* Deep night sky */
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            color: #f8fafc;
        }
        .card {
            background: rgba(30, 41, 59, 0.8);
            padding: 40px;
            border-radius: 24px;
            border: 1px solid #334155;
            box-shadow: 0 0 50px rgba(251, 191, 36, 0.2);
            text-align: center;
            max-width: 450px;
        }
        .moon {
            font-size: 80px;
            margin-bottom: 20px;
            filter: drop-shadow(0 0 15px #fbbf24);
        }
        h1 {
            font-size: 2.5rem;
            margin: 10px 0;
            background: linear-gradient(45deg, #fbbf24, #f59e0b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        p {
            color: #94a3b8;
            font-size: 1.1rem;
        }
        #countdown {
            margin-top: 30px;
            font-weight: bold;
            font-size: 1.2rem;
            color: #fbbf24;
            display: flex;
            justify-content: center;
            gap: 15px;
        }
    </style>
</head>
<body>

<div class="card">
    <div class="moon">🌙</div>
    <h1>Ramadan Kareem</h1>
    <p>May this month be filled with peace, blessing, and reflection.</p>
    
    <div id="countdown">
        Loading countdown...
    </div>
</div>

<script>
    // Set the date we're counting down to
    const countDownDate = new Date("Mar 10, 2026 00:00:00").getTime();

    const x = setInterval(function() {
        const now = new Date().getTime();
        const distance = countDownDate - now;

        const days = Math.floor(distance / (1000 * 60 * 60 * 24));
        const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));

        document.getElementById("countdown").innerHTML = `${days}d ${hours}h until Ramadan`;

        if (distance < 0) {
            clearInterval(x);
            document.getElementById("countdown").innerHTML = "Ramadan Mubarak!";
        }
    }, 1000);
</script>

</body>
</html>
