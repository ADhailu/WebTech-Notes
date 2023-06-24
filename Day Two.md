# Web Technology



---
# Bootstrap

Bootstrap is a popular front-end framework for building responsive and mobile-first websites. It includes a variety of pre-built components, such as buttons, forms, and navigation menus, that can be easily customized to fit the needs of a specific project.


---

****Breakpoints****

**Breakpoints are customizable widths that determine how your responsive layout behaves across device or viewport sizes in Bootstrap.**

## **Core concepts**

- **Breakpoints are the building blocks of responsive design.** Use them to control when your layout can be adapted at a particular viewport or device size.
- **Use media queries to architect your CSS by breakpoint.** Media queries are a feature of CSS that allow you to conditionally apply styles based on a set of browser and operating system parameters. We most commonly use `min-width` in our media queries.
- **Mobile first, responsive design is the goal.** Bootstrap’s CSS aims to apply the bare minimum of styles to make a layout work at the smallest breakpoint, and then layers on styles to adjust that design for larger devices. This optimizes your CSS, improves rendering time, and provides a great experience for your visitors.

# **Containers**

Containers are a fundamental building block of Bootstrap that contain, pad, and align your content within a given device or viewport.

Containers are the most basic layout element in Bootstrap and are **required when using our default grid system**. Containers are used to contain, pad, and (sometimes) center the content within them. While containers *can* be nested, most layouts do not require a nested container.

Bootstrap comes with three different containers:

## **Default container**

Our default `.container` class is a responsive, fixed-width container, meaning its `max-width` changes at each breakpoint.

Copy

`<div class="container">
  <!-- Content here -->
</div>`

## **Responsive containers**

Responsive containers allow you to specify a class that is 100% wide until the specified breakpoint is reached, after which we apply `max-width`s for each of the higher breakpoints. For example, `.container-sm`is 100% wide to start until the `sm` breakpoint is reached, where it will scale up with `md`, `lg`, `xl`, and `xxl`.

Copy

`<div class="container-sm">100% wide until small breakpoint</div>
<div class="container-md">100% wide until medium breakpoint</div>
<div class="container-lg">100% wide until large breakpoint</div>
<div class="container-xl">100% wide until extra large breakpoint</div>
<div class="container-xxl">100% wide until extra extra large breakpoint</div>`

## **Fluid containers**

Use `.container-fluid` for a full width container, spanning the entire width of the viewport.

Copy

`<div class="container-fluid">
  ...
</div>`

# **Grid system**

Use our powerful mobile-first flexbox grid to build layouts of all shapes and sizes thanks to a twelve column system, six default responsive tiers, Sass variables and mixins, and dozens of predefined classes.

****Example****

`<div class="container">
  <div class="row">
    <div class="col">
      Column
    </div>
    <div class="col">
      Column
    </div>
    <div class="col">
      Column
    </div>
  </div>
</div>`

The above example creates three equal-width columns across all devices and viewports using our predefined grid classes. Those columns are centered in the page with the parent `.container`.

## **Grid options**

Bootstrap’s grid system can adapt across all six default breakpoints, and any breakpoints you customize. The six default grid tiers are as follow:

- Extra small (xs)
- Small (sm)
- Medium (md)
- Large (lg)
- Extra large (xl)
- Extra extra large (xxl)

# **Columns**

Learn how to modify columns with a handful of options for alignment, ordering, and offsetting thanks to our flexbox grid system. Plus, see how to use column classes to manage widths of non-grid elements.

## **How they work**

