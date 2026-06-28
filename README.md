# css
/* Configurações Globais (Reset) */
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

/* Layout do Cabeçalho */
.cabecalho {
    background-color: #1a2530;
    color: #ffffff;
    padding: 20px 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.cabecalho__logo span {
    font-size: 24px;
    font-weight: bold;
    color: #2a9d8f;
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

/* Alinhamento dos Cartões */
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

/* Estrutura do Cartão e Efeito 3D */
.cartao {
    width: 300px;
    height: 400px;
    perspective: 1000px; /* Crucial para o efeito de virar funcionar em 3D */
    cursor: pointer;
}

.cartao__conteudo {
    width: 100%;
    height: 100%;
    position: relative;
    transform-style: preserve-3d;
    transition: transform 0.6s ease;
}

/* Faz o cartão girar no eixo Y ao passar o mouse */
.cartao:hover .cartao__conteudo {
    transform: rotateY(180deg);
}

/* Configurações das Faces do Cartão */
.cartao__conteudo__frente, 
.cartao__conteudo__verso {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden; /* IMPORTANTE: Esconde o verso enquanto a frente aparece */
    -webkit-backface-visibility: hidden; /* Correção para navegadores antigos/safari */
    border-radius: 20px;
    box-shadow: 4px 4px 15px rgba(0, 0, 0, 0.15);
    display: flex;
    flex-direction: column;
    padding: 25px;
    text-align: center;
}

/* Face da Frente */
.cartao__conteudo__frente {
    background-color: #ffffff;
    color: #ffffff;
    background-size: cover;
    background-position: center;
    justify-content: flex-end; /* Texto alinhado na base */
    transform: rotateY(0deg); /* Começa virado para frente */
    position: relative;
    overflow: hidden;
}

/* Filtro escuro para dar contraste ao texto branco */
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

/* Imagens reais dos cartões */
.card-elefante {
    background-image: url('https://picsum.photos/id/1024/300/400');
}

.card-tromba {
    background-image: url('https://picsum.photos/id/244/300/400');
}

.card-fake {
    background-image: url('https://picsum.photos/id/124/300/400');
}

/* Face do Verso (Escondida) */
.cartao__conteudo__verso {
    background-color: #2a9d8f;
    color: #ffffff;
    justify-content: center; /* Centraliza o texto explicativo */
    transform: rotateY(180deg); /* Começa invertido e oculto */
}

.cartao__conteudo__verso p {
    font-size: 16px;
    line-height: 1.6;
}

/* Rodapé */
.rodape {
    background-color: #1a2530;
    color: #ffffff;
    text-align: center;
    padding: 15px;
    font-size: 16px;
    border-top: 3px solid #2a9d8f;
}

 
