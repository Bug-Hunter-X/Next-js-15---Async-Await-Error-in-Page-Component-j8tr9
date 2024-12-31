# Next.js 15 - Async/Await Error in Page Component

This repository demonstrates a common error encountered when using async/await in Next.js 15 page components. The issue occurs because the component attempts to use data from an asynchronous operation before the operation completes. 

## Problem
The `pages/about.js` file uses async/await to fetch data. However, the `await` keyword is used outside of an `async` function. This causes an error because `fetch` is an asynchronous function which returns a promise that needs to be resolved.

## Solution
The solution involves wrapping the asynchronous operations within an async function and using a loading state to display a message while awaiting the results. The `pages/aboutSolution.js` file shows the corrected code. 

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm run dev` to start the development server.
4. Navigate to `/about`.

You should see an error in your browser's console.