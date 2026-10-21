<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Oportoview Alegria Apartment - Guia Local</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            --primary: #1A5F7A;
            --secondary: #229396;
            --accent: #E67E22;
            --bg-color: #F5F5DC; /* Bege Claro */
            --card-bg: #FFFFFF;
            --text-main: #333333;
            --text-light: #666666;
            --btn-bg: #000080; /* Azul Marinho */
            --btn-text: #FFD700; /* Dourado */
        }

        body {
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            margin: 0;
            padding: 0;
            line-height: 1.6;
        }

        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            text-align: center;
            padding: 4rem 1rem;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        header h1 {
            font-size: 3rem;
            margin: 0 0 10px 0;
            font-weight: 700;
            letter-spacing: 1px;
        }

        header p {
            font-size: 1.3rem;
            margin: 0 0 20px 0;
            opacity: 0.9;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .intro {
            background-color: var(--card-bg);
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            margin-bottom: 2rem;
            text-align: left;
        }
        
        .intro h2 {
            color: var(--primary);
            margin-top: 0;
            font-size: 2rem;
        }

        .intro-desc {
            font-size: 1.1rem;
            color: var(--text-light);
            margin-bottom: 2rem;
        }

        .location-info {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .location-item {
            display: flex;
            gap: 15px;
            align-items: flex-start;
        }

        .location-item i {
            color: var(--accent);
            font-size: 1.5rem;
            margin-top: 4px;
        }

        .filters {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
            margin-bottom: 3rem;
            /* Sticky properties removed so buttons scroll normally */
        }

        .filter-btn {
            background-color: var(--btn-bg);
            border: 2px solid var(--btn-bg);
            color: var(--btn-text);
            padding: 10px 20px;
            border-radius: 25px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .filter-btn:hover, .filter-btn.active {
            background-color: var(--btn-text);
            color: var(--btn-bg);
            border-color: var(--btn-text);
        }

        .section-title {
            color: var(--primary);
            font-size: 2rem;
            border-bottom: 3px solid var(--accent);
            padding-bottom: 10px;
            margin: 3rem 0 2rem 0;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .section-desc {
            font-size: 1.1rem;
            color: var(--text-light);
            margin-bottom: 2rem;
            font-style: italic;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 20px;
        }

        .card {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            border-left: 5px solid var(--secondary);
            transition: transform 0.3s, box-shadow 0.3s;
            display: flex;
            flex-direction: column;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            border-left-color: var(--accent);
        }

        .card-header {
            margin-bottom: 15px;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .card-title {
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
        }

        .card-actions {
            display: flex;
            gap: 10px;
            align-items: center;
            flex-wrap: wrap;
        }

        .btn-clique {
            background-color: var(--btn-bg);
            color: var(--btn-text);
            font-size: 0.85rem;
            padding: 6px 12px;
            border-radius: 20px;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 5px;
            width: fit-content;
            text-decoration: none;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            transition: all 0.2s ease;
        }
        
        .btn-clique-header {
            font-size: 1rem;
            padding: 8px 20px;
        }

        .card-title:hover {
            color: var(--accent);
        }
        
        .btn-clique:hover {
            background-color: var(--btn-text);
            color: var(--btn-bg);
        }

        .distance-badge {
            background-color: #E8F4F8;
            color: var(--primary);
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: bold;
            display: inline-block;
            margin: 0;
        }

        .card-notes {
            color: var(--text-light);
            font-size: 1.05rem;
            line-height: 1.5;
            flex-grow: 1;
            margin-top: 15px;
            border-top: 1px solid #f0f0f0;
            padding-top: 15px;
        }

        footer {
            background-color: var(--primary);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 4rem;
        }

        .category-section {
            animation: fadeIn 0.5s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @media (max-width: 768px) {
            header h1 { font-size: 2rem; }
            .grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <header>
        <h1>Oportoview Alegria Apartment</h1>
        <p>Rua da Alegria 208, 4000-034 Porto</p>
        <a href="https://share.google/mrdK0vKM0lZ1ZLqWH" target="_blank" class="btn-clique btn-clique-header">
            <i class="fas fa-hand-pointer"></i> Rota Mapas
        </a>
    </header>

    <div class="container">
        
        <!-- Intro & Location -->
        <div class="intro">
            <h2>Os nossos locais favoritos perto do apartamento</h2>
            <p class="intro-desc">Bem-vindo! Aqui estão os locais que adoramos e recomendamos aos nossos hóspedes, desde o primeiro café do dia até à última bebida.</i>.</p>
            
            <h3 style="color: var(--primary); font-size: 1.5rem; margin-bottom: 1rem;">📍 Localização e Transportes</h3>
            <div class="location-info">
                <div class="location-item">
                    <i class="fas fa-walking"></i>
                    <div>
                        <strong>A pé:</strong> O coração comercial do Porto (<a href="https://www.google.com/maps/search/?api=1&query=Rua+de+Santa+Catarina+Porto" target="_blank">Rua de Santa Catarina</a>, <a href="https://www.google.com/maps/search/?api=1&query=Mercado+do+Bolhao+Porto" target="_blank">Mercado do Bolhão</a>, <a href="https://www.google.com/maps/search/?api=1&query=Capela+das+Almas+Porto" target="_blank">Capela das Almas</a>) fica a apenas 2 a 5 minutos a pé. A Baixa está literalmente à sua porta.
                    </div>
                </div>
                <div class="location-item">
                    <i class="fas fa-subway"></i>
                    <div>
                        <strong>De metro:</strong> A <a href="https://www.google.com/maps/search/?api=1&query=Estacao+do+Bolhao+Metro+Porto" target="_blank">Estação do Bolhão</a> (a ~3 min a pé) liga-o a quase todas as linhas da cidade (A, B, C, E, F). A <strong>Linha E (Violeta)</strong> tem ligação direta ao Aeroporto. Se quiser visitar as Caves do Vinho do Porto ou ver o pôr-do-sol no Jardim do Morro, basta apanhar o metro no Bolhão, sair na Trindade (1 paragem) e trocar para a Linha D (Amarela) em direção a Santo Ovídio.
                    </div>
                </div>
                <div class="location-item">
                    <i class="fas fa-parking"></i>
                    <div>
                        <strong>Estacionamento:</strong> Se se desloca de carro, o apartamento tem um acordo com desconto para os hóspedes no parque de estacionamento situado na <a href="https://www.google.com/maps/search/?api=1&query=Rua+da+Alegria+35+Porto" target="_blank">Rua da Alegria 35, 4000-300 Porto</a>, sendo uma solução prática, segura e económica nas imediações.
                    </div>
                </div>
            </div>
        </div>

        <!-- Filters -->
        <div class="filters">
            <button class="filter-btn active" onclick="filterData('all')">Ver Todos</button>
            <button class="filter-btn" onclick="filterData('sights')">Pontos de Interesse</button>
            <button class="filter-btn" onclick="filterData('groceries')">Supermercados</button>
            <button class="filter-btn" onclick="filterData('breakfast')">Pequeno-almoço</button>
            <button class="filter-btn" onclick="filterData('restaurants')">Restaurantes</button>
            <button class="filter-btn" onclick="filterData('fado')">Fado</button>
            <button class="filter-btn" onclick="filterData('nightlife')">Noite & Cultura</button>
            <button class="filter-btn" onclick="filterData('caves')">Caves de Vinho</button>
            <button class="filter-btn" onclick="filterData('laundry')">Lavandarias</button>
        </div>

        <div id="content-area">
            
            <!-- Pontos de Interesse -->
            <div class="category-section sights">
                <h2 class="section-title">📸 Pontos de Interesse (Sights)</h2>
                <p class="section-desc">Os locais de visita obrigatória no Porto, ordenados do mais próximo para o mais distante.</p>
                <div class="grid">
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Capela das Almas</span>
                            <div class="card-actions">
                                <span class="distance-badge">2 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Capela+das+Almas+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">A principal artéria pedonal do Porto e a famosa igreja revestida a azulejos azuis.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Mercado do Bolhão</span>
                            <div class="card-actions">
                                <span class="distance-badge">4 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Mercado+do+Bolhao+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">O mercado tradicional mais icónico da cidade, recentemente renovado.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Majestic Café</span>
                            <div class="card-actions">
                                <span class="distance-badge">5 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Majestic+Cafe+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">O café histórico mais luxuoso do Porto.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Estação de São Bento</span>
                            <div class="card-actions">
                                <span class="distance-badge">10 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Estacao+de+Sao+Bento+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Famosa pelos seus 20.000 azulejos pintados à mão no átrio.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Avenida dos Aliados</span>
                            <div class="card-actions">
                                <span class="distance-badge">11 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Avenida+dos+Aliados+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">A imponente sala de visitas e coração cívico da cidade, ladeada por edifícios arquitetónicos magníficos.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Torre dos Clérigos</span>
                            <div class="card-actions">
                                <span class="distance-badge">14 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Torre+dos+Clerigos+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">O ex-líbris barroco da cidade. Com mais de 75 metros de altura, oferece uma vista inesquecível de 360°.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Livraria Lello</span>
                            <div class="card-actions">
                                <span class="distance-badge">15 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Livraria+Lello+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Considerada uma das livrarias mais bonitas do mundo, de inspiração neogótica. Compre bilhete com antecedência.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Igreja do Carmo</span>
                            <div class="card-actions">
                                <span class="distance-badge">16 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Igreja+do+Carmo+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Impressionante igreja famosa pela imensa fachada lateral totalmente revestida por painéis de azulejos.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Sé do Porto (Catedral)</span>
                            <div class="card-actions">
                                <span class="distance-badge">16 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Se+do+Porto+Catedral" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Situada num ponto alto, com vista deslumbrante sobre a cidade antiga.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Ponte Dom Luís I</span>
                            <div class="card-actions">
                                <span class="distance-badge">17 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Ponte+Dom+Luis+I+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Atravessá-la a pé nos seus dois níveis (tabuleiro superior e inferior) é obrigatório!</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Ribeira do Porto</span>
                            <div class="card-actions">
                                <span class="distance-badge">20 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Ribeira+do+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">A icónica zona histórica ribeirinha da cidade, repleta de casas coloridas e esplanadas junto ao rio.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Muralhas Fernandinas do Porto</span>
                            <div class="card-actions">
                                <span class="distance-badge">20 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Muralhas+Fernandinas+do+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Vestígios da antiga muralha medieval da cidade, com vistas panorâmicas sobre o rio Douro.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Escadas do Codeçal</span>
                            <div class="card-actions">
                                <span class="distance-badge">20 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Escadas+do+Codecal+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Uma descida icónica e íngreme desde a zona da Sé até à Ribeira.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Funicular dos Guindais</span>
                            <div class="card-actions">
                                <span class="distance-badge">21 min a pé / Funicular</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Funicular+dos+Guindais+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">O famoso transporte panorâmico que liga rapidamente a zona da Batalha/Sé à Ribeira.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Jardim do Morro</span>
                            <div class="card-actions">
                                <span class="distance-badge">25 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Jardim+do+Morro+Gaia" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Localizado logo após a Ponte D. Luís, é um dos melhores locais da cidade para assistir ao pôr-do-sol.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Miradouro da Serra do Pilar</span>
                            <div class="card-actions">
                                <span class="distance-badge">30 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Miradouro+da+Serra+do+Pilar" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Oferece uma das vistas mais clássicas e fotogénicas do Porto e da Ponte D. Luís.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Super Bock Arena Pavilhão Rosa Mota</span>
                            <div class="card-actions">
                                <span class="distance-badge">30 min a pé / Autocarro</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Super+Bock+Arena+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Nos Jardins do Palácio de Cristal. A cúpula oferece vistas 360° impressionantes.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Mercado Bom Sucesso</span>
                            <div class="card-actions">
                                <span class="distance-badge">De Metro / Autoc.</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Mercado+Bom+Sucesso+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Mercado moderno com diversas bancas de gastronomia.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Casa da Música</span>
                            <div class="card-actions">
                                <span class="distance-badge">De Metro / Autoc.</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Casa+da+Musica+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Apanhe qualquer metro no Bolhão (direção Boavista/Senhora da Hora). Demora cerca de 10 min.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Parque da Cidade do Porto</span>
                            <div class="card-actions">
                                <span class="distance-badge">De Autocarro</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Parque+da+Cidade+do+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">O maior parque urbano do país, com ligação direta à praia.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Museu de Serralves e Foz</span>
                            <div class="card-actions">
                                <span class="distance-badge">De Autocarro</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Museu+de+Serralves+e+Foz" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Apanhe um autocarro nos Aliados ou o Elétrico 1 junto à Igreja de São Francisco.</p>
                    </div>

                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Tram Linha 1 - Passeio Alegre</span>
                            <div class="card-actions">
                                <span class="distance-badge">De Elétrico Histórico</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Tram+Linha+1+Passeio+Alegre" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Viagem panorâmica de elétrico antigo pela marginal do rio Douro.</p>
                    </div>
                </div>
            </div>

            <!-- Mercearias e Supermercados -->
            <div class="category-section groceries">
                <h2 class="section-title">🛒 Mercearias e Supermercados (Groceries)</h2>
                <div class="grid">
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Pingo Doce - Rua da Alegria</span>
                            <div class="card-actions">
                                <span class="distance-badge">2 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Pingo+Doce+Rua+da+Alegria+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Opção mais próxima e conveniente, num centro comercial com entrada direta pela rua.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Continente Bom Dia - Via Catarina</span>
                            <div class="card-actions">
                                <span class="distance-badge">3 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Continente+Bom+Dia+Via+Catarina" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Supermercado prático situado na praça de alimentação do Via Catarina.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Mercado do Bolhão</span>
                            <div class="card-actions">
                                <span class="distance-badge">4 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Mercado+do+Bolhao+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Excelente para produtos frescos, pão e queijo locais (Terça a Sábado: 08h-20h).</p>
                    </div>
                </div>
            </div>

            <!-- Pequeno-almoço e Brunch -->
            <div class="category-section breakfast">
                <h2 class="section-title">🥐 Pequeno-almoço e Brunch (Breakfast & Brunch)</h2>
                <div class="grid">
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Confeitaria do Bolhão</span>
                            <div class="card-actions">
                                <span class="distance-badge">4 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Confeitaria+do+Bolhao" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Clássico centenário em frente ao mercado para pequeno-almoço tradicional.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Fábrica da Nata</span>
                            <div class="card-actions">
                                <span class="distance-badge">3 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Fabrica+da+Nata+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Na Rua de Santa Catarina, ideal para saborear um pastel de nata quente.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Manteigaria</span>
                            <div class="card-actions">
                                <span class="distance-badge">3 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Manteigaria+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Junto ao Bolhão, conhecida por muitos como tendo os melhores pastéis de nata.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Zenith Brunch & Cocktails</span>
                            <div class="card-actions">
                                <span class="distance-badge">12 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Zenith+Brunch+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Na Praça de Carlos Alberto, ideal para panquecas e ovos benedict.</p>
                    </div>
                </div>
            </div>

            <!-- Restaurantes Locais -->
            <div class="category-section restaurants">
                <h2 class="section-title">🍷 Restaurantes Locais (Local Restaurants)</h2>
                <div class="grid">
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Casa Guedes</span>
                            <div class="card-actions">
                                <span class="distance-badge">6 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Casa+Guedes+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Famosa pela lendária sande de pernil e excelente rooftop na Praça dos Poveiros.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Restaurante Santiago</span>
                            <div class="card-actions">
                                <span class="distance-badge">6 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Restaurante+Santiago+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Paragem obrigatória para provar a verdadeira Francesinha da cidade.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Abadia do Porto</span>
                            <div class="card-actions">
                                <span class="distance-badge">6 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Abadia+do+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Cozinha tradicional portuguesa muito fiável (bacalhau e tripas).</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Cervejaria Gazela</span>
                            <div class="card-actions">
                                <span class="distance-badge">7 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Cervejaria+Gazela+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Instituição perto da Batalha famosa pelos icónicos e picantes "cachorrinhos".</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Brasão Aliados</span>
                            <div class="card-actions">
                                <span class="distance-badge">12 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Brasao+Aliados+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Francesinha de excelência e cervejas artesanais num espaço decorado (requer reserva).</p>
                    </div>
                </div>
            </div>

            <!-- Fado -->
            <div class="category-section fado">
                <h2 class="section-title">🎸 Onde Ouvir Fado Tradicional (Fado Experience)</h2>
                <div class="grid">
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Casa da Guitarra</span>
                            <div class="card-actions">
                                <span class="distance-badge">12 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Casa+da+Guitarra+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Espaço intimista na Ribeira com espetáculos de Fado ao vivo e Vinho do Porto.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Ideal Clube de Fado</span>
                            <div class="card-actions">
                                <span class="distance-badge">15 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Ideal+Clube+de+Fado+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Casa de fados tradicional perto de São Bento com acústica fantástica.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Caves Cálem</span>
                            <div class="card-actions">
                                <span class="distance-badge">25 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Caves+Calem+Gaia" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Oferecem uma experiência única que junta degustação com espetáculo de Fado.</p>
                    </div>
                </div>
            </div>

            <!-- Nightlife -->
            <div class="category-section nightlife">
                <h2 class="section-title">🌙 Noite, Bares e Cultura (Nightlife & Culture)</h2>
                <div class="grid">
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Galerias Paris e R. Cândido dos Reis</span>
                            <div class="card-actions">
                                <span class="distance-badge">12 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Galerias+Paris+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">O epicentro da vida noturna da Baixa, repletas de bares e pubs animados.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Ribeira do Porto</span>
                            <div class="card-actions">
                                <span class="distance-badge">20 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Ribeira+do+Porto" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Perfeita para um copo ao fim de tarde junto ao rio, com esplanadas e vistas maravilhosas.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">WOW - World of Culture</span>
                            <div class="card-actions">
                                <span class="distance-badge">25 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=WOW+World+of+Wine+Gaia" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Em Vila Nova de Gaia, com museus, restaurantes e uma vista panorâmica sumptuosa sobre o Douro.</p>
                    </div>
                </div>
            </div>

            <!-- Caves Vinho -->
            <div class="category-section caves">
                <h2 class="section-title">🍇 Descubra as Caves do Vinho do Porto (Explore the Port Wine Cellars)</h2>
                <div class="grid">
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Cálem</span>
                            <div class="card-actions">
                                <span class="distance-badge">25 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Caves+Calem+Gaia" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">As mais centrais, junto ao tabuleiro inferior da Ponte D. Luís (provas e museu interativo).</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Sandeman</span>
                            <div class="card-actions">
                                <span class="distance-badge">27 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Sandeman+Gaia" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">A 2 minutos a pé da Cálem, com visitas guiadas pelos icónicos guias com a capa negra do "Don".</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Porto Ferreira</span>
                            <div class="card-actions">
                                <span class="distance-badge">28 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Porto+Ferreira+Caves+Gaia" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Um marco histórico na região, muito ligado à figura de D. Antónia Adelaide Ferreira.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Taylor's</span>
                            <div class="card-actions">
                                <span class="distance-badge">32 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Taylor's+Port+Gaia" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Provas num belíssimo jardim sossegado, acompanhadas por um audioguia moderno.</p>
                    </div>
                    
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Graham's</span>
                            <div class="card-actions">
                                <span class="distance-badge">De Táxi / Uber</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Graham's+Port+Lodge+Gaia" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Experiência premium com vinhos superiores e uma vista panorâmica incrível (recomendamos ir de táxi).</p>
                    </div>
                </div>
            </div>

            <!-- Lavandarias -->
            <div class="category-section laundry">
                <h2 class="section-title">🫧 Lavandarias (Laundry)</h2>
                <div class="grid">
                    <div class="card">
                        <div class="card-header">
                            <span class="card-title">Lavandaria Self-service Marlinwash</span>
                            <div class="card-actions">
                                <span class="distance-badge">1 min a pé</span>
                                <a href="https://www.google.com/maps/search/?api=1&query=Lavandaria+Marlinwash+Rua+da+Alegria" target="_blank" class="btn-clique"><i class="fas fa-hand-pointer"></i> Rota Mapas</a>
                            </div>
                        </div>
                        <p class="card-notes">Localizada na Rua da Alegria nº 166, ideal para lavar roupa de forma rápida bem perto de casa.</p>
                    </div>
                </div>
            </div>

        </div>
    </div>

    <footer>
        <p>&copy; 2026 Oportoview Alegria Apartment. Todos os direitos reservados.</p>
    </footer>

    <script>
        function filterData(category) {
            // Update active button state
            const buttons = document.querySelectorAll('.filter-btn');
            buttons.forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');

            // Filter sections
            const sections = document.querySelectorAll('.category-section');
            sections.forEach(section => {
                if (category === 'all') {
                    section.style.display = 'block';
                } else {
                    if (section.classList.contains(category)) {
                        section.style.display = 'block';
                    } else {
                        section.style.display = 'none';
                    }
                }
            });
        }
    </script>
</body>
</html>
