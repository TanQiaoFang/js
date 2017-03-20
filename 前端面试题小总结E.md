# js 
 get和post的区别？  get是从后台获取数据，post是把表单的数据传送到服务器。get安全性能比较低；post安全性能高。get方法从后台获取的数据会显示在URL中，用户
 可以看到，post表单内容是随head头部一起传递到后台，用户看不见。
 对与get方式，服务器端用request、querystring获取变量的值，对与post方式，服务器端用request.form获取提交的数据。
 get传递的数据量较小，不能大于2KB，post传递的数据量较大，一般被默认为不受限制，但理论上，11s4中最大量为80KB，11S5中为100KB。
 # sessionstorage、localstorage和cookie之间的区别。
 cookie存储容量较小，本地离线存储容量较大。cookie是永久保存，用户不手动清除，缓存会一直存在，本地离线存储不会传递到服务器，只会保存在本地。
 localstorage是把缓存保存在本地，即使浏览器关闭，也会有保留；sessionstorage是浏览器窗口关闭前有效，浏览器窗口已关闭，缓存就会被清除。
 作用域不同，sessionstorage不在不同的浏览窗口中共享，即使是同一个页面；localstorage在所有同源窗口中都是共享的；cookie也是在所有同源窗口中都是共享的。
 ##h5的新特性
 页面头部更加简洁，书写更加方便。
 新增header、footer、audio、video等语义化的标签，去除不常用的标签。
 新增canvas动画。
 新增localstorage和sessionstorage，本地离线存储。
 新增表单更多空间，如：date、time、email、URL、search等。
 ###写出ie6 bug的解决方法
 双边距bug float引起的，使用display
 3像素问题 使用float引起的，使用display-inline -3px.
 超链接hover点击后失败，使用正确的书写顺序 link visited hover active.
 le z-index问题给父级添加position：relative。
 png透明，使用js代码改。
 min-height最小高度 ！important解决。
 select在ie6下遮盖，使用iframe嵌套。
 为什么没用办法定义1px左右的宽度容器，（IE6默认的行高造成的，使用over：hidden，zoom：0.08，line-height:1px）
 ###<img>标签上tittle与alt属性的区别是什么？
 Alt当图片不显示是用文字代表
 Tittle为该属性提供信息。
 ###css选择符有哪些？哪些属性可以继承？优先级算法如何计算？内联合important哪个优先级高？
 标签选择符 类选择符 id选择符
 继承不如指定id>class>标签选择  后者优先级高
 ####什么是语义化HTML？有何意义？为什么要做到语义化？
 语义化的HTML就是正确的标签，做正确的事情，符合内容的结构化（内容语义化），选择合适的标签（代码语义化），能够使于开发者阅读和写出更优雅的代码的同事让网络爬虫很好地解析。
 在做前端开发的时候要记住：HTML告诉我们一块内容是什么（或其意义），而不是它长什么样子，它的样子应该由css来决定（即结构与样式分离！）
 有利于SEO，有利于搜索引擎爬虫更好的理解我们的网页，从而获取更多的有效信息，提升网页的权重，在没有css的时候能够清晰的看出网页的结构，增强可读性。
 便于团队开发和维护，语义化的HTML可以让开发者更容易的看明白，从而提高团队的效率和协同能力。
 支持多终端设备的浏览器渲染。
 ###前端页面有哪三层构成？分别是什么？作用是什么？
 结构层（HTML）、表示层（css）、行为层（js）.
 ###你做的页面在哪些浏览器测试过？这些浏览器的内核分别是什么？
 IE（IE内核）、火狐（Geko）、谷歌（webkit）、opear(Presto)。
 ###描述css reset的作用和用途
 reset重置浏览器的css默认属性浏览器的品种不同，样式不同，然后重置、让他们统一。
 ###解释css sprites,如何使用
 css精灵 把一堆小的图片整合到一张大的图片上，减轻服务器对图片的请求数量。
 ###浏览器标准模式和怪异模式之间的区别是什么？
 盒子模型 渲染模式不同。
 使用window.top.document.compatMode可显示为什么模式。
 ###你如何对网站的文件和资源进行优化？期待的解决方案包括：
 文件合并、文件最小化/文件压缩、使用CDN托管、缓存的使用。
 ###清除浮动的几种方式，各自的优缺点：
 使用空标签清除浮动 clear：both（理论上能清楚任何标签，增加无意义的标签）
 使用overflow:auto（空标签元素清除浮动而不得不增加无意代码的弊端，使用zoom：1用于兼容IE）
 使用after为元素清除浮动（用于IE浏览器）
 ###例举3中强制类型转换和2种隐式类型转换？
 强制（parseInt、parseFloat、number）
 隐式（== - ===）
 ###数组方法pop()push()unshift()shift()
 push()尾部添加 pop（）尾部删除  UNshift（）头部添加  shift（）头部删除
 ###IE和DOM事件流的区别
 执行顺序不一样  参数不一样  事件加不加on  this指向的问题。
 apply、call、bind三者是用来改变函数的this对象的指向的；
 apply、call、bind 三者第一个参数都是this要指向的对象，也就是想指定的上下文。
 apply、call、bind三者都可以利用后续参数传参，bind是返回对应函数，便于稍后调用：apply、call则是立即调用。
 ###javascript中出现undefined的情况有哪些？
 函数没有返回值，或者返回值为空，出现undefined。
 变量定义了为赋值。
 引用没有提供实参函数形参的值，出现undefined。
 查询一个对象属性或者数组元素的值不存在，出现undefined。
 ###"=="、"="、"==="有什么区别？
 "=="表示比较，会做类型转化，然后再进行比较。
 "="表示赋值，例如a=1,相当于把1赋值给a .
 "==="表示严格比较，不会做类型转化。
