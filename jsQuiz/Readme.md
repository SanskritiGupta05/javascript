# Quiz JS App

A Vanilla JS quiz app which fetches trivial general knowledge questions from an API.

## Checklist
- [x] Created homepage
- [x] Created and styled the game page
- [x] Displayed hardcoded questions 
- [x] Display red for wrong and green for right answers
- [] Create the Highscore Display
- [] Create and style the End Page
- [] Save Highscores in Local Display
- [] Load and Display Highscores from local storage.
- [] Fetch questions from Local JSON File
- [] Fetch API Questions from Open Trivia API

### Things I've learned while making this project :

* Using `Splice()` method for remove the current question & answers from display and display the next question & answers from the Array. <br>
[Javascript.info](https://javascript.info/array-methods)

* Use `forEach()` mathod - arr.forEach method allows to run a function for every element of the array.

* Using The read-only target property of the Event interface which creates a reference to the object onto which the event was triggered. i.e. `event.target` <br>
[MDN Docs](https://developer.mozilla.org/en-US/docs/Web/API/Event/target)

* Using the `Set.prototype.add()` method in js to add the const- classToApply which basically display red if the clicked option is a wrong answer and displays green when answer is right. [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set/add)
Similarly with `Set.prototype.remove()` method. [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/API/Element/remove) <br>

* Using `setTimeout()` method to remove the class (which display red on wronganwer and green on right answer) after getting applied not immediately but by creating some delay.
