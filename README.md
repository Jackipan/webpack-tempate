# webpack-tempate

webpack it

一步一步去深入了解webpack配置

## 一些必要插件

### clean-webpack-plugin:

### html-webpack-plugin:

### uglifyjs-webpack-plugin: 代码压缩，用于生产环境插件

其他类似插件： BabelMinifyWebpackPlugin / ClosureCompilerPlugin

### source-map: 在生产环境中使用devtool，对调试源码和运行基准测试很有用

### lodash 

避免在生产中使用 inline-`***` 和 eval-***，因为它们可以增加 bundle 大小，并降低整体性能。


- 使用webpack的内置的`DefinePlugin`方法来指定环境(优选)
- 在命令行使用 --optimize-minimize(会在后台调用UglifyJSPlugin)
- --define process.env.NODE_ENV="'production'"

* 这些简便方式虽然都很不错，但是我们通常建议只使用配置方式，因为在这两种场景中下，配置方式能够更好地帮助你了解自己正在做的事情。配置方式还可以让你更方便地控制这两个插件中的其他选项。


多入口
entry:{
    foo: './src/foo.js',
    bar: './src/bar.js'
}