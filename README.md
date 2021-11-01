# 前端样式规范-PC

### 背景

因各项目繁多，UI设计稿仅能作为参考，为统一各项目的样式，利用sass预处理语言和html-class特性使用本规范作为前端开发指南。



### Font-size规范

##### 项目中仅使用fs-12、fs-14、fs-16、fs-18、fs-20, 5种字体大小进行开发（特殊情况除外）。

###### <img src="https://i.loli.net/2021/10/27/8CLES67GHznxhMy.png" alt="image-20211027094425462" style="zoom:80%;" />

##### fs-14例子：

###### ![image-20211027094415032](https://i.loli.net/2021/10/27/Ks3NgaJf7rB4mOH.png)



### Padding规范

| class                            | css                                      |
| -------------------------------- | ---------------------------------------- |
| p-6、 p-12、  p-24、 p-48、 p-96 | padding: 6px; ...                        |
| pt-6、pt-12、pt-24、pt-48、pt-96 | padding-top: 6px;...                     |
| pb-6 ...                         | padding-bottom: 6px;...                  |
| pl-6 ...                         | padding-left: 6px;...                    |
| pr-6 ...                         | padding-right: 6px;...                   |
| ptb-6 ...                        | padding-top: 6px; padding-bottom:6px;... |
| plr-6 ...                        | padding-left: 6px; padding-right:6px;... |



### Margin规范（同上）

| class                            | css                                    |
| -------------------------------- | -------------------------------------- |
| m-6、m-12、  m-24、 m-48、 m-96  | margin: 6px; ...                       |
| mt-6、mt-12、mt-24、mt-48、mt-96 | margin-top: 6px;...                    |
| mb-6 ...                         | margin-bottom: 6px;...                 |
| ml-6 ...                         | margin-left: 6px;...                   |
| mr-6 ...                         | margin-right: 6px;...                  |
| mtb-6 ...                        | margin-top: 6px; margin-bottom:6px;... |
| mlr-6 ...                        | margin-left: 6px; margin-right:6px;... |

### 其他常用class，Text-align、Font-weight

| class | css                 |
| ----- | ------------------- |
| ta-l  | text-align: left;   |
| ta-r  | text-align: right;  |
| ta-c  | text-align: center; |
| fw-b  | font-weight: bold;  |
|       |                     |

### 安装方法：

###### 安装y2t-common-css并改造vue.config.js

```javascript
npm install y2t-common-css
```

###### 在main.js（入口文件）中引入，用于支持  <u>使用方法：1.1</u> 

```javascript
//引入了y2t0common-css/index.css
import 'y2t-common-css';
```

###### 	改造vue.config.js中sass的配置，让y2t-common-css可以全局进行使用, 用于支持 <u>使用方法：1.2</u> 

```javascript
module.exports = {
  devServer: {},
  chainWebpack: config => {
  },
  css: {
    loaderOptions: {
      sass: {
        // so this assumes you have a file named `y2t-common-css/@extend.scss`
        data: `
               @import "y2t-common-css/@extend.scss";
              `
      }
    }
  }
};
```

### 使用方法：

###### 			1.1   直接class应用

###### 			![image-20211027094355917](https://i.loli.net/2021/10/27/DLHu3i5povGStqK.png)

###### 			1.2   .scss文件中或.vue文件中使用@extend 继承（利用sass语法）

###### ![image-20211028134436214](https://i.loli.net/2021/10/28/vVohls5NHnp8uqG.png)

