# Viewport Helper

A css-only helper to show the currently active viewport.

## Installation

Install via your preferred package manager.

```bash
npm install --save msc-viewport-helper
```

Include the helper in your main scss file.

```scss
@import '~msc-viewport-helper';
```

Set the breakpoint variable in your variables file.

```scss
$viewport-helper-breakpoints: $breakpoints;
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

To enable the viewport helper you need to set the `$viewport-helper-enabled` variable to `true`. When using Webpack you can automate this by [injecting the scss variable](https://webpack.js.org/loaders/sass-loader/#additionaldata):

```js
{
    loader: 'sass-loader',
    options: {
        sourceMap: true,
        additionalData: isProduction ? '' : '$viewport-helper-enabled: true;',
    },
}
```

If you are using `sass-loader < 9` you need to use the property `prependData` instead.

## Used By

This project is used by the following companies:

-   [MASSIVE ART](https://massiveart.com)

## License

[MIT](https://choosealicense.com/licenses/mit/)
