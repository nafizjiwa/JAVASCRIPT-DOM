# JAVASCRIPT-DOM

Document Object Model [DOM] - a tree-like structure that organizes the elements on a web page
                            - implemented by browser
How do we access DOM - document object<br>
document object allows scripts (JS) to access children of the DOM as properties<br>
To access the <body> element we access IT as a property of document --> document.body <br>

      document.body.innerHTML = 'The cat loves the dog.';
        -assign contents of the <body> element to this text
- This property returns the body element of the DOM<br>

![image](https://github.com/nafizjiwa/JAVASCRIPT-DOM/assets/56348190/81e4a279-6378-48f8-a26b-be8cb06f0cb1)
DOM allows the modification, creation, and removal of elements
|Methods | function|
|----|----|
|.removeChild()|removes element|
|.createElement()|adds an element|
|.hidden| allows an element to be hidden|
Methods and properties<br>

## Select and then Modify an Element

- we can use DOM in script to acces HTML elements
|ELEMENTS| ELEMENTS JOB | PROPERTIES | PROPERTIES JOB |
|----|----|----|----|
|document| allow access to this element and properties| .innerHTML| allows you to set the contents of an element |
|body| .innerHTML|||
|ELEMENTS| .innerHTML|||

|METHODS|How is the element Modified|


CSS selectors define the elements to which a set of CSS rules apply, but we can also use these same selectors to access DOM elements with JavaScript! Selectors can include a tag name, a class, or an ID.

The method .querySelector('css selector as string') returns the 1st element matching the selector

     document.querySelector('p') ----> returns the first paragraph

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

## Style an Element
- modify an element by changing its CSS style --> .style property<br>
##### SYNTAX
`element.style.CSSProperty`<br>

      let blueElement = document.querySelector('.blue');
      blueElement.style.backgroundColor = 'blue';
      -----SHORT FORM------
      document.querySelector('.blue').style.backgroundColor = 'blue';
      document.querySelector('.blue').style.fontFamily = 'Roboto';
      //Select the 1st element with a class of blue and assigns blue as the background-color

      document.body.style.backgroundColor=('pink');
      // style the background color of the body element to pink
      document.querySelector('.heading').style.fontFamily = ('Roboto');
      // Change the font family of element with a heading class to Roboto

## Traversing the DOM
|ELEMENT PROPERTIES| Action |
|-------| ----- |
|.parentNode| return the parent of the specified element|
|document.parentNode | = null as document is the root node|
|.children | returns an array of the specified element’s children|
|document.child | = null if no children |
|document.body.children[0]|looks for the first child of the document body|

const first = document.body.children[0];    
    //get the first child of the document body
first.parentNode.style.backgroundColor = 'beige';    
    //access the parent element of variable first and modify its background color

## Create and Insert Elements 
DOM allows an element to be modified and created <br>
    .createElement('tagName') method creates a new element based on tag string <br>
let paragraph = document.createElement('p') ===> creates empty p element assign it a variable<br>
Now assign values to its properties<br>

      paragraph.id = 'info';         
        //use id property to assign an ID
      paragraph.innerHTML = 'The text inside the paragraph'; 
        //Use innerHTML property to add content to p

To create an element we must assign it to be the child of an element that exists already ==> append

      --> use .appendChild() method to append as the last child of a parent
    document.body.appendChild(paragraph) 
          ---> append element stored in paragaph to document body as last child

      const newAttraction = document.createElement('li');
          //create a li element save to newAttraction
      newAttraction.id='vespa'; //assign wlement an id
      newAttraction.innerHTML = 'Rent a Vespa';  //assign element a text 
      document.getElementById('italy-attractions').appendChild(newAttraction);
         //append newAttraction element to a list with ID italy-attractions
         
## Remove an Element 

      let paragraph = document.querySelector('p');
        //querySelector method return first paragraph
        
      document.body.removeChild(paragraph);
        //paragraph is then passed in and first paragraph from document body is removed

      document.getElementById('sign').hidden = true;
        //found the element with ID of 'sign' and hide it

      const elementToRemove = document.getElementById('vespa');
        //save the element with id = vespa
      document.getElementById('italy-attractions').removeChild(elementToRemove);
        //Find the parent element with id 'italy-attractions' and remove the child with id=vespa


## Add Click Interactivity

- Make an element interacrive by assigning a function to an event (ex. clicks)
- How is an element modified
-  
