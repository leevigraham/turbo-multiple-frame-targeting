# @miii/turbo-multiple-frame-targeting
> Add support for multiple frame targeting in Turbo

## 💡&nbsp; Motivation
See [hotwired/turbo#475](https://github.com/hotwired/turbo/issues/475)

## 📦&nbsp; Setup
```sh
$ npm install @miii/turbo-multiple-frame-targeting
```

```js
import * as Turbo from '@hotwired/turbo'
import enableMultiFrameSupport from '@miii/turbo-multiple-frame-targeting'

Turbo.start()
enableMultiFrameSupport()
```

### Alternative setup
```js
import * as Turbo from '@hotwired/turbo'
import { enable, disable } from '@miii/turbo-multiple-frame-targeting'

Turbo.start()
enable()

// Later...
disable()
```

## 🚀&nbsp; Usage
This package will enable you to provide a space-separated list of identifiers, much like [Stimulus](https://stimulus.hotwired.dev/reference/controllers#multiple-controllers).
```html
<form data-turbo-frame="row_21 sidebar">
  ...
</form>

<a data-turbo-frame="row_21 sidebar">
  ...
</a>
```