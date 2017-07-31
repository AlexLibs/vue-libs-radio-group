# Vue Simple Toggle (Switch)

A simple and super light Vue.js component for fancy radio group (state switch).

No dependencies. No sass/less compilation. Very easy to use :).

<img src="https://github.com/AlexLibs/vue-libs-radio-group/blob/master/demo/vue-libs-radio-group-demo.png" /><br>

## Installation

```bash
npm install vue-libs-radio-group --save
```

## Basic Usage

```javascript
import GroupButton from 'vue-libs-radio-group';

new Vue({

    components: {
        GroupButton
    },

    data () {
        return {
            currentState: 'all'
        }
    }
};
```

```html

<group-button v-bind:options="{active: 'Show Active', inactive: 'Show Inactive', all: 'Show All'}" v-model="currentState"></group-button>

```

## Customization

Override the relevant classes to customize it. For example, to make it all blue instead of #dc0606:

```css
    .vue-libs-radio-group {
        border: 1px solid blue;
    }
    .vue-libs-radio-group label {
        border-right: 1px solid blue;
    }
    .vue-libs-radio-group input[type="radio"]:checked + label {
        background-color: blue;
    }
```
