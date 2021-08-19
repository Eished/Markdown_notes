## 常用快捷键

基础的到处使用类似于`ctr+c`是复制这种“客套话”就不说了....以下快捷键组合都是以**MAC**为例，**不过带`cmd`键的你只要换成`ctr`在**Win**上也都是好使的**。当然这些都是默认的快捷键，你自己改掉了一些快捷键不能说我赖皮。

### 常用`cmd+shift+?`系列

| 快捷键         | 功能                               |
| -------------- | ---------------------------------- |
| cmd+shift+D    | 打开Debugger                       |
| cmd+shift+K    | 删除光标所在的一整行               |
| cmd+shift+L    | 选择当前文件中所有你当前选中的词汇 |
| cmd+shift+F    | 打开全局搜索                       |
| cmd+shift+M    | 打开你的问题面板                   |
| cmd+shift+H    | 对当前文件的查询替换               |
| cmd+shift+S    | 文件另存为                         |
| cmd+shift+T    | 打开最近关闭的那个文件             |
| cmd+shift+X    | 打开安装插件的入口                 |
| cmd+shift+V    | 预览MarkDown                       |
| cmd+shift+空格 | 参数提示                           |
| cmd+shift+\    | 光标跳转到花括号闭合处             |

### 常用的`cmd+?`系列

| 快捷键  | 功能                       |
| ------- | -------------------------- |
| cmd+B   | 打开或者关闭侧边栏         |
| cmd+W   | 关闭当前窗口               |
| cmd+P   | 打开最近关闭的文件         |
| cmd+]/[ | 左右控制行缩进             |
| cmd+/   | 注释一行或取消当前行的注释 |
| cmd+F   | 查询在当前文件             |
| cmd+,   | 打开用户设置               |
| cmd+N   | 新建一个文件               |
| cmd+O   | 打开一个文件               |
| ctr+`   | 打开集成的终端             |

### 常用的`cmd+K ?`系列

在Vscode中的`cmd+k`我觉得像是vim中的退出到命令执行模式,他会等待你继续按下下面的命令，你也可以认为一系列的`cmd+k`系的都是组合件

![img](https:////upload-images.jianshu.io/upload_images/8098263-66db4117f7430a52.png?imageMogr2/auto-orient/strip|imageView2/2/w/694/format/webp)

cmd+k.png


 所以接下来就是`cmd+k`系列的快捷键了



| 快捷键      | 功能                                                         |
| ----------- | ------------------------------------------------------------ |
| cmd+k cmd+s | 打开快捷键设置(其实每个人的操作习惯不同，在此你可以自定义你的键组合) |
| cmd+k U     | 关闭工作区中没有更改的编辑窗口                               |
| cmd+k Z     | 进入zen模式，就是删除所有其他让人分心的元素，安心写代码的模式 |
| cmd+k R     | 在mac中是在文件系统（Finder）中显示你正在编辑的文件          |
| cmd+k P     | 复制当前文件的绝对路径                                       |

其余的我不常用的就不列举了，可以在快件键设置中查找或者自定义你的指法:)



作者：RayLeo
链接：https://www.jianshu.com/p/c56ea43b2b34
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

## 代码导航[#](https://code.visualstudio.com/Docs/languages/javascript#_code-navigation)

代码导航可让您快速导航 JavaScript 项目。

- **转到定义** F12 - 转到符号定义的源代码。
- **Peek Definition** Alt+F12 - 调出一个 Peek 窗口，显示符号的定义。
- **转到引用** Shift+F12 - 显示对符号的所有引用。
- **转到** 未分配的**类型定义**- 转到定义符号的类型。对于类的实例，这将显示类本身而不是定义实例的位置。

您可以使用**命令面板中**的**转到符号**命令( Ctrl+Shift+P )通过符号搜索进行导航。

- **转到文件中的符号** Ctrl+Shift+O
- **转到工作区中的符号** Ctrl+T

## 重命名[#](https://code.visualstudio.com/Docs/languages/javascript#_rename)

按F2重命名 JavaScript 项目中光标下的符号：

## 重构[#](https://code.visualstudio.com/Docs/languages/javascript#_refactoring)

VS Code 包括一些方便的 JavaScript 重构，例如**Extract function**和**Extract constant**。只需选择您要提取的源代码，然后单击装订线中的灯泡或按 ( Ctrl+. ) 即可查看可用的重构。

可用的重构包括：

- 提取到方法或函数。
- 提取到常数。
- 在命名导入和命名空间导入之间转换。
- 移动到新文件。

见[的重构](https://code.visualstudio.com/docs/editor/refactoring)有关重构的更多信息以及如何配置个人重构的键盘快捷键。



## References CodeLens

要启用引用 CodeLens，请设置`"javascript.referencesCodeLens.enabled"`为`true`.

显示类的引用数量.



