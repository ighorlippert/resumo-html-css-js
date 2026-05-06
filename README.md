## Nome: Ighor Rossetto Lippert

# HTML 📄

### O que é HTML

O HTML ele não é uma linguagem de programação, mas sim uma linguagem de marcação usada para estruturar e dar significado ao conteúdo da web.



### Estrutura Do Documento

**`<!DOCTYPE html>`**: Informa ao navegador que estamos usando a versão mais recente do HTML (HTML5).

**`<html>`**: A tag raiz que envolve todo o código. O atributo **`lang="pt-BR"`** ajuda motores de busca e leitores de tela a saberem o idioma do site.

**`<head>`**: O "cérebro" da página. Contém metadados invisíveis para o usuário final, como a codificação de caracteres (**`<meta charset="UTF-8">`**), configurações de responsividade (**`viewport`**) e o título da aba do navegador (**`<title>`**).

**`<body>`**: O corpo da página. Tudo o que o usuário vê (*textos, imagens, botões*) fica aqui dentro.

    <!DOCTYPE html>
    <html lang="pt-BR">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Minha Primeira Página</title>
    </head>
    <body>
        <h1>Olá, Mundo!</h1>
    </body>
    </html>

>**Em Visual Code, usando `!` ele já cria a estrutura.**

### Tags Mais Usadas

Tags sempre tem uma abertura `<tag>` e uma de fechamento `</tag>`. Sempre que abrir uma, logo em seguida fechar para não se acabar se perdendo.

### Textos e Títulos

 **`<h1>`** a **`<h6>`**: Definem títulos e subtítulos. O **`<h1>`** é o mais importante (*o título principal da página*) e o **`<h6>`** é o menos importante. Nunca use essas tags apenas para deixar o texto maior ou em negrito; elas servem para hierarquia de informação.
    
**`<p>`**: Define um parágrafo de texto.

    <h1>Receita de Bolo de Cenoura</h1>
    
    <p>Esta é uma receita de família muito fácil de fazer e que fica uma delícia!</p>
    
    <h2>Ingredientes</h2>
    <p>Você vai precisar de cenouras, farinha, açúcar, ovos e óleo.</p>
    
    <h2>Modo de Preparo</h2>
    
    <h3>Preparando a Massa</h3>
    <p>Bata as cenouras com o óleo e os ovos no liquidificador.</p>
    
    <h3>Preparando a Cobertura</h3>
    <p>Misture o chocolate em pó com a manteiga e o leite no fogo.</p>

### Estrutura e Containers

**`<div>`**: É um contêiner genérico de bloco. Usado para agrupar elementos, principalmente para aplicar estilos com CSS ou manipular com JavaScript.
    
**`<span>`**: Similar à **`<div>`**, mas é um contêiner _inline_ (*em linha*). Usado para estilizar uma pequena parte de um texto dentro de um parágrafo, por exemplo.

    <div class="cartao-produto">
        <h2>Tênis de Corrida</h2>
        
        <p>Compre agora por apenas <span style="color: red; font-weight: bold;">R$ 199,00</span>!</p>
        
        <p>Este tênis é perfeito para corridas longas e caminhadas.</p>
    </div>
    
    <div class="avisos">
        <p>Atenção: Promoção válida apenas até amanhã.</p>
    </div>

### Links e Mídia

**`<a>`**: Cria um hiperlink. Usa o atributo **`href`** para indicar o destino (*uma URL ou outra seção da mesma página*). Exemplo:**`<a href="https://google.com">Ir para o Google</a>`**.
    
 **`<img>`**: Insere uma imagem. **Não possui tag de fechamento.** Usa o atributo **`src`** para o caminho da imagem e **`alt`** para o texto alternativo (*crucial para acessibilidade*). Exemplo: **`<img src="foto.jpg" alt="Cachorro brincando no parque">`**.

    <p>Para mais informações, <a href="https://pt.wikipedia.org">leia o artigo na Wikipedia</a>.</p>
    
    <a href="https://google.com" target="_blank">Pesquisar no Google</a>
    
    <img src="foto-da-praia.jpg" alt="Pessoas caminhando na areia da praia ao pôr do sol">
    
    <a href="https://meusite.com/produtos">
        <img src="banner-promocao.png" alt="Clique aqui para ver nossos produtos em promoção">
    </a>

