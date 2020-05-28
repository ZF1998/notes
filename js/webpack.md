# Webpack

webpack是一个资源打包工具，用于整合和处理项目中依赖的资源。



## Webpack 配置组成

```
module.exports = {
  entry: './src/index.js', ------------- 打包的入口文件
  output: './dist/bundle.js', ---------- 打包的输出文件
  module: {
    rules: [ --------------------------- Loader 配置
      {
        test: /\.js$/,
        use: 'babel-loader'
      }
    ]
  },
  plugins: [ --------------------------- 插件配置
    new HtmlwebpackPlugin({
      template: './src/index.html'
    })
  ]
}
```



## 部分常用 Loader 的作用

默认 webpack 只能处理 js 和 json 后缀的文件，如果需要处理其它后缀的文件，需要添加对应的 loader。



**css-loader**: 将 css 文件转换成 common-js，通常配合 style-loader 使用。

**style-loader**: 将 css-loader 处理后的结果用 style 标签包裹起来，插入到页面的 head 标签中。

**file-loader**:  解析代码中依赖的文件，并输出到打包结果目录中。

**url-loader**: 将文件转换为 base64。

