# project related to dom
## project link
[click here](https://stackblitz.com/edit/dom-project-chaiaurcode?file=index.html)

# solution code
## project 1
```javascript
console.log("hitesh")
const buttons = document.querySelectorAll('.button');
console.log(buttons);
const body = document.querySelector('body');
buttons.forEach(function (button) {
  console.log(button);
  button.addEventListener('click', function (e) {
    console.log(e);
    console.log(e.target);
    if (e.target.id == 'grey') {
      body.style.backgroundColor = e.target.id;
    }
    if (e.target.id == 'blue') {
      body.style.backgroundColor = e.target.id;
    }
    if (e.target.id == 'white') {
      body.style.backgroundColor = e.target.id;
    }
    if (e.target.id == 'yellow') {
      body.style.backgroundColor = e.target.id;
    }
    if (e.target.id == 'purple') {
      body.style.backgroundColor = e.target.id;
    }
  });
});


```
# solution code
## project 2
```javascript
const form = document.querySelector('form');
// this case will give you empty
// const height=parseInt(document.querySelector('#height').value)

form.addEventListener('submit', function (e) {
  e.preventDefault();
  const height = parseInt(document.querySelector('#height').value);
  const weight = parseInt(document.querySelector('#weight').value);
  const results = document.querySelector('#results');

  if (height === '' || height < 0 || isNaN(height)) {
    //results.innerHTML = 'please give a valid height';
    results.innerHTML = `please give a valid height ${height}`;
  } else if (weight === '' || weight < 0 || isNaN(weight)) {
    //results.innerHTML = 'please give a valid height';
    results.innerHTML = `please give a valid weight ${weight}`;
  } else {
    const bmi = (weight / ((height * height) / 10000)).toFixed(2);
    results.innerHTML = `<span>${bmi}</span>`;

    if (bmi < 18.6) {
      results.innerHTML = `${bmi} <br> underweight`;
    } else if ((bmi) => 18.6 && bmi <= 24.9) {
      results.innerHTML = `${bmi} <br> normal range`;
    } else {
      results.innerHTML = `${bmi} <br> overweight`;
    }
  }
});

```
