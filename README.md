# Vue test App

It's my first [**Vuejs**](https://vuejs.org/) application.

## How to run it at localhost
* Clone the Repository
  * Use the command `git clone https://github.com/e-azocar/vue-test-app`
* Install dependencies
  * Enter to the project folder using `cd vue-test-app`
  * Then use `npm i` or `yarn` to install the dependencies
* Run the app
  * Use `npm run serve` or `yarn serve` to run at localhost
  * And go to http://localhost:8080 in your browser
 
 *If you have another process running at port **8080** the Vuejs server will run at other port*
 
 ## How it's works
 
It's a very simple app, the **Home Page** has a form and a button. When the button is clicked the form's data is saved in `sessionStorage`, and the user is redirected to **Result Page**, where is there a title, and the user data saved in `sessionStorage`.

Mainly the app's purpose is learn how to create Vue components (with their props), use the Vue router, the events, and basic features of this Javascript Framework.