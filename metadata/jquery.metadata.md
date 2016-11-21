##jquery metadata
metadata是一个用来解析DOM结构中的元数据的插件，有了jquery.metadata.js之后， 其他的插件就可以直接在DOM元素的属性中添加数据并且可以被争取的解析。

## How to use

```javascript
npm install jquery-metadata
```

然后直接在HTML中引入即可。因为metadata主要是为了其他的插件提供服务，因此最好放在head标签中。

1.第一种使用方法是直接在class标签中添加数据，这种方式是默认的
```javascript
<li class="someclass {some: 'data'} anotherclass">...</li>
```

2.第二种用法是在某个属性中添加数据


```html
<li data="{some:'random', json: 'data'}">...</li>
```

3.第三种方法是使用script标签来附加数据


```html
<li><script type="data">{some:"json",data:true}</script> ...</li>
```