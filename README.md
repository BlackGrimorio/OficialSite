<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Black Grimório - O Jogo</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Roboto:wght@300;400&display=swap');

        :root {
            --cor-principal: #1a1a1a;
            --cor-secundaria: #f0f0f0;
            --cor-destaque: #e6b800;
        }

        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--cor-principal);
            color: var(--cor-secundaria);
            line-height: 1.6;
            background-image: url('https://via.placeholder.com/1920x1080?text=Imagem+de+Fundo+do+Jogo');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }

        header {
            background-color: rgba(0, 0, 0, 0.7);
            color: var(--cor-secundaria);
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            font-family: 'Cinzel', serif;
            font-size: 2rem;
            font-weight: 700;
            color: var(--cor-destaque);
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }

        nav li {
            margin-left: 2rem;
        }

        nav a {
            text-decoration: none;
            color: var(--cor-secundaria);
            font-weight: 700;
            font-family: 'Cinzel', serif;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: var(--cor-destaque);
        }

        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            background-color: rgba(0, 0, 0, 0.6);
            padding: 0 2rem;
        }

        .hero-title {
            font-family: 'Cinzel', serif;
            font-size: 4rem;
            font-weight: 700;
            color: var(--cor-destaque);
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.8);
            margin-bottom: 1rem;
        }

        .hero-subtitle {
            font-size: 1.5rem;
            max-width: 700px;
            color: var(--cor-secundaria);
        }

        .btn {
            background-color: var(--cor-destaque);
            color: var(--cor-principal);
            padding: 1rem 2rem;
            text-decoration: none;
            font-weight: 700;
            font-family: 'Cinzel', serif;
            border-radius: 5px;
            transition: background-color 0.3s ease, transform 0.3s ease;
            margin: 0.5rem;
            display: inline-block;
        }

        .btn:hover {
            background-color: #ffd700;
            transform: scale(1.05);
        }

        .content {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: auto;
            background-color: rgba(0, 0, 0, 0.8);
            border-radius: 10px;
            margin-top: -100px;
            position: relative;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
        }

        h2 {
            font-family: 'Cinzel', serif;
            font-size: 2.5rem;
            text-align: center;
            color: var(--cor-destaque);
            margin-bottom: 2rem;
            text-transform: uppercase;
            position: relative;
        }

        h2::after {
            content: '';
            display: block;
            width: 80px;
            height: 3px;
            background-color: var(--cor-destaque);
            margin: 10px auto 0;
        }

        .section {
            margin-bottom: 4rem;
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            text-align: center;
        }

        .feature-card {
            background-color: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 10px;
            border-left: 3px solid var(--cor-destaque);
        }

        .feature-card h3 {
            font-family: 'Cinzel', serif;
            color: var(--cor-destaque);
            font-size: 1.5rem;
        }

        footer {
            text-align: center;
            padding: 2rem;
            background-color: rgba(0, 0, 0, 0.7);
            margin-top: 4rem;
        }

        .button-group {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 2rem;
        }

        @media (max-width: 768px) {
            header {
                flex-direction: column;
                padding: 1rem;
            }

            .logo {
                font-size: 1.5rem;
                margin-bottom: 1rem;
            }

            nav ul {
                flex-direction: column;
                align-items: center;
                width: 100%;
            }

            nav li {
                margin: 0.5rem 0;
            }

            .hero-title {
                font-size: 2.5rem;
            }

            .hero-subtitle {
                font-size: 1.2rem;
            }

            .content {
                padding: 2rem 1rem;
                margin-top: -50px;
            }

            h2 {
                font-size: 2rem;
            }

            .grid-container {
                grid-template-columns: 1fr;
            }

            .button-group {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">Black Grimório</div>
        <nav>
            <ul>
                <li><a href="#historia">História</a></li>
                <li><a href="#recursos">Recursos</a></li>
                <li><a href="#jogar">Informações</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="hero">
            <h1 class="hero-title">Black Grimório</h1>
            <p class="hero-subtitle">Mergulhe em um mundo de magia, mistérios antigos e batalhas épicas. O destino do reino está em suas mãos.</p>
        </section>

        <div class="content">
            <section id="historia" class="section">
                <h2>A História</h2>
                <p>Em Black Grimório, você assume o papel de um mago novato em um mundo à beira do colapso. O lendário "Grimório Negro", uma fonte de poder inimaginável, foi roubado, e a escuridão ameaça engolir o reino. Sua jornada começa com a missão de encontrar e recuperar o grimório, desvendando segredos antigos e enfrentando criaturas sombrias que guardam seus mistérios.</p>
                <p>Navegue por florestas proibidas, cidades esquecidas e ruínas amaldiçoadas. Suas escolhas moldarão o futuro do mundo. Você será o herói que todos esperam ou sucumbirá ao poder da escuridão?</p>
            </section>

            <section id="recursos" class="section">
                <h2>Recursos do Jogo</h2>
                <div class="grid-container">
                    <div class="feature-card">
                        <h3>Sistema de Magia Profundo</h3>
                        <p>Domine centenas de feitiços únicos e combine-os para criar efeitos devastadores. Personalize seu estilo de jogo com um vasto sistema de habilidades mágicas.</p>
                    </div>
                    <div class="feature-card">
                        <h3>Mundo Aberto Rico</h3>
                        <p>Explore um vasto e detalhado mundo aberto, repleto de cidades vibrantes, masmorras perigosas e segredos escondidos à espera de serem descobertos.</p>
                    </div>
                    <div class="feature-card">
                        <h3>Batalhas Estratégicas</h3>
                        <p>Enfrente hordas de inimigos e chefes épicos em um sistema de combate que recompensa a estratégia e o planejamento. Use suas habilidades no momento certo para triunfar.</p>
                    </div>
                    <div class="feature-card">
                        <h3>Gráficos Imersivos</h3>
                        <p>Experimente o mundo de Black Grimório com gráficos de última geração e efeitos visuais deslumbrantes que dão vida à sua aventura.</p>
                    </div>
                </div>
            </section>

            <section id="jogar" class="section">
                <div class="button-group">
                    <a href="https://youtube.com/@johnny_dev021?si=AXcalOJXsQqYKmlR" class="btn">Youtube</a>
                    <a href="https://discord.gg/A7TaW4aaDJ" class="btn">Entrar no Discord</a>
                </div>
            </section>
        </div>
    </main>

    <footer>
        <p>&copy; 2025 Black Grimório. Todos os direitos reservados.</p>
    </footer>

</body>
</html>
