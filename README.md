# css
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projeto Final - Flashcards de Estudo</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="cabecalho">
        <div class="cabecalho__logo">
            <span>BioWeb Cards</span>
        </div>
        <nav class="cabecalho__menu">
            <a href="#">Home</a>
            <a href="#">Meus Cards</a>
        </nav>
    </header>

    <main class="conteudo-principal">
        <section class="container-cards">

            <div class="cartao">
                <div class="cartao__conteudo">
                    <div class="cartao__conteudo__frente card-elefante">
                        <h3>Qual é o maior mamífero terrestre do planeta?</h3>
                    </div>
                    <div class="cartao__conteudo__verso">
                        <p><strong>O Elefante Africano!</strong><br><br>Eles podem pesar até 7 toneladas e medir cerca de 3,3 metros de altura. Suas grandes orelhas ajudam a irradiar calor para manter o corpo fresco.</p>
                    </div>
                </div>
            </div>

            <div class="cartao">
                <div class="cartao__conteudo">
                    <div class="cartao__conteudo__frente card-tromba">
                        <h3>Para que serve a tromba do elefante?</h3>
                    </div>
                    <div class="cartao__conteudo__verso">
                        <p>A tromba serve para respirar, cheirar, beber água, pegar objetos e se comunicar. Ela contém mais de 40.000 músculos e nenhuma estrutura óssea!</p>
                    </div>
                </div>
            </div>

            <div class="cartao">
                <div class="cartao__conteudo">
                    <div class="cartao__conteudo__frente card-fake">
                        <h3>NASA confirma 15 dias de escuridão total na Terra em 2026?</h3>
                    </div>
                    <div class="cartao__conteudo__verso">
                        <p><strong>FALSA!</strong><br><br>Essa notícia é um boato que circula desde 2015[cite: 12]. A NASA nunca fez tal anúncio e o planeta sempre terá iluminação solar em pelo menos um hemisfério[cite: 12].</p>
                    </div>
                </div>
            </div>

        </section>
    </main>

    <footer class="rodape">
        <p>Desenvolvido por: <strong>[Insira Seu Nome Aqui]</strong></p>
    </footer>

</body>
</html>
