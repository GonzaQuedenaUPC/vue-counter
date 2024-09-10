# Counter App
## Summary
A simple counter application built with Vue 3. It allows users to increment, decrement, and reset a counter, with dynamic color changes based on the counter's value. This project demonstrates the usage of Vue's composition API, reactive references, and dynamic styling.

## Features
Increment, decrement, and reset counter values.
Dynamic color change of the counter label:
Red for negative values.
Green for positive values.
Black for zero.
Smooth hover animations for buttons.
Responsive design with centered counter on the screen.

## Framework and Dependencies
This project is built using the Vue 3 Framework and the following core features:

* Composition API with ref for reactivity (https://vuejs.org/api/reactivity-core.html#ref)
* Scoped CSS for component-specific styling
* Template and script setup syntax in Vue 3 (https://vuejs.org/guide/scaling-up/sfc.html#script-setup)

## Project Structure
* Script Setup: Simplified code with the setup tag in Vue components.
* Template: The counter UI, including buttons and dynamic counter display.
* Style: Scoped CSS to ensure styles are isolated to the component.

## Usage
To run the project, you need to have Node.js installed. Clone the repository, then run:
````
npm install
npm run serve
````