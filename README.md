# 安装
##　`mkdir browserify-learn && cd browserify-learn`
## `npm i npm -g`
## `npm init -y`
## `npm install browserify --save-dev`

# 新建测试demo
* 根目录下新建source文件夹，该文件下新建moudle.js
* 根目录下新建dist文件夹

```js [moudle.js]
function test(  ){
	alert(1)
}
```
# 修改package.json
```js
// > 可改成 -o
{
   ...
  "scripts": {
    "build": "browserify source/module.js > dist/dist.js"
  }
  ... 
}
```
`npm run build`
结果：生成对应的dist.js文件

```js [dist.js]
(function e(t,n,r){function s(o,u){if(!n[o]){if(!t[o]){var a=typeof require=="function"&&require;if(!u&&a)return a(o,!0);if(i)return i(o,!0);var f=new Error("Cannot find module '"+o+"'");throw f.code="MODULE_NOT_FOUND",f}var l=n[o]={exports:{}};t[o][0].call(l.exports,function(e){var n=t[o][1][e];return s(n?n:e)},l,l.exports,e,t,n,r)}return n[o].exports}var i=typeof require=="function"&&require;for(var o=0;o<r.length;o++)s(r[o]);return s})({1:[function(require,module,exports){
/**
 * Created by rawraw on 2017/6/20.
 */
function test(  ){
	alert(1)
}

},{}]},{},[1]);
```
