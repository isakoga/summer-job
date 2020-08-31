// GABARITOS 

EXERCICIO 1

``` JAVASCRIPT
  const button = document.getElementById('button-submit');
  const outputResult = document.getElementById('result');
  button.addEventListener('click', function() {
    const inputName = document.getElementById('name-input').value;
    const inputAge = document.getElementById('age-input').value;
    const inputBirthplace = document.getElementById('birthplace-input').value;
    const inputLikeToDo = document.getElementById('like-input').value;
    const inputHobby = document.getElementById('free-time-input').value;

    if (!inputName || !inputAge || !inputBirthplace || !inputLikeToDo || !inputHobby) {
      return window.alert('Erro! Preencha os campos corretamente');
    }
    return outputResult.innerHTML = 'Olá ' + inputName + ', você possui ' + inputAge + ' anos, nasceu em ' + inputBirthplace + '. Gosta de ' + inputLikeToDo + ' e no seu tempo livre seu hobby é ' + inputHobby
  });
```

EXERCICIO 2

```JAVASCRIPT
  const output = document.getElementById('result');
  
  const evenButton = document.getElementById('even-button');
  evenButton.addEventListener('click', function() {
    const number1 = document.getElementById('number-input1').value;
    const number2 = document.getElementById('number-input2').value;
    const number3 = document.getElementById('number-input3').value;
    const number4 = document.getElementById('number-input4').value;
    const number5 = document.getElementById('number-input5').value;
    const firstArray = [number1, number2, number3, number4, number5];
    let newArray = [];
    for (let i = 0; i < firstArray.length; i += 1) {
      if (firstArray[i] % 2 === 0) {
        newArray.push(firstArray[i]);
      }
      output.innerText = newArray;
    }
  });

  const oddButton = document.getElementById('odd-button');
  oddButton.addEventListener('click', function() {
    const number1 = document.getElementById('number-input1').value;
    const number2 = document.getElementById('number-input2').value;
    const number3 = document.getElementById('number-input3').value;
    const number4 = document.getElementById('number-input4').value;
    const number5 = document.getElementById('number-input5').value;
    const firstArray = [number1, number2, number3, number4, number5];
    let newArray = [];
    for (let i = 0; i < firstArray.length; i += 1) {
      if (firstArray[i] % 2 !== 0) {
        newArray.push(firstArray[i]);
      }
      output.innerText = newArray;
    }
  });
```

EXERCICIO 3

``` JAVASCRIPT
  const greenEvent = document.getElementById('green-div');
  greenEvent.addEventListener('mouseover', function() {
    document.body.style.backgroundColor = 'green';
  });
  const redEvent = document.getElementById('red-div');
  redEvent.addEventListener('mouseover', function() {
    document.body.style.backgroundColor = 'red';
  });
  const blueEvent = document.getElementById('blue-div');
  blueEvent.addEventListener('mouseover', function() {
    document.body.style.backgroundColor = 'blue';
  });
  const blackEvent = document.getElementById('black-div');
  blackEvent.addEventListener('mouseover', function() {
    document.body.style.backgroundColor = 'black';
  });
  const brownEvent = document.getElementById('brown-div');
  brownEvent.addEventListener('mouseover', function() {
    document.body.style.backgroundColor = 'brown';
  });

  const whiteDivs = document.getElementById('white-bgc-div');
  const phraseOutput = document.getElementById('phrase');

  whiteDivs.addEventListener('dblclick', function() {
    phraseOutput.innerHTML = 'Estou manipulando elementos';
  });
```