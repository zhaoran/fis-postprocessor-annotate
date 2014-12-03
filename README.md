fis-postprocessor-annotate
==========================

add ng-annotate for angularjs in fis postprocessor

在fis里继承ng-annotate的功能

> 安装

```javascript
    npm install -g fis-postprocessor-annotate
```

> 然后再fis-conf.js中开始annotate插件

```javascript
fis.config.merge({
    modules : {
        postprocessor : {
            js : 'annotate'
        }
    }
})
```
> 使用 [ng-annotate](https://github.com/olov/ng-annotate),默认是add，如果想remove，可以再fis中添加以下配置

```javascript
fis.config.merge({
    settings : {
        postprocessor : {
            annotate: {
                annotate:'remove'
            }
        }
    },
})
```

> 然后fis release的时候，就会加入ng-annotate的编译，让angular的代码可编译

> 此插件还用了 [semi](https://github.com/yyx990803/semi),在代码之后自动加上分号，也是方便压缩用的

