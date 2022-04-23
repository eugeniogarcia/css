# Introduction

The CSS position property defines the position of an element in a document. This property works with the left, right, top, bottom and z-index properties to determine the final position of an element on a page (The z-index property specifies the stack order of an element. An element with greater stack order is always in front of an element with a lower stack order. z-index only works on positioned elements (absolute, relative, fixed, or sticky) and flex items (elements that are direct children of display:flex elements. If two positioned elements overlap without a z-index specified, the element positioned last in the HTML code will be shown on top).

There are five values the position property can take. They are:

- static
- relative
- absolute
- fixed
- sticky

## Static

This __is the default value for elements__. The __element is positioned according to the normal flow of the document__. __The left, right, top, bottom and z-index properties do not affect an element with position: static__.

## Relative

Elements with position: relative __remain in the normal flow of the document__. But, unlike static elements, __the left, right, top, bottom and z-index properties affect the position of the element__. An offset, based on the values of left, right, top and bottom properties, __is applied to the element relative to itself__.

## Absolute

Elements with position: absolute are __positioned relative to their parent elements__. In this case, __the element is removed from the normal document flow. The other elements will behave as if that element is not in the document. No space is created for the element in the page layout__. The values of left, top, bottom and right determine the final position of the element.

One thing to note is that __an element with position: absolute is positioned relative to its closest positioned ancestor__. That means that the parent element has to have a position value __other than position: static__.

If the closest parent element is not positioned, it is positioned relative to the next parent element that is positioned. __If there's no positioned ancestor element, it is positioned relative to the <html> element__.

## Fixed

Fixed position elements are __similar to absolutely positioned elements__. __They are also removed from the normal flow of the document__. But unlike absolutely positioned element, __they are always positioned relative to the <html> element__.

__One thing to note is that fixed elements are not affected by scrolling__. __They always stay in the same position on the screen__.

## Sticky

position: sticky __is a mix of position: relative and position: fixed__. It acts like a relatively positioned element until a certain scroll point and then it acts like a fixed element. Scroll on the result tab to see the result. You see it acts as a relative element until it gets to a certain point on the screen, top: 10px and then it gets there just like a fixed element.
