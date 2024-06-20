# JAVASCRIPT-DOM

## Select and then Modify an Element

|METHODS|How is the element Modified|

CSS selectors define the elements to which a set of CSS rules apply, but we can also use these same selectors to access DOM elements with JavaScript! Selectors can include a tag name, a class, or an ID.

The .querySelector() method specifies a CSS selector as a string and returns the first element that matches that selector. 
  `document.querySelector('p') ----> returns the first paragraph`

JavaScript has methods that select elements based on class, id, or tag name.

`.getElementById() --> Access element by id`
Eg document.getElementById('bio').innerHTML = 'The description';<br>

In this example, we’ve selected the element with an ID of 'bio' and set its .innerHTML to the text 'The description'.
.getElementsByClassName() ---> retruns an array of elements
.getElementsByTagName() ---> retruns an array of elements
Then use bracket notation to access individual elements of those arrays
// Set first element of .student class as 'Not yet registered'
  document.getElementsByClassName('student')[0].innerHTML = 'Not yet registered';

// Set second <li> tag as 'Cedric Diggory'
  document.getElementsByTagName('li')[1].innerHTML = 'Cedric Diggory`;
