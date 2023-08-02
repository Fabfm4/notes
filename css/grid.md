# This MD file is for rememeber how to build a web page with grid

## To Start
To start with grid We need a HTML tag container parent where we define a style as : `display: grid;`
This convert the container as a grid container, where all children element are available to use grid concepts

## Number of columns
### Grid template columns
To define the number of columns that we manage we use the style in the container parent is: `grid-template-columns`
You need define the number of spaces that you need, there are different ways:
* use `px` value: `grid-template-columns: 300px 300px 300px;` this defines 3 columns spaces as `300px`.
* use `fr` value: `grid-template-columns: 1fr 1fr 1fr;` this defines 3 columns spaces with size of 1fr or 1 fraction to define this you need define the size of container parent with `width: 900px` each fr gets the value of `300px`.
* use `repeat` function: `grid-template-columns: repeat(3, 300px);` or `width: 900px; grid-template-columns: repeat(3, 1fr);` those define 3 columns spaces as `300px.
### Grid Column
Sometimes we need to more spaces in earch item, for this we have the instruction `grid-column`, this instruction commonly recive a mix between 2 values divided for `/`
the instruction is `grid-column: 1 / 3;` `1` is the value where it start, and `3` is the value final position
```
|         |    |  <-- here we difine the item clas as `1 / 3` that means it start in the begin of first position and end in the begin of threeth item
|    |    |    |
|    |    |    |
```
There is another way to interpret the second element, it is for define what is the spaces wich element takes, you need use `span`
`grid-column: 1 / span 2;` how we saw in the previous example we define 3 as the end position but it create a element where the space is equals to 2 spaces, `span` is more usefully to understand the size of element
### Grid template rows
To define the number of rows that we manage we use the style in the container parent is: `grid-template-rows`
You need define the number of spaces that you need, there are different ways:
* use `px` value: `grid-template-rows: 300px 300px 300px;` this defines 3 columns spaces as `300px`.
* use `fr` value: `grid-template-rows: 1fr 1fr 1fr;` this defines 3 columns spaces with size of 1fr or 1 fraction to define this you need define the size of container parent with `width: 900px` each fr gets the value of `300px`.
* use `repeat` function: `grid-template-rows: repeat(3, 300px);` or `width: 900px; grid-template-rows: repeat(3, 1fr);` those define 3 columns spaces as `300px.

## Gap
Gap is the instruction to define the space between each element: `gap: 20px`

## Justify and Aling
`justify-items: value;`: this instruction set the aling horizontally for each child element, this instruction is defined in container parent
value can be:
* end
* start
* center
* stretch --> default
`aling-items: value;`: this instruction set the aling vertically for each child element, this instruction is defined in container parent
value can be:
* end
* start
* center
* stretch --> default

`justify-self: value;`: this instruction set the aling horizontally an specific child , this instruction is defined in specific child
value can be:
* end
* start
* center
* stretch --> default

`aling-self: value;`: this instruction set the aling vertically an specific child , this instruction is defined in specific child
value can be:
* end
* start
* center
* stretch --> default


[Official Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/grid)
