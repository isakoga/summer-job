EVENTOS JAVASCRIPT

- O que vamos aprender?

  Você já aprendeu que é possível utilizar o JavaScript para manipular elementos HTML e até mesmo pra estilizar sua página Web!!!
  Agora é hora de dar mais um passo e aprender a manipular esses elementos para que suas funções em Js possam ser executadas quando algum usuário estiver usando ou quando houver uma interação do navegador com a sua página!!! \o/

- Porque isso é importante?

  Imagina que você está em uma página onde precisa preencher um formulário, mas esse formulário só aparece quando você clica na aba escrita "Preencha aqui seu formulário", quando você clica ali acontece um novo carregamento de página e abre uma página idêntica a que você estava, a única diferença é que agora existe um formulário abaixo da aba que você clicou.
  Não seria muito mais rápido e prático se o formulário apenas aparecesse ali "automágicamente" quando você clicasse na aba, sem um novo load na página inteira?
  É pra isso que nosso querido JavaScript e seus eventos existem!!! A partir do momento que usamos o JavaScript pra fazer esse tipo de interação entre usuário, navegador e sua página Web, conseguimos deixar uma página simples muito mais dinâmica e interativa pra quem ta acessando ela, além de poupar o tempo tanto de quem a desenvolveu como de quem está utilizando! Incrível, não é mesmo??? 🤩

- Você será capaz de:

  Fazer alterações dinâmicas na sua página, tanto em estrutura como estilização
  Aplicar o que chamamos de Eventos dentro do JavaScript, por exemplo 'onclick', 'change', entre outros

- Conteúdos

  Parte I - Eventos

    Eventos são ações que acontecem no nosso sistema a partir de alguma interação do usuário com a página. Esses eventos começam a ser executados a partir do momento em que seu escutador, ou em inglês, event listener é acionado.
    Há uma infinidade de eventos listados no JavaScript, essas interações podem acontecer desde um click em um elemento da página até a passagem do mouse por cima de uma frase. Abaixo temos alguns exemplos de eventos para você começar a se familiarizar.

      Change => Aciona o evento quando o conteúdo de um elemento, seleção ou estado muda.
      Click => Aciona o evento quando o usuário clica em um elemento.
      Dblclick => Aciona o evento quando o usuário clica duas vezes em um elemento.
      Keyup => Aciona o evento quando o usuário aperta uma tecla do teclado.
      Mouseover => Aciona o evento quando o usuário passa o mouse por cima de um elemento.

    Para saber mais eventos, consulte a lista nesse link -> https://www.w3schools.com/jsref/dom_obj_event.asp;

  Parte II - Escutador de eventos(event listener)

    O escutador de eventos nada mais é do que aquele código que vai ficar ali esperando que o evento ocorra em seu determinado elemento para que ele comece a executar a função pré-determinada.

      Mas e então, como eu escrevo esse escutador de eventos no meu projeto??

    Para adicionar um evento utilizamos a função 'addEventListener' que tem como parâmetros o tipo de evento que vai ser escutado e qual a função que ele vai executar.
      
      variavel.addEventListener('event', function)
    
    Você lembra como podemos acessar elementos HTML usando o DOM, certo? Aqui vamos utilizá-los muito!!
    
    Vamos supor que temos uma página HTML com um botão com o id 'button-submit' e uma div com o id 'output' vazia, ao clicar no botão eu quero que ele acrescente a frase 'Estou aprendendo a trabalhar com eventos!' na div, como fariamos isso em códigos?
    Veja os passos a seguir e reproduza em sua máquina:
      1 - Resgatamos os elementos HTML e encapsulamos em variáveis dentro do meu JS.
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

    Copie o código abaixo e rode na sua máquina, ali temos uma página HTML com um quadrado e quatro botões, conforme vc aperta algum dos botões a classe da estilização do quadrado muda para a classe com a cor de fundo igual a cor do botão que você apertou.
    Tente trocar o evento dos escutadores para dblclick ou mouseover, procure mais eventos na lista que falamos ali em cima e se divirta!!!

    //EXEMPLO COMO FUNCIONA UM ADDEVENTLISTENER 

- Exercícios



- Recursos Adicionais