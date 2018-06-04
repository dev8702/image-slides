# React Image Slides

[![codecov](https://codecov.io/gh/loadingwyn/react-imageslides/branch/master/graph/badge.svg)](https://codecov.io/gh/loadingwyn/react-imageslides)

> A mobile friendly images slideshow react component

## Example

![demo1](demo/demo1.gif)
![demo2](demo/demo2.gif)

[![Edit l2xpwy3xrq](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/l2xpwy3xrq?view=preview)

## Features

* Close to the native experience(use [Alloyfinger](https://github.com/AlloyTeam/AlloyFinger))
* Pinch to zoom in/out
* No unnecessary rendering( the component only renders no more than 3 images at a time)

## Get Started

1.  Run `yarn add react-imageslides react react-dom alloyfinger`
    The package has peer dependencies on `react@^16.0.0`, `react-dom@16.0.0`, and `alloyfinger`.

2.  Render it!

```js
import React from 'react';
import ReactDOM from 'react-dom';
import ImageSlides from 'react-imageslides';
const images = [
  'http://img.zcool.cn/community/0101f856cfff206ac7252ce6214470.jpg',
  'http://a4.att.hudong.com/05/55/01200000033533115855502090905.jpg',
  'http://img.zcool.cn/community/0101f856cfff206ac7252ce6214470.jpg',
  'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1503235534249&di=4c198d5a305627d12e5dae4c581c9e57&imgtype=0&src=http%3A%2F%2Fimg2.niutuku.com%2Fdesk%2Fanime%2F0529%2F0529-17277.jpg',
];
ReactDOM.render(
  <ImageSlides images={images} isOpen />,
  document.getElementById('root'),
);
```

## Apis

| Property    |     Type     | Default | Required | Description                                                         |
| :---------- | :----------: | :-----: | :------: | :------------------------------------------------------------------ |
| addon       |     func     |         |          | Display extra content of the image (addon must return a react node) |
| images      |    array     |         |   yes    | Image urls to display                                               |
| isOpen      |     bool     |  false  |          | Whether the component is open                                       |
| index       |    number    |    0    |          | Index of the first image to display                                 |
| loadingIcon | func \| node |         |          | The component displayed when the image is loading                   |
| noTapClose  |     bool     |  false  |          | If `true`, the close event will not be triggered by single tap.     |
| onClose     |     func     |         |          | Callback fired when the component closes                            |
| onChange    |     func     |         |          | Callback fired when the url                                         |