### Formulários

Usados para coletar dados do usuário.

**`<form>`**: O contêiner principal do formulário.
    
**`<input>`**: Cria campos de entrada de dados. O tipo muda conforme o atributo **`type`** (**`text`, `email`, `password`, `checkbox`, `radio`**, etc.). Não tem tag de fechamento.
    
**`<label>`**: Define um rótulo descritivo para o **`<input>`**. Muito importante para usabilidade e acessibilidade.
    
**`<button>`**: Cria um botão clicável (*para enviar o formulário ou disparar uma ação*).

    <form action="/cadastrar-usuario">
        
        <div>
            <label for="nome">Nome Completo:</label>
            <input type="text" id="nome" name="nome" placeholder="Digite seu nome">
        </div>
        
        <div>
            <label for="email">E-mail:</label>
            <input type="email" id="email" name="email" placeholder="seu@email.com">
        </div>
        
        <div>
            <label for="senha">Senha:</label>
            <input type="password" id="senha" name="senha">
        </div>
    
        <div>
            <p>Qual seu período favorito?</p>
            
            <input type="radio" id="manha" name="periodo" value="manha">
            <label for="manha">Manhã</label>
            
            <input type="radio" id="tarde" name="periodo" value="tarde">
            <label for="tarde">Tarde</label>
        </div>
        
        <button type="submit">Criar Conta</button>
    
    </form>


### Listas

**`<ul>`**: Lista não ordenada (*com marcadores/bolinhas*).
    
**`<ol>`**: Lista ordenada (*com números*).
    
**`<li>`**: Cada item dentro de uma lista **`<ul>`** ou **`<ol>`**.
#### Lista Não Ordenada
    <h3>Lista de Compras do Supermercado</h3>
    <ul>
        <li>Maçã</li>
        <li>Leite</li>
        <li>Pão de forma</li>
        <li>Café</li>
    </ul>

#### Lista Ordenada

    <h3>Como trocar uma lâmpada</h3>
    <ol>
        <li>Desligue o interruptor de energia.</li>
        <li>Espere a lâmpada antiga esfriar.</li>
        <li>Desrosqueie a lâmpada velha com cuidado.</li>
        <li>Rosqueie a lâmpada nova no bocal.</li>
        <li>Ligue o interruptor para testar.</li>
    </ol>
    
#### Listas Aninhadas / Menu de Navegação

    <ul>
        <li>Primeiro item solto</li>
        <li>Segundo item solto</li>
        <li>Terceiro item solto</li>
    </ul>
    
    <ol>
        <li>Primeiro passo</li>
        <li>Segundo passo</li>
        <li>Terceiro passo</li>
    </ol>

### Boas Praticas

**HTML Semântico:** Use tags que expliquem o que o conteúdo é (como **`<header>`, `<main>`, `<footer>`**) em vez de empilhar dezenas de **`<div>`** genéricas. Isso faz o Google adorar o seu site (*SEO*) e ajuda pessoas com deficiência visual.
    
   **Identação (Alinhamento):** Dê espaços (*Tabs*) no teclado para empurrar o código "filho" mais para a direita do que o código "pai". Um código organizado visualmente evita muita dor de cabeça na hora de encontrar erros.
    
**Acessibilidade (a11y):** Não deixe ninguém de fora. Sempre coloque textos explicativos nas suas imagens usando o atributo **`alt`** e conecte os rótulos (**`<label>`**) aos campos de digitação.
    
**Use Letras Minúsculas:** O padrão profissional mundial é escrever tudo em minúsculo (ex: **`<section>`**, nunca **`<SECTION>`**). Fica mais limpo e rápido de digitar.
    
