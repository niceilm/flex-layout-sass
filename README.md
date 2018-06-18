Flex Layout Sass
---

[Angular Flex-Layout](https://github.com/angular/flex-layout) inspired

# install
```
npm i flex-layout-sass
```

# usages
## sass import
```
@import "~flex-layout-sass/mixin";
```

# mixin documents
## fx-layout
`@include fx-layout(<direction [wrap]>, [main-axis-value [cross-axis-value]], [layout-gap-value]);`
* direction: row, column, row-reverse, column-reverse (default row)
* wrap: none, wrap (default none)
* main-axis-value: null, start, center, end, space-around, space-between, space-evenly
* cross-axis-value: null, start, center, end, space-around, space-between, space-evenly, stretch
* layout-gap-value: % | px | vw | vh

### reference
* [fxLayout](https://github.com/angular/flex-layout/wiki/fxLayout-API)
* [fxLayoutAlign](https://github.com/angular/flex-layout/wiki/fxLayoutAlign-API)
* [fxLayoutGap](https://github.com/angular/flex-layout/wiki/fxLayoutGap-API)

### example
```scss
@import "~flex-layout-sass/mixin";

.selector {
  @include fx-layout(row wrap, center center, 10px);
}
```

## fx-flex
`@include fx-flex(<flex-value>, [parent-direction]);`
* flex-value: "" | px | % | vw | vh | <grow> <shrink> <basis>,;
* parent-direction: row, column, row-reverse, column-reverse default row;
    *  If parent-direction is not set, the last direction value of fx-layout is used.

### references
* [fxFlex](https://github.com/angular/flex-layout/wiki/fxFlex-API)

### example
```scss
@import "~flex-layout-sass/mixin";

.selector {
  @include fx-flex;
}
.selector {
  @include fx-flex(10px);
}
.selector {
  @include fx-flex(auto);
}
.selector {
  @include fx-flex(1 1 10px);
}
```

## fx-flex-order
`@include fx-flex-order(<order-value>);`
* order-value: int

### refereces
* [fxFlexOrder](https://github.com/angular/flex-layout/wiki/fxFlexOrder-API)

### example
```scss
@import "~flex-layout-sass/mixin";

.selector {
  @include fx-flex-order(1);
}
```

## fx-flex-offset
`@include fx-flex-offset(<offset-value>, [parent-direction]);`
* offset-value: % (default) | px | vw | vh
* parent-direction: row, column, row-reverse, column-reverse default row;
    *  If parent-direction is not set, the last direction value of fx-layout is used.

### refereces
* [fxFlexOffset](https://github.com/angular/flex-layout/wiki/fxFlexOffset-API)

### example
```scss
@import "~flex-layout-sass/mixin";

.selector {
  @include fx-flex-offset(10px);
}
```

## fx-flex-align
`@include fx-flex-align(<align-value>);`
* align-value: start, center, end, baseline, stretch

### refereces
* [fxFlexAlign](https://github.com/angular/flex-layout/wiki/fxFlexAlign-API)

### example
```scss
@import "~flex-layout-sass/mixin";

.selector {
  @include fx-flex-align(start);
}
```

## fx-flex-fill
`@include fx-flex-fill;`
* alias **fx-fill**

### refereces
* [fxFlexFill](https://github.com/angular/flex-layout/wiki/fxFlexFill-API)

### example
```scss
@import "~flex-layout-sass/mixin";

.selector {
  @include fx-flex-fill;
}
```