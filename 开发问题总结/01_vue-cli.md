# vue-cli插件使用
## 1. 说明:
	vue-cli是vue官方提供的脚手架工具
	github: https://github.com/vuejs/vue-cli

## 2. 使用vue-cli快速创建工程化vue项目
	npm install -g vue-cli    //下载脚手架包**（对于这命令电脑中全局安装一次即可，不需要重复安装）**
### 使用基于webpack的完整模板创建项目: webpack_demo(项目名字)
    vue init webpack webpack_demo（项目名字）
    cd webpack_demo
    npm install
    npm run dev
    访问: http://localhost:8080/
### 模板项目的结构
	|-- build : webpack相关的配置文件夹(基本不需要修改)
    	|-- dev-server.js : 通过express启动后台服务器
	|-- config: webpack相关的配置文件夹(基本不需要修改)
    	|-- index.js: 指定的后台服务的端口号和静态资源文件夹
	|-- node_modules:引入的组件化文件都在这里面
	|-- src : 源码文件夹
    	|-- components: vue组件及其相关资源文件夹
      	|-- App.vue: 应用根主组件
    	|-- main.js: 应用入口js
	|-- static: 静态资源文件夹
	|-- .babelrc: babel的配置文件---Babel是一个广泛使用的转码器，可以将ES6代码转为ES5代码
	|-- .editorconfig文件可以编辑统一开发的风格（比如‘空格键’、tab键的缩进问题等等）
	|-- .eslintignore: eslint检查忽略的配置
	|-- .eslintrc.js: eslint检查的配置
	|-- .gitignore: git版本管制忽略的配置
	|-- index.html: 主页面文件
	|-- package.json: 应用包配置文件 
	|-- README.md: 应用描述说明的readme文件

## 3. 编码测试与打包发布项目
### 编码测试:
	npm run dev
    访问: http://localhost:8080
    编码, 自动编译打包(HMR), 查看效果
### 打包发布
    npm run build
    npm install -g pushstate-server
    pushstate-server dist
    访问: http://localhost:9000