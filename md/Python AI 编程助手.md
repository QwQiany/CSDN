> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.runoob.com](https://www.runoob.com/python3/fitten-code.html) [Python3 VScode](https://www.runoob.com/python3/python-vscode-setup.html "Python3 VScode")[Python3 基础语法](https://www.runoob.com/python3/python3-basic-syntax.html "Python3 基础语法")

这两年 AI 发展迅猛，作为开发人员，我们总是追求更快、更高效的工作方式，AI 的出现可以说改变了很多人的编程方式。

AI 对我们来说就是一个可靠的编程助手，给我们提供了实时的建议和解决方案，无论是快速修复错误、提升代码质量，或者查找关键文档和资源，AI 作为编程助手都能让你事半功倍。

今天为大家推荐一款适配了 Viusal Studio，VS Code(本文使用)，JetBrains 系列 (本文使用) 以及 Vim 等多种编译器环境的插件 Fitten Code，Fitten Code 是由非十大模型驱动的 AI 编程助手，它可以自动生成代码，提升开发效率，帮您调试 Bug，节省您的时间，另外还可以对话聊天，解决您编程碰到的问题。

Fitten Code 免费且支持 80 多种语言：Python、C++、Javascript、Typescript、Java 等。

目前对于 Python 语言，Fitten Code 支持在多种文本编辑器或 IDE 上使用，接下来我们来详细看看 VS Code 与 PyCharm 两款 IDE 的安装与使用：

**[一、VS Code 版](#post-25200--2)**

*   [1. 安装](#post-25200-2-1)
*   [2. 智能补全](#post-25200-2-2)
*   [3. AI 问答](#post-25200-2-3)
*   [4. 生成代码](#post-25200-2-4)
*   [5. 代码翻译](#post-25200-2-5)
*   [6. 生成注释](#post-25200-2-6)
*   [7. 解释代码](#post-25200-2-7)
*   [8. 生成测试](#post-25200-2-8)
*   [9. 检查 BUG](#post-25200-2-9)
*   [10. 编辑代码](#post-25200-2-10)
*   [11. 常见问题](#post-25200-2-11)

**[二、PyCharm 版](#post-25200--1)**

*   1. 安装
*   [2. 智能补全](#post-25200-2)
*   [3. AI 问答](#post-25200-3)
*   [4. 生成代码](#post-25200-4)
*   [5. 代码翻译](#post-25200-5)
*   [6. 生成注释](#post-25200-6)
*   [7. 解释代码](#post-25200-7)
*   [8. 生成测试](#post-25200-8)
*   [9. 检查 BUG](#post-25200-9)
*   [10. 编辑代码](#post-25200-10)

一、Visual Studio 版本
------------------

### 1、安装

如果您已经安装 VS Code 且版本大于等于 1.68.0，请直接跳过此步骤，否则请点击[下载](https://code.visualstudio.com/download)前往官网下载安装 VS Code。

打开 VS Code，点击左侧 Extensions（扩展）按钮：

![](https://www.runoob.com/wp-content/uploads/2024/03/img_256.png)

在搜索框中搜索关键字 Fitten Code：

![](https://www.runoob.com/wp-content/uploads/2024/03/img_256-1.png)

在搜索结果中点击 Install：

![](https://www.runoob.com/wp-content/uploads/2024/03/img_256-2.png)

登录注册后即可开始使用：

![](https://www.runoob.com/wp-content/uploads/2024/03/img_256.jpeg)

### 2、智能补全

打开代码文件，输入一段代码，Fitten Code 就会为您自动补全代码：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-23.png)

按下 Tab 键接受所有补全建议：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-24.png)

按下 Ctrl+→ 键 (mac 系统为 Command+→) 接收单个词补全建议：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-25.png)

### 3、AI 问答

用户可通过点击左上角工具栏中的 Fitten Code – 开始对话或者使用快捷键 Ctrl+Alt+C(mac 系统为 Control+Option+C) 打开对话窗口进行对话：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-26.png)

当用户选中代码段再进行对话时，Fitten Code 会自动引用用户所选中的代码段，此时可直接针对该代码段进行问询等操作：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-27.png)

### 4、生成代码

可在左侧 Fitten Code 工具栏中选择 "Fitten Code - 生成代码" 或者使用快捷键 Ctrl+Alt+G (mac 系统为 Control+Option+G)，如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-28.png)

然后在输入框中输入指令即可生成代码：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-29.png)

利用对话功能生成代码：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-30.png)

### 5、代码翻译

编辑代码功能可以实现不同语言之间的转换，如 Python 语法转换成 C++ 语法等。选中需要进行编辑的代码段，右键选择 "Fitten Code – 编辑代码" 或点击左侧工具栏中的 "Fitten Code – 编辑代码" 或者使用快捷键 Ctrl+Alt+E (mac 系统为 Control+Option+E)，如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-31.png)

然后在输入框中输入需求 (如此处要求 Fitten 将 python 代码转为 C++ 代码)：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-32.png)

也可以在 Chat 界面实现：选中需要进行编辑的代码段，右键选择 "Fitten Code – 开始聊天" 或点击左侧工具栏中的 "Fitten Code – 开始聊天" 或者使用快捷键 Ctrl+Alt+C, 如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-33.png)

### 6、生成注释

Fitten Code 能够根据您的代码自动生成相关注释，通过分析您的代码逻辑和结构，为您的代码提供清晰易懂的解释和文档，不仅提高代码的可读性，还方便其他开发人员理解和使用您的代码。先选中需要生成注释的代码段，然后右键选择 "Fitten Code – 生成注释"：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-34.png)

即可生成对应注释如下图所示，点击 "Apply" 后即可应用：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-35.png)

### 7、解释代码

Fitten Code 可以对一段代码进行解释，可以通过选中代码段然后右键选择 "Fitten Code – 解释代码" 进行解释，如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-36.png)

此外，还可以进一步回答用户关于这段代码的疑问，如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-37.png)

### 8、生成测试

Fitten Code 拥有自动生成单元测试的功能，可以根据代码自动产生相应的测试用例，提高代码质量和可靠性。通过选中代码段后右键选择 "Fitten Code – 生成单元测试" 来实现，如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-38.png)

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-39.png)

### 9、检查 BUG

Fitten Code 可以对一段代码检查可能的 bug，并给出修复建议。选中对应代码段，然后右键选择 "Fitten Code 查找 Bug"，如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-40.png)

### 10、编辑代码

Fitten Code 可根据用户指示对选定的代码块进行编辑，用户点击 "Apply" 后即可应用变更。通过选中代码段右键选择 "Fitten Code – 编辑代码" 或在左上角工具栏点击 "Fitten Code – 编辑代码"，如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-41.png)

随后，用户可在输入框中输入指示，Fitten Code 会新建一个窗口对比显示更改前和更改后的内容，用户可通过点击 "Apply" 应用更改，如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-42.png)

### 11、常见问题

如果 VSCode 远程服务器 remote 无法连接外网时，请点击左下角⚙按钮，再点击设置：

![](https://www.runoob.com/wp-content/uploads/2024/03/img_277.png)

然后在设置页面点击右上角 "打开设置 (JSON)":

![](https://www.runoob.com/wp-content/uploads/2024/03/img_278.png)

最后只需在在弹出的 settings.json 文件中添加以下内容即可:

```
"remote.extensionKind": { "FittenTech.Fitten-Code": ["ui"] }
```

![](https://www.runoob.com/wp-content/uploads/2024/03/img_279.png)

更多内容参考官网：[https://code.fittentech.com/](https://code.fittentech.com/)

支持以下 4 种编辑器与开发环境：

*   [VS Code](https://code.fittentech.com/tutor_vscode_zh)：本文已详细介绍
*   [JetBrains IDE 系列（包括 PyCharm）](https://code.fittentech.com/tutor_jetbrains_zh)
*   [Visual Studio](https://code.fittentech.com/tutor_vs_zh)
*   [Vim](https://code.fittentech.com/tutor_vim_zh)

二、PyCharm 版本
------------

### 1、安装

点击左上方 "文件" 再点击 "设置"，如下图所示

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-1.png)

接着点击左侧 "插件" 选择 "Marketplace"，并搜索 "Fitten Code"，然后点击 "安装" 进行安装

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-2.png)

安装完成后左侧会出现 Fitten Code 插件图标, 注册登录后即可开始使用

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-3.png)

### 2、智能补全

打开代码文件，输入一段代码，Fitten Code 就会为您自动补全代码：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-4.png)

按下 Tab 键接受所有补全建议：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-5.png)

按下 Ctrl+→ 键接收单个词补全建议：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-6.png)

### 3、AI 问答

用户可通过点击左上角工具栏中的 Fitten Code – 开始新对话打开对话窗口进行对话：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-7.png)

当选中代码段再通过右键的开始聊天功能进行对话时，Fitten Code 会自动引用所选中的代码段，此时可直接针对该代码段进行问询等操作：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-8.png)

### 4、生成代码

可在左侧 Fitten Code 工具栏中选择 "Fitten Code - 生成代码"  ，然后在输入框中输入指令即可生成代码：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-9.png)

利用注释后的自动补全功能生成代码

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-10.png)

也可以利用对话功能生成代码

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-11.png)

### 5、代码翻译

Fitten Code 可以实现代码的语义级翻译，并支持多种编程语言之间的互译。有以下两种方法可以实现。

（1）选中需要进行翻译的代码段，右键选择 "Fitten Code – 编辑代码"，然后在输入框中输入需求即可完成转换

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-12.png)

（2）选中需要进行翻译的代码段，点击左侧工具栏中的 "开始新对话"。然后在输入框中输入需求即可完成转换

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-13.png)

### 6、生成注释

Fitten Code 能够根据您的代码自动生成相关注释，通过分析您的代码逻辑和结构，为您的代码提供清晰易懂的解释和文档，不仅提高代码的可读性，还方便其他开发人员理解和使用您的代码。先选中需要生成注释的代码段，然后右键选择 "Fitten Code – 生成注释"：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-14.png)

### 7、解释代码

Fitten Code 可以对一段代码进行解释，可以通过选中代码段然后右键选择 "Fitten Code – 解释代码" 进行解释，如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-15.png)

### 8、生成测试

Fitten Code 拥有自动生成单元测试的功能，可以根据代码自动产生相应的测试用例，提高代码质量和可靠性。通过选中代码段后右键选择 "Fitten Code – 生成单元测试" 来实现，如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-16.png)

### 9、检查 BUG

Fitten Code 可以对一段代码检查可能的 bug，并给出修复建议。选中对应代码段，然后右键选择 "Fitten Code 查找 Bug"，如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/unnamed-file.png)

### 10、编辑代码

Fitten Code 可根据用户指示对选定的代码块进行编辑。通过选中代码段右键选择 "Fitten Code – 编辑代码" ，如下图所示：

![](https://www.runoob.com/wp-content/uploads/2024/03/word-image-25200-18.png)

更多内容参考官网：[https://code.fittentech.com/](https://code.fittentech.com/)

支持以下 4 种编辑器与开发环境：

*   [VS Code](https://code.fittentech.com/tutor_vscode_zh) ：本文已详细介绍
*   [JetBrains IDE 系列（包括 PyCharm）](https://code.fittentech.com/tutor_jetbrains_zh)：本文已详细介绍
*   [Visual Studio](https://code.fittentech.com/tutor_vs_zh)
*   [Vim](https://code.fittentech.com/tutor_vim_zh)