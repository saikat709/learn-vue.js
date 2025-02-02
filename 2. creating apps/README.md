# # Creating apps
**App**'s are the entry point of vue framework. Note that -
1. We can have multiple apps in a single page - if needed.
2. every app runs without interrupting others.
3. we need a target element that vue will use to render the elements. and it should be unique for each app.

## # Syntax
```js
// create app with a object
const app = createApp({
    data(){
        return {
            count: 12
        }
    },
    template: `
        <h1>Count is: {{count}}</h1>
    `,
});

// mount a dom element with the selector it has.
app.mount("#target");
```

## createApp()
createApp takes an object as parameter.
   - It has:
     - data
     - template
     - methods
     - coumputed
     - props
     - components

Every of them has specific usage

Note:
1. Specifying a `template` will override the innerHtml of the element it is being mounted to e.g. #app. Overthise vue will use the use the innerHtml of the #target element.
2. We can separate the object  of the app in a different file. For this we would do-
    ```js
    // app_comp.js
    export default {
        data(){
            return {
                count: 12,
            }
        }
    }

    // main.js or index.js type=module
    import { createApp } from 'vue'
    import MyApp from './app_comp.js'

    createApp(MyApp).mount('#app')
    ```