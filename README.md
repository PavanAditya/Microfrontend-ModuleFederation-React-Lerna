# Micro Frontends

```
Micro Frontends is a concept of sharing components as modules/services with different frontend applications, without actually exporting the app as a whole.
This is a frontend-replica to the concept of Microservices used in any API building backend.
```


## Tech Stack

- React: A Frontend Library used to build applications using HTML/CSS/JS ![Know More](https://reactjs.org/),
- Typescript: A Wrapper language applied over javascript to perform type casting rules ![Know More](https://www.typescriptlang.org/),
- Chakra UI: Simple, modular and accessible component library that gives you the building blocks you need to build your React applications ![Know More](https://chakra-ui.com/),
- Webpack: Module bundler. Its main purpose is to bundle JavaScript files for usage in a browser ![Know More](https://webpack.js.org/),
- Lerna: Monorepo system for managing and publishing multiple JavaScript/TypeScript packages from the same repository. ![Know More](https://lerna.js.org/)

- This app uses ![Module Federation](https://webpack.js.org/concepts/module-federation/) plugin from Webpack to share and consume components as micro frontends.

## About

This project consist of three pieces, a host app `container` and two remotes `app1` `app2`.

Workflow:

- `app1` expose CounterAppOne component.
- `app2` expose CounterAppTwo header component.
- `container` import CounterAppOne and CounterAppTwo component.

## Running Demo

In order to run the demo I highly recommend installing lerna globally via

```bash
npm i -g lerna
```

Then,

```bash
lerna bootstrap
```

Run the command above at the root of your project. This command will make sure you have dependencies you need in order to run this project.

Finally,

```bash
npm run start
```

Lerna will start all your projects parallelly and open your browser.

- http://localhost:3000/ (container)
- http://localhost:3001/ (app1)
- http://localhost:3002/ (app2)

## Screenshots

![App Screenshot](./app.png)

## Article

POC made with reference to the article on Micro Frontends. ![Introduction to Micro Frontends with Module Federation, React and Typescript](https://ogzhanolguncu.com/blog/micro-frontends-with-module-federation)
