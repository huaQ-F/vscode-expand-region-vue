[![Build Status](https://travis-ci.org/windwp/vscode-expand-region.svg?branch=master)](https://travis-ci.org/windwp/vscode-expand-region)  

# vscode-expand-region-vue  
expand selection , It works similar to ExpandRegion for Emacs and “Structural Selection” (Control-W) in the JetBrains IDE's (i.e. IntelliJ IDEA).  

# 源码说明  
是修改 https://github.com/windwp/vscode-expand-region 原作者的库，添加了 vue 文件识别和在 html/vue 文件中自动识别 js 区域和 DOM 区域(原作者 html/vue 文件只看作 html/vue 功能扩展选择，不会识别 html/vue 里面 script 标签里面的 js 区域转换成 js 扩展选择)  

### 目前只支持HTML 、VUE、JAVASCRIPT、PHP  

JavaScript  

将选择扩展到单词  
将选择扩展到引号（仅限内容）  
将选择扩展到引号（带引号）  

将选择扩展到方括号  
将选择扩展到表达式  
将选择扩展到大括号的内容（在这种情况下为所有参数）  
将选择扩展到行  
将选择扩展到函数体（不带花括号）  
将选择扩展到函数体（带花括号）  
等等...  

HTML/PHP/VUE  

将选择扩展到单词  
将选择扩展到引号（仅限内容）  
将选择扩展到引号（带引号）  
展开选择以完成自闭标签  
将选择扩展到父节点内容  
展开选择以完成节点  
将选择扩展到父节点内容   
等等...  

#基础功能  
支持多光标  
undo_expand_region 递减选择功能  

#使用  
设置键盘快捷键。打开"键绑定"并添加以下代码：  
{
"key"："ctrl+w" ，"command"："expand_region" ， "when"："editorTextFocus"
},  
{
"key"："ctrl+shift+w" ，"command"："undo_expand_region" ， "when"："editorTextFocus && editorHasSelection"
}  

#发展  
npm 安装  
npm compile  
npm test:watch（运行 mocha 进行测试）  
变更日志  
0.1.27  
支持 vue、自动将 html/vue 文件下 script 标签里转 js 扩展  
0.0.1  
首次发布  


## 三个修改的插件
- 扩展选区插件  
[expand-region-vue](https://marketplace.visualstudio.com/items?itemName=huaQ-F.expand-region-vue)

- 用模板右键创建 html、js、vue2、python文件  
[Vue Py Template](https://marketplace.visualstudio.com/items?itemName=huaQ-F.vue2-html-python-template)

- translation 中文翻译转换变量  
[translation 中文翻译转换变量](https://marketplace.visualstudio.com/items?itemName=huaQ-F.translation2var)
