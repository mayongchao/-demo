# 使用vue配置rem适配
# 1.配置 flexible
## 安装 lib-flexible
	npm i lib-flexible --save`
# 2.在项目中引入lib-flexible
    1. //main.js
    2.import 'lib-flexible
# 3.添加meta标签
##在项目根目录的 index.html 中添加如下 meta
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
# 4.安装 px2rem-loader（px转rem）

## 实际开发中，我们通过设计稿得到的值单位是 px，所以要将 px 转换成 rem 再写进样式中。将 px 转换成 rem 我们将使用 px2rem 这个工具，它有 webpack 的 loader：px2rem-loader
	npm install px2rem-loader
# 5.配置 px2rem-loade
###在 vue-cli 生成的 webpack 配置中，vue-loader 的 options 和其他样式文件 loader 最终是都是由 build/utils.js 里的一个方法生成的。

###我们只需在 cssLoader 后再加上一个 px2remLoader 即可，px2rem-loader 的 remUnit 选项意思是 1rem=多少像素，结合 lib-flexible 的方案，我们将 px2remLoader 的 options.remUnit 设置成设计稿宽度的 1/10，这里我们假设设计稿宽为 750px。
	// utils.js
	var cssLoader = {
	  loader: 'css-loader',
	  options: {
	    minimize: process.env.NODE_ENV === 'production',
	    sourceMap: options.sourceMap
	  }
	}
	var px2remLoader = {
	  loader: 'px2rem-loader',
	  options: {
	    remUnit: 75
	  }
	}
	// .
###并放进 loaders 数组中

	// utils.js
	function generateLoaders(loader, loaderOptions) {
	  var loaders = [cssLoader, px2remLoader]
	  // ...
###修改配置后需要重启，然后我们在组件中写单位直接写 px，设计稿量多少就可以写多少了，舒服多了