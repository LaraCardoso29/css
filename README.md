# css
/* Configurações Globais para zerar margens */
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

/* Estrutura Flexível do Cabeçalho */
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

/* Área de Distribuição dos Cards na Tela */
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

/* Tamanho do Cartão e Perspectiva */
.cartao {
    width: 300px;
    height: 400px;
    perspective: 1000px; /* Ativa o efeito 3D no navegador */
    cursor: pointer;
}

/* O container que vai girar */
.cartao__conteudo {
    width: 100%;
    height: 100%;
    position: relative;
    transform-style: preserve-3d;
    transition: transform 0.6s ease;
}

/* Gira o card horizontalmente ao passar o mouse */
.cartao:hover .cartao__conteudo {
    transform: rotateY(180deg);
}

/* Configuração idêntica para as duas faces (Frente e Verso) */
.cartao__conteudo__frente, 
.cartao__conteudo__verso {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden; /* CORREÇÃO CRÍTICA: Esconde o lado
