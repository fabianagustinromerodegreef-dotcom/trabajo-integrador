# trabajo-integrador
IDW-grupo34

inicio
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CentMed - Centro Médico </title>
    <link rel="stylesheet" href="https://www.linkedin.com/redir/redirect?url=http%3A%2F%2Fcentronuevasalud%2Ecom%2Ear%2F&urlhash=X4hJ&trk=about_website">
    <style>
        /* Variables de colores y estilos para sector salud */
        :root {
            --color-primary: #2b5e8e;
            --color-secondary: #4fb0c6;
            --color-accent: #ff6b6b;
            --color-light: #f8f9fa;
            --color-dark: #2c3e50;
            --spacing-sm: 0.5rem;
            --spacing-md: 1rem;
            --spacing-lg: 2rem;
            --spacing-xl: 4rem;
            --border-radius: 8px;
            --box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        /* Estilos generales */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 var(--spacing-md);
        }

        /* Header y navegación */
        header {
            background-color: white;
            color: var(--color-primary);
            padding: var(--spacing-md) 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: var(--box-shadow);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            display: flex;
            align-items: center;
        }

        .logo i {
            margin-right: var(--spacing-sm);
            color: var(--color-secondary);
        }

        .logo span {
            color: var(--color-primary);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: var(--spacing-lg);
        }

        nav ul li a {
            color: var(--color-dark);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            padding: var(--spacing-sm) 0;
            position: relative;
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--color-secondary);
            transition: var(--transition);
        }

        nav ul li a:hover::after,
        nav ul li a.active::after {
            width: 100%;
        }

        nav ul li a:hover,
        nav ul li a.active {
            color: var(--color-secondary);
        }

        .emergency-button {
            background-color: var(--color-accent);
            color: white;
            padding: var(--spacing-sm) var(--spacing-md);
            border-radius: var(--border-radius);
            text-decoration: none;
            font-weight: bold;
            transition: var(--transition);
            display: flex;
            align-items: center;
        }

        .emergency-button i {
            margin-right: var(--spacing-sm);
        }

        .emergency-button:hover {
            background-color: #ff5252;
            transform: scale(1.05);
        }

        /* Sección Hero */
        .hero {
            background: linear-gradient(rgba(43, 94, 142, 0.8), rgba(43, 94, 142, 0.8)), url('https://images.unsplash.com/photo-1532938911079-1b06ac7ceec7?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: var(--spacing-xl) 0;
            text-align: center;
            margin-bottom: var(--spacing-xl);
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 2.8rem;
            margin-bottom: var(--spacing-md);
            animation: fadeInDown 1s ease;
        }

        .hero p {
            font-size: 1.2rem;
            margin: 0 auto var(--spacing-lg);
            max-width: 600px;
            animation: fadeInUp 1s ease;
        }

        .btn {
            display: inline-block;
            background-color: var(--color-secondary);
            color: white;
            padding: var(--spacing-sm) var(--spacing-lg);
            border-radius: var(--border-radius);
            text-decoration: none;
            font-weight: bold;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            animation: fadeIn 1.5s ease;
        }

        .btn:hover {
            background-color: #3a9aad;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .btn-secondary {
            background-color: transparent;
            border: 2px solid white;
            margin-left: var(--spacing-md);
        }

        .btn-secondary:hover {
            background-color: white;
            color: var(--color-primary);
        }

        /* Sección de servicios */
        .services {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: var(--spacing-lg);
            margin-bottom: var(--spacing-xl);
        }

        .section-title {
            text-align: center;
            margin-bottom: var(--spacing-xl);
            color: var(--color-primary);
            position: relative;
            padding-bottom: var(--spacing-md);
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--color-secondary);
        }

        .service-card {
            background-color: white;
            padding: var(--spacing-lg);
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            transition: var(--transition);
            text-align: center;
            border-top: 4px solid var(--color-secondary);
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .service-icon {
            font-size: 2.5rem;
            color: var(--color-secondary);
            margin-bottom: var(--spacing-md);
        }

        .service-card h3 {
            color: var(--color-primary);
            margin-bottom: var(--spacing-md);
        }

        /* Sección de especialidades */
        .specialties {
            background-color: var(--color-light);
            padding: var(--spacing-xl) 0;
            margin-bottom: var(--spacing-xl);
        }

        .specialty-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: var(--spacing-lg);
        }

        .specialty-card {
            background-color: white;
            padding: var(--spacing-lg);
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            text-align: center;
            transition: var(--transition);
        }

        .specialty-card:hover {
            transform: translateY(-5px);
        }

        .specialty-icon {
            width: 70px;
            height: 70px;
            background-color: var(--color-light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto var(--spacing-md);
            color: var(--color-primary);
            font-size: 1.8rem;
        }

        /* Sección de testimonios */
        .testimonials {
            padding: var(--spacing-xl) 0;
            margin-bottom: var(--spacing-xl);
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: var(--spacing-lg);
        }

        .testimonial-card {
            background-color: white;
            padding: var(--spacing-lg);
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            border-left: 4px solid var(--color-secondary);
        }

        .testimonial-text {
            font-style: italic;
            margin-bottom: var(--spacing-md);
            position: relative;
            padding: var(--spacing-md);
        }

        .testimonial-text::before,
        .testimonial-text::after {
            content: '"';
            font-size: 3rem;
            color: var(--color-secondary);
            opacity: 0.3;
            position: absolute;
        }

        .testimonial-text::before {
            top: 0;
            left: 0;
        }

        .testimonial-text::after {
            bottom: -1.5rem;
            right: 0;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
        }

        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: var(--color-secondary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            margin-right: var(--spacing-md);
        }

        /* Sección de llamada a la acción */
        .cta {
            background: linear-gradient(135deg, var(--color-primary) 0%, var(--color-secondary) 100%);
            color: white;
            padding: var(--spacing-xl) 0;
            text-align: center;
            border-radius: var(--border-radius);
            margin-bottom: var(--spacing-xl);
        }

        .cta h2 {
            margin-bottom: var(--spacing-md);
        }

        .cta p {
            max-width: 600px;
            margin: 0 auto var(--spacing-lg);
        }

        /* Sección de información de contacto */
        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: var(--spacing-lg);
            margin-bottom: var(--spacing-xl);
        }

        .info-card {
            background-color: white;
            padding: var(--spacing-lg);
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            text-align: center;
        }

        .info-icon {
            font-size: 2rem;
            color: var(--color-secondary);
            margin-bottom: var(--spacing-md);
        }

        /* Footer */
        footer {
            background-color: var(--color-dark);
            color: white;
            padding: var(--spacing-lg) 0;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: var(--spacing-xl);
            margin-bottom: var(--spacing-lg);
        }

        .footer-column h3 {
            color: var(--color-secondary);
            margin-bottom: var(--spacing-md);
            position: relative;
            padding-bottom: var(--spacing-sm);
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 2px;
            background-color: var(--color-secondary);
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: var(--spacing-sm);
        }

        .footer-column ul li a {
            color: #ddd;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-column ul li a:hover {
            color: var(--color-secondary);
            padding-left: var(--spacing-sm);
        }

        .social-links {
            display: flex;
            gap: var(--spacing-md);
            margin-top: var(--spacing-md);
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: var(--transition);
        }

        .social-links a:hover {
            background-color: var(--color-secondary);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: var(--spacing-lg);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Animaciones */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInUp {
            from { 
                opacity: 0;
                transform: translateY(20px);
            }
            to { 
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInDown {
            from { 
                opacity: 0;
                transform: translateY(-20px);
            }
            to { 
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: var(--spacing-md);
                justify-content: center;
                flex-wrap: wrap;
            }
            
            nav ul li {
                margin: 0 var(--spacing-sm);
            }
            
            .emergency-button {
                margin-top: var(--spacing-md);
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero-buttons {
                display: flex;
                flex-direction: column;
                gap: var(--spacing-md);
            }
            
            .btn-secondary {
                margin-left: 0;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .footer-column h3::after {
                left: 50%;
                transform: translateX(-50%);
            }
            
            .social-links {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fas fa-hospital"></i>
                Clínica<span>Salud Integral</span>
            </div>
            <nav>
                <ul>
                    <li><a href="#" class="active">Inicio</a></li>
                    <li><a href="#">Servicios</a></li>
                    <li><a href="#">Especialidades</a></li>
                    <li><a href="#">Médicos</a></li>
                    <li><a href="#">Contacto</a></li>
                </ul>
            </nav>
            <a href="tel:123456789" class="emergency-button">
                <i class="fas fa-phone"></i>Urgencias
            </a>
        </div>
    </header>

    <!-- Sección Hero -->
    <section class="hero">
        <div class="container hero-content">
            <h1>Cuidamos de tu salud con excelencia y calidez humana</h1>
            <p>Tu bienestar es nuestra prioridad. Contamos con tecnología de punta y un equipo médico de primer nivel para brindarte la mejor atención.</p>
            <div class="hero-buttons">
                <a href="#" class="btn">Solicitar cita</a>
                <a href="#" class="btn btn-secondary">Conoce más</a>
            </div>
        </div>
    </section>

    <!-- Sección de servicios -->
    <section class="container">
        <h2 class="section-title">Nuestros Servicios</h2>
        <div class="services">
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-stethoscope"></i>
                </div>
                <h3>Consulta General</h3>
                <p>Atención médica integral para toda la familia con profesionales altamente capacitados.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-heartbeat"></i>
                </div>
                <h3>Chequeos Preventivos</h3>
                <p>Programas de prevención y detección temprana de enfermedades para cuidar tu salud.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-ambulance"></i>
                </div>
                <h3>Urgencias 24/7</h3>
                <p>Atención de urgencias las 24 horas con equipos de respuesta inmediata y profesionales especializados.</p>
            </div>
        </div>
    </section>

    <!-- Sección de especialidades -->
    <section class="specialties">
        <div class="container">
            <h2 class="section-title">Nuestras Especialidades</h2>
            <div class="specialty-grid">
                <div class="specialty-card">
                    <div class="specialty-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3>Neurología</h3>
                </div>
                <div class="specialty-card">
                    <div class="specialty-icon">
                        <i class="fas fa-heart"></i>
                    </div>
                    <h3>Cardiología</h3>
                </div>
                <div class="specialty-card">
                    <div class="specialty-icon">
                        <i class="fas fa-baby"></i>
                    </div>
                    <h3>Pediatría</h3>
                </div>
                <div class="specialty-card">
                    <div class="specialty-icon">
                        <i class="fas fa-x-ray"></i>
                    </div>
                    <h3>Radiología</h3>
                </div>
                <div class="specialty-card">
                    <div class="specialty-icon">
                        <i class="fas fa-teeth"></i>
                    </div>
                    <h3>Odontología</h3>
                </div>
                <div class="specialty-card">
                    <div class="specialty-icon">
                        <i class="fas fa-eye"></i>
                    </div>
                    <h3>Oftalmología</h3>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección de testimonios -->
    <section class="testimonials">
        <div class="container">
            <h2 class="section-title">Opiniones de Nuestros Pacientes</h2>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        Excelente atención. Los médicos son muy profesionales y el personal siempre está dispuesto a ayudar. Las instalaciones son modernas y limpias.
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">M</div>
                        <div>
                            <h4>María González</h4>
                            <p>Paciente</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        Llevo a mi familia aquí desde hace años. La confianza y calidad en el servicio es incomparable. Siempre solucionan nuestros problemas de salud.
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">J</div>
                        <div>
                            <h4>Jorge Martínez</h4>
                            <p>Paciente</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        Tuve una emergencia y me atendieron inmediatamente. El equipo de urgencias fue rápido y eficiente. Gracias por salvar mi vida.
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">C</div>
                        <div>
                            <h4>Carlos López</h4>
                            <p>Paciente</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección de información de contacto -->
    <section class="container">
        <h2 class="section-title">Cómo Contactarnos</h2>
        <div class="contact-info">
            <div class="info-card">
                <div class="info-icon">
                    <i class="fas fa-map-marker-alt"></i>
                </div>
                <h3>Ubicación</h3>
                <p>Av. Principal #123, Ciudad</p>
            </div>
            <div class="info-card">
                <div class="info-icon">
                    <i class="fas fa-phone"></i>
                </div>
                <h3>Teléfonos</h3>
                <p>Consultas: (123) 456-7890</p>
                <p>Urgencias: (123) 456-HELP</p>
            </div>
            <div class="info-card">
                <div class="info-icon">
                    <i class="fas fa-clock"></i>
                </div>
                <h3>Horarios</h3>
                <p>Lunes a Viernes: 7:00 am - 9:00 pm</p>
                <p>Sábados: 8:00 am - 6:00 pm</p>
            </div>
        </div>
    </section>

    <!-- Sección de llamada a la acción -->
    <section class="container">
        <div class="cta">
            <h2>¿Necesitas atención médica?</h2>
            <p>No esperes más, agenda tu cita ahora mismo y cuida de tu salud con los mejores profesionales.</p>
            <a href="#" class="btn">Agendar cita en línea</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Clínica Salud Integral</h3>
                    <p>Brindamos servicios de salud de alta calidad con tecnología de punta y un equipo médico de excelencia.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Enlaces rápidos</h3>
                    <ul>
                        <li><a href="#">Inicio</a></li>
                        <li><a href="#">Servicios</a></li>
                        <li><a href="#">Especialidades</a></li>
                        <li><a href="#">Médicos</a></li>
                        <li><a href="#">Contacto</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Servicios</h3>
                    <ul>
                        <li><a href="#">Consulta General</a></li>
                        <li><a href="#">Chequeos Preventivos</a></li>
                        <li><a href="#">Urgencias</a></li>
                        <li><a href="#">Laboratorio</a></li>
                        <li><a href="#">Imagenología</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Horario de Atención</h3>
                    <ul>
                        <li>Lunes a Viernes: 7:00 am - 9:00 pm</li>
                        <li>Sábados: 8:00 am - 6:00 pm</li>
                        <li>Domingos: Solo urgencias</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Clínica Salud Integral. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>

    <script>
        // Animación para los elementos al hacer scroll
        document.addEventListener('DOMContentLoaded', function() {
            const observerOptions = {
                root: null,
                rootMargin: '0px',
                threshold: 0.1
            };

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('animate');
                    }
                });
            }, observerOptions);

            // Observar elementos que deben animarse al aparecer
            document.querySelectorAll('.service-card, .specialty-card, .testimonial-card, .info-card').forEach(el => {
                observer.observe(el);
            });

            // Efecto de escritura para el título principal
            const heroTitle = document.querySelector('.hero h1');
            const originalText = heroTitle.textContent;
            heroTitle.textContent = '';
            
            let i = 0;
            function typeWriter() {
                if (i < originalText.length) {
                    heroTitle.textContent += originalText.charAt(i);
                    i++;
                    setTimeout(typeWriter, 50);
                }
            }
            
            // Iniciar efecto de escritura
            setTimeout(typeWriter, 500);
        });
    </script>
</body>
</html>

