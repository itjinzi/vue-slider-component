# Events

### change

- **Type**: `(value) => void`

- **Arguments**:

  - `{number | string | number[] | string[]} value`

- **Usage**:

  The event that is triggered when the value changes.

### dragStart

- **Type**: `() => void`

- **Usage**:

  The event that is triggered when the mouse/finger presses the slider.

### dragging

- **Type**: `(value) => void`

- **Arguments**

  - `{number | string | number[] | string[]} value`

- **Usage**:

  The event that is triggered when the slider is dragged.

  `value` is the value inside the component, and the internal value can be obtained when `lazy = true`.

### dragEnd

- **Type**: `() => void`

- **Usage**:

  Drag and drop the event that triggered.

### error

- **Type**: `(type, message) => void`

- **Arguments**

  - `{ERROR_TYPE} type` Error type

  - `{string} message` Error message

  ```ts
    enum ERROR_TYPE {
      VALUE = 1, // Value is illegal
      INTERVAL = 2, // `interval` cannot be divisible by `(max - min)`
      MIN, // Value is less than min
      MAX, // Value is greater than max
      ORDER, // When `order` is false, `minRange/maxRange/enableCross/fixed` is still set
    }
  ```

- **Usage**:

  Event triggered when an error occurs in a component

- **See also**: <router-link :to="$route.meta.lang + ' advanced/input'">The \<input> linkage</router-link>

