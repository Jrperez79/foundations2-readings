# Reading 02

## Applying Atomic Design - Part 1
Visually Breaking Down UI Components using Atomic Design

Start big and work your way down
 - Organisms are large sections that we can easily extract from the page.
 - Molecules are sections that we can easily extract from an Organism.
 - Atoms include basic HTML elements like form labels, inputs, buttons, and others that can’t be broken down any further without ceasing to be functional.

Atomic Design Model
 - Split the page design into large sections — Organisms
 - Next, divide your Organisms into Molecules, Look out for sections that are repeated frequently
 - Then, Extract your atoms from the Molecules. Remember elements that can’t be broken up any further

 ## Applying Atomic Design (building with React) - Part 2
In order to make it easier to find and identify the different types of components, it is more advisable to separate our components into different folders representing the different atomic stages; atoms, molecules, and organisms as shown below.

A folder structure should follow a consistent pattern, to allow you (and other people) browse through the files quickly and easily

When visually breaking down a design into components, we start big and work our way down. On the other hand, when building these components with code, it is preferable to do the exact opposite. Build the smaller components first and then use them to compose the larger ones.

For components to be reusable and composable, you have to make them as small and as independent as possible

 - We split the page design visually into components
 - Next, we structured our folder to follow a consistent pattern
 - Then, we built out the components starting from the atoms, and we worked our way up to the organisms.

## More Examples of Atomic Design
Components weren’t just self-contained UI features but rather compositions of functional or visual units that then became larger, composed functional and/or visual units. Without that realisation there is a lot of duplication in both styling work and css output.

Without governance this will easily lead to one or more of these effects:

    - The developer is wasting time by re-implementing patterns you already have
    - The developer is contributing to the inflation of your stylesheets by adding the same styles again and again out of lack of awareness that they already exist
    - The developer will notice that his styles interfere with other styles and will add a surplus of css overrides to force his component into shape
    - The developer will not notice that his styles interfere with other styles and will break the barstool in the other bar

All of the UI features above consist of one or more of the following:

- Frames:
standalone frame (aka card frame — has rounded corners and drop shadow)
embedded frame or no frame at all (has no shadow and no rounded corners)
- Marker:
indicates a colour-coded status, e.g. success, failure, info, warning, …
comes in the form of a left-hand coloured border
- Icon:
an illustration or icon to enable quicker grasping of the nature or context of the content
- Progress Bar:
indicates an expiry timeout or a progress indication
- Title:
a quick-grasp title to indicate the nature of the content
- Message:
a piece of actual content
- Link:
one or more actions to take in text link form
- Button:
one or more actions to take in button form
- Close button:
some of these may feature a ‘close button’ in the form of a cross in the upper right corner
- Message layout:
a layout that places icon, title and content in a 2 column, 1 + 2 row grid

## Thinking in React
Step 1: Break The UI Into A Component Hierarchy
The first thing you’ll want to do is to draw boxes around every component (and subcomponent) in the mock and give them all names.

One such technique is the single responsibility principle, that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

## UI components by design (sketch.com)
Express design as working components
Components let you split the UI into independent, reusable pieces, and think about each piece in isolation.

Though both the designer and developer are thinking in a way that makes sense to themselves, they’re speaking different languages. As a result, the conversation’s fraught with misinterpretations and mistakes.
 
Two Types of Components​
- Foundation Components are the primary expression of the design language of the system. They’re the defining parts of the experience, and very targeted in scope. They ensure a consistent underlying interface. UI Developers on the design team will build them.
- Application Components are specific to one of the applications being built, and not seen as a defining, foundational part of the UI. They’re usually larger in scope, and almost always composed of one or many Foundation Components. Some Application Components may eventually transition into Foundation Components. The application teams will build them.

