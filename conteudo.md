EVENTOS JAVASCRIPT

- O que vamos aprender?

  Você já aprendeu que é possível utilizar o JavaScript para manipular elementos HTML e até mesmo pra estilizar sua página Web!!!
  Agora é hora de dar mais um passo e aprender a manipular esses elementos para que suas funções em Js possam ser executadas quando algum usuário estiver usando ou quando houver uma interação do navegador com a sua página!!! \o/

- Porque isso é importante?

  Imagina que você está na página de uma galeria de imagens, ali você encontra diversas imagens diferentes mas sem um título ou uma descrição e para acessar as informações de alguma imagem você tem que clicar na imagem onde acontece um novo load de página carregando as informações desejadas.
  Não seria muito mais fácil se apenas ao passar o mouse por cima da imagem já aparecesse alguma descrição? Ou que ao clicar na imagem, ao invés de carregar uma página novamente com ela ampliada e com mais informações, ela apenas aparecesse ali "automágicamente"?
  É pra isso que nosso querido JavaScript e seus eventos existem!!! A partir do momento que usamos o JavaScript pra fazer esse tipo de interação entre usuário, navegador e sua página Web, conseguimos deixar uma página simples muito mais dinâmica e interativa pra quem ta acessando ela <s>além de poupar o tempo do desenvolvedor</s>! Incrível, não é mesmo??? 🤩

- Você será capaz de:

  Fazer alterações dinâmicas na sua página, tanto em estrutura como estilização
  Aplicar o que chamamos de Eventos dentro do JavaScript, por exemplo 'onclick', 'change', entre outros

