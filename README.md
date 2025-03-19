# Propuesta-Alisson
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mensaje especial</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            overflow: hidden;
            position: relative;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .background-slideshow {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
        
        .slide {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-size: cover;
            background-position: center;
            opacity: 0;
            transition: opacity 2s ease-in-out;
        }
        
        .message-container {
            background-color: rgba(255, 255, 255, 0.85);
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            padding: 30px;
            max-width: 600px;
            text-align: center;
            animation: fadeIn 1s ease-in;
            position: relative;
            z-index: 10;
            margin: 20px;
        }
        
        h1 {
            color: #e91e63;
            margin-bottom: 25px;
        }
        
        p {
            font-size: 18px;
            line-height: 1.6;
            color: #333;
        }
        
        .emoji {
            font-size: 22px;
            margin: 0 3px;
        }
        
        .question {
            margin-top: 30px;
            font-size: 20px;
            font-weight: bold;
            color: #e91e63;
        }
        
        .buttons {
            margin-top: 20px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }
        
        .btn {
            padding: 10px 30px;
            border-radius: 50px;
            border: none;
            font-size: 16px;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            text-decoration: none;
            display: inline-block;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        .btn-yes {
            background-color: #4CAF50;
            color: white;
        }
        
        .btn-no {
            background-color: #f44336;
            color: white;
        }
        
        .final-message {
            margin-top: 30px;
            font-size: 16px;
            font-style: italic;
            color: #555;
            border-top: 1px solid #ddd;
            padding-top: 20px;
        }
        
        .sound-control {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: rgba(255, 255, 255, 0.7);
            padding: 10px;
            border-radius: 50%;
            cursor: pointer;
            z-index: 100;
            font-size: 24px;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        /* Animaciones para emojis flotantes */
        .floating-emoji {
            position: absolute;
            font-size: 30px;
            animation-name: float;
            animation-timing-function: ease-in-out;
            animation-iteration-count: infinite;
            z-index: 1;
            opacity: 0.8;
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) rotate(360deg);
                opacity: 0;
            }
        }
        
        #overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            cursor: pointer;
        }
        
        #overlay-text {
            color: white;
            font-size: 24px;
            text-align: center;
            padding: 20px;
        }
    </style>
