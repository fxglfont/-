# 命名规范
HTML属性：以 data- (如：data-quantity, data-price) 作为前缀  
# 代码格式规范
用两个空格来代替制表符（tab） -- 这是唯一能保证在所有环境下获得一致展现的方法  
嵌套元素应当缩进一次（即两个空格）  
对于属性的定义，确保全部使用双引号，绝不要使用单引号。  
属性顺序: class,id, name,data-*,src, for, type, href, value,title, alt,role, aria-*  
# 标签使用规则
自闭合（self-closing）标签，无需闭合 ( 例如： img input br hr 等 )；  
多媒体回溯 对页面上的媒体而言，像图片、视频、canvas 动画等，要确保其有可替代的接入接口  
不使用行内样式（<style>.no-good {}</style>）  
不在元素上使用 style 属性（<hr style="border-top: 5px solid black">）  
不使用行内脚本（<script>alert('no good')</script>）  
不使用表象元素（i.e. <b>, <u>, <center>, <font>, <b>）  
不要使用<em>和<strong>(主要)  
不要使用<i>和<b>(主要)  
不使用表象 class 名（i.e. red, left, center）  
HTML 内容至上：不要让非内容信息污染了你的 HTML  
Tab Index 在可用性上的运用 依据元素的重要性来重新排列其 tab 切换顺序  
ID 和锚点: 通常一个比较好的做法是将页面内所有的头部标题元素都加上 ID  
块元素可以包含内联元素或某些块元素，但内联元素却不能包含块元素  
块级元素不能放在<p>里面  
h1、h2、h3、h4、h5、h6、p、dt只能包含内嵌元素，不能再包含块级元素  
内嵌元素与内嵌元素并列，块级元素与块级元素并列  
li 或者 dt 标签必须被包含在ul, ol 或者 dl 这些容器  
# 最佳实践代码
为文档设置IE兼容规则  
   <!-- 兼容IE低版本的浏览器 -->  
   <!DOCTYPE html>  
   <!--[if lt IE 7]>  <html class="no-js lt-ie9 lt-ie8 lt-ie7" lang="zh"> <![endif]-->  
   <!--[if IE 7]>    <html class="no-js lt-ie9 lt-ie8" lang="zh"> <![endif]-->  
   <!--[if IE 8]>    <html class="no-js lt-ie9" lang="zh"> <![endif]-->  
   <!--[if gt IE 8]>  <html class="no-js" lang="zh"> <![endif]-->  









