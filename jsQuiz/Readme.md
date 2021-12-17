# Quiz JS App

A Vanilla JS quiz app which fetches trivial general knowledge questions from an API.

## Checklist
- [x] Created homepage
- [x] Created and styled the game page
- [x] Displayed hardcoded questions 
- [x] Display red for wrong and green for right answers
- [x] Create the Highscore Display
- [x] Create and style the End Page
- [x] Save Highscores in Local Display
- [ ] Load and Display Highscores from local storage.
- [ ] Fetch questions from Local JSON File
- [ ] Fetch API Questions from Open Trivia API

### Things I've learned while making this project :

* Using `Splice()` method for remove the current question & answers from display and display the next question & answers from the Array. <br>
[Javascript.info](https://javascript.info/array-methods)

* Use `forEach()` mathod - arr.forEach method allows to run a function for every element of the array.

* Using The read-only target property of the Event interface which creates a reference to the object onto which the event was triggered. i.e. `event.target` <br>
[MDN Docs](https://developer.mozilla.org/en-US/docs/Web/API/Event/target)

* Using the `Set.prototype.add()` method in js to add the const- classToApply which basically display red if the clicked option is a wrong answer and displays green when answer is right. [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set/add)
Similarly with `Set.prototype.remove()` method. [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/API/Element/remove)

* Using `setTimeout()` method to remove the class (which display red on wrong answer and green on right answer) after getting applied not immediately but by creating some delay.

* Using the `keyup` event in end.js file, to enable the saving of highscore only when a character of the username is typed inside the input field otherwise disable it. [Javascript.info](https://javascript.info/keyboard-events) 

* Using `localStorage` and its method `setItem()` to store currentHighScore in localStorage. it is read-only. [Link](https://www.javatpoint.com/javascript-localstorage)

* Since localStorage only uses key value pairs with the value being a `String`. to convert them to arrays, we do `JSON.parse()`.
