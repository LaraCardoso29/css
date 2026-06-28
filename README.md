# css
/* Configurações Globais */
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

/* Estilização do Cabeçalho (Aula 5 e Aula 6) */
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

/* Área dos Cards (Aula 5) */
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

/* Estrutura dos Flashcards (Aula 4, Aula 7 e Aula 8) */
.cartao {
    width: 300px;
    height: 400px;
    perspective: 1000px; /* Efeito 3D */
    cursor: pointer;
}

.cartao__conteudo {
    width: 100%;
    height: 100%;
    position: relative;
    transform-style: preserve-3d;
    transition: transform 0.6s;
    border-radius: 20px; /* Bordas arredondadas (Aula 7) */
    box-shadow: 4px 4px 15px rgba(0, 0, 0, 0.15); /* Sombra (Aula 7) */
}

/* Efeito de virar o card ao passar o mouse */
.cartao:hover .cartao__conteudo {
    transform: rotateY(180deg);
}

/* Faces do Cartão */
.cartao__conteudo__frente, .cartao__conteudo__verso {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden; /* Esconde a face de trás */
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 25px;
    text-align: center;
    border-radius: 20px;
}

/* Estilo da Frente (Aula 6) */
.cartao__conteudo__frente {
    background-color: #ffffff;
    color: #1a2530;
    border: 2px solid #e2e8f0;
}

/* Espaço reservado para a imagem usando um placeholder temático */
.cartao__conteudo__frente::before {
    content: "";
    width: 120px;
    height: 120px;
    margin-bottom: 20px;
    background-image: url('https://via.placeholder.com/120/2a9d8f/ffffff?text=Elefante');
    background-size: cover;
    background-position: center;
    border-radius: 50%;
    border: 3px solid #2a9d8f;
}

.cartao__conteudo__frente h3 {
    font-size: 20px;
    font-weight: 600;
}

/* Estilo do Verso (Aula 6) */
.cartao__conteudo__verso {
    background-color: #2a9d8f;
    color: #ffffff;
    transform: rotateY(180deg);
}

.cartao__conteudo__verso p {
    font-size: 16px;
    line-height: 1.6;
}

/* Estilização do Rodapé (Aula 3, Aula 6) */
.rodape {
    background-color: #1a2530;
    color: #ffffff;
    text-align: center;
    padding: 15px;
    font-size: 16px;
    border-top: 3px solid #2a9d8f;
}
