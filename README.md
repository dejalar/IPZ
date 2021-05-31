# Object Tracking JavaScript SDK
[![NPM Version](https://img.shields.io/npm/v/@cloud-annotations/object-tracking.svg)](https://npmjs.org/package/@cloud-annotations/object-tracking)
[![NPM Downloads](https://img.shields.io/npm/dm/@cloud-annotations/object-tracking.svg)](https://npmjs.org/package/@cloud-annotations/object-tracking)

![Demo](cat.gif)

### Посилання для редагування та тестування
https://codesandbox.io/s/pedantic-cherry-npfol?file=/src/index.js

### Просте відстеження об'єктів за допомогою TensorFlow.js.

Просто намалюйте квадрат та відстежуйте його, як він рухається в відео, ніякого навчання не потрібно.

## Встановлення
```bash
npm install @cloud-annotations/object-tracking
```

## Використання
```js
import objectTracker from '@cloud-annotations/object-tracking'

const frame1 = document.getElementById('img1')
const frame2 = document.getElementById('img2')
const frame3 = document.getElementById('img3')
//    ...
const frameN = document.getElementById('imgN')

const tracker = objectTracker.init(frame1, [x, y, width, height])
const box2 = await tracker.next(frame2)
const box3 = await tracker.next(frame3)
//    ...
const boxN = await tracker.next(frameN)

// box =>
[x, y, width, height]
```

## Використання за допомогою тегу скрипта
```html
<script src="https://cdn.jsdelivr.net/npm/@cloud-annotations/object-tracking"></script>
```
