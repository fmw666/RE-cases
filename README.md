
### 读取 css 名

`/(?<=[\.#]|^)[\w-\[\]]+(?=[ :\[\.]|$)/g`

```js
strs = [
    '.logoCustom .form-pl25 .left-tips',
    '.disabled:hover',
    '.node-disk[disabled]',
    '#disk-info > div',
    '.voi-tabs-top.tab-content-border > .tab-content',
    '.example',
    'div',
    '[treecontrol]',
]

strs.forEach(str => {
    var res = str.match(/(?<=[\.#]|^)[\w-\[\]]+(?=[ :\[\.]|$)/g)

    console.log(res, res[0])
});
```

```
[ 'logoCustom', 'form-pl25', 'left-tips' ] logoCustom
[ 'disabled' ] disabled
[ 'node-disk[disabled]' ] node-disk[disabled]
[ 'disk-info' ] disk-info
[ 'voi-tabs-top', 'tab-content-border', 'tab-content' ] voi-tabs-top
[ 'example' ] example
[ 'div' ] div
[ '[treecontrol]' ] [treecontrol]
```
