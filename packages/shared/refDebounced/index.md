---
category: Reactivity
alias: useDebounce, debouncedRef
---

# refDebounced

Debounce execution of a ref value.

## Usage

```js {5}
import { refDebounced } from '@vueuse/core'
import { shallowRef } from 'vue'

const input = shallowRef('foo')
const debounced = refDebounced(input, 1000)

input.value = 'bar'
console.log(debounced.value) // 'foo'

await sleep(1100)

console.log(debounced.value) // 'bar'
```

You can also pass an optional 3rd parameter including maxWait option. See `useDebounceFn` for details.

## Recommended Reading

- [**Debounce vs Throttle**: Definitive Visual Guide](https://kettanaito.com/blog/debounce-vs-throttle)
