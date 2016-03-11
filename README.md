# animated-scroll-behavior

A generic behavior for visually scrolling the page ("smooth scrolling," as the kids used to say).

## Usage

1. First define AnimatedScrollBehavior as a behavior on an element.

```javascript
Polymer({
  is: 'scroll-button',
  extends: 'button',
  behaviors: [
    AnimatedScrollBehavior
  ]
});
```

In this case we're merely extending the native `button` element.

2. Specify a selector in the `scroll-to` attribute. Optionally supply an easing function:

`<button is="scroll-button" scroll-to="#the-end" easing="cubic-bezier(0.1, 0.7, 1.0, 0.1)"></button>`

3. The behavior will listen for click and tap events and then scroll there, using the specified easing.

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install


## Playing with `animated-scroll-behavior`

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at
`http://localhost:8080/components/animated-scroll-behavior/`, where `animated-scroll-behavior` is the name of the directory containing it.


## Running tests

Simply navigate to the `/test` directory of your element to run its tests. If
you are using Polyserve: `http://localhost:8080/components/animated-scroll-behavior/test/`

### web-component-tester

The tests are compatible with [web-component-tester](https://github.com/Polymer/web-component-tester).
Install it via:

    npm install -g web-component-tester

Then, you can run your tests on _all_ of your local browsers via:

    wct

#### WCT Tips

`wct -l chrome` will only run tests in chrome.

`wct -p` will keep the browsers alive after test runs (refresh to re-run).

`wct test/some-file.html` will test only the files you specify.
