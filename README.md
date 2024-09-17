<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>动态爱心</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        .heart {
            font-size: 100px;
            color: red;
            animation: pulse 1s infinite;
        }
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>
    <div class="heart">❤️</div>
    <script>
        document.querySelector('.heart').addEventListener('click', function() {
            this.style.animation = 'none';
            setTimeout(() => this.style.animation = '', 10);
        });
    </script>
</body>
</html>
