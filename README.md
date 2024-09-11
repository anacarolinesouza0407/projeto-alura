# projeto-alura
projeto aluraflix, painel de vídeos selecionados do youtube e com a linguagem css e html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vídeos de Beleza</title>
    <style>
        body {
            background-color: #fbeffb; /* Rosa claro */
            margin: 0;
            font-family: Arial, sans-serif;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        .main-title {
            font-size: 36px;
            font-weight: bold;
            color: #FF69B4; /* Rosa forte */
            text-align: center;
            margin-bottom: 40px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }
        .button-container {
            margin-bottom: 20px;
            text-align: center;
        }
        .button-container button {
            background-color: #b0e0e6; /* Azul bebê */
            border: none;
            color: #fff;
            padding: 10px 20px;
            font-size: 16px;
            border-radius: 5px;
            margin: 0 10px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .button-container button:hover {
            background-color: #87ceeb; /* Azul mais claro */
        }
        .video-section {
            display: none;
        }
        .video-section.active {
            display: block;
        }
        .video-list {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        .video-item {
            flex: 1 1 calc(33.333% - 20px);
            border: 4px solid #b0e0e6; /* Azul bebê */
            border-radius: 10px;
            overflow: hidden;
            background-color: #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .video-item:hover {
            transform: scale(1.05); /* Efeito de destaque */
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
        }
        .video-item iframe {
            width: 100%;
            height: 168px; /* Proporção 16:9 */
        }
        .video-title {
            font-weight: bold;
            font-size: 18px;
            color: #000;
            margin: 10px;
        }
        .video-description {
            font-size: 14px;
            color: #333;
            margin: 0 10px 10px;
        }
        .hair-section {
            background-color: #e8f4f8; /* Azul muito claro */
            padding: 20px;
            border-radius: 10px;
        }
        .clothing-section {
            background-color: #f8e8f4; /* Rosa muito claro */
            padding: 20px;
            border-radius: 10px;
        }
        .skin-section {
            background-color: #e8f8e8; /* Verde muito claro */
            padding: 20px;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="main-title">
            Cuidados Pessoais para Garotas
        </div>

        <div class="button-container">
            <button onclick="showSection('hair')">Cabelo</button>
            <button onclick="showSection('clothing')">Roupa</button>
            <button onclick="showSection('skin')">Pele</button>
        </div>

        <div id="hair" class="video-section hair-section">
            <h2>Cabelo</h2>
            <div class="video-list">
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/PoGeiS5gLhk?si=e7ezBj9JufLBJsBi" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 1</div>
                    <div class="video-description">Descrição do vídeo 1: Cuidados e dicas para cabelos.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/kDSN__2aKqM?si=btWCKgzHsQj6aERi" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 2</div>
                    <div class="video-description">Descrição do vídeo 2: Estilos e tendências para cabelo.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/riDAjeFEMKE?si=yKXAzjmD_k-d-W5V" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 3</div>
                    <div class="video-description">Descrição do vídeo 3: Cuidados especiais para cabelos.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/T6FROhpSs2Y?si=Zck6ADhfNrrD9idf" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 4</div>
                    <div class="video-description">Descrição do vídeo 4: Dicas de penteados e tratamentos.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/r95PNWUmFTI?si=xADPni7l6j1Qb9qL" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 5</div>
                    <div class="video-description">Descrição do vídeo 5: Produtos recomendados para cabelo.</div>
                </div>
            </div>
        </div>

        <div id="clothing" class="video-section clothing-section">
            <h2>Roupa</h2>
            <div class="video-list">
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/IJSGXS4nrRw?si=03lBLP-zqhPrTHsN" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 1</div>
                    <div class="video-description">Descrição do vídeo 1: Tendências de moda e estilo.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/mZTKYRfHz3I?si=7ZzGeXttwvqQw90z" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 2</div>
                    <div class="video-description">Descrição do vídeo 2: Looks para diferentes ocasiões.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/yHLtUMgIRrc?si=G6az9fGQpYlv6Bro" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 3</div>
                    <div class="video-description">Descrição do vídeo 3: Dicas de combinação de roupas.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/PdaiuFPa9fo?si=epLDVx0yyLRQyLxW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 4</div>
                    <div class="video-description">Descrição do vídeo 4: Como escolher a roupa ideal.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/OAlngENqHJA?si=SenZRRVuLPUexlnO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 5</div>
                    <div class="video-description">Descrição do vídeo 5: Estilos e tendências de moda.</div>
                </div>
            </div>
        </div>

        <div id="skin" class="video-section skin-section">
            <h2>Pele</h2>
            <div class="video-list">
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/NJIhVj1x-k4?si=YJC8mnxLwyWXWUm8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 1</div>
                    <div class="video-description">Descrição do vídeo 1: Cuidados com a pele para todos os tipos.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/ldI2GJNDZwU?si=u-iinrCmh7E2v2FN" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 2</div>
                    <div class="video-description">Descrição do vídeo 2: Dicas de cuidados diários com a pele.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/qa9h7vA_IYY?si=3MUJsucuPnaQmC-G" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 3</div>
                    <div class="video-description">Descrição do vídeo 3: Rotina de cuidados para pele saudável.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/05A0jxlx9Ks?si=K0J8ZVEklJz3r7Bk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 4</div>
                    <div class="video-description">Descrição do vídeo 4: Produtos recomendados para cuidados com a pele.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/vxmvNeShK3g?si=GhTuoyUh0tmmCzn9" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 5</div>
                    <div class="video-description">Descrição do vídeo 5: Tendências e cuidados para a pele.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/L4n_d5EFHb4?si=SD6WmygvdGRYcEBB" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 6</div>
                    <div class="video-description">Descrição do vídeo 6: Cuidados essenciais com a pele.</div>
                </div>
                <div class="video-item">
                    <iframe src="https://www.youtube.com/embed/Ed-TAuZxwIo?si=GRQLS8qNQySiE54_" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                    <div class="video-title">Título do Vídeo 7</div>
                    <div class="video-description">Descrição do vídeo 7: Como manter a pele saudável e bonita.</div>
                </div>
            </div>
        </div>
    </div>

    <script>
        function showSection(sectionId) {
            // Ocultar todas as seções
            document.querySelectorAll('.video-section').forEach(section => {
                section.classList.remove('active');
            });
            // Mostrar a seção selecionada
            document.getElementById(sectionId).classList.add('active');
        }
        // Mostrar a primeira seção por padrão
        document.addEventListener('DOMContentLoaded', () => {
            showSection('hair');
        });
    </script>
</body>
</html>
