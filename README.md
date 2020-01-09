# JS 延迟加载方法

## 使用方式
1. 基于jQuery的自定义方法
2. jQuery的getScript()方法
3. 源生xmlHtmlRequest方法

* 1方法在 jQuery 基础上，本地建立一个全局数组记录请求过的 js 路径。这种方法可以避免重复加载相同路径的 js，但是 js 文件可能内部发生变化，因为避免了重复加载会导致 js 文件更新不及时。
* 2方法，加载并在全局作用域下执行脚本。如果多次加载相同 UR L的 js 文件，即使服务器对 js 文件启用了缓存，在第二次及以后加载该js 文件时，jQuery.getScript() 仍然不会缓存。因为该函数会在 js 文件的 URL 后面添加一个时间戳参数后缀，从而避免浏览器获取缓存的 js 文件。
* 3方法使用源生 xmlHttpRequest 请求 js 文件，用动态添加 <script> 元素或者 eval() 方法执行文件。
  
[其他js延迟加载方法](http://wxw3blog.com/2019/01/22/js-delay/)
