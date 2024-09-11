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