**Sempre Feche as Tags:** O que você abre, você tem que fechar (ex: abriu **`<p>`**, feche com **`</p>`**). Esquecer uma simples barra **`/`** pode quebrar todo o visual do site.


# CSS 🎨

### O que é CSS

Voltando à nossa analogia da casa, se o HTML constrói as paredes, o CSS é responsável pela pintura, pelos quadros e pela disposição dos móveis.

### Seletor

Para o CSS estilizar um elemento, ele precisa saber "quem" ele deve alterar. Fazemos isso através dos **seletores**.

**Seletor de Tag:** Altera todos os elementos daquela tag no site.

    p {
        color: blue; /* Deixa todos os parágrafos azuis */
    }

**Seletor de Classe (`.`):** É o mais utilizado. Você cria uma classe no HTML (ex: **`<div class="destaque">`**) e a chama no CSS usando um ponto. Pode ser repetida várias vezes.

    .destaque {
        font-size: 20px;
    }

**Seletor de ID (`#`):** Usado para um elemento **único** na página (ex: **`<div id="cabecalho">`**). Chamado com a hashtag.

    #cabecalho {
        background-color: black;
    }

### Propriedades Essenciais

O CSS possui centenas de propriedades, mas você usará um grupo pequeno na maior parte do tempo.

#### Textos e Cores

**`color`**: Muda a cor do texto (ex: **`color: red;`** ou **`color: #ff0000;`**).
    
**`font-size`**: Altera o tamanho da fonte (ex:**`font-size: 16px;`**).

    .titulo-principal {
        color: #2b2b2b; /* Um tom de cinza bem escuro */
        font-size: 36px; /* Deixa a fonte grande */
    }
    
    .texto-destaque {
        color: blue; /* Deixa o texto azul */
        font-size: 18px; /* Tamanho um pouco maior que o padrão */
    }

#### O Modelo de Caixa (Box Model)

Na web, **absolutamente tudo é uma caixa retangular**, mesmo que a imagem pareça redonda. Entender as caixas é o segredo do CSS.

**`padding` (Preenchimento):** É o espaço **interno**. A distância entre o conteúdo (*o texto, por exemplo*) e a borda da caixa. Se você aumentar o padding de um botão, ele fica mais "gordinho".
    
**`margin` (Margem):** É o espaço **externo**. Ele empurra as outras caixas para longe (*ex: a distância entre dois parágrafos*).

    .botao-comprar {
        background-color: green;
        color: white;
        
        /* PADDING (Espaço Interno): 15px em cima/embaixo, 30px nas laterais */
        padding: 15px 30px; 
        
        /* MARGIN (Espaço Externo): Empurra os parágrafos de cima e de baixo para longe em 20px */
        margin: 20px 0; 
        
        /* Bônus: arredonda as pontas da caixa */
        border-radius: 5px; 
        
        /* Tira o sublinhado padrão do link */
        text-decoration: none; 
        
        /* Necessário para o margin funcionar corretamente em elementos <a> */
        display: inline-block; 
    }
    
#### Layout e Posicionamento

A propriedade **`display`** define como a caixa se comporta na tela.

**`display: none;`**: Esconde o elemento da tela.
    
**`display: block;`**: O elemento ocupa toda a largura disponível (como um `<p>` ou `<div>`), empurrando o resto para a linha de baixo.
    
**`display: inline;`**: O elemento ocupa apenas o seu próprio tamanho e permite que outros fiquem do lado (como um `<a>` ou `<span>`).

    .caixa-escondida {
        display: none; /* O elemento some completamente da tela */
    }
    
    .em-linha {
        display: inline; /* Comportamento padrão do <span>. Ficam na mesma linha */
        background-color: yellow;
    }
    
    .em-bloco {
        display: block; /* Comportamento padrão da <div>. Quebra a linha */
        background-color: lightblue;
    }
        

#### Flexbox e Grid (Layouts Modernos)

Antigamente, posicionar elementos lado a lado era um pesadelo. Hoje, temos duas ferramentas incríveis embutidas no CSS:

