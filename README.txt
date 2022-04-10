#Requirements#

- Node.js version ≥ v12.x installed in your local development environment
- Access to a package manager like npm or Yarn
- Basic knowledge of Node.js and Express

#Project init: package.json#

- mkdir xdev.bdm-fmw
- cd xdev.bdm-fmw
- npm init --yes

Rmq: --yes flag uses de default settings you have set up from your npm config

# Create a minimal server with Express#

- npm install express dotenv
Rmq: the dotenv package is useful for reading .env files

- Create the .env file with the following content
    PORT=8000

- create the application entry point index.js

    const express = require('express');
    const dotnev = require('dotenv');

    dotenv.config();

    const app = express();
    const port = process.env.PORT;

    app.get('/', (req, res) => {
    res.send('Express + TypeScript Server');
    });

    app.listen(port, () => {
    console.log(`[server]: Server is running at https://localhost:${port}`);
    });

# Installing TypeScript




https://blog.logrocket.com/how-to-set-up-node-typescript-express/