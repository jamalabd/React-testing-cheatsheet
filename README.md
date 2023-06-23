# React-testing-cheatsheet
One-stop shop for brushing up on/learning testing in React. Created to help make picking up testing in React simple.

## React Testing Library ( RTL )
RTL is an "opinionated" library meaning there is a certain way the software is designed to be used to get the most out of it.
Some of these include:
- Testing your software the way you would use it.
- Finding elements by accessibility markers similar to how screen readers find elements.

### RTL vs Jest
RTL
- Provides a virtual Dom for testing without a browser 

Jest
- A test runner 
- finds tests
- run tests
- determine if they pass or fail

### App.test.js
Here is a breakdown of what's going on in the App.test.js file when we run our tests ( npm test ).

The Render method gets called and it will create a virtual Dom for whatever JSX you provide as an argument ( App ). 

Once the virtual Dom is rendered you access it with the "screen" global object seen below.

Here we are using "screen.getByText(/learn to react/i)" to get the element containing the text "learn react".

Last we have our assertion ( expect(linkElement).toBeInTheDocument() ), an assertion is basically the test criteria that determine whether or not our test succeeds or fails.

<img width="675" alt="Screenshot 1444-11-22 at 8 26 02 AM" src="https://github.com/jamalabd/React-testing-cheatsheet/assets/45414121/e7b96fd5-abad-44a8-928c-cf847051fd12">

### Assertions 
Assertions are our test criteria for our test. They determine instead or not a test passes or fails. Looking at the image above take a look at the expect method.

They all start with the "expect" method. The expected method is globl so it will always be available without any extra importing. The expect method is followed by a matcher. Matchers essentially set what type of assertion we want or you could say they better describe what we should "expect"