A component-centric workflow
- Design
A designer starts by designing a part of the experience, keeping in mind the overall context of the application and the current components available in the design language.
- Isolate and elaborate
The designer collaborates with a UI developer to isolate core UI elements so that they can elaborate on their structure, appearance, and behaviors.
- Build
Using the agreed specification, the UI developers build the Foundation Component as a React component.
- Integrate and Learn
Foundation Components are published so that application developers can bring them into applications and assemble them into larger, more complex components. New components are fed back into the design process so they can be reused and iterated on.
- Treat Foundation Components as a product
The UI component library is the expression of the visual and interaction design for the product. It enables teams to build consistent interfaces quickly by giving them the building blocks for their applications. Application developers focus on implementing complex business logic, rather than fussing over user interface details.

## Callbacks

### What are JavaScript Callbacks?
A callback is a function that is to be executed after another function (normally asynchronous) has finished executing — hence the name ‘call back’.

In JavaScript, functions are objects. Because of this, functions can take functions as arguments, and can be returned by other functions. Functions that do this are called higher-order functions. Any function that is passed as an argument and subsequently called by the function that receives it, is called a callback function.

For one very important reason — JavaScript is an event driven language. This means that instead of waiting for a response before moving on, JavaScript will keep executing while listening for other events.

Callbacks are a way to make sure certain code doesn’t execute until other code has already finished execution.

### JavaScript Callback Functions
- A JavaScript function is a block of code that will be executed when you call it
- Because JavaScript functions are first-class objects, you can pass functions to other functions as variables
- The method of passing in functions as parameters to other functions to use them inside is used in JavaScript libraries almost everywhere
- A JavaScript Callback Function is a function that is passed as a parameter to another JavaScript function, and the callback function is run inside of the function it was passed into
- JavaScript Callback Functions can be used synchronously or asynchronously

### First-class Function
A programming language is said to have First-class functions when functions in that language are treated like any other variable. For example, in such a language, a function can be passed as an argument to other functions, can be returned by another function and can be assigned as a value to a variable.

### Callback Function
A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.

Note, however, that callbacks are often used to continue code execution after an asynchronous operation has completed — these are called asynchronous callbacks. A good example is the callback functions executed inside a .then() block chained onto the end of a promise after that promise fulfills or rejects. This structure is used in many modern web APIs, such as fetch().

### Class basic Syntax
In the modern JavaScript, there’s a more advanced “class” construct, that introduces great new features which are useful for object-oriented programming.

No commas between class methods.

What class User {...} construct really does is:
- Creates a function named User, that becomes the result of the class declaration. The function code is taken from the constructor method (assumed empty if we don’t write such method).
- Stores class methods, such as sayHi, in User.prototype.

Class Expression
Just like functions, classes can be defined inside another expression, passed around, returned, assigned, etc.

Getters/Setters
Just like literal objects, classes may include getters/setters, computed properties etc.

### Intro to Object-oriented programming in JavaScript
Objects in JavaScript
Classes in JavaScript
A class is “a set or category of things having some property or attribute in common and differentiated from others by kind, type, or quality.”
An object is an instance of a class. This means that, using a class, I can create many objects and they all share methods and properties.

A good object oriented way of defining classes should provide:
- A simple syntax to declare a class
- A simple way to access to the current instance, a.k.a. this
- A simple syntax to extend a class
- A simple way to access the super class instance, a.k.a. super
possibly, a simple way of telling if an object is an instance of a particular class. obj instance of AClass should return true if that object is an instance of that class.

Instead use this convention: any function whose name begins with a capital letter is a class and must be called using the new operator.

Each time you declare a method inside a class, you actually add that method to the prototype of the corresponding function.

New operator in JavaScript
It means that you can create objects that inherit all the properties defined in the prototype of the function that was called with the new operator.

### Object Methods
“this” in methods
To access the object, a method can use the this keyword.
The value of this is the object “before dot”, the one used to call the method.

Arrow functions have no “this”
Arrow functions are special: they don’t have their “own” this. If we reference this from such a function, it’s taken from the outer “normal” function.