**Flexbox (`display: flex;`):** Perfeito para alinhar elementos em **uma direção** (*uma linha ou uma coluna*). É ideal para menus de navegação, para centralizar perfeitamente um botão no meio da tela ou para alinhar itens dentro de um cartão.

    .menu-flex {
        display: flex; /* Ativa o Flexbox no contêiner "pai" */
        
        /* Distribui o espaço entre os itens uniformemente */
        justify-content: space-around; 
        
        /* Centraliza os itens verticalmente (se o contêiner fosse mais alto) */
        align-items: center; 
        
        background-color: #eee;
        padding: 20px;
    }
    
**Grid (`display: grid;`):** Perfeito para layouts em **duas dimensões** (*linhas e colunas ao mesmo tempo*). É ideal para construir a "planta baixa" do seu site, dividindo onde fica o cabeçalho, a barra lateral, a área principal e o rodapé.

    .layout-grid {
        display: grid; /* Ativa o Grid no contêiner "pai" */
        
        /* Cria duas colunas: 
           A primeira ocupa 70% do espaço (1 fracionamento maior) 
           A segunda ocupa 30% do espaço */
        grid-template-columns: 70% 30%; 
        
        /* Cria um espaço (vão) de 20px entre as colunas */
        gap: 20px; 
    }
    
    .conteudo {
        background-color: #f9f9f9;
        padding: 20px;
    }
    
    .barra-lateral {
        background-color: #ddd;
        padding: 20px;
    }


### Boas Práticas

**CSS Externo:** Separe as responsabilidades. Mantenha o HTML em um arquivo e o CSS em outro (**`style.css`**). Isso deixa o código mais limpo e o site mais rápido.
    
**Foque nas Classes:** Use e abuse das classes (**`.minha-classe`**). Elas são flexíveis e reutilizáveis, ao contrário dos IDs (**`#meu-id`**), que são rígidos e só podem ser usados uma vez por página.
    
**Mobile-First (Celular Primeiro):** Comece estilizando o seu site para telas pequenas (*celulares*). Depois, use _Media Queries_ (**`@media`**) para adaptar e expandir o layout para tablets e computadores.
    
**Organize e Comente:** Use comentários **`/* assim */`** para dividir seu arquivo CSS em blocos lógicos (*ex: separando o estilo do cabeçalho, do conteúdo e do rodapé*). Isso salva muito tempo na hora de procurar e corrigir um erro depois.

## JavaScript ⚡

### O que é JavaScript

Se o HTML constrói as paredes e o CSS pinta, o JavaScript é o que faz a luz acender quando você aperta o interruptor. Ele permite que o site seja interativo, tome decisões e responda às ações do usuário.

### Variáveis (Guardando Informações)

Variáveis são como "caixas" onde você guarda dados (*textos, números, listas*) para usar depois. No JavaScript moderno, usamos principalmente duas palavras-chave para criar essas caixas:

**`let`**: Usado quando o valor da variável **pode mudar** no futuro (*como a pontuação de um jogo*).
    
**`const`**: Usado quando o valor é **constante e não deve mudar** (*como a sua data de nascimento ou o botão principal do site*).

    // Usando const para algo que não vai mudar
    const nomeDoUsuario = "Maria";
    
    // Usando let para algo que vai mudar
    let idade = 25;
    
    // Mudando o valor da variável let depois
    idade = 26;


### Funções (Ações Reutilizáveis)

Uma função é um bloco de código criado para realizar uma tarefa específica. Pense nela como uma "receita de bolo": você escreve o passo a passo uma vez e, sempre que quiser o bolo, basta chamar a receita.

    // Criando (declarando) a função
    function darBoasVindas(nome) {
        alert("Olá, " + nome + "! Bem-vindo ao nosso site.");
    }
    
    // Executando (chamando) a função
    darBoasVindas("João");
    darBoasVindas("Ana");

### O DOM (A Ponte entre o JS e o HTML)

Para o JavaScript conseguir alterar o texto de um **`<p>`** ou a cor de uma **`<div>`**, ele precisa entender o HTML. Ele faz isso através do **DOM (Document Object Model)**.

