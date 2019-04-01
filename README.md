# JsDelay
js延迟加载方法

使用三种方式：
</br>1.基于jQuery的自定义方法
</br>2.jQuery的getScript()方法
</br>3.源生xmlHtmlRequest方法
</br>实现js的延迟加载。

</br>其中2 jquery.getScript()方法，加载并在全局作用域下执行脚本。如果多次加载相同URL的js文件，即使服务器对js文件启用了缓存，在第二次及以后加载该js文件时，jQuery.getScript()仍然不会缓存。因为该函数会在js文件的URL后面添加一个时间戳参数后缀，从而避免浏览器获取缓存的js文件。
</br>1方法在jQuery基础上，本地建立一个全局数组记录请求过的js路径。这种方法可以避免重复加载相同路径的js，但是js文件可能内部发生变化，因为避免了重复加载会导致js文件更新不及时。
</br>3方法使用源生xmlHttpRequest请求js文件，用动态添加<script>元素或者eval()方法执行文件。
