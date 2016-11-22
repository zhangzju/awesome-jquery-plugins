## jquery modal

jquery modal是一款模态框插件，在bootstrap中，模态框是用来替代浏览器自身的alert，prompt和confirm的重要工具，jquery modal则可以理解为独立的不需要额外支持的模态框。



## How to use

首先npm安装这个依赖：

```javascript
npm install jquery-modal
```

然后在页面中导入文件，

```javascript
<script src="jquery.modal.min.js" type="text/javascript" charset="utf-8"></script>
```

在引入文件后，先添加需要加载的模态框组件：

```html
<form id="login-form" class="modal">
  ...
</form>
```

组件会使用到这个模态组件的id和class两个属性。关于模态框的样式，你可以自行设置。

模态框组件也可以是外部的HTML，因为组件也支持AJAX的方式载入模态框。

添加一个用于触发模态框出现事件的组件：

```html
<a href="#login-form" rel="modal:open">Login</a>
```

这里的href属性，在使用外部文件作为模态框时，只需要改为外部文件的链接地址即可。rel属性是必须的。

然后，对模态框进行初始化，这里有两个方法，第一个是：

```javascript
$('a[data-modal]').click(function(event) {
  $(this).modal();
  return false;
});
```

modal()可以添加许多参数来控制模态框的失效时间，延迟时间以及能否被关闭等等属性，详细的API参考文档。

第二个比较简单的方法就是：

```html
<a href="#ex5" data-modal>Open a DOM element</a>
<a href="ajax.html" data-modal>Open an AJAX modal</a>
```

直接在DOM元素中使用data-modal属性来给这个元素附加触发事件的功能。