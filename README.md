#  CDN Source Fast

![npm](https://img.shields.io/npm/v/cdnsf)

CDN Source Fast 是一个轻量级的纯前端工具，允许开发者通过一个 <script> 标签，在 HTML 中动态加载多个 CDN 资源，并支持通过 JSON 文件进行统一管理。

CDN Source Fast is a lightweight, pure frontend tool that allows developers to dynamically load multiple CDN resources in HTML using a single <script> tag. It also supports unified management of resources via a JSON file.

## 快速开始 Quick Start
### 1.配置CDN源 Configure CDN Sources

在**cdn-config.json**文件中添加CDN源，例如：

Add CDN sources to a cdn-config.json file, for example:

```
{
  "libraries": {
    "jquery": "https://code.jquery.com/jquery-3.6.0.min.js",
    "lodash": "https://cdn.jsdelivr.net/npm/lodash@4.17.21/lodash.min.js",
    "axios": "https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"
  }
}
```
### 2.引入<script> Add a <script> Tag

在你的前端页面引入script标签：

Include the <script> tag in your frontend page:

```
<script data-cdn="jquery,lodash,axios" src="cdn-loader.js"></script>
```
在**data-cdn**属性中输入**cdn-config.json**中配置库的键值，即可引入对应的库。

Enter the keys of the libraries configured in cdn-config.json in the data-cdn attribute to load the corresponding libraries.

或者使用CDN:

Alternatively, use a CDN:

```
<script data-cdn="jquery,lodash,axios" src="https://unpkg.com/cdnsf@1.0.1/cdn-loader.js"></script>
```



