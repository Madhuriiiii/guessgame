let max = prompt("Enter maximum number");

if (max === "quit") {
   console.log("You quit the game");
}
else {
   max = Number(max);

   if (isNaN(max)) {
      let invalid=prompt("Invalid maximum number");
   }
   else {

      let random = Math.floor(Math.random() * max) + 1;
      let guess = prompt("Guess the number");

      while (true) {

         if (guess === "quit") {
            console.log("You quit the game");
            break;
         }

         let numGuess = Number(guess);

         if (isNaN(numGuess)) {
            guess = prompt("Please enter a valid number or type 'quit'");
         }
         else if (numGuess === random) {
            console.log("Congrats! Random number is", random);
            break;
         }
         else if (numGuess < random) {
            guess = prompt("Your number is small, guess a larger one");
         }
         else {
            guess = prompt("Your number is large, guess a smaller one");
         }
      }
   }
}