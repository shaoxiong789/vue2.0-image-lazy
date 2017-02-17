# vue2.0-image-lazy
A image lazy loading plugin for vue.

## Demo
[Click me](https://shaoxiong789.github.io/vue2.0-image-lazy/example/demo.html).

## Brower compatibility
IE9+


## Env
vue@2.0 + webpack + es6

## Install
#### npm
```shell
$ npm install vue2.0-image-lazy
```

## Usage
#### Example
```html
<div id="app">
    <img v-lazy="img" v-for="img in imgs">
</div>

<script>
	import 'babel-polyfill'; // es6 shim
	import Vue from 'vue';
	import vueLazy from 'vue2.0-image-lazy';

    Vue.use(vueLazy, {
    	loading: 'imgs/default.jpg', //default image, if element has 'src' attribute, ignore this
    	error: 'imgs/error.jpg' //if image load failed, try to load the image
    });

    new Vue({
    	el: '#app',
    	data: {
    		imgs: [
    			'imgs/1.jpg',
    			'imgs/2.jpg',
    			'imgs/3.jpg',
    			'imgs/4.jpg',
    			'imgs/5.jpg',
    			'imgs/6.jpg',
    			'imgs/7.jpg',
    			'imgs/8.jpg'
    		]
    	}
    });

</script>
```