</head>
<body>
    <!-- Overlay para iniciar música -->
    <div id="overlay">
        <div id="overlay-text">
            <p>Haz clic en cualquier parte para ver el mensaje con música 🎵</p>
        </div>
    </div>
    
    <!-- Fondo de atardeceres -->
    <div class="background-slideshow" id="backgroundSlideshow">
        <!-- Las imágenes se cargarán por JavaScript -->
    </div>

    <div class="message-container">
        <h1>Mensaje para la princesa hermosaa bonita que esta leyendo esto <span class="emoji">❤️</span><span class="emoji">💕</span><span class="emoji">💖</span></h1>
        <p>
            Para hacerlo formal quiero que el día de mañana después de que salgas del trabajo vayamos a comer algo tranqui 
            <span class="emoji">✨</span>, un helado o algo por el estilo 
            <span class="emoji">🍦</span> jsjs 
            <span class="emoji">😊</span>
        </p>
        <p>
            El día de hoy te hubiera insistido más pero tenía que quedarme en mi trabajo si o si
            <span class="emoji">💼</span>, no iba a venir el otro diseñador
            <span class="emoji">🎨</span>, aparte no me respondías los mensajes
            <span class="emoji">📱</span>
        </p>
        
        <div class="question">
            ¿Quieres salir el día de mañana? <span class="emoji">🥰</span><span class="emoji">💝</span><span class="emoji">🌹</span>
        </div>
        
        <div class="buttons">
            <a href="https://wa.me/51941272637?text=Si%20quiero%20%F0%9F%A5%BA" class="btn btn-yes" target="_blank">SÍ</a>
            <a href="https://wa.me/51941272637?text=%F0%9F%98%94" class="btn btn-no" target="_blank">NO</a>
        </div>
        
        <div class="final-message">
            Más allá de tu respuesta, la verdad que me hace muy feliz hacerte este tipo de detalles, porque imagino que te hago feliz así. En verdad espero hacerlo. 
            <br><br>
            Por cierto, sales guapísima en tu foto de perfil de TikTok jsjs 
            <span class="emoji">😍</span><span class="emoji">❤️</span><span class="emoji">💖</span><span class="emoji">💕</span><span class="emoji">✨</span>
        </div>
    </div>
    
    <!-- Control de sonido -->
    <div class="sound-control" id="soundControl" title="Activar/Desactivar música">🔊</div>
    
    <!-- Reproductor de YouTube oculto -->
    <div id="player" style="display:none;"></div>

    <script>
        // Imágenes de atardeceres
        const sunsetImages = [
            'https://images.unsplash.com/photo-1506815444479-bfdb1e96c566?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80',
            'https://images.unsplash.com/photo-1472120435266-53107fd0c44a?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80',
            'https://images.unsplash.com/photo-1476673160081-cf065607f449?ixlib=rb-1.2.1&auto=format&fit=crop&w=1352&q=80',
            'https://images.unsplash.com/photo-1530508777238-14544088c3ed?ixlib=rb-1.2.1&auto=format&fit=crop&w=1334&q=80',
            'https://images.unsplash.com/photo-1494548162494-384bba4ab999?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80'
        ];
        
        // Crear emojis flotantes animados
        const emojis = ['❤️', '💕', '💖', '💗', '💓', '💝', '🌷', '🌹', '🌸', '💐'];
        const totalEmojis = 50;
        let player;
        let isMuted = false;
        let currentSlide = 0;
        
        function createFloatingEmojis() {
            for (let i = 0; i < totalEmojis; i++) {
                const emoji = document.createElement('div');
                emoji.className = 'floating-emoji';
                emoji.textContent = emojis[Math.floor(Math.random() * emojis.length)];
                
                // Posición inicial aleatoria
                emoji.style.left = Math.random() * 100 + 'vw';
                emoji.style.bottom = '-50px';
                
                // Animación con duración y retraso aleatorios
                const duration = 7 + Math.random() * 15;
                const delay = Math.random() * 15;
                emoji.style.animationDuration = duration + 's';
                emoji.style.animationDelay = delay + 's';
                
                document.body.appendChild(emoji);
            }
        }
        
        // Configurar el fondo de atardeceres
        function setupBackgroundSlideshow() {
            const slideshow = document.getElementById('backgroundSlideshow');
            
            // Crear slides para cada imagen
            sunsetImages.forEach((image, index) => {
                const slide = document.createElement('div');
                slide.className = 'slide';
                slide.style.backgroundImage = `url('${image}')`;
                if (index === 0) slide.style.opacity = 1;
                slideshow.appendChild(slide);
            });
            
            // Iniciar el cambio de diapositivas
            setInterval(changeSlide, 5000);
        }
        
        function changeSlide() {
            const slides = document.querySelectorAll('.slide');
            slides[currentSlide].style.opacity = 0;
            currentSlide = (currentSlide + 1) % slides.length;
            slides[currentSlide].style.opacity = 1;
        }
        
        // API de YouTube
        function onYouTubeIframeAPIReady() {
            player = new YT.Player('player', {
                height: '0',
                width: '0',
                videoId: '2YHzJCEIXZk', // ID del video de YouTube
                playerVars: {
                    'autoplay': 0,
                    'controls': 0,
                    'showinfo': 0,
                    'rel': 0,
                    'loop': 1,
                    'playlist': '2YHzJCEIXZk'
                },
                events: {
                    'onReady': onPlayerReady
                }
            });
        }
        
        function onPlayerReady(event) {
            // El reproductor está listo pero no inicia automáticamente
        }
        
        // Control de sonido
        document.getElementById('soundControl').addEventListener('click', function() {
            if (isMuted) {
                player.unMute();
                this.textContent = '🔊';
                isMuted = false;
            } else {
                player.mute();
                this.textContent = '🔇';
                isMuted = true;
            }
        });
        
        // Iniciar música y animaciones al hacer clic en el overlay
        document.getElementById('overlay').addEventListener('click', function() {
            this.style.display = 'none';
            if (player && player.playVideo) {
                player.playVideo();
            }
            createFloatingEmojis();
        });
        
        // Cargar la API de YouTube
        function loadYouTubeAPI() {
            const tag = document.createElement('script');
            tag.src = "https://www.youtube.com/iframe_api";
            const firstScriptTag = document.getElementsByTagName('script')[0];
            firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);
        }
        
        // Inicializar al cargar la página
        window.onload = function() {
            loadYouTubeAPI();
            setupBackgroundSlideshow();
        };
    </script>
</body>
</html>
