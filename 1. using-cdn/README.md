## 1. Index.js ( javascript type - default  )
Note: **vue.global.js**
```html
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

<script>
    const { createApp } = Vue
<script>

```

## 2. Index2.js ( module type )
Note: **vue.esm-browser.js**
```html
<script type="module">
import { createApp } from 'https://unpkg.com/vue@3/dist/vue.esm-browser.js'
```


## 3. Index3.js ( importmap + module type )
Note: **vue.esm-browser.js**

```html
<script type="importmap">
    {
        "imports": {
            "vue": "https://unpkg.com/vue@3/dist/vue.esm-browser.js"
        }
        }
</script>

<script type="module">
    import { createApp } from 'vue';
</script>
```


`
As we know, type='javascript' script linking, links all files linked to that html file. So no import is needed. module type is required if want to use import.
`