<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Загрузка Space Enemies</title>
    <style>
        body { font-family: sans-serif; text-align: center; padding: 50px; background: #1a1a1a; color: white; }
        .btn { background: #007bff; color: white; padding: 15px 30px; text-decoration: none; border-radius: 5px; font-size: 20px; }
        .btn:hover { background: #0056b3; }
        .info { margin-top: 20px; color: #888; }
    </style>
</head>
<body>
    <h1>Space Enemies Update Server</h1>
    <p>Нажмите кнопку ниже, если загрузка не началась автоматически в приложении.</p>
    <br><br>
    <a href="spaceenemies.apk" class="btn">Скачать APK</a>
    
    <div class="info">
        Текущая версия: <span id="version">Загрузка...</span>
    </div>

    <script>
        fetch('version.txt')
            .then(response => response.text())
            .then(data => document.getElementById('version').innerText = data);
    </script>
</body>
</html>
