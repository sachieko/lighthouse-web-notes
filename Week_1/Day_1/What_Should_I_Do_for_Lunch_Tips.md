### Tips

Try experimenting with the comparison operators (`<`, `>`, `===`, etc.) in the node REPL, which you can launch using the `node` command in WSL.

Work on your code iteratively – that means in small pieces. 

To help you figure out how to use `hungry` and `availableTime` inside your function, try outputting their values to the Terminal as follows.

### Reply

I eat these operators in their sleep. Teach me how to iterate over an array diagonally efficiently. :D

```javascript
/* eslint-disable no-console */
/*
 * Modify the contents of the function below, such that:
 *
 * If we're not hungry, we want to tell ourselves to get back to work.
 * Otherwise, we want to pick something up and eat it in the lab when
 * we've got less than 20 minutes or to try a place nearby if we've
 * got between 20 and 30 minutes. If we have any more time than that,
 * we want to remind ourselves that we're in a bootcamp and that we
 * should reconsider how much time we actually have to spare.
 *
 * hungry is a Boolean, representing if you're hungry or not.
 * availableTime is a Number representing the time you have for lunch,
 * in minutes.
 */
// eslint-disable-next-line func-names
const whatToDoForLunch = function(hungry, availableTime) {
  if (hungry === true) {
    if (availableTime > 30) {
      console.log('You should re-evaluate how much time you actually have to spare.');
    } else if (availableTime >= 20 && availableTime <= 30) {
      console.log('You should try a place nearby.');
    } else if (availableTime < 20) {
      console.log('You should pick something up or eat something at home.');
    }
  } else {
    console.log('You\'re not hungry, you should get back to work!');
  }
};

/*
 * This is some test runner code that's simply calling our whatToDoForLunch function
 * defined above to verify we're making the right decisions. Do not modify it!
 */

console.log('I\'m hungry and I have 20 minutes for lunch.');
whatToDoForLunch(true, 20);
console.log('---');

console.log('I\'m hungry and I have 50 minutes for lunch.');
whatToDoForLunch(true, 50);
console.log('---');

console.log('I\'m not hungry and I have 30 minutes for lunch.');
whatToDoForLunch(false, 30);
console.log('---');

console.log('I\'m hungry and I have 15 minutes for lunch.');
whatToDoForLunch(true, 15);

```