# CSS Transitions

CSS transitions provide a way to control animation speed when changing CSS properties. Instead of having property changes take effect immediately, you can cause the changes in a property to take place over a period of time. The browser will come up with the intermediate states of the properties you are animating, and you can even control the interval and acceleration of an animation.

##### `transition-property`
Specifies the name or names of the CSS properties to which transitions should be applied. Only properties listed here are animated during transitions; changes to all other properties occur instantaneously as usual.

##### `transition-duration`
Specifies the duration over which transitions should occur. You can specify a single duration that applies to all properties during the transition, or multiple values to allow each property to transition over a different period of time.

##### `transition-timing-function`
Specifies a function to define how intermediate values for properties are computed. Timing functions determine how intermediate values of the transition are calculated.

Here are the possible timing function values:
- `ease` - transition effect with a slow start, then fast, then end slowly (this is default)
- `linear` - transition effect with the same speed from start to end
- `ease-in` - transition effect with a slow start
- `ease-out` - transition effect with a slow end
- `ease-in-out` - transition effect with a slow start and end
- `cubic-bezier(n,n,n,n)` - lets you define your own values in a cubic-bezier function

##### transition-delay
Defines how long to wait between the time a property is changed and the transition actually begins.

### `transition` shortcut form
```css
div {
    transition: <property> <duration> <timing-function> <delay>;
}```

## How to Use
In order to use CSS Transitions, you must have the following 3 things:
- Specify which CSS properties to transition
- Specify the duration of the transition (default is 0)
- Have something cause the specified CSS property to change (often an external script or something like a `:hover` state in the CSS)

### Example

The following setup should result in a red box that transitions to become wider over 2 seconds when hovered.

```html
<div class='embiggen'>Watch me grow</div>
```

```css
.embiggen {
  width: 200px;
  height: 100px;
  background: red;
  transition: width 2s;
}
.embiggen:hover {
  width: 400px;
}
```

Note that the transition also takes 2 seconds when the hover state is released and the box returns to its original width.

### Compatibility
Some older browsers need specific prefixes (`-webkit-`) to understand the transition properties, but for the most part this is [very widely supported](https://caniuse.com/#feat=css-transitions).
