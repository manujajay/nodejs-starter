# Node.js Starter

This repository serves as a beginner's guide to Node.js, providing the essentials needed to set up a Node.js environment and develop simple applications. It covers basic server setups, module management, and an introduction to core Node.js functionalities.

## Prerequisites

- Basic knowledge of JavaScript
- Node.js installed on your machine

## Installation

1. **Install Node.js**:
   - Download and install Node.js from [Node.js official website](https://nodejs.org/).

## Creating a Basic Server

1. **Create a new directory for your project**:
   ```bash
   mkdir mynodeapp
   cd mynodeapp
   ```

2. **Initialize a new Node.js project**:
   ```bash
   npm init -y  # Creates a new package.json file
   ```

3. **Create a `server.js` file**:
   ```javascript
   const http = require('http');

   const server = http.createServer((req, res) => {
       res.statusCode = 200;
       res.setHeader('Content-Type', 'text/plain');
       res.end('Hello World\n');
   });

   const PORT = process.env.PORT || 3000;

   server.listen(PORT, () => {
       console.log(`Server running on port ${PORT}/`);
   });
   ```

4. **Run your server**:
   ```bash
   node server.js
   ```

## Core Concepts

- **Modules**: Node.js uses a module system based on the CommonJS specification. Modules help organize the code in separate files and folders.
- **NPM**: Node.js's package manager, npm, helps with installing third-party modules and managing project dependencies.

## Example - Using External Modules

1. **Install an external module (e.g., Express)**:
   ```bash
   npm install express
   ```

2. **Modify `server.js` to use Express**:
   ```javascript
   const express = require('express');
   const app = express();

   app.get('/', (req, res) => {
       res.send('Hello World with Express!');
   });

   app.listen(3000, () => {
       console.log('App running on port 3000');
   });
   ```

## Contributing

Contributions that enhance the guide, improve examples, or provide additional resources are welcome. Please fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
