![slogan](https://user-images.githubusercontent.com/11075892/42421484-e620f0d8-8308-11e8-8b6c-0e659eadfcd3.png)     
   
   
# vue-ins-progress-bar    

[![license](https://img.shields.io/badge/license-MIT-4cb9f2.svg)](https://revolunet.mit-license.org/) [![downloads](https://img.shields.io/badge/downloads-200+/month-b041a8.svg)](https://www.npmjs.com/package/vue-ins-progress-bar)     
   
`a vue component of ins-style progress bar`   
   
`一款 ins 风格的 vue 进度条组件`   
   
## Demo    
    
[Live Demo](https://meloalright.github.io/vue-ins-progress-bar/)   
   
## Install    
    
```shell
$ npm i vue-ins-progress-bar   
```
   
## Usage    
   
`main.js`   
   
```JavaScript
import VueInsProgressBar from 'vue-ins-progress-bar'

const options = {
  position: 'fixed',
  show: true,
  height: '3px'
}

Vue.use(VueInsProgressBar, options)
```
    
    
    
`App.vue`    
    
```vue    
<template>
  <div id="app">
    <router-view/>
    <vue-ins-progress-bar></vue-ins-progress-bar>
  </div>
</template>

<script>
export default {
  name: 'App',
  mounted () {
    this.$insProgress.finish()
  },
  created () {
    this.$insProgress.start()

    this.$router.beforeEach((to, from, next) => {
      this.$insProgress.start()
      next()
    })

    this.$router.afterEach((to, from) => {
      this.$insProgress.finish()
    })
  }
}
</script>
```
   
## APIs   
   
```JavaScript
this.$insProgress.start() // start the loading
```
   
```JavaScript
this.$insProgress.finish() // finish the loading
```
   
```JavaScript
this.$insProgress.height(4) // resize the height of loading bar to 4px
```
   
   
## Source    
   
Repository: [vue-ins-progress-bar](https://github.com/meloalright/vue-ins-progress-bar)      
   
Author: [@meloalright](https://github.com/meloalright)   
   
   
## License   
   
[MIT](https://opensource.org/licenses/MIT)   
