# css
/* Configurações Globais para Resetar Margens */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #f4f6f9;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

/* AULA 5 e 6: Cabeçalho com Flexbox e Cores Alteradas */
.cabecalho {
    background-color: #1a2530;
    color: #ffffff;
    padding: 20px 40px;
    display: flex;
    justify-content: space-between; /* Desafio Aula 5 */
    align-items: center;            /* Desafio Aula 5 */
}

.cabecalho__logo span {
    font-size: 24px; /* Desafio Aula 6 */
    font-weight: bold;
    color: #2a9d8f;  /* Desafio Aula 6 */
}

.cabecalho__menu a {
    color: #ffffff;
    text-decoration: none;
    margin-left: 20px;
    font-size: 18px;
    transition: color 0.3s;
}

.cabecalho__menu a:hover {
    color: #2a9d8f;
}

/* AULA 5: Distribuição Espacial dos Cards */
.conteudo-principal {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 40px;
}

.container-cards {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
    justify-content: center;
}

/* AULA 4, 7 e 8: Estrutura Físico-Visual do Cartão */
.cartao {
    width: 300px;  /* Dimensões Desafio Aula 4 */
    height: 400px; /* Dimensões Desafio Aula 4 */
    perspective: 1000px; /* Ativa o ambiente 3D */
    cursor: pointer;
}

.cartao__conteudo {
    width: 100%;
    height: 100%;
    position: relative;
    transform-style: preserve-3d;
    transition: transform 0.6s ease;
}

/* AULA 8: Animação que faz o Flashcard Virar */
.cartao:hover .cartao__conteudo {
    transform: rotateY(180deg);
}

/* Configurações de Ocultação Traseira para Corrigir o Preview */
.cartao__conteudo__frente, 
.cartao__conteudo__verso {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden; /* CORREÇÃO: Esconde o verso enquanto a frente aparece */
    -webkit-backface-visibility: hidden;
    border-radius: 20px; /* Bordas Arredondadas - Desafio Aula 7 */
    box-shadow: 4px 4px 15px rgba(0, 0, 0, 0.15); /* Sombra - Desafio Aula 7 */
    display: flex;
    flex-direction: column;
    padding: 25px; /* Padding Desafio Aula 4 */
    text-align: center;
}

/* Visual Frontal Base (Preview Inicial Alinhado) */
.cartao__conteudo__frente {
    background-color: #ffffff;
    color: #ffffff;
    background-size: cover;
    background-position: center;
    justify-content: flex-end; /* Garante o texto na base sobre a imagem */
    transform: rotateY(0deg);  /* Fixa a orientação correta inicial */
    position: relative;
    overflow: hidden;
}

/* Filtro escuro para dar contraste e permitir a leitura correta das frases */
.cartao__conteudo__frente::after {
    content: "";
    position: absolute;
    top: 0; left: 0; width: 100%; height: 100%;
    background: linear-gradient(to bottom, rgba(0,0,0,0) 40%, rgba(0,0,0,0.8) 100%);
    border-radius: 20px;
    z-index: 1;
}

.cartao__conteudo__frente h3 {
    font-size: 20px;
    font-weight: 600;
    z-index: 2;
    text-shadow: 1px 1px 4px rgba(0,0,0,0.8);
}

/* Imagens Temáticas Reais Aplicadas nos Flashcards */
.card-elefante {
    background-image: url('https://picsum.photos/id/1024/300/400');
}

.card-tromba {
    background-image: url('https://picsum.photos/id/244/300/400');
}

.card-fake {
    background-image: url('https://picsum.photos/id/124/300/400');
}

/* Estilização Interna do Verso (Resposta Oculta) */
.cartao__conteudo__verso {
    background-color: #2a9d8f; /* Cor do Verso */
    color: #ffffff;
    justify-content: center;
    transform: rotateY(180deg); /* Mantém virado para trás inicialmente */
}

.cartao__conteudo__verso
