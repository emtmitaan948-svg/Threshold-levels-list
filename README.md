<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Threshold Levels List</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #0b0b10;
            color: white;
        }

        header {
            padding: 40px 20px;
            text-align: center;
            background: linear-gradient(135deg, #171722, #0b0b10);
            border-bottom: 1px solid #292936;
        }

        header h1 {
            margin: 0;
            font-size: 42px;
        }

        header p {
            color: #999;
            font-size: 16px;
        }

        .container {
            max-width: 1000px;
            margin: 35px auto;
            padding: 0 20px;
        }

        .level {
            display: flex;
            align-items: center;
            gap: 20px;

            padding: 20px;
            margin-bottom: 12px;

            background: #15151d;
            border: 1px solid #292936;
            border-radius: 12px;

            transition: 0.2s;
        }

        .level:hover {
            transform: translateY(-2px);
            border-color: #555566;
            background: #1a1a24;
        }

        .rank {
            width: 55px;
            font-size: 25px;
            font-weight: bold;
            text-align: center;
        }

        .info {
            flex: 1;
        }

        .info h2 {
            margin: 0;
            font-size: 21px;
        }

        .info p {
            margin: 6px 0 0;
            color: #888;
        }

        .difficulty {
            padding: 8px 12px;
            border-radius: 8px;
            background: #252532;
            color: #ccc;
            font-size: 13px;
            font-weight: bold;
        }

        footer {
            text-align: center;
            padding: 40px;
            color: #555;
        }
    </style>
</head>

<body>

<header>
    <h1>Threshold Levels List</h1>
    <p>The hardest levels. Ranked by difficulty.</p>
</header>

<div class="container">

    <div class="level">
        <div class="rank">#1</div>
        <div class="info">
            <h2>Level Name</h2>
            <p>Creator Name</p>
        </div>
        <div class="difficulty">Extreme Demon</div>
    </div>

    <div class="level">
        <div class="rank">#2</div>
        <div class="info">
            <h2>Another Level</h2>
            <p>Creator Name</p>
        </div>
        <div class="difficulty">Extreme Demon</div>
    </div>

    <div class="level">
        <div class="rank">#3</div>
        <div class="info">
            <h2>Third Level</h2>
            <p>Creator Name</p>
        </div>
        <div class="difficulty">Extreme Demon</div>
    </div>

    <div class="level">
        <div class="rank">#4</div>
        <div class="info">
            <h2>Fourth Level</h2>
            <p>Creator Name</p>
        </div>
        <div class="difficulty">Extreme Demon</div>
    </div>

</div>

<footer>
    Threshold Levels List © 2026
</footer>

</body>
</html>