O DOM pega todo o seu código HTML e o transforma em uma "árvore", onde cada tag vira um "objeto" (*ou "nó"*) que o JavaScript pode acessar, modificar, deletar ou criar.

#### Como selecionar elementos do HTML:

Usamos o objeto global **`document`** para procurar coisas na página.

    // Pega um elemento pelo seu ID (ex: <h1 id="titulo-principal">)
    const titulo = document.getElementById("titulo-principal");
    
    // Pega um elemento usando a mesma lógica do CSS (ex: a primeira tag <p> com a classe .texto)
    const paragrafo = document.querySelector(".texto");

### Eventos e Manipulação do DOM

**Eventos** são coisas que acontecem no sistema, como um clique do mouse, o rolar da página ou o apertar de uma tecla. O JavaScript pode "ficar escutando" esses eventos e disparar uma função quando eles acontecerem. Usamos o **`addEventListener`** para isso.

Aqui é onde a mágica acontece. Juntando Variáveis, Funções, DOM e Eventos, podemos **manipular a página**.

    // 1. Selecionamos o botão e o texto no HTML
    const botao = document.querySelector("#meu-botao");
    const mensagem = document.querySelector("#minha-mensagem");
    
    // 2. Adicionamos um "ouvinte de eventos" no botão
    botao.addEventListener("click", function() {
        
        // 3. O que acontece quando clicar? Manipulamos o DOM!
        mensagem.textContent = "Você clicou no botão! Parabéns!";
        mensagem.style.color = "green"; // Mudamos o CSS via JavaScript
        
    });

### Exemplo Prático: Um Contador Simples

Aqui está um exemplo completo combinando HTML e JavaScript para criar um botão que conta quantas vezes foi clicado.

    HTML
    
    <div>
        <h2>Cliques: <span id="contador-texto">0</span></h2>
        <button id="botao-clique">Clique em mim!</button>
    </div>



    JavaScript
    
    // 1. Criamos a variável que vai guardar o número
    let cliques = 0;
    
    // 2. Selecionamos os elementos do HTML
    const textoDoContador = document.getElementById("contador-texto");
    const botao = document.getElementById("botao-clique");
    
    // 3. Criamos a interação (Evento)
    botao.addEventListener("click", function() {
        
        // Aumentamos o número de cliques em 1
        cliques = cliques + 1;
        
        // Atualizamos o texto do HTML com o novo número
        textoDoContador.textContent = cliques;
        
    });


### Boas praticas

**Esqueça o `var`:** Use **`const`** para valores que nunca mudam e **`let`** para valores que vão mudar.
    
**Nomes Óbvios e em `camelCase`:** Batize suas variáveis e funções de um jeito que qualquer um entenda (ex: **`let precoTotal`**, em vez de **`let p`**). Junte as palavras e coloque maiúsculas a partir da segunda.
    
**JS em Arquivo Separado:** Mantenha a casa arrumada. Coloque seu código em um arquivo **`script.js`** e não misturado no meio do HTML.
    
**Uma Função = Uma Tarefa:** Não crie funções "faz-tudo". Se a função se chama **`calcularImposto`**, ela deve apenas calcular o imposto, e não salvar no banco de dados e mudar a cor da tela ao mesmo tempo.
    
**Comente o "Porquê":** O seu código já diz _o que_ está acontecendo. Use os comentários (**`//`**) para explicar _por que_ você escolheu fazer daquele jeito.
    
**Fuja de Variáveis Globais:** Tente criar suas variáveis sempre **dentro** das funções. Variáveis soltas pelo arquivo inteiro podem causar conflitos e bugs difíceis de rastrear.

 
 ## internet, PWAs e armazenamento de dados 💻

### Como a Internet Funciona (Cliente e Servidor)

Tudo na internet se baseia em uma relação de **Cliente** (*você*) e **Servidor** (*o computador onde o site mora*).

