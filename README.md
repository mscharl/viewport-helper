# Viewport Helper

A css-only helper to show the currently active viewport.

## Installation

Install via your preferred package manager.

```bash
npm install --save msc-viewport-helper
```

Create a helper file that includes and renders the viewport helper:

```scss
@use '~msc-viewport-helper' as helper;

$viewport-helper-breakpoints: $breakpoints;

@include helper.viewport-helper($breakpoints);
```

Your Breakpoint map should look like this. And make sure that the breakpoints are sorted by size.

```scss
$breakpoints: (
    xs: 0,
    sm: 576px,
    md: 768px,
    lg: 992px,
    xl: 1200px,
    hg: 1440px,
);
```

To enable the viewport helper you need to include the created helper file to your compiler settings. You also may want to only do this when _not_ building for production.

```js
{
    entry: {
        main: ['./src/js/main.js', './src/scss/main.scss'].concat(
            isProduction ? [] : ['./src/scss/viewport-helper.scss']
        );
    }
}
```

## Used By

This project is used by the following companies:

-   [MASSIVE ART](https://massiveart.com)

## License

[MIT](https://choosealicense.com/licenses/mit/)
