## Transform

Transform allows elements styled with CSS to be transformed in two-dimensional space. Using the `translate()` function to change the position of an item, such as sliding something into view, is generally going to be more performant than manipulating its position. The same can be said about `scale()` over changing an element’s height or width such as expanding or collapsing a menu or accordion. The `rotate()` function is often used in microanimations. We can also use `opacity()`.

## Transition

When the styles for an element are changed, transitions allow for the shift from initial state to the new state to be visually smooth.As its name implies, __the transition property controls the visual aspect of how values change from one state to another over time__.

The transition property is the shorthand property for the following: property, duration, timing function, and delay.

## Keyframe Animations

Unlike transitions, which can only happen once when the user triggers the event, animations can be repeated over an indefinite period of time. They can also be applied when an element is added to the DOM such as an element going from a display:none to display:block.

```css
animation: name duration timing-function delay iteration-count direction fill-mode;
```

Another property that can be used with animation is __animation-play-state__ which allows the developer to pause and start an animation. When resumed, the animation will restart where it was paused rather than the beginning of the sequence. The default value for animation-play-state is __running__.

### Easing Functions

Easing functions define smooth transitions based on the Bézier curve. The curve is parametric,8 and the cubic variant is defined by four points: P0, P1, P2, and P3. P0 and P3 define the beginning and end of the curve, respectively. P1 and P2 represent the control points which give the curve its shape. Each point is defined by (x, y) coordinates.

### Stepping Functions

A stepping function which divides the animation into equal segments across time can also be used. Two values are used to define the animation’s timing: number of steps (n) and step position.
