This project is based on [Create React App Lambda]https://github.com/netlify/create-react-app-lambda). (For more information about Create react App, check their repo over at netlify. This project adds authentication with Netlify identity and mongodb jsdocs, eslint with google standard and other bells and whistles. 

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/aslanvaroqua/one-click-deploy-react-lambda-auth)

* new
added identity, mongodb, eslint, eslint google, jdovd automated, and some pentesting..
## Babel/webpack compilation

All functions are compiled with webpack using the Babel Loader, so you can use modern JavaScript, import npm modules, etc., without any extra setup.

## Local Development

Before developing, clone the repository and run `yarn` from the root of the repo to install all dependencies.

### Run the functions dev server

From inside the project folder, run:

```
yarn start:lambda
```

This will open a local server running at `http://localhost:9000` serving your Lambda functions, updating as you make changes in the `src/lambda` folder.

You can then access your functions directly at `http://localhost:9000/{function_name}`, but to access them with the app, you'll need to start the app dev server.

### Run the app dev server

While the functions server is still running, open a new terminal tab and run:

```
yarn start
```

This will start the normal create-react-app dev server and open your app at `http://localhost:3000`.

Local in-app requests to the relative path `/.netlify/functions/*` will automatically be proxied to the local functions dev server.
