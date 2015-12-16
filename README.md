## Thinking In React (updated)

Originally created by following https://facebook.github.io/react/docs/thinking-in-react.html

However, that article is old, and the following modifications have been made:

* use ES6 classes
    - this required changing `getInitialState` into `constructor`
* use ES6 modules
    - this allows for moving react components into app.js and importing them in entry.js.
* use react version 0.14.x
    - this fixes `refs` not being found (see https://facebook.github.io/react/blog/2015/10/07/react-v0.14.html#dom-node-refs)
    - using a string for a `ref` is now considered legacy, and has been replaced with arrow-function callbacks
* use react-dom (version 0.14.x)
    - this is required since React.render() - used to mount a react component on a page - has been moved into ReactDOM.render().

# Setup

```
npm install
```

Set `INTERFACE` to the address that the webpack server should listen on in webpack.config.js.

# Usage

```
npm start
```

This will start a webpack-dev-server with hot module reloading, babel transformation using stage0, and serve an in-memory bundle.js.