- **Columns build on the grid’s flexbox architecture.** Flexbox means we have options for changing individual columns and [modifying groups of columns at the row level](https://getbootstrap.com/docs/5.0/layout/grid/#row-columns). You choose how columns grow, shrink, or otherwise change.
- **When building grid layouts, all content goes in columns.** The hierarchy of Bootstrap’s grid goes from [container](https://getbootstrap.com/docs/5.0/layout/containers/) to row to column to your content. On rare occasions, you may combine content and column, but be aware there can be unintended consequences.
- **Bootstrap includes predefined classes for creating fast, responsive layouts.** With [six breakpoints](https://getbootstrap.com/docs/5.0/layout/breakpoints/)and a dozen columns at each grid tier, we have dozens of classes already built for you to create your desired layouts. This can be disabled via Sass if you wish.

## **Alignment**

Uses flexbox alignment utilities to vertically and horizontally align columns.

# **Gutters**

Gutters are the padding between your columns, used to responsively space and align content in the Bootstrap grid system.

## **How they work**

- **Gutters are the gaps between column content, created by horizontal `padding`.** We set `padding-right` and `padding-left` on each column, and use negative `margin` to offset that at the start and end of each row to align content.
- **Gutters start at `1.5rem` (`24px`) wide.** This allows us to match our grid to the [padding and margin spacers](https://getbootstrap.com/docs/5.0/utilities/spacing/) scale.
- **Gutters can be responsively adjusted.** Use breakpoint-specific gutter classes to modify horizontal gutters, vertical gutters, and all gutters.

## **Horizontal gutters**

Example

```
<div class="container px-4">
  <div class="row gx-5">
    <div class="col">
     <div class="p-3 border bg-light">Custom column padding</div>
    </div>
    <div class="col">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
  </div>
</div>
```

****Vertical gutters****

```
<div class="container overflow-hidden">
  <div class="row gy-5">
    <div class="col-6">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
  </div>
</div>
```

---

## **Horizontal & vertical gutters**

`.g-*` classes can be used to control the horizontal gutter widths, for the following example we use a smaller gutter width, so there won’t be a need to add the `.overflow-hidden` wrapper class.

`<div class="container">
  <div class="row g-2">
    <div class="col-6">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
  </div>
</div>`

## **Row columns gutters**

Gutter classes can also be added to [row columns](https://getbootstrap.com/docs/5.0/layout/grid/#row-columns). In the following example, we use responsive row columns and responsive gutter classes.

`<div class="container">
  <div class="row row-cols-2 row-cols-lg-5 g-2 g-lg-3">
    <div class="col">
      <div class="p-3 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-3 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-3 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-3 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-3 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-3 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-3 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-3 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-3 border bg-light">Row column</div>
    </div>
    <div class="col">
      <div class="p-3 border bg-light">Row column</div>
    </div>
  </div>
</div>`

## **No gutters**

The gutters between columns in our predefined grid classes can be removed with `.g-0`. This removes the negative `margin`s from `.row` and the horizontal `padding` from all immediate children columns.

**Need an edge-to-edge design?** Drop the parent `.container` or `.container-fluid`.

In practice, here’s how it looks. Note you can continue to use this with all other predefined grid classes (including column widths, responsive tiers, reorders, and more).

.col-sm-6 .col-md-8

.col-6 .col-md-4

Copy

`<div class="row g-0">
  <div class="col-sm-6 col-md-8">.col-sm-6 .col-md-8</div>
  <div class="col-6 col-md-4">.col-6 .col-md-4</div>
</div>`

## **Change the gutters**

Classes are built from the `$gutters` Sass map which is inherited from the `$spacers` Sass map.

Copy

`$grid-gutter-width: 1.5rem;
$gutters: (
  0: 0,
  1: $spacer * .25,
  2: $spacer * .5,
  3: $spacer,
  4: $spacer * 1.5,
  5: $spacer * 3,
);`
  

1. CSS stands for Cascading Style Sheets, which is a language used to describe the presentation of HTML and XML documents. Here are 10 CSS tags:
- `font-size`: sets the size of the font
- `color`: sets the color of the text
- `background-color`: sets the background color of an element
- `margin`: sets the margin around an element
- `padding`: sets the padding inside an element
- `border`: sets the border around an element
- `text-align`: sets the horizontal alignment of text
- `display`: sets how an element is displayed
- `float`: sets the alignment of an element
- `position`: sets the position of an element
1. SCSS stands for Sassy CSS and is a type of preprocessor for CSS. It allows for the use of variables, functions, and nesting, making it easier to write and maintain large CSS files. One example of a difference between CSS and SCSS is that in SCSS, you can define a variable for a color and use it throughout the file, making it easier to update the color in the future.
2. Computer resistors are electronic components that resist the flow of electrical current. They work by reducing the amount of current that flows through a circuit, which can be useful for controlling the voltage of a circuit. Resistors are typically made of a material that resists the flow of electricity, such as carbon or metal. The resistance of a resistor is measured in ohms and is represented by a color code on the resistor itself.

