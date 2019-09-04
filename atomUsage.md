## atom编辑器使用总结
### 快捷键
+ `Ctrl + left`-移动到单词开头
+ `Ctrl + right`-移动到单词结尾
+ `Home`-移动到本行开头
+ `End`-移动到本行末尾
+ `Ctrl+Home` - 移动到文件开头
+ `Ctrl+End`- 移动到文件结尾
+ `Ctrl+G`- 移动到特定行特定列
+ `Ctrl+Shift+P`-打开命令面板(里面有所有的快捷命令，包括大量没有绑定快捷键的)
> atom支持自定义快捷键：点击头部的`Edit`按键->选择`Keymap`->编辑`keymap.cson`文件，具体语法参见https://flight-manual.atom.io/using-atom/sections/basic-customization/#customizing-keybindings

+ `Ctrl+Shift+F2`-当前行添加书签
+ `F2`-跳转到下一书签所在的行
+ `Shift-F2`-向后循环跳转到下一书签所在的行
+ `Ctrl+F2`-列出当前项目所有书签支持搜索选择跳转
+ `Ctrl+R`-列出当前文件所有符号支持搜索选择跳转
+ `Ctrl+T`-列出当前项目所有文件支持搜索选择跳转
+ `Shift+Up` - Select up
+ `Shift+Down` - Select down
+ `Shift+Left` - Select previous character
+ ` Shift+Right` - Select next character
+ `Ctrl+Shift+Left `- Select to beginning of word1
+ `Ctrl+Shift+Right` - Select to end of word
+ `Shift+End` - Select to end of line
+ `Shift+Home` - Select to first character of line
+ `Ctrl+Shift+Home` - Select to top of file
+ `Ctrl+Shift+End` - Select to bottom of file
+ `Ctrl+L` - Select the entire line
+ `Ctrl+J` - Join the next line to the end of the current line
+ `Ctrl+Up/Down` - Move the current line up or down
+ `Ctrl+Shift+D` - Duplicate the current line
+ `Ctrl+K Ctrl+U` - Upper case the current word
+ `Ctrl+K Ctrl+L` - Lower case the current word
+ `Alt+Ctrl+Q`-格式化选中区域（`editor.preferredLineLength`制定最大行长度）
+ `Ctrl+Shift+K` - Delete current line
+ `Ctrl+Backspace` - Delete to beginning of word
+ `Ctrl+Delete` - Delete to end of word
#### 多游标操作
+ `Ctrl+Click` - Add a new cursor at the clicked location
+ `Alt+Shift+Up/Down` - Add another cursor above/below the current cursor
+ `Ctrl+D` - Select the next word in the document that is the same as the currently selected word
+ `Alt+F3` - Select all words in the document that are the same as the currently selected word

#### 光标对齐相关
+ `Ctrl+M`-跳转到与光标相邻的括号
+ `Alt+Ctrl+,`- 选中当前括号内的内容
+ `Alt+Ctrl+.`- Close the current XML/HTML tag

#### 查找和替换相关
+ `Ctrl+F` - 在当前文件内查找
+ `Ctrl+Shift+F` - 在整个工程内查找

#### 代码块折叠
+ `Alt+Ctrl+[ `-折叠当前代码块
+ `Alt+Ctrl+] `-展开当前代码块
+ `Alt+Ctrl+Shift+[ `-折叠全部代码块
+ `Alt+Ctrl+Shift+] `-展开全部代码块

#### 语法选择器
+  `Ctrl+Shift+L`-打开语法选择器

### Snippets(片段)
在snippet.cson中可以自定义片段。可以通过点击面板`Edit`->`Snippets...`编辑snippet.cson

片段格式如下:
```
'.source.js':
  'Snippet Name':
    'prefix': 'Snippet Trigger'
    'body': 'Hello World!'
```
多行模板：
```
'.source.js':
  'if, else if, else':
    'prefix': 'ieie'
    'body': """
      if (${1:true}) {
        $2
      } else if (${3:false}) {
        $4
      } else {
        $5
      }
    """
```
多个snippet;
```
'.source.gfm':
  'Hello World':
    'prefix': 'hewo'
    'body': 'Hello World!'

  'Github Hello':
    'prefix': 'gihe'
    'body': 'Octocat says Hi!'

  'Octocat Image Link':
    'prefix': 'octopic'
    'body': '![GitHub Octocat](https://assets-cdn.github.com/images/modules/logos_page/Octocat.png)'
```
### 版本管理
+ `Alt+Cmd+Z`-分离头指针
> 分离头指针是一种快速方法，可以放弃所做的任何已保存和暂存的更改，并将文件还原到HEAD提交中的版本。
+ `Cmd+T`或`Ctrl+T`-快速打开项目中的文件
+ `Cmd+B`或`Ctrl+B`-快速跳转已打开的窗口
+ `Cmd+Shift+B`或`Ctrl+Shift+B`-显示未被追踪和已修改未提交的文件，相当于运行`git status`的效果
