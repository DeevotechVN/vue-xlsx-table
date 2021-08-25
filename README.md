Forked from [https://github.com/GeoffZhu/vue-xlsx-table](https://github.com/GeoffZhu/vue-xlsx-table)

# vue-xlsx-table

> No need to upload, view xlsx or xls file directly in your browser, Supported by [js-xlsx](https://github.com/SheetJS/js-xlsx).


## Requirements
- vue: ^2.0.0

## Usage
#### install

``` sh
 npm install @deevotechvn/vue-xlsx-table --save
```

#### main.js

```javascript
import vueXlsxTable from 'vue-xlsx-table'
Vue.use(vueXlsxTable, {rABS: false}) //Browser FileReader API have two methods to read local file readAsBinaryString and readAsArrayBuffer, default rABS false
```

#### file.vue

```vue
<template>
  <div id="app">
    <h1>vue-xlsx-table</h1>
    <vue-xlsx-table @on-select-file="handleSelectedFile"></vue-xlsx-table>
  </div>
</template>

<script>
export default {
  name: 'app',
  methods: {
    handleSelectedFile (convertedData) {
      console.log(convertedData)
    }
  }
}
</script>
```

## Develop
```
npm run dev  //develop
npm run build //production
```


