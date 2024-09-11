# JavaScript-day3
## Booleans and If-Statements:
a. Create a variable called 'hour' and save the current hour of the day (use 24-hour format and save it as a number between 0 and 23).
If hour is between 6 and 12, display 'Good morning!' in the console
If hour is between 13 and 17, display 'Good afternoon!' in the console
Otherwise, display 'Good night!' in the console
```
<script>
  let hour=19;
  if(hour>6 && hour<12){
    console.log("Good Morning");
  }
  else if(hour>13 && hour<17)
  {
    console.log("Good AfterNoon");
  }
  else{
    console.log('Good Night');
  }
</script>
```
b. Continuing from 6a, try changing the value in the 'hour' variable to make it display different messages.
```
let hour=19;
  if(hour>6 && hour<12){
    console.log("Good Morning");
  }
  else if(hour>13 && hour<17)
  {
    console.log("Good AfterNoon");
  }
  else{
    console.log('Good Night');
  }
```
c. Continuing from 6a, create a variable called 'name' and save your name inside (as a string). Update the if-statement to display your name in each message. For example: 'Good morning ${name}!'
```
let name='Umar Mohamed E';
  if(hour>6 && hour<12){
    console.log(`Good Morning ${name}`);
  }
```
6d. Imagine an amusement park that has a discount for children (6 years and younger) or seniors (65 years and older).
Create a variable 'age' and save a person's age inside.
Create an if-statement that checks if the person qualifies for a discount. If they do, display 'Discount' in the console. Otherwise, display 'No discount' in the console.
Note: try to use the || operator in your solution.
• Try changing the 'age' variable to display different messages.
```
<script>
  let age=22;
  if(age<=6 || age>=65)
    {
      console.log("Congratulations, You are elegible for a discount");
    }
  else
    {
      console.log('No doscount');
    }
</script>
```
6e. Continuing from exercise 6d, let's say the discount is only available if it is not a holiday. Create a variable: const isHoliday = true;
• Update the code so that in order to get a discount, people must meet the age requirement and it is also not a holiday.
• Note: && has a higher priority than || so you may need to use brackets () to control which code gets done first.
Try changing the value of isHoliday to display different messages.
```
let age=5;
  const isHoliday=false;
  if(isHoliday && (age<=6 || age>=65))
    {
      console.log("Congratulations, You are elegible for a discount");
    }
  else
    {
      console.log('No doscount');
    }
```
f. Generate a random number with Math.random(). Save it in a variable.
```
let randomNumber=Math.random();
  console.log(randomNumber);
```
g. Create an if-statement and check:
. If the number is less than 0.5, then display 'heads' in the console.
• Else display 'tails' in the console.
```
if(randomNumber>0 && randomNumber<1/2){
 console.log('Heads');
  }
  else{
    console.log('tails');
  }
```
h. Instead of displaying 'heads' or 'tails' in the console, save the result in a variable called 'result'.
```
let result='';
  if(randomNumber>0 && randomNumber<1/2){
    result='Heads';
    console.log(result);
  }
  else{
    result='Tails';
    console.log(result);
  }
```
6i. Let's say we're trying to guess the result. Create a variable called 'guess' and save your guess ('heads' or 'tails').
• If your guess matches the result, display 'You win!' in the console
• If your guess does not match the result, display 'You lose!'
```
let guess='Heads';
  if(result===guess){
    console.log('You win!');
  }
  else{
    console.log('You Lose!');
  }
```
6j. (Challenge) Instead of using if-statements in the previous exercises, try switching them into ternary operators (condition? A: B).
```
result=randomNumber < 0.5 ? 'Heads':'Tails';
console.log(guess===result ? 'You win!' : 'You Lose!');
```
6k. Let's say the cart has a maximum quantity of 10. Before updating the quantity, check if the quantity will be greater than 10: • If it will, display a popup saying 'The cart is full' and don't update
the quantity.
• Otherwise, update the quantity and console.log() it as usual. A
```
 <button onclick="
  if(cartquan+1>10){
    alert('The cart is full');
  }
  else{
    cartquan++;
  }
  
  console.log(`Cart Quantity is: ${cartquan}`);">Add to cart</button>
  <button onclick="
  if(cartquan+2>10){
    alert('The cart is full');
  }
  else{
    cartquan+=2;
  }
  
  console.log(`Cart Quantity is: ${cartquan}`);">+2</button>
  <button onclick="
  if(cartquan+3>10){
    alert('The cart is full');
  }
  else{
    cartquan+=3;
  }
  console.log(`Cart Quantity is: ${cartquan}`);">+3</button>
  <button onclick="
  if(cartquan+4>10){
    alert('The cart is full');
  }
  else{
    cartquan+=4;
  }
  console.log(`Cart Quantity is: ${cartquan}`);">+4</button>
  <button onclick="
  if(cartquan+5>10){
    alert('The cart is full');
  }
  else{
    cartquan+=5;
  }
  console.log(`Cart Quantity is: ${cartquan}`);">+5</button>
```
61. In exercises 5i - 5k, we created the 'Remove from cart', '-2', and '-3' buttons. Before updating the quantity, check if it will go below 0:
If it will, create a popup saying 'Not enough items in the cart' and don't update the quantity.
Otherwise, update the quantity and console.log() it as usual.
```
<button onclick="
  if(cartquan-1<0){
    alert('Not enough items in the cart');
  }
  else{
    cartquan--;
  }
  console.log(`Cart Quantity is: ${cartquan}`);">Remove from cart</button>
  <button onclick="
  if(cartquan-2<0){
    alert('Not enough items in the cart');
  }
  else{
    cartquan-=2;
  }
  console.log(`Cart Quantity is: ${cartquan}`);">-2</button>
  <button onclick="
  if(cartquan-3<0){
    alert('Not enough items in the cart');
  }
  else{
    cartquan-=3;
  }
  console.log(`Cart Quantity is: ${cartquan}`);">-3</button>
```
## Functions
a. Create a function called 'greet' that displays the message 'Hello!' in the console. Call / run this function a few times using: greet();
```
function greet(){
 console.log('hello!');
}
greet();
```
b. Continuing from 7a, add a parameter called 'name' to the 'greet' function and display the message: 'Hello ${name}!' Call the function a few times with different names: greet('Simon');
```
function greet(name){
  console.log(`Hello ${name}`);
}
greet('Umar');
```
c. Try calling greet() without a name (it will display 'Hello undefined!") Modify the function so that if 'name' is undefined, it will display 'Hi there!' instead.
(Hint: use an if-statement. Since undefined is a falsy value, you can use: if (!name) { ... } to check if 'name' is undefined).
```
function greet(name){
    if(!name){
    console.log(' Hello There!');
  }
  else{
    console.log(`Hello ${name}`);
  }
  }
  greet();
```
d. Create a function 'convertToFahrenheit(celsius)' that takes a number in degrees Celsius and returns a number in degrees Fahrenheit.
• Formula: Fahrenheit = (Celsius * 9/5) + 32
• convertToFahrenheit(25) => 77
```
 function convertToFahrenheit(celcius){
  let fahrenheit=(celcius*9/5)+32;
  console.log(fahrenheit);
}
convertToFahrenheit(25);
```
e. Create a function 'convertToCelsius (fahrenheit)' that takes a number in degrees Fahrenheit and returns a number in degrees Celsius.
• Formula: Celsius = (Fahrenheit - 32) * 5/9
• convertToCelsius(86) => 30
```
function converttoCelcius(fahrenheit){
  let celcius=(fahrenheit-32)*5/9;
  console.log(celcius);
}
converttoCelcius(86);
```
f. Create a function 'convertTemperature(degrees, unit)' that takes a number and a unit ('C' or 'F'), and converts it into the other unit.
• convertTemperature(25, 'C') => '77F'
• convertTemperature (86, 'F') => '30C'
Note: return a string, and try to reuse the functions from 7d and 7e.
```
function convertTemp(degrees,unit){
  if(unit==='C'){
    const result=convertToFahrenheit(degrees);
    return `${result} F`;
  }
  else if(unit==='F'){
    const result=converttoCelcius(degrees);
    return `${result} C`;
  }
}
console.log(convertTemp(25, 'C'));
console.log(convertTemp(86, 'F'));
```
g. Create a function convertLength(length, from, to) that takes a number and a unit ('km' or 'miles') and converts the length to another unit ('km' or 'miles'). Note: 1 mile = 1.6 km (approximately).
• convertLength(50, 'miles', 'km') => '80 km'
• convertLength(32, 'km', 'miles') => '20 miles'
• convertLength(50, 'km', 'km') => '50 km'
```
function convertLength(length,from,to){
  if(from==='miles' && to==='km'){
    const result= length*1.6;
    return `${result} ${to}`;
  }
  else if(from==='km' && to==='miles'){
    const result= length/1.6;
    return `${result} ${to}`;
  }
  else{
    const result= length;
    return `${result} ${to}`;
  }
  }
  console.log(`${convertLength(50, 'miles', 'km')}`);
  console.log(convertLength(32, 'km', 'miles'));
  console.log(convertLength(50, 'km', 'km'));
```
h. Update convertLength to support converting between km, miles, and also feet. Note: 1 mile = 5280 ft, 1 km = 3281 ft (approximately).
• convertLength(5, 'miles', 'km') => '8 km'
• convertLength(5, 'miles', 'ft') => '26400 ft'
• convertLength(5, 'km', 'ft') => '16405 ft'
```
function convertLength(length,from,to){
  if(from==='miles' && to==='km'){
    const result= length*1.6;
    return `${result} ${to}`;
  }
  else if(from==='miles' && to==='ft'){
    const result= length*5280;
    return `${result} ${to}`;
  }
  else if(from==='km' && to==='ft'){
    const result= length*3281;
    return `${result} ${to}`;
  }
  }
  console.log(`${convertLength(5, 'miles', 'km')}`);
  console.log(convertLength(5, 'miles', 'ft'));
  console.log(convertLength(5, 'km', 'ft'));
```
i. Update convertLength so that if you give it an invalid unit, it will return 'Invalid unit: ${unit}`.
• convertLength(5, 'lbs', 'lbs') => 'Invalid unit: Ibs'
```
else if(from==='lbs' && to==='lbs'){
  const result= 'Invalid Unit';
  return `${result}: ${to}`;
}
```
j. Create a copy of the Calculator project from exercise 5r (if you didn't
do 5r, copy the code for 5r from the solutions).
• Notice there's a lot of duplicated code in the buttons.
• Create a function 'updateCalculation' and reuse the code.
```
<!DOCTYPE html>
<html>
  <head>
    <title>
      <b>
        Calculator
      </b>
    </title>
  </head>
  <body>
    <p>
    <button onclick="
      calculate('1');">1
    </button>
    <button onclick="
      calculate('2');">2
    </button>
    <button onclick="
      calculate('3');">3
    </button>
    <button onclick="
      calculate(' + ')">+
    </button>
    </p>
    <p>
      <button onclick="
      calculate('4');">4
    </button>
    <button onclick="
      calculate('5');">5
    </button>
    <button onclick="
      calculate('6');">6
    </button>
    <button onclick="
      calculate(' - ')">-
    </button>
    </p>
    <p>
      <button onclick="
      calculate('7');">7
    </button>
    <button onclick="
      calculate('8');">8
    </button>
    <button onclick="
      calculate('9');">9
    </button>
    <button onclick="
      calculate(' * ')">*
    </button>
    </p>
    <p>
      <button onclick="
      calculate('0');">0
    </button>
    <button onclick="
      calculate('.');">.
    </button>
    <button onclick="
      calculate('/');">/
    </button>
    <button onclick="
      calculations=eval(calculations);
      console.log(calculations)">=
    </button>
    </p>
    <button onclick="
      calculations=' ';
    ">clear</button>
    
    <script>
      let calculations='';
      function calculate(value)
      {
        calculations+=value;
        console.log(calculations);
      }
    </script>
  </body>
</html>
```
k. Create a copy of the Cart Quantity project from exercise 61.
• Create a function 'updateCartQuantity' and reuse the code.
```
function updateCartquantity(quantity)
      {
        if(cartquan+quantity>10){
          alert('The cart is Full');
        }
        else if(cartquan+quantity<0){
          alert('Not enough items in the cart')
        }
        else{
          cartquan+=quantity;
          console.log(`Cart Quantity is: ${cartquan}`);
        }
        
      }
```
l. Modify 'updateCartQuantity' so that if the quantity is invalid, alert(); and then return; (this is called an early return). An early return make our code cleaner because we can remove the 'else-if' / 'else'.
```
function updateCartquantity(quantity)
      {
        if(cartquan+quantity>10){
          alert('The cart is Full');
          return
        }
        if(cartquan+quantity<0){
          alert('Not enough items in the cart');
          return
        }
          cartquan+=quantity;
          console.log(`Cart Quantity is: ${cartquan}`);       
      }
```
