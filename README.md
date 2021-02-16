# jbook (WIP)
A CLI to launch an interactive development environment for writing and documenting code. (similar to codepen or code sandbox something like that)

## Table of contents
* [Screenshot](#screenshot)
* [Technologies](#technologies)
* [Features](#features)
* [Challenges](#challenges)

## Screenshot:

## Technologies
- react
- typescript
- ESBuild

## Features

## Challenges
#### Q1: Code might include advanced JS syntax that browser can't execute  
A: Code transpiling is required.    
- Option 1: Remote transpiling
- Option 2: In-Browser transpiling (approach we takes in this app)

#### Q2: Code might have import statement for other JS files or CSS that need to handle before executing the code    
A: Bundler is required. 
1. Read the contents of the entry file (index.js)
2. Automatically found all the different require/import/export statements
3. ***Automatically found all the modules the user has imported from NPM*** -> Manually fetch packages from NPM via UNPKG to avoid CORS issue
4. Link files together into a single output file

As webpack doesn't work correctly in browser, we use another bundle package called ***ESBuild*** which can transpile and bundle in the browser at the same time.

## Usage

In the root directory, to install all the dependencies, you should respectively run:

#### `npm install`

#### `npm start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.
