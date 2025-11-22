<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Кейс-дослідження: Професійна освіта</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

    <style>
        /* --- Основні стилі --- */
        body {
            font-family: 'Segoe UI', 'Open Sans', sans-serif;
            line-height: 1.6;
            background-color: #f4f6f8;
            color: #333;
            margin: 0;
            padding: 0;
        }

        /* --- Навігація --- */
        nav {
            background-color: #2c3e50;
            padding: 15px 0;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        nav a {
            color: #ecf0f1;
            text-decoration: none;
            margin: 0 15px;
            font-weight: 600;
            font-size: 1.1rem;
            transition: color 0.3s;
        }

        nav a:hover { color: #3498db; }

        /* --- Заголовок --- */
        .hero {
            /* Фото: Інженерне креслення (Стабільне фото з Wikimedia) */
            background: linear-gradient(rgba(44, 62, 80, 0.9), rgba(44, 62, 80, 0.7)), url('https://upload.wikimedia.org/wikipedia/commons/thumb/0/02/Engineering_drawing_p1090449.jpg/1280px-Engineering_drawing_p1090449.jpg') no-repeat center center/cover;
            color: white;
            text-align: center;
            padding: 80px 20px;
            margin-bottom: 30px;
        }

        .hero h1 { font-size: 2.5em; margin-bottom: 10px; }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* --- Блоки країн --- */
        section {
            background: white;
            border-radius: 10px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
        }

        h2 {
            color: #2c3e50;
            border-bottom: 3px solid #3498db;
            display: inline-block;
            margin-top: 0;
        }

        .country-card {
            display: flex;
            gap: 30px;
            margin-top: 25px;
            align-items: flex-start;
        }

        .country-card.reversed { flex-direction: row-reverse; }

        /* --- Фото країн --- */
        .country-img {
            width: 45%;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            border: 1px solid #ddd;
        }

        .content { flex: 1; }

        ul { padding-left: 20px; }
        li { margin-bottom: 8px; }

        /* --- Відео --- */
        .video-wrapper {
            margin-top: 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            overflow: hidden;
            background: #000;
        }

        .video-container {
            position: relative;
            padding-bottom: 56.25%; /* 16:9 */
            height: 0;
        }

        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: 0;
        }

        /* Кнопка резервного посилання */
        .video-fallback {
            display: inline-block;
            margin-top: 8px;
            font-size: 0.9em;
            color: #3498db;
            text-decoration: none;
            font-weight: bold;
        }
        .video-fallback:hover { text-decoration: underline; }

        /* --- Таблиця --- */
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        th, td {
            border: 1px solid #eee;
            padding: 12px;
            text-align: left;
        }
        th { background-color: #34495e; color: white; }
        tr:nth-child(even) { background-color: #f9f9f9; }

        footer {
            text-align: center;
            padding: 30px;
            margin-top: 50px;
            color: #7f8c8d;
            font-size: 0.9em;
        }

        /* Адаптивність для мобільних */
        @media (max-width: 768px) {
            .country-card, .country-card.reversed { flex-direction: column; }
            .country-img { width: 100%; height: auto; }
            table, thead, tbody, th, td, tr { display: block; }
            thead tr { display: none; }
            tr { margin-bottom: 10px; border: 1px solid #ccc; }
            td { border: none; border-bottom: 1px solid #eee; position: relative; padding-left: 50%; }
            td:before { position: absolute; left: 10px; font-weight: bold; content: attr(data-label); }
        }
    </style>
</head>
<body>

    <nav>
        <a href="#germany">Німеччина</a>
        <a href="#switzerland">Швейцарія</a>
        <a href="#austria">Австрія</a>
        <a href="#comparison">Порівняння</a>
    </nav>

    <div class="hero">
        <h1>Професійна освіта: DACH</h1>
        <p>Аналіз моделей підготовки технічних фахівців</p>
    </div>

    <div class="container">
        
        <section id="germany">
            <h2><i class="fas fa-flag"></i> Німеччина</h2>
            <div class="country-card">
                <img class="country-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/46/VW_Wolfsburg_Produktion_Halle_54_Golf_Montage.jpg/800px-VW_Wolfsburg_Produktion_Halle_54_Golf_Montage.jpg" alt="Завод Volkswagen">
                
                <div class="content">
                    <p><b>Модель:</b> Класична дуальна система. Робота на заводі + теорія в школі.</p>
                    <ul>
                        <li><i class="fas fa-cogs"></i> <b>Масштаб:</b> Понад 300 професій.</li>
                        <li><i class="fas fa-euro-sign"></i> <b>Оплата:</b> Учні отримують зарплату.</li>
                    </ul>
                    
                    <div class="video-wrapper">
                        <div class="video-container">
                            <iframe src="https://www.youtube.com/embed/sXhBEtt2gMk" allowfullscreen></iframe>
                        </div>
                    </div>
                    <a href="https://www.youtube.com/watch?v=sXhBEtt2gMk" target="_blank" class="video-fallback">
                        <i class="fas fa-external-link-alt"></i> Якщо відео не працює, натисніть тут
                    </a>
                </div>
            </div>
        </section>

        <section id="switzerland">
            <h2><i class="fas fa-flag"></i> Швейцарія</h2>
            <div class="country-card reversed">
                <img class="country-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/CERN_LHC_Tunnel_HDR.jpg/800px-CERN_LHC_Tunnel_HDR.jpg" alt="Технології CERN">
                
                <div class="content">
                    <p><b>Модель:</b> Високотехнологічна та гнучка. Престижний вибір для молоді.</p>
                    <ul>
                        <li><i class="fas fa-university"></i> <b>ВНЗ:</b> Легкий шлях до вищої освіти.</li>
                        <li><i class="fas fa-microchip"></i> <b>Інновації:</b> Швидке оновлення програм.</li>
                    </ul>

                    <div class="video-wrapper">
                        <div class="video-container">
                            <iframe src="https://www.youtube.com/embed/Qx0uL2_x4_U" allowfullscreen></iframe>
                        </div>
                    </div>
                    <a href="https://www.youtube.com/watch?v=Qx0uL2_x4_U" target="_blank" class="video-fallback">
                        <i class="fas fa-external-link-alt"></i> Якщо відео не працює, натисніть тут
                    </a>
                </div>
            </div>
        </section>

        <section id="austria">
            <h2><i class="fas fa-flag"></i> Австрія</h2>
            <div class="country-card">
                <img class="country-img" src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/88/HTL_M%C3%B6dling_Hauptgeb%C3%A4ude.jpg/800px-HTL_M%C3%B6dling_Hauptgeb%C3%A4ude.jpg" alt="HTL Коледж">
                
                <div class="content">
                    <p><b>Модель:</b> Унікальне поєднання дуальної системи та технічних коледжів (HTL).</p>
                    <ul>
                        <li><i class="fas fa-school"></i> <b>HTL:</b> 5 років навчання = інженер.</li>
                        <li><i class="fas fa-shield-alt"></i> <b>Гарантії:</b> Держава підтримує кожного.</li>
                    </ul>

                    <div class="video-wrapper">
                        <div class="video-container">
                            <iframe src="https://www.youtube.com/embed/J72cPhyQWqA" allowfullscreen></iframe>
                        </div>
                    </div>
                    <a href="https://www.youtube.com/watch?v=J72cPhyQWqA" target="_blank" class="video-fallback">
                        <i class="fas fa-external-link-alt"></i> Якщо відео не працює, натисніть тут
                    </a>
                </div>
            </div>
        </section>

        <section id="comparison">
            <h2><i class="fas fa-table"></i> Порівняння</h2>
            <table>
                <thead>
                    <tr>
                        <th>Характеристика</th>
                        <th>Німеччина 🇩🇪</th>
                        <th>Швейцарія 🇨🇭</th>
                        <th>Австрія 🇦🇹</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td data-label="Характеристика"><b>Роль бізнесу</b></td>
                        <td data-label="Німеччина">Висока</td>
                        <td data-label="Швейцарія">Дуже висока</td>
                        <td data-label="Австрія">Висока + Палати</td>
                    </tr>
                    <tr>
                        <td data-label="Характеристика"><b>Унікальність</b></td>
                        <td data-label="Німеччина">Масштабність</td>
                        <td data-label="Швейцарія">Проникність</td>
                        <td data-label="Австрія">Коледжі HTL</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <footer>
            <p>&copy; 2025 Дослідження освітніх систем.</p>
        </footer>

    </div>

</body>
</html>
