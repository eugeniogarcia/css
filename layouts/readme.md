## Box-sizing

### content-box

__Box-sizing__ , or the property that defines the height and width of an element, __by default__ has a value of __content-box__ which means that when a __width and height__ is defined for an element, it is only applied to the __content__. __Adding padding or margin to the element therefore increases the percentage width of the total available viewport that the element utilizes__.

### border-box

Assigning box-sizing: __border-box__ changes how an element’s width and height is calculated. Instead of encompassing just the content, it takes in the content, padding, and border. When __padding or border is added, the width and height of the content itself__ is therefore decreased. __The margin still behaves the same way as with content-box__.

## Display

Margin and padding allow for manipulating the display of the element; the display property manipulates how elements are displayed in relationship to one another by specifying the type of rendering the box uses for the element

### Outside

These keywords specify the element's outer display type, which is essentially its role in flow layout:

- __Block__. The element generates a block element box, generating line breaks both before and after the element when in the normal flow. Also considered flow content, block elements stack atop one another unless they are affected by another property such as float. Es la opción por defecto en los siguientes elementos:

```html
<address>, <article>, <aside>, <blockquote>, <details>, <dialog>, <dd>, <div>, <dl>, <dt>, <fieldset>, <figcaption>, <figure>, <footer>, <form>, <h1>, <h2>, <h3>, <h4>, <h5>, <h6>, <header>, <hgroup>, <hr>, <li>, <main>, <nav>, <ol>, <p>, <pre>, <section>, <table>, <ul>
```

- __Inline__. The element generates one or more inline element boxes that do not generate line breaks before or after themselves. In normal flow, the next element will be on the same line if there is space. When the content is displayed inline, by default elements go from left to right and set themselves side to side, width permitting. By default, elements, regardless of padding, and margin, will align themselves to the text baseline. Es la opción por defecto en los siguientes elementos:

```html
<a>, <abbr>, <acronym>, <audio> (if it has visible controls), <b>, <bdi>, <bdo>, <big>, <br>, <button>, <canvas>, <cite>, <code>, <command>∗∗, <data>, <datalist>, <del>, <dfn>, <em>, <embed>, <i>, <iframe>, <img>, <input>, <ins>, <kbd>, <keygen>*, <label>, <map>, <mark>, <meter>, <noscript>, <object>, <output>, <picture>, <progress>, <q>, <ruby>, <s>, <samp>, <script>, <select>, <slot>, <small>, <span>, <strong>, <sub>, <sup>, <svg>, <template>, <textarea>, <time>, <u>, <tt>, <var>, <video>, <wbr>
```

- Inline-Block. Inline-block utilizes concepts from both block and inline. It will behave like a block element but flow with the surrounding content as if it were inline.

### Inside

- flow. The element lays out its contents using flow layout (block-and-inline layout). If its outer display type is inline or run-in, and it is participating in a block or inline formatting context, then it generates an inline box. Otherwise it generates a block container box.

- flow-root .The element generates a block element box that establishes a new block formatting context, defining where the formatting root lies.

- flex. The element behaves like a block element and lays out its content according to the flexbox model.
  - flex-direction. row, row-reverse, column, and column-reverse, where row is the default
  - flex-wrap. nowrap, wrap and wrap-reverse
  - justify-content. flex-start, flex-end, center, space-around, space-evenly and space-between

- grid. The element behaves like a block element and lays out its content according to the grid model.
  - grid-gap. This will determine how much space is between each row and/or column. For example, grid-gap: 5px 2rem would set a gap of 5 pixels between each row and a gap of 2 rems between each column.
  - justify-content. flex-start, flex-end, center, space-around, space-evenly and space-between
  - grid-auto-flow. Controla como se rellenan las celdas. _row_ o _column_ rellena por filas o por columnas. Añadiendo la opción _dense_ hace que se rellenen los gaps que puedan exitir - así especificaríamos _column-dense_, por ejemplo