# Python 交互式教学

一个纯前端、开箱即用的 Python 分等级交互式学习网站。

AI 发展太快，编程能力大幅提升，视频平台教学也很完善，可是提升不大，资料查找也不容易。所以我用 AI 辅助设计了这个交互式学习项目，方便自己也方便其他想系统学习 Python 的同学。项目采用分等级（Lv.1～Lv.10）递进式教学，从零基础启蒙到深度学习实战，边学边练。项目还有不少不完善的地方，欢迎理解和交流。

**在线体验：** [Python教学](https://lingxiao-x.github.io/Python/)

---

## 功能特点

- **10 个等级递进式教学（Lv.1～Lv.10）**：从零基础启蒙到深度学习实战，层层递进
- **13+ 学习章节 + 知识百科**：覆盖 Python 基础语法、核心数据类型、标准库、公共基础、面向对象、正则等
- **交互式章节测验**：每章配有选择题测验，提交后即时判分、显示解析
- **模拟测验系统**：公共基础 / Python 专项 / 标准库 / 综合模拟多种模式
- **学习进度追踪**：环形进度条 + 章节完成度统计，数据自动保存
- **知识点搜索**：支持按关键词快速查找知识点和代码示例
- **编程练习场**：每章附带可运行的代码练习，带分步提示与参考答案
- **本地数据持久化**：学习进度自动保存到浏览器 localStorage，刷新不丢失
- **响应式设计**：适配桌面、平板和手机

## 技术栈

- 纯 HTML + CSS + JavaScript，零依赖，无需安装任何包
- 单文件部署，无需后端服务器
- 数据全部内嵌于文件中，离线可用

---

## 使用说明

### 方式一：直接在线使用

打开 [https://lingxiao-x.github.io/Python/](https://lingxiao-x.github.io/Python/) 即可，无需下载、无需安装。

### 方式二：本地使用

1. 下载本仓库中的 `index.html` 文件
2. 双击用浏览器打开（推荐 Chrome / Edge）
3. 直接开始学习，无需联网（首次加载后完全离线可用）

### 学习流程

1. 从左侧导航栏选择章节，按顺序或按需学习知识点
2. 学完一章后，拉到页面底部做「章节测验」，提交后会立即显示对错和解析
3. 想重新练习某一章，点击「重做」按钮即可清空该章成绩重新开始
4. 所有做题记录会自动保存在浏览器本地（localStorage），下次打开网页会自动恢复进度
5. 章节学完后，进入「模拟测验中心」做综合模拟考试，检验整体水平
6. 随时可在「学习进度」页面查看各章节完成情况和历史得分

### 数据说明

- 所有学习进度、答题记录保存在**你自己浏览器的本地存储**中，不会上传到任何服务器
- 换浏览器、换设备、清除浏览器缓存都会导致进度丢失，请注意
- 如果重做某章测验，该章旧成绩会被覆盖

---

## 等级学习路线

| 等级 | 内容 | 目标 |
| ---- | ---- | ---- |
| **Lv.1 启蒙入门** | 第 1 章 | 认识 Python，搭建环境，写出第一个程序 |
| **Lv.2 基础语法** | 第 2-3 章 | 掌握变量、数据类型、运算符与表达式 |
| **Lv.3 程序控制** | 第 4-5 章 | 掌握分支结构与循环结构 |
| **Lv.4 函数与模块** | 第 6 章 | 掌握函数定义、参数、返回值与模块导入 |
| **Lv.5 组合数据** | 第 7-8 章 | 掌握列表、元组、字典、集合 |
| **Lv.6 文件与IO** | 第 9 章 | 掌握文件读写、CSV、with 语句 |
| **Lv.7 标准库实战** | 第 10-12 章 | 掌握 turtle、random、jieba、pandas 等库 |
| **Lv.8 通识与测验** | 第 13 章 + 模拟测验 | 公共基础知识、综合模拟考试 |
| **Lv.9 深度学习基础** | 深度学习拓展 1-3 | Tensor、autograd、线性神经网络 |
| **Lv.10 深度学习进阶** | 深度学习拓展 4-8 | CNN、RNN、优化算法、CV/NLP 实战 |

学完 Lv.1～Lv.7 后，可进入 Lv.8「通识与测验」做综合模拟，检验整体水平。

## 浏览器兼容性

- Chrome / Edge（推荐）
- Firefox
- Safari
- 移动端浏览器

---

## 作者

**lingxiao-x**
GitHub: [@lingxiao-x](https://github.com/lingxiao-x)

## 开源协议

本项目采用 [MIT 许可证](./LICENSE) 开源。

你可以自由地使用、复制、修改、合并、发布、分发本项目，只需在副本中保留原始的版权声明和本许可声明即可。

```
MIT License

Copyright (c) 2026 lingxiao-x

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 贡献

欢迎提交 Issue 来改进内容。如果你发现了题目错误或有更好的代码示例，欢迎一起完善。

---

祝你学习顺利，编程愉快！ 🎉
