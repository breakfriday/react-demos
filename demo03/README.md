## Demo01: Render JSX ([source](https://github.com/ruanyf/react-demos/blob/master/demo01/index.html))

The template syntax in React is called [JSX](http://facebook.github.io/react/docs/displaying-data.html#jsx-syntax). It is allowed in JSX to put HTML tags directly into JavaScript codes. React.render() is the method which translates JSX into HTML, and renders it into the specified DOM node.

```js
React.render(
  <h1>Hello, world!</h1>,
  document.getElementById('example')
);
```

Please be minded that you have to use `<script type="text/jsx">` to indicate JSX codes, and include `JSXTransformer.js` to actually perform the transformation in the browser.

## Demo02: Use JavaScript in JSX ([source](https://github.com/ruanyf/react-demos/blob/master/demo02/index.html))

You could also use JavaScript in JSX. It takes angle brackets (&lt;) as the beginning of HTML syntax, and curly brackets ({) as the beginning of JavaScript syntax.

```js
var names = ['Alice', 'Emily', 'Kate'];

React.render(
  <div>
  {
    names.map(function (name) {
      return <div>Hello, {name}!</div>
    })
  }
  </div>,
  document.getElementById('example')
);
```

## Demo03: Use array in JSX ([source](https://github.com/ruanyf/react-demos/blob/master/demo03/index.html))

If a JavaScript variable is array, JSX will implicitly concat all members of the array.

```js
var arr = [
  <h1>Hello world!</h1>,
  <h2>React is awesome</h2>,
];
React.render(
  <div>{arr}</div>,
  document.getElementById('example')
);
```