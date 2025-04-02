<!DOCTYPE html><html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Invitación a la Fiesta</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #1c1c1c;
            color: white;
            padding: 20px;
        }
        .countdown {
            font-size: 24px;
            margin: 20px 0;
        }
        .button {
            display: inline-block;
            padding: 10px 20px;
            background-color: #d4af37;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            margin: 10px 0;
        }
    </style>
    <script>
        function countdown() {
            const eventDate = new Date("March 29, 2025 19:30:00").getTime();
            const interval = setInterval(() => {
                const now = new Date().getTime();
                const distance = eventDate - now;
                if (distance < 0) {
                    clearInterval(interval);
                    document.getElementById("countdown").innerHTML = "¡El evento ha comenzado!";
                    return;
                }
                const days = Math.floor(distance / (1000 * 60 * 60 * 24));
                const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((distance % (1000 * 60)) / 1000);
                document.getElementById("countdown").innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s`;
            }, 1000);
        }
    </script>
</head>
<body onload="countdown()">
    <h1>¡Estás invitado!</h1>
    <p>La fiesta será el sábado 29 de marzo a las 19:30 en Salón Origami, Av. Costanera 7450, CABA.</p>
    <div class="countdown" id="countdown"></div>
    <a href="#" class="button">Ver Mapa</a>
    <h2>Confirmar Asistencia</h2>
    <a href="#" class="button">Confirmar</a>
    <h2>Dress Code</h2>
    <p>El código de vestimenta será elegante (No White, No Silver).</p>
    <h2>#TiziFest</h2>
    <p>Usa el hashtag de la fiesta para subir tus fotos y videos.</p>
    <a href="#" class="button">Ver en Instagram</a>
    <h2>¡Los espero!</h2>
</body>
</html>
