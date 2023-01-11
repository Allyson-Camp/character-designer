# Dropdown Character Maker

## Learning Objectives

- Use a for/of loop to run a function against every item in an array (i.e., console.log , alert ).
- In response to a user event, add a new item to a state array and display the new state to the user (i.e., add a new todo).
- Use the .value property to get the value of a 'grabbed' HTML form input tag
- Use .createElement() and .append() to display a new HTML tag (with .textContent ) to a grabbed DOM element on click.
- Use .createElement() and .append() to add a list of new DOM  elements to a grabbed DOM element on click
- Create a select element to create a dropdown.
- Use `+` and `${}` to concatenate strings.
- Identify what variables are in a given scope/closure

## Live Example:

https://alchemycodelab.github.io/web-01-character-designer/

## Getting Started

User [this repository](https://github.com/alchemycodelab/half-baked-web-01-character-designer) as a template for this deliverable.

## Rubric

The following is required for your assignment to be graded:

- PR open from dev to main
- PR Passes CI (lint + tests)
- PR preview on netlify
- At least 4 commits (for the individual working features)

| Events . . .                                                                                                                                          |     |
| :---------------------------------------------------------------------------------------------------------------------------------------------------- | --: |
| Select from at least three dropdowns with at least three options each                                                                                 |   2 |
| On choosing an option from the dropdown and see the change reflected in the UI with a new image                                                       |   1 |
| When submitting a catchphrase, add it to an array of catchphrases, clear the current DOM's list of catchphrases, and list all catchphrases in the DOM |   3 |
| See displayed how many times each dropdown has been changed in the current session                                                                    |   1 |

| Functions                                                                                                                                   |     |
| :------------------------------------------------------------------------------------------------------------------------------------------ | --: |
| IMPURE: `displayStats() : mutates the DOM to display a string describing the counts.`                                                       |   1 |
| IMPURE: `displayCatchphrases() : clears out the old list from the DOM, loops through catchphrases, renders and appends to the list element` |   2 |

Stretch Ideas for fun:

- Add some conditional logic that prevents a catch phrase from being added if value is empty
- Add the option for the user to name the character and store the name in state. Display that name in big letters at the top.
- Make three arrays of objects of this kind of shape: [ { display: "Duck head", value: "1" }, { display: "Blue Bird Head", value: "2" }, { display: "Horse Head", value: "3" ]. Now, instead of hard coding your dropdown options, generate them dynamically by looping over these arrays.
- Wrap the catchphrase input and button in a form tag and use a 'submit' handler with the new FormData() constructor to get data from the input. (Hint: Look up e.preventDefault() and why it's useful in this case)
- Use a radio button (probably the most challenging form input) to change between 'cartoon mode' and 'photo mode'. Load a different set of images (photo of duck vs cartoon duck, etc) depending on the mode.
- In addition to keeping track of the number of times each dropdown was changed, keep track of (and display to the user) a "history" of those changes.

my plan:
## html setup
    **html can either change or show the state
    3 dropdown menus
    Why? Let the user select different options
    Why? To find out what the user selected
    How? `selectEl.value`
    Slogan Input field <input>
    Why? To put in their slogan
    Why? To find out what the user typed
    How? `inputEl.value`
    Why? Track a list of all the users slogans
    How? ‘myArray = [ ]
    myArray.push(‘inputEl.value`)
    Push in the value of the inut el to the array
    Submit button <button>
    Why? To submit what is put in the input
    How? buttonEl.addEventListener(`click`, () =>{});
    3 places for photos to go <img />
    Why? Showing users selections visually (from the state)
    How? `imgEl.src = someImgUrl`
    Div for slogans <div> (purple squiggles)
    <p> within 
    Why? To list the slogans (from the state)
    How?? TO BE CONTINUED..

    ##state
    Waterfront/first photo option
    Skyline/second photo option
    Park/third photo option
    List of slogans

    ##slices of work / distinct features
    3 dropdowns change state and update images
    Need to build one  dropdown at a time in HTML w/ ids/values
    Then grab that dropdown in app.js
    Then add a change event listener to dropdown
    In the change listener need to figure out what the user selected
    Finally use the user selection to change to a matching image
    Keep track of every time each dropdown has been changed, display on page
    1 at a time
    Should have already done event listener
    We need count to go up over time, add some state for the count(start at 0)
    In event listener we increment nameOfPlaceCount
    After we increment it we display it on the sire
    Grab html
    Change its textContent
    We track list of what user typed and display that list
    Need to initialize slogans state as an empty array
    Need to add input element and button to the HTML
    Grab the input el and button el in app.js
    Add eventlistener to the button
    on click we need to figure out what the user typed
    Take what the user typed and put it into the state array
    Finally, add the slogan to the DOM
    For now add the most recent slogan to the DOM
    Function `createElement(‘p’) that will create a <p> for us
    Another function myParentEl.append(myChildEl` will inject myChild El into the parentEl
    How put elements into DOM so user can see them
