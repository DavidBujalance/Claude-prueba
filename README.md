<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página de Prueba</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            max-width: 600px;
            width: 100%;
            animation: fadeIn 0.6s ease-in;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        h1 {
            color: #333;
            margin-bottom: 20px;
            text-align: center;
            font-size: 2.5em;
        }

        .subtitle {
            color: #666;
            text-align: center;
            margin-bottom: 30px;
            font-size: 1.1em;
        }

        .features {
            margin: 30px 0;
        }

        .feature-item {
            background: #f8f9fa;
            padding: 15px;
            margin: 10px 0;
            border-radius: 10px;
            border-left: 4px solid #667eea;
            transition: transform 0.3s ease;
        }

        .feature-item:hover {
            transform: translateX(5px);
        }

        .feature-item h3 {
            color: #667eea;
            margin-bottom: 5px;
        }

        .feature-item p {
            color: #666;
            font-size: 0.95em;
        }

        .button {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1em;
            border-radius: 25px;
            cursor: pointer;
            width: 100%;
            margin-top: 20px;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .button:active {
            transform: translateY(0);
        }

        .counter {
            text-align: center;
            margin-top: 20px;
            font-size: 1.2em;
            color: #667eea;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🚀 Página de Prueba</h1>
        <p class="subtitle">Una demo simple pero elegante</p>

        <div class="features">
            <div class="feature-item">
                <h3>✨ Diseño Moderno</h3>
                <p>Interfaz limpia y atractiva con gradientes y animaciones</p>
            </div>

            <div class="feature-item">
                <h3>📱 Responsive</h3>
                <p>Se adapta perfectamente a cualquier tamaño de pantalla</p>
            </div>

            <div class="feature-item">
                <h3>⚡ Interactivo</h3>
                <p>Incluye elementos interactivos con JavaScript</p>
            </div>
        </div>

        <button class="button" onclick="incrementCounter()">
            ¡Haz clic aquí!
        </button>

        <div class="counter">
            Clicks: <span id="count">0</span>
        </div>
    </div>

    <script>
        let count = 0;

        function incrementCounter() {
            count++;
            document.getElementById('count').textContent = count;
            
            if (count === 10) {
                alert('¡Felicidades! Has alcanzado 10 clicks 🎉');
            }
        }
    </script>
</body>
</html>
