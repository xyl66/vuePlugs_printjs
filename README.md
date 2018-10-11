# vuePlugs_printjs
vue打印插件
**使用方法**

```
import Print from '@/plugs/print'
Vue.use(Print) // 注册
<template>
<section ref="print">
	打印内容
	<div class="no-print">不要打印我</div>
</section>
</template>
this.$print(this.$refs.print) // 使用
```
<font color=#c00 >注意事项</font>
需使用ref获取dom节点，若直接通过id或class获取则webpack打包部署后打印内容为空
**指定不打印区域**
方法一. 添加no-print样式类
```
<div class="no-print">不要打印我</div>
```
方法二. 自定义类名
```
<div class="do-not-print-me-xxx">不要打印我</div>
this.$print(this.$refs.print,{'no-print':'.do-not-print-me-xxx'}) // 使用
```
