# font-awesome-zTree

[Font Awesome](http://fontawesome.io/) theme for [zTree](http://www.ztree.me/).

## Demos

* [Full demos](http://wenzhixin.github.io/font-awesome-zTree/assets/zTree_v3/demo/en/)
* [完整例子](http://wenzhixin.github.io/font-awesome-zTree/assets/zTree_v3/demo/cn/)
* [jsFiddle: Standard Data](https://jsfiddle.net/wenyi/rx9nv1ts/)
* [jsFiddle: Simple Data](https://jsfiddle.net/wenyi/rx9nv1ts/1/)

## API Document

[Official API Document](http://www.ztree.me/v3/api.php)

## Usage

Include Font Awesome library (if your project doesn't use it already), `zTreeStyle.css` and `font-awesome-zTree.css` in the head tag your html document.

```html
<link rel="stylesheet" href="https://unpkg.com/@fortawesome/fontawesome-free@5.15.4/css/all.min.css">
<link rel="stylesheet" href="dist/zTreeStyle.css">
<link rel="stylesheet" href="dist/font-awesome-zTree.css">
```

Include jQuery library (if your project doesn't use it already) and zTree library in the head tag or at the very bottom of your document, just before the closing body tag (usually recommended for better performance).

```html
<script src="https://unpkg.com/jquery@3.7.0/dist/jquery.min.js"></script>
<script src="dist/jquery.ztree.all-3.5.min.js"></script>
```
Create a tree element with id:

```html
<ul id="tree" class="ztree"></ul>
```

Call with standard Data:
```js
var setting = {};

var zNodes = [
    {
        name: "pNode 01", open: true,
        children: [
            {
                name: "pNode 11",
                children: [
                    {name: "leaf node 111"},
                    {name: "leaf node 112"},
                    {name: "leaf node 113"},
                    {name: "leaf node 114"}
                ]
            },
            {
                name: "pNode 12",
                children: [
                    {name: "leaf node 121"},
                    {name: "leaf node 122"},
                    {name: "leaf node 123"},
                    {name: "leaf node 124"}
                ]
            },
            {name: "pNode 13 - no child", isParent: true}
        ]
    },
    {
        name: "pNode 02",
        children: [
            {
                name: "pNode 21", open: true,
                children: [
                    {name: "leaf node 211"},
                    {name: "leaf node 212"},
                    {name: "leaf node 213"},
                    {name: "leaf node 214"}
                ]
            },
            {
                name: "pNode 22",
                children: [
                    {name: "leaf node 221"},
                    {name: "leaf node 222"},
                    {name: "leaf node 223"},
                    {name: "leaf node 224"}
                ]
            },
            {
                name: "pNode 23",
                children: [
                    {name: "leaf node 231"},
                    {name: "leaf node 232"},
                    {name: "leaf node 233"},
                    {name: "leaf node 234"}
                ]
            }
        ]
    },
    {name: "pNode 3 - no child", isParent: true}
];

$(document).ready(function () {
    $.fn.zTree.init($("#tree"), setting, zNodes);
});
```

Call with simple data:

```js
var setting = {
    data: {
        simpleData: {
            enable: true
        }
    }
};

var zNodes =[
    { id:1, pId:0, name:"pNode 1", open:true},
    { id:11, pId:1, name:"pNode 11"},
    { id:111, pId:11, name:"leaf node 111"},
    { id:112, pId:11, name:"leaf node 112"},
    { id:113, pId:11, name:"leaf node 113"},
    { id:114, pId:11, name:"leaf node 114"},
    { id:12, pId:1, name:"pNode 12"},
    { id:121, pId:12, name:"leaf node 121"},
    { id:122, pId:12, name:"leaf node 122"},
    { id:123, pId:12, name:"leaf node 123"},
    { id:124, pId:12, name:"leaf node 124"},
    { id:13, pId:1, name:"pNode 13 - no child", isParent:true},
    { id:2, pId:0, name:"pNode 2"},
    { id:21, pId:2, name:"pNode 21", open:true},
    { id:211, pId:21, name:"leaf node 211"},
    { id:212, pId:21, name:"leaf node 212"},
    { id:213, pId:21, name:"leaf node 213"},
    { id:214, pId:21, name:"leaf node 214"},
    { id:22, pId:2, name:"pNode 22"},
    { id:221, pId:22, name:"leaf node 221"},
    { id:222, pId:22, name:"leaf node 222"},
    { id:223, pId:22, name:"leaf node 223"},
    { id:224, pId:22, name:"leaf node 224"},
    { id:23, pId:2, name:"pNode 23"},
    { id:231, pId:23, name:"leaf node 231"},
    { id:232, pId:23, name:"leaf node 232"},
    { id:233, pId:23, name:"leaf node 233"},
    { id:234, pId:23, name:"leaf node 234"},
    { id:3, pId:0, name:"pNode 3 - no child", isParent:true}
];

$(document).ready(function(){
    $.fn.zTree.init($("#tree"), setting, zNodes);
});
```

## LICENSE

**NOTE:** font-awesome-zTree is licensed under the [The MIT License](https://github.com/wenzhixin/font-awesome-zTree/blob/master/LICENSE). Completely free, you can arbitrarily use and modify this plugin. If this plugin is useful to you, you can **Star** this repo, your support is my biggest motive force, thanks.
