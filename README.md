#  CDN Source Fast
CDN Source Fast 是一个轻量级的纯前端工具，允许开发者通过一个 <script> 标签，在 HTML 中动态加载多个 CDN 资源，并支持通过 JSON 文件进行统一管理。

## 快速开始
### 1.配置CDN源
在**cdn-config.json**文件中添加CDN源，例如：
```
{
  "libraries": {
    "jquery": "https://code.jquery.com/jquery-3.6.0.min.js",
    "lodash": "https://cdn.jsdelivr.net/npm/lodash@4.17.21/lodash.min.js",
    "axios": "https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"
  }
}
```
### 2.引入<script>
在你的前端页面引入script标签：
```
<script data-cdn="jquery,lodash,axios" src="cdn-loader.js"></script>
```
在**data-cdn**属性中输入**cdn-config.json**中配置库的键值，即可引入对应的库。

或者使用CDN:
<script data-cdn="jquery,lodash,axios" src="https://unpkg.com/cdnsf@1.0.1/cdn-loader.js"></script>



