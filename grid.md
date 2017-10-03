# Grid Layout

Method of using a grid concept to lay out content, providing a mechanism for authors to divide available space for layout into columns and rows using a set of predictable sizing behaviors

Source: 

https://css-tricks.com/snippets/css/complete-guide-grid/

https://css-tricks.com/getting-started-css-grid/

### Browser support: 
http://caniuse.com/#search=grid

IE 11, Edge 14, 15 has partial support but otherwise most of modern browsers support unprefixed 68.14%

## Grid Value

- `grid` - generates a block-level grid
- `inline-grid` - generates an inline-level grid
- `subgrid` - if your grid container is itself a grid item (i.e. nested grids), you can use this property to indicate that you want the sizes of its rows/columns to be taken from its parent rather than specifying its own. **`subgrid` is not yet implemented in any browsers, and the specification is subject to change.**


## grid-template-columns grid-template-rows

Defines the columns and rows of the grid with a space-separated list of values. The values represent the track size, and the space between them represents the grid line.

https://codepen.io/peeweemiwie/pen/jGyVdZ

### `fr`

The fr unit allows you to set the size of a track as a fraction of the free space of the grid container. For example, this will set each item to one third the width of the grid container:

``` 
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```
or
``` 
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```

**`repeat` is not supported by IE, Edge nor Safari


## `grid-column-gap` `grid-row-gap`

Specifies the size of the grid lines. You can think of it like setting the width of the gutters between the columns/rows.

Sort of like `margin-right` `margin-bottom` to separate content and provide space between the elements.

```
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 10rem auto;
  grid-column-gap: 1rem;
  grid-row-gap: 1.5rem;
}
```
