# Random Student Picker

Build a website which randomly selects a student's name from a list.

## Installation

Run `npm install`

## Usage

In the terminal, run the following command:

`npm run start`

## Advanced Usage

- To check your JavaScript with ESlint, run `npm run eslint`

## Assignments

We are going to build a website which will randomly select a student's name from a list, and display it on the screen.

There are many problems we must solve in order to achieve this,
so let's break these down into smaller parts.

Before we start, ask your teacher for a list of student names.
They could be names from your class. This should be an array of strings.

Things we will use / learn:

- generating a random number
- setInterval function
- responding to a click event (onclick)

### Assignment 1 - Name randomiser

Let us start with the randomisation of the names.

Research: [Math.random() [English]](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)

Research: [Math.random() [Deutsch]](https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Global_Objects/Math/math.random)

1. Inside the file `js/app.js`, create a function which will select a random name from the array of names. You could call it "getRandomName".

2. The function should receive 1 argument, which will be the list of names (the array).

3. The function should return the randomly selected name when you call it.

4. Call function you just created, passing into the function the array of student names.

> Hint: Think about how we can limit the range of the selected
> random number to the number of items in the array

### Assignment 2 - Connecting our JavaScript to our HTML

Just as we did in the past with our CSS stylesheets, to access our JavaScript from our HTML, we need to include it on the page.

We do this via the use of the `<script></script>` tag.

Using the `<script></script>` tags we can either:

- import a JavaScript file
- write JavaScript directly into the file

In this case, we will import the file `js/app.js`

1. After the `<body></body>` tag, insert the line `<script src="js/app.js"></script>`

### Assignment 3 - Random name in the HTML

Now we have our function which randomly selects a name, we want
to connect the output to our website.

1. Inside the file `index.html`, create the HTML tag `<h1></h1>`.

2. Create a new function to update the HTML on the page. You could call this function "updateHTML". Inside this function, place the call to the function you created in Assignment 1.

3. Inside this function, access the `<h1></h1>` tag as an object from the DOM, and place this into a variable.

> Hint: There are many ways you can access HTML tags via the DOM

> Hint: For example, you could give the `<h1></h1>` tag an ID or a class

> Hint: You could then use DOM methods such as `document.querySelector()` or `document.getElementById()` to get the tag as an object

4. Once you have your object, modify the `innerText` property of the object with the result of the random name from the function you created in Assignment 1.

You should now have a website, which when you hit refresh, will show a random name on the screen.

### Assignment 4 - Adding a button

We want to make our website interactive. If we add a `<button></button>`, and link the `onclick` attribute to our JavaScript, we can choose a new random name by clicking the button.

Research: [onclick [English]](https://developer.mozilla.org/en-US/docs/Web/API/GlobalEventHandlers/onclick)

Research: [onclick [Deutsch]](https://developer.mozilla.org/de/docs/Web/API/GlobalEventHandlers/onclick)

1. Add a `<button></button>` tag into our HTML with some text of your choice

2. We need to capture the mouse "click" event from the button. An easy way to do this is to add an attribute called "onclick" on the `<button></button>` tag. The value of this attribute should be the name of the function we want to call, followed by parentheses "()". For example, if the function we want to call is "updateHTML", the value we use for the "onclick" attribute would be "updateHTML()".

3. Click the button! Does the name randomly change on the webpage?

### Assignment 5 - Image randomiser

Let's make it a little more fun. If you look in the `js/app.js` file, you will notice an array of strings called "imageUrls". Each string is a URL for an image.

1. Inside the file `js/app.js`, create a function which will select a random image from the array "imageUrls". You could call it "getRandomImage".

2. The function should receive 1 argument, which will be the list of image URLs (the array "imageUrls").

3. The function should return the randomly selected image URL when you call it.

### Assignment 6 - Inserting the random image into our HTML

Research: [Element.setAttribute() [English]](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute)

Research: [Element.setAttribute() [Deutsch]](https://developer.mozilla.org/de/docs/Web/API/Element/setAttribute)

- Add an `<img />` tag into your HTML, with an empty "src" attribute. Give it a class or an id so you can select it more easily later.

- Inside the function you created in Assignment 3 (you may have called this "updateHTML"), create a variable to store the DOM object for the `<img />` tag you just created.

- Call the function you created in Assignment 5 (you may have called this "getRandomImage") and use the result to set the attribute "src" in your `<img />` tag.

When you click the button on your webpage, do you get a random image?

> Hint: You can use the setAttribute() method to adjust the "src" attribute

### Assignment 7 - Styling it up!

Our website looks very plain and boring.

1. Spend some time making your page look nice by adding CSS (and perhaps other HTML elements) on your page. You can use the provided `styles/styles.css` file; it has already been imported into the `index.html` file.

### Assignment 8 - Adding some delay

> Teachers: You may want to pause here to demonstrate the `setTimeout` and `setInterval` functions

Showing a random name after 0.00001 seconds is quite boring.

We will use a global function called `setInterval` to add some delay between each named which is displayed. This function runs a callback (an anonymous function) after a specified time (set in milliseconds).

![Preview](assignment-6-preview.gif)

Research: [setInterval() [English]](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/setInterval)

- Use a `setInterval` function inside the function you created in Assignment 3, to delay the display of the name on the screen. Use a delay of 100 milliseconds.

- Unlike `setTimeout`, `setInterval` will continue forever until you tell it to stop. Use the `clearInterval` function to force the `setInterval` function to stop when certain conditions are met.

> Hint: How would you keep track of how many times the `setInterval` callback has been executed?

### Assignment 9 - Taking it further (BONUS)

## Preview

Here is an example of how it could look.

![Preview](preview.gif)
