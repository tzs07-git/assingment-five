1. Difference between getElementById, getElementsByClassName, querySelector, querySelectorAll?

  1.getElementById("idName") → Selects only one element with the specific id.

  2.getElementsByClassName("className") → Selects all elements that have the same class (returns a collection).

  3.querySelector("cssSelector") → Selects the first element that matches any CSS selector.

  4.querySelectorAll("cssSelector") → Selects all elements that match the CSS selector (returns a list).



2. How do you create and insert a new element into the DOM?

We can create a new element by using createElement() method in Javascipt file. Then we insert this element in DOM to use appendChild() method. Now I am showing what does it looks like:-

    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Creating Element</title>
    </head>
    <body>
        
        <script>
            const title = document.createElement("h3");
            title.innerText = "Hello Pragramming Hero";
            document.body.appendChild(title);
        </script>
    </body>
    </html>


3. What is Event Bubbling and how does it work?

Event bubbling means when you click on a child element, the event doesn’t stop there — it “bubbles up” to its parent, then to the parent’s parent, and so on, until it reaches the top.

click on a li inside an ol which is inside a div.

First the click is handled by the li.

Then the same event moves up to the ol.

it goes to the div.

Finally, it reaches the document.


4. What is Event Delegation in JavaScript? Why is it useful?

Event delegation is a technique where instead of adding event listeners to many child elements, you add one listener to their parent. That parent catches events as they bubble up, and you check which child triggered it.

Less code → one listener instead of many.

Better performance → especially when there are lots of elements.

Dynamic elements → it works even if new child elements are added later.


5. What is the difference between preventDefault() and stopPropagation() methods?

preventDefault() = block browser’s default behavior.

stopPropagation() = block event from moving to parent.