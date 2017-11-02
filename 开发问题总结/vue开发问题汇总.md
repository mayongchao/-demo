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
##传递数据的两种方式
##1.父组件向子组件传递使用props
##2.子组件向父组件传递使用“自定义事件”
