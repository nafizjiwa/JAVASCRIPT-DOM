# JAVASCRIPT-DOM

Document Object Model [DOM] - a tree-like structure that organizes the elements on a web page
                            - implemented by browser
How do we access DOM - document object<br>
document object allows scripts (JS) to access children of the DOM as properties<br>
to access the <body> element we access as a property of document --> document.body <br>
      document.body.innerHTML = 'The cat loves the dog.';
        -assign contents of the <body> element to this text
This property returns the body element of the DOM<br>
![image](https://github.com/nafizjiwa/JAVASCRIPT-DOM/assets/56348190/81e4a279-6378-48f8-a26b-be8cb06f0cb1)

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

      
   

