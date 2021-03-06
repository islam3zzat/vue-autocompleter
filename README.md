# vue-autocompleter

> yet another autocomplete plugin

## Installing
```bash
# using yarn
yarn add vue-autocompleter
# using npm
npm install --save vue-autocompleter
```
``` javascript
# in main.js for example
// ...
import Autocomplete 'vue-autocompleter'
```
## Usage
``` html
<Autocomplete
  :placeholder=<placeholder>
  :limit=<limit>
  :transform=<path>
  :api=<api>
  :param=<param>
  :method=<method>
  :closeOnSelect=<closeOnSelect>
  :resetOnSelect=<resetOnSelect>
  :optionsStyles=<optionsStyles>
  :optionStyles=<optionStyles>
  :inputStyles=<inputStyles>
  :optionsClass=<optionsClass>
  :optionClass=<optionClass>
  :inputClass=<inputClass>
  v-model=<msg>
  >
</Autocomplete>
```

## Documentation

| Prop          |  Type          |      Description      |  Default value |
|---------------|:--------------:|:---------------------|:---------------|
| placeholder   | String         | input Placeholder     | Placeholder    |
| limit         | Number         | results limit         | 5              |
| transform     | [Function, String]  | transformer function to map response to the desired option, or just a string representing key to grap from response |null |
| api           | String         | api endpoint          | null |
| param         | String         | param for search value| q (demo)|
| otherParams   | Object         | other  params passed with the request| {} |
| method        | String         | Api http method       | GET|
| closeOnSelect | Boolean        | Close dropdown once select an element | true |
| resetOnSelect | Boolean        | Reset dropdown once select an element | true |
| inputStyles   | Object         | inline styles for input |{}|
| optionsStyles | Object         | inline styles for options |{}|
| optionStyles  | Object         | inline styles for option item |{}|
| inputClass    | String         | input class | null |
| optionsClass  | String         | input class | null |
| optionClass   | String         | input class | null |
| beforeSearch  | Function       | functions gets called before sending api request, accepts two params (url, query) | null|
| filterMethod  | Function       | method to be used to filter provided options (should return boolean) | null|
| afterSearch | Function       | functions called after api response, accepts one param (response) | null|
| beforeUpdateValue | Function       | functions called before update value, accepts one param (value) | null|
| shouldUpdateValue | Function       | functions called before update value, accepts one param (value) and returns boolean wether to update value or not | null|
| afterUpdateValue | Function       | functions called after update value, accepts one param (value) | null|

## Customize option
You can customize how the option will be displayed by adding your template
```html
<!-- example -->
  <template  scope="{option, index}">
    <div class="option">
      <strong>{{index}}</strong>
      <span>{{option}}</span>
    </div>
  </template>

```


## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

