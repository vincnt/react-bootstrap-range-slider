[![License: MIT](https://img.shields.io/github/license/jaywilz/react-bootstrap-range-slider)](https://github.com/jaywilz/react-bootstrap-range-slider/blob/master/LICENSE) [![NPM version](https://img.shields.io/npm/v/react-bootstrap-range-slider)](https://www.npmjs.com/package/react-bootstrap-range-slider) [![NPM downloads](https://img.shields.io/npm/dw/react-bootstrap-range-slider)](https://www.npmjs.com/package/react-bootstrap-range-slider) [![Required react version](https://img.shields.io/npm/dependency-version/react-bootstrap-range-slider/peer/react)](https://github.com/jaywilz/react-bootstrap-range-slider/blob/master/package.json) [![Issues](https://img.shields.io/github/issues/jaywilz/react-bootstrap-range-slider)](https://github.com/jaywilz/react-bootstrap-range-slider/issues)


# React Bootstrap Range Slider

A range slider with tooltips for React Bootstrap v1.0.0+ / Bootstrap 4 that extends the HTML `<input type="range">` element.

Check out the [Examples Page](https://jaywilz.github.io/react-bootstrap-range-slider/) for live demos of all main slider features.

<a href="https://jaywilz.github.io/react-bootstrap-range-slider/">
<img src="./screenshots/react-bootstrap-range-slider-screenshot.png?raw=true" alt="React Bootstrap Range Slider screenshot showing rendered slider component with various options applied, including tooltips and color variants" width="452">
</a>

## Installation

    yarn add react-bootstrap-range-slider

or

    npm install react-bootstrap-range-slider

### Prerequisites

[React Bootstrap](https://github.com/react-bootstrap/react-bootstrap) must be installed and the [Bootstrap CSS](https://react-bootstrap.netlify.com/getting-started/introduction#stylesheets) imported (or included).

## Usage

In your `index.js` or similar:

```JavaScript
import 'bootstrap/dist/css/bootstrap.css'; // or include from a CDN
import 'react-bootstrap-range-slider/dist/react-bootstrap-range-slider.css';
```

Your component:

```JavaScript
import React, { useState } from 'react';
import RangeSlider from 'react-bootstrap-range-slider';

const MyComponent = () => {

  const [ value, setValue ] = useState(0); 

  return (
    <RangeSlider
      value={value}
      onChange={changeEvent => setValue(Number(changeEvent.target.value))}
    />
  );

};
```

## Features

 - Compatible with React Bootstrap v1.0.0+ and Bootstrap 4;
 - Implemented using HTML5 `<input type="range">` element;
 - A tooltip can be configured to automatically display on hover or be constantly visible;
 - A custom tooltip formatter function can be provided.
 - Aligns horizontally with Bootstrap form controls;
 - Bootstrap small (`sm`) and large (`lg`) sizes are supported;
 - Bootstrap button color variants such as 'primary' and 'secondary' are supported;

## Options (as React props)

| Property | Type | Default | Description |
| --- | --- | --- | --- |
| `value` | `number` | | The current value of the slider. |
| `onChange` | `function` | | A callback fired when the range slider's value changes. |
| `onAfterChange` | `function` | | A callback fired after interaction with the slider. |
| `min` | `number` | `0` | The minimum value of the slider. |
| `max` | `number` | `100` | The maximum value of the slider. |
| `step` | `number` | `1` | The granularity with which the slider can step through values. |
| `disabled` | `boolean` | `false` | Disables the slider. |
| `size` | `'sm'` \| `'lg'` | | Input size variants, for compatibility with other Bootstrap form components. |
| `variant` | `string` | `'primary'` | Color variant, equivalent to the Bootstrap Button color variant. One of: `'primary'`, `'secondary'`, `'success'`, `'danger'`, `'warning'`, `'info'`, `'dark'`, `'light'` |
| `tooltip` | `'auto'` \| `'on'` \| `'off'` | `'auto'` | If `'auto'` the tooltip will be visible only when hovered. If `'on'` the tooltip will always be visible. If `'off'` no tooltip will be displayed.  |
| `tooltipPlacement` | `'top'` \| `'bottom'` | `'bottom'` | Placement of tooltip relative to slider thumb. |
| `tooltipLabel` | `function` | | A function that returns the tooltip's content (either a string or element). The function's first argument is the current slider value. |
| `tooltipStyle` | `object` | | Style to be applied to tooltip div. |
| `tooltipProps` | `object` | | Properties applied to the tooltip's `<div>` element. |
| `inputProps` | `object` | | Properties applied to the `<input>` element. |
| `ref` | `ReactRef` | | If provided, ref will be forwarded to the underlying `<input>` element. |
| `bsPrefix` | `string` | `'range-slider'` | Change the underlying component CSS base class name and modifier class names prefix. **This is an escape hatch** for working with heavily customized bootstrap css. |

## Browser Compatibility

React Bootstrap Range Slider works in most modern web browsers and in Internet Explorer 10+ (with [polyfills](https://create-react-app.dev/docs/supported-browsers-features/#supported-browsers) required for React to work).

| Browser | Supported |
| --- | --- |
| Chrome | Yes |
| Edge | Yes |
| Firefox | Yes |
| Internet Explorer | 10, 11 |
| Opera | Yes |
| Safari | Yes |
| Samsung Internet | Yes |
| UC | Yes |
| Yandex | Yes |

## License

Copyright (c) 2020 Jason Wilson

[MIT License](./LICENSE)
