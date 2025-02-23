# article2card
一个把长文转款成摘要卡片/图片的前端应用，使用 Kimi 对文章进行结构化总结。

## 更新
@[kedyyan](https://github.com/kedyyan) 增加了一些模板和批量下载功能

## 如何使用
- 下载代码，运行`index.html`在浏览器打开
- 把要转写的文章链接输入，点击跳转到kimi进行重构
- 将Kimi 生成的内容复制粘贴到工具文本框即可
- 注意：
    - Kimi 有时会输出非 JSON 格式的内容，需要自行删除无效文本，仅保留第一个`{`到最后一个`}`之间的内容
    - 大文本框内容可编辑，如果 Kimi 总结的内容超出图片区域，手动编辑一下再重新预览。

## 背景多模板切换
在预览区支持多模板切换，以便于生成不同背景模板的内容卡片。

## 支持批量下载
支持批量下载，同时会下载一个含有文章标题与摘要的txt文件，便于内容发布。


## 更换背景图
- 替换`/assets/img/thumb1`文件下的`cover-card-default`和`detail-card-default`即可（需为png格式）
- 如需要多套模板，则需要制作cover-card-{新名字}和detail-card-{新名字}的图片，并修改index.html中 <option value="Climber">Climber</option>这部分内容，将Climber修改为与{新名字}匹配的内容，推荐写英文字符串。
- 图片尺寸为1200×1600
- 具体布局参考 `/assets/img`文件下的 `cover-card_demo`和`detail-card_demo`

## 项目依赖
- [html2canvas](https://github.com/niklasvh/html2canvas)
- [FileSaver.js](https://github.com/eligrey/FileSaver.js)
