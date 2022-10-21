## Vue-custom-select-box

Quick start [install component NPM packages](https://www.npmjs.com/package/vue-custom-select-box).

## Documentation

1.  __[Installation](#installation)__
1. __[Example](#usage)__
1. __[Browser globals](#browser-globals)__
1.  __[Props](#props)__
1. __[Slots](#slots)__

## Installation
 install component from [NPM](https://www.npmjs.com/package/vue-custom-select-box)
 
 - **NPM**
   
    ```sh
    # npm
    npm install --save vue-custom-select-box
    
    # yarn
    yarn add vue-custom-select-box
    ``` 
    
- **Global setup**
   
    ```javascript
    import VueCustomSelectBox from 'vue-custom-select-box';
    import "vue-custom-select-box/style.css";
    
    new Vue({
      components: {
        VueCustomSelectBox,
      },
    });
    
    // or
    Vue.component('vue-custom-select-box', require('vue-custom-select-box'));
    // or
    Vue.component('v-spinner', VueCustomSelectBox);
    ``` 
- **Local setup**
    
    ```javascript
    import VueCustomSelectBox from 'vue-custom-select-box';
    import "vue-custom-select-box/style.css";

    export default {
        // ...
        components: { VueCustomSelectBox }
        // ...
    }
    
    ``` 
- **Example**
    > Install component first then import it as you want as `Global` `Local` 
    ```html
    <template>
      <div>
        <VueCustomSelectBox 
            v-model="result"
            :options="options"
            option-value="id"
            option-text="title"
        />
      </div>
    </template>
    ```
    ```javascript
    import VueCustomSelectBox from 'vue-custom-select-box';
    import "vue-custom-select-box/style.css";

    export default {
        // ...
        data(){
            return {
                options: [
                    // ...
                    {
                        title: "Hello world",
                        id: 1
                    }
                    // ...
                ],
                result: null
            }
        },
        components: { VueCustomSelectBox } 
        // ...
    }
    
    ``` 
- **Browser globals**

    The dist folder contains vue-custom-select-box.umd.cjs and vue-custom-select-box.js
    ```html
    <link rel="stylesheet" href="path/to/style.css" />
    <script src="path/to/vue.js"></script>
    <script src="path/to/vue-custom-select-box/dist/vue-custom-select-box.js"></script>
    // or
    <script src="path/to/vue-custom-select-box"></script>
    <script>
      var app = new Vue({
        el: '#app',
        components: {
          VueCustomSelectBox,
        },
      });
    </script>
    ```

## Props

|                    |      Default       |               Type                |  Required  |
| ------------------ | :----------------: | :-------------------------------: | :--------: |
| placeholder        |   `-- Select --`   |             `String`              | `optional` |
| searchPlaceholder  | `Search e.g abc..` |             `String`              | `optional` |
| selectAllLabel     |    `Select all`    |             `String`              | `optional` |
| limit              |    `undefined`     |             `Number`              | `optional` |
| selectAll          |       `true`       |             `Boolean`             | `optional` |
| multiple           |      `false`       |             `Boolean`             | `optional` |
| options            |        `[]`        |              `Array`              | `required` |
| value              |    `undefined`     | `[Array, Object, String, Number]` | `required` |
| optionValue        |    `undefined`     |             `String`              | `optional` |
| optionText         |    `undefined`     |             `String`              | `optional` |
| trackBy            |    `undefined`     |             `String`              | `optional` |
| animated           |       `true`       |             `Boolean`             | `optional` |
| disabled           |      `false`       |             `Boolean`             | `optional` |
| closeOnSelect      |      `false`       |             `Boolean`             | `optional` |
| clearInputOnSelect |      `false`       |             `Boolean`             | `optional` |

## Slots

| Name         |                                                Example                                                |
| ------------ | :---------------------------------------------------------------------------------------------------: |
| selectButton | ` <template v-slot:selectButton="{open, tags, multiple, originalLimit, limited, label}"></template> ` |
| option       |                            ` <template v-slot:option="item"></template> `                             |
| noResult     |                          ` <template v-slot:noResult="search"></template> `                           |


> *want to see more features? [Contact me](https://own-portfolio-tree.vercel.app/)*