- Conteúdos

  Parte I - Eventos

    Eventos são ações que acontecem no nosso sistema a partir de alguma interação do usuário com a página. Esses eventos começam a ser executados a partir do momento em que seu escutador, ou em inglês, _event listener_ é acionado.
    Há uma infinidade de eventos listados no JavaScript, essas interações podem acontecer desde um click em um elemento da página até a passagem do mouse por cima de uma frase. Abaixo temos alguns exemplos de eventos para você começar a se familiarizar.

      Change => Aciona o evento quando o conteúdo de um elemento, seleção ou estado muda.
      Click => Aciona o evento quando o usuário clica em um elemento.
      Dblclick => Aciona o evento quando o usuário clica duas vezes em um elemento.
      Keyup => Aciona o evento quando uma tecla é levantada(após o toque no teclado).
      Mouseover => Aciona o evento quando o usuário passa o mouse por cima de um elemento.

    Para saber mais eventos, consulte a lista [nesse link](https://www.w3schools.com/jsref/dom_obj_event.asp);

  Parte II - Escutador de eventos(event listener)

    O escutador de eventos nada mais é do que aquele código que vai ficar ali esperando que o evento ocorra em seu determinado elemento para que ele comece a executar a função pré-determinada.

      **Mas e então, como eu escrevo esse escutador de eventos no meu projeto??**

    Para adicionar um evento utilizamos a função 'addEventListener' que tem como parâmetros o tipo de evento que vai ser escutado e qual a função que ele vai executar.
      
      HTMLelement.addEventListener('event', function())
    
    Você lembra como podemos acessar elementos HTML usando o DOM, certo? Aqui vamos utilizá-los muito!!
    
    Abaixo temos uma página HTML com um botão com o id 'button-submit' e uma div com o id 'output' vazia, ao clicar no botão eu quero que ele acrescente a frase 'Estou aprendendo a trabalhar com eventos!' na div, como fariamos isso em códigos?

      <!DOCTYPE html>
        <html lang="en">
          <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Document</title>
          </head>
          <body>
            <button id="button-submit">Adicione a frase</button>
            <div id="output"></div>
          </body>
        </html>

    Veja os passos a seguir e reproduza em sua máquina:
  
      1 - Resgatamos os elementos HTML e encapsulamos em variáveis dentro do JS.
        const buttonSubmit = document.getElementById('button-submit');
        const divOutput = document.getElementById('output');

      2 - Agora que já temos nossos elementos em variáveis podemos adicionar o escutador de eventos e fazer a execução dele!
        buttonSubmit.addEventListener('click', addPhrase);
        function addPhrase() {
          divOutput.innerHTML = 'Estou aprendendo a trabalhar com eventos!'
        }
      3 - Prontinho agora quando você clicar no botão a frase vai aparecer!!! 

    Acabamos de ver como funciona um escutador de eventos e como podemos montá-lo em nosso código, é importante você saber que dentro do nosso escutador de eventos podemos chamar uma função externa como vimos no exemplo anterior, ou podemos chamar uma função anônima dentro do próprio escutador!
    Observe a refatoração do exemplo anterior com o uso de uma função anônima:
      
      const buttonSubmit = document.getElementById('button-submit');
      const divOutput = document.getElementById('output');

      buttonSubmit.addEventListener('click', function() {
          divOutput.innerHTML = 'Estou aprendendo a trabalhar com eventos!'
      });

    Viu como o código ficou menor? Você pode usar a função anônima sempre que quiser, mas sempre lembrando que funções anônimas não podem ser chamadas mais de uma vez dentro de um script. Caso você vá utilizar uma função mais de uma vez dentro do seu código é muito melhor escrevê-la normalmente e apenas chamá-la no seu escutador, como no primeiro exemplo que fizemos.

    Agora que você já viu como trabalhar com eventos, vamos praticar mais um pouco!

    Copie o código abaixo e rode na sua máquina, ali temos uma página HTML com um quadrado e quatro botões, apenas o primeiro botão(cor vermelha) está funcionando, faça com que os outros botões funcionem também!
    Em seguida, tente trocar o evento dos escutadores para dblclick, mouseover ou algum outro evento(lembre-se do link ali em cima com a lista de eventos), se quiser troque as cores, adicione mais botões de cores, frases dentro do quadrado, o importante é praticar e se divertir!!!

```HTML
<!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>addEventListener Example</title>
      <style>
        .color {
          background-color: orange;
          border: 1px solid black;
          height: 250px;
          width: 250px;
          margin: 20px;
        }

        .red-color {
          background-color: red;
          border: 1px solid black;
          height: 250px;
          width: 250px;
          margin: 20px;
        }

        .green-color {
          background-color: green;
          border: 1px solid black;
          height: 250px;
          width: 250px;
          margin: 20px;
        }

        .blue-color {
          background-color: blue;
          border: 1px solid black;
          height: 250px;
          width: 250px;
          margin: 20px;
        }

        .yellow-color {
          background-color: yellow;
          border: 1px solid black;
          height: 250px;
          width: 250px;
          margin: 20px;
        }

      </style>
    </head>
    <body>
      <div class="color" id="color-div">
      </div>
      <button type="submit" id="red-button">VERMELHO</button>
      <button type="submit" id="green-button">VERDE</button>
      <button type="submit" id="blue-button">AZUL</button>
      <button type="submit" id="yellow-button">AMARELO</button>

      <script>
        const colorDiv = document.getElementById('color-div');

        const redButton = document.getElementById('red-button');
        redButton.addEventListener('click', function() {
          colorDiv.className = 'red-color';
        });
      </script>
    </body>
  </html>
```

- Exercícios

  A seguir você encontra uma página HTML para cada exercício que você precisa fazer.
  Não há nenhum script ou arquivo externo js, isso é com você!

  1 - A seguir você encontra um formulário para preenchimento de alguns dados, após o preenchimento desses dados, ao clicar no botão 'Submit', deverá aparecer uma frase na tela com os dados preenchidos no formulário. Ex.: Olá _João_, você possui _28_ anos, nasceu em _São Paulo_. Gosta de _escrever códigos_ e no seu tempo livre você adora _andar de bike_!
  
  Se algum dos inputs estiver em branco deverá aparecer um alerta de erro na página.

```HTML
  <!DOCTYPE html>
    <html lang="en">
      <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Formando a frase</title>
        <style>
          section {
            display: flex;
            flex-direction: column;
            width: 30%;
            margin: 10px;
          }
          input {
            margin: 5px;
          }
          button {
            margin: 5px;
          }
        </style>
      </head>
      <body>
        <header>
          <h1>Criando uma frase usando eventos</h1>
        </header>
        <section id="form" class="form-sect">
          <label for="name-input">Nome:</label><input type="text" id="name-input" placeholder="nome">
          <label for="name-input">Idade:</label><input type="text" id="age-input" placeholder="Idade">
          <label for="name-input">Local de nascimento:</label><input type="text" id="birthplace-input" placeholder="Local de Nascimento">
          <label for="name-input">O que gosta de fazer?</label><input type="text" id="like-input" placeholder="O que gosta de fazer">
          <label for="name-input">No tempo livre, o que você faz?</label><input type="text" id="free-time-input" placeholder="Hobby">
          <button type="submit" id="button-submit">Criar frase!</button>
        </section>
        <section id="result"></section>
      </body>
    </html>
```

  2 - A partir de cinco inputs de números e dois botões (par e ímpar). Você deve criar as funções para que ao receber os números e clicar em um dos botões, apareça um array na seção "result" apenas com os números condizentes com o botão apertado.

  ```HTML
  <!DOCTYPE html>
    <html lang="en">
      <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Trybe numbers</title>
        <style>
          .numbers {
            display: flex;
            flex-direction: column;
            width: 300px;
            margin: 10px;
          }
        </style>
      </head>
      <body>
        <header>
          <h1>Bem vindo ao selecionador de números</h1>
        </header>
        <section class="numbers">
          <label for="number-input1">Digite um número:</label><input type="number" id="number-input1">
          <label for="number-input2">Digite um número:</label><input type="number" id="number-input2">
          <label for="number-input3">Digite um número:</label><input type="number" id="number-input3">
          <label for="number-input4">Digite um número:</label><input type="number" id="number-input4">
          <label for="number-input5">Digite um número:</label><input type="number" id="number-input5">
        </section>
        <section class="buttons">
          <button type="submit" id="even-button">Par</button>
          <button type="submit" id="odd-button">Impar</button>
        </section>
        <section class="result"></section>
      </body>
    </html>
```
       
  3 - O código abaixo gera uma página com cinco quadrados de cores diferentes e cinco quadrados brancos.
      Ao passar o mouse por cima de algum dos quadrados, a cor de fundo da tela deverá mudar para cor do respectivo quadrado.
      Ao clicar uma vez em algum dos quadrados brancos, a frase "Estou manipulando elementos" deve aparecer na seção abaixo deles.
      Ao clicar duas vezes o texto desaparece.

  ```HTML
  <!DOCTYPE html>
    <html lang="en">
      <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Troque a cor</title>
        <style>
          section {
            display: flex;
          }
          div {
            width: 100px;
            height: 100px;
            border: 1px solid black;
            margin: 5px;
          }
        </style>
      </head>
      <body>
        <section>
          <div style= "background-color: green" id="green-div"></div>
          <div style= "background-color: red" id="red-div"></div>
          <div style= "background-color: blue" id="blue-div"></div>
          <div style= "background-color: black" id="black-div"></div>
          <div style= "background-color: brown" id="brown-div"></div>
        </section>
        <section>
          <div class="white-div" id="white-bgc-div"></div>
          <div class="white-div" id="white-bgc-div"></div>
          <div class="white-div" id="white-bgc-div"></div>
          <div class="white-div" id="white-bgc-div"></div>
          <div class="white-div" id="white-bgc-div"></div>
        </section>
        <section id="phrase"></section>
      </body>
    </html>
  ```

- Recursos Adicionais

[MDN Web docs](https://developer.mozilla.org/pt-BR/docs/Aprender/JavaScript/Elementos_construtivos/Events)

[Eloquent JS - Artigo + Exercicios](https://eloquentjavascript.net/15_event.html)

[Mais exercicios](https://oscarrobertrodriguez.github.io/exercisesModernDeveloper/javascript-events-in-depth/)

[Khan Academy](https://www.khanacademy.org/computing/computer-programming/html-css-js)