# Software Engineer UI Code Challenge

## Challenge Description

We’ve included a simple Autocomplete/Typeahead component in vanilla ES2015 that lets you type in a query in a dropdown in order to see a list of matching results.

To see this component in action, let's set up the repo:

1. Run `yarn install`
1. Run `yarn start` (runs `webpack-dev-server`)
1. Open `http://localhost:8080` in your browser

Type "new" in the input, and you'll get a list of matching US states that start with "new".

### Task

Currently, the component can only query against a static data array. Your task is to:

1. Enhance the component so that it also accepts an HTTP endpoint as a data source.

   For example, if you wire up the component to use  and type `foo` in the input, the component dr`https://api.github.com/search/users?q={query}&per_page={numOfResults}`opdown should show Github users with logins that start with `foo`. When you select a user from the results, `item` in the `onSelect(item)` callback should be the selected Github user's id.

2. Implement keyboard shortcuts to navigate the results dropdown using up/down arrow keys and to select a result using the Enter key.

3. When an item in the dropdown is selected by mouse click or by hitting the Enter key, show the selected item below the search input(s).

4. Implement all stubbed tests in `./tests/Autocomplete-test.js` and ensure that `yarn run test` passes.

Uncomment the relevant sections in `index.js` and `index.html` to implement a demo that looks like this:

![Demo example screenshot](example.png)

### Additional Requirements

- The component should be reusable. It should be possible to have multiple instances of the component on the same page.
- The "States" example that uses a data array should be enhanced with your code and continue to work.
- Your component should work correctly in Chrome, don’t worry about cross-browser compatibility.
- You can use small DOM helpers like jQuery or utilities from Lodash, but not larger libraries/frameworks like React, Angular or Vue.js
- You don't need to preserve any of the existing code; feel free to modify it as you wish.
- New APIs and your notes should be documented in `SOLUTION.md`.
