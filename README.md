# vue2-countdown

基于vue2.0的活动倒计时组件  
可以使用服务端当前时间  
在倒计时开始或者结束的时候,可以自定义回调.  
文档：<a href="https://cgygd.github.io/vue2-countdown/">https://cgygd.github.io/vue2-countdown/</a>  
demo：<a href="https://cgygd.github.io/vue2-countdown/example/index.html" target="_blank">https://cgygd.github.io/vue2-countdown/example/index.html</a>

## Install
```
npm install vue2-countdown --save

```

## Usage

```js
import CountDown from 'vue2-countdown'
components: {
    CountDown
},
methods: {
  countDownS_cb: function (x) {
    console.log(x)
  },
  countDownE_cb: function (x) {
    console.log(x)
  }
}
```

```html
<count-down v-on:start_callback="countDownS_cb(1)" v-on:end_callback="countDownE_cb(1)" :currentTime="1481450106" :startTime="1481450110" :endTime="1481450115" :tipText="'距离开始文字1'" :tipTextEnd="'距离结束文字1'" :endText="'结束自定义文字2'" :dayTxt="'天'" :hourTxt="'小时'" :minutesTxt="'分钟'" :secondsTxt="'秒'"></count-down>
```

### options
1. **currentTime** - 当前时间戳,如果不传,默认获取用户本地的时间(建议传服务器的当前时间) 
    - **type**: Number
    - **required** : false
    - **default** : ( new Date() ).getTime()
2. **startTime** - 开始时间戳
    - **type**: Number
    - **required** : true
3. **endTime** - 结束时间戳
    - **type**: Number
    - **required** : true
4. **tipText** - 开始倒计时之前的提示文字
    - **type**: String
    - **required** : false
    - **default** : 距离开始
5. **tipTextEnd** - 开始倒计时之后的提示文字
    - **type**: String
    - **required** : false
    - **default** : 距离结束
6. **endText** - 倒计时结束之后的提示文字
    - **type**: String
    - **required** : false
    - **default** : 已结束
7. **dayTxt** - 自定义显示的天数文字
    - **type**: String
    - **required** : false
    - **default** : :
8. **hourTxt** - 自定义显示的小时文字
    - **type**: String
    - **required** : false
    - **default** : :
9. **secondsTxt** - 自定义显示的分钟文字
    - **type**: String
    - **required** : false
    - **default** : :
10. **secondsFixed** - 自定义显示的秒数文字
    - **type**: String
    - **required** : false
    - **default** : :
### callBack
1. **start_callback** - 开始倒计时结束之后的回调方法
    - **type**: Function
    - **required** : false
2. **end_callback** - 活动倒计时结束之后的回调方法
    - **type**: Function
    - **required** : false