![client server architecture diagram, gerada com IA](https://encrypted-tbn0.gstatic.com/licensed-image?q=tbn:ANd9GcToFQoFTY6RjotpZa5DRY7AbfFP-9A-oCWcUA8ou9q7tePT_gVszDLXyrN4cQdFDzIw34nh7z9kwTO38K6deBrtbiCtxFCNEfMDz5fUtIZKsrBj754)
Pense em um restaurante:

**O Cliente (Você no navegador):** Você senta na mesa e faz um pedido (digita **`www.google.com`**).
    
**A Internet (O Garçom):** Leva o seu pedido até a cozinha.
    
**O Servidor (A Cozinha):** É um computador superpotente ligado 24 horas por dia. Ele recebe o pedido, "cozinha" os arquivos (*HTML, CSS, JS, Imagens*) e entrega para o garçom.
    
**O Retorno:** O garçom traz a comida (*o site*) para a sua tela.

### PWA (Progressive Web Apps)

PWA, ou Aplicativo Web Progressivo, é uma tecnologia que dá "superpoderes" a um site comum, fazendo com que ele se comporte como um aplicativo de celular nativo.

**Não precisa de App Store:** O usuário entra no seu site pelo navegador (*Chrome, Safari*) e clica em "Adicionar à Tela Inicial". O site vira um ícone no celular igual a um app comum.
    
**Funciona Offline:** Usando uma tecnologia chamada _Service Workers_, a PWA consegue salvar partes do site para que o usuário continue navegando mesmo se perder o sinal de internet (*como ler notícias já baixadas*).
    
**Notificações Push:** Permite enviar aquelas notificações na tela do celular do usuário, mesmo quando ele não está com o site aberto.

### Bancos de Dados e Cache

Todo site que permite criar uma conta, salvar favoritos ou fazer compras precisa guardar essas informações em algum lugar.

**Banco de Dados (A Memória de Longo Prazo):** É como um grande arquivo de aço ou uma planilha do Excel gigante. É onde informações vitais e permanentes ficam guardadas com segurança (*ex: senhas, histórico de compras, catálogo de produtos*). Exemplos comuns: MySQL, PostgreSQL, MongoDB.
    
**Cache (A Memória de Curto Prazo):** Buscar dados no Banco de Dados o tempo todo é lento e custa caro. O Cache é como deixar o livro que você está lendo em cima da mesa, em vez de guardá-lo na estante toda vez. Ele salva temporariamente as informações mais acessadas (*como a página inicial do site ou a foto de perfil do usuário*) para que a página carregue quase instantaneamente no próximo acesso.

### APIs (Application Programming Interfaces)

A API é a "ponte" de comunicação entre dois sistemas diferentes que não falam a mesma língua.

**Como funciona:** Imagine que você criou um site de viagens e quer mostrar a previsão do tempo. Você não precisa construir satélites meteorológicos. Você simplesmente se conecta à **API** de um instituto de meteorologia. O seu site "pergunta" como está o tempo, e a API devolve apenas os dados (*ex: "25 graus, ensolarado"*), que você exibe no seu HTML.
    
**Exemplos reais:** Fazer login usando o Google em um site de terceiros, mapas do Uber (*que usam a API do Google Maps*), ou pagamentos com cartão (*usando a API de um banco*).

### Boas Práticas (Conceitos Gerais)

Para criar aplicações web modernas e eficientes, tenha em mente estas regras:

**Segurança Primeiro (HTTPS):** Nunca construa um site que lide com dados de usuários sem um certificado SSL (*aquele cadeadinho verde ao lado da URL*). O HTTPS embaralha os dados para que hackers não consigam roubar senhas no meio do caminho.
    
**Performance:** A internet tem pressa. Comprima suas imagens, use Cache sempre que possível e evite carregar arquivos gigantescos de JavaScript se não forem estritamente necessários.
    
**Não confie no usuário:** Se você tem um formulário no seu site, sempre verifique (*valide*) o que foi digitado antes de salvar no Banco de Dados para evitar que pessoas mal-intencionadas enviem códigos maliciosos no lugar dos nomes.
