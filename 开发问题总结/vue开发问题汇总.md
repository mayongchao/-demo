# vue开发问题汇总 #
##|----.editorconfig文件可以编辑统一开发的风格（比如‘空格键’、tab键的缩进问题等等）
![](https://i.imgur.com/OBMOecE.png)
###可以通过indent_size = intValue 来修改缩进的值
##|----.eslintignore: eslint检查忽略的配置
开发中可根据实际情况忽略检查文件
有一种强制性忽略配置 开发中慎用
![](https://i.imgur.com/ZOM3LFX.png)
##|----使用webstorm创建template模板
1. ![](https://i.imgur.com/VAyHjrD.png)
2. ![](https://i.imgur.com/hwcNF0w.png)
3. ![](https://i.imgur.com/cuaGTUv.png)
4. ![](https://i.imgur.com/9DAkTe1.png)
5. ![](https://i.imgur.com/4tXNpyY.png)
##|----解决vue运行过程中端口占用的错误：
###之所以报错是因为本地的端口号被占用，需要手动修改运行时的端口号
1. ![](https://i.imgur.com/faeFkU5.png)
2. ![](https://i.imgur.com/WKTm83J.png)
## vue在使用css预处理器的时候npm命令需要安装两个包分别是
###npm install stylus --save-dev 
![](https://i.imgur.com/3mA9vBg.png)
###npm install stylus-loader
![](https://i.imgur.com/gFaK6o4.png)
##组件遇到的问题
###1.引入的组件的时候需要在components：【】 中声明组件
![](https://i.imgur.com/laGTKye.png)
###2.在标签命名中不要使用大写，标签名必须用短横线隔开
![](https://i.imgur.com/IsuroeJ.png)
###3组件模板中只可以使用一个根元素，不能使用并列标签，并且不可以在根元素中使用模板语法
![](https://i.imgur.com/iru7v1q.png)
###否则会报如下错误：译文：不能在有状态组件根元素上使用v字，因为它会呈现多个元素
![](https://i.imgur.com/h5eqnIW.png)
##传递数据的两种方式
##1.父组件向子组件传递使用props
###注意：是父组件向子组件传递，父组件使用标签属性的方式向子组件传递数据（类型可以是String、Number、Function、Array、Object、Boolean）
![](https://i.imgur.com/FfBGrJP.png)
###组件通过props的方式接受数据，需要注意的是需要声明接收数据的类型
![](https://i.imgur.com/970PKmf.png)
##2.子组件向父组件传递使用“自定义事件”
##首先在父组件中定义方法，通过标签属性的方式传递给子组件
![](https://i.imgur.com/Bx2Xry3.png)
![](https://i.imgur.com/eKrdDIL.png)
##然后在子组件中调用父组件定义的方法，并且传递参数（其实传递的参数就是子组件在向父组件传递数据）
![](https://i.imgur.com/1mRP5XP.png)
![](https://i.imgur.com/2oWutJT.png)



