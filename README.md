
# Simple JS App Skeleton

Here's an app skeleton that binds together common frameworks du-jour:

* [Babel](https://babeljs.io/)
* [Bootstrap](http://getbootstrap.com/)
* [Browserify](http://browserify.org/)
* [ES6](https://babeljs.io/docs/learn-es2015/)
* [React](https://facebook.github.io/react/)
* [React Router](https://github.com/reactjs/react-router)
* [StandardJS](http://standardjs.com/)

_Note: The purpose of this skeleton is to provide a simple UI skeleton that can be supplemented with backend/deployment specific tools (Node, Ethereum, Mobile, etc)._

## Install Dependencies

Run in the project root folder:

```bash
npm install
```

## Run

The following command serves all HTML/JS/CSS and watches all changes to `ui/*.jsx`

```bash
npm start
```

UI is running at [http://localhost:3000/](http://localhost:3000/)

To check [StandardJS](http://standardjs.com/) compliancy run `standard` in the project root.

## Directory Structure

* `package.json` - Configure dependencies, Babel transpilers and support scripts
* `public/js/main.js` - This is generated by Browserify/Watchify with JS from `ui/*` and `node_modules/*`
* `public/styles/app.css` - Custom app css (overrides Bootstrap styles)
* `public/index.html` - App HTML container (only used for initial page meta-data and initialization)
* `scripts/serve.js` - Simple Express server that serves `public/` static content (compressed). Non-static hits serve `public/index.html`
* `ui/components/*.jsx` - React components for UI
* `ui/components/main.jsx` - Main UI entrypoint and Router (uses pushState by default)
* `ui/utils/*` - Location of helper JS libs, example of Api client class
