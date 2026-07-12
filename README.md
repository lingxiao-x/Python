# Python 二级交互式教学

一个纯前端、开箱即用的 Python 二级考试学习网站。

AI 发展太快，编程能力大幅提升，视频平台教学也很完善，可是提升不大，资料查找也不容易。所以我用 AI 辅助设计了这个交互式学习项目，方便自己也方便其他备考的同学。项目还有不少不完善的地方，欢迎理解和交流。

**在线体验：** [Python二级教学](https://lingxiao-x.github.io/Python/)

---

## 功能特点

- **12 个学习章节**：从 Python 基础入门到 pandas / matplotlib 标准库
- **交互式章节测验**：每章配有选择题测验，提交后即时判分、显示解析
- **模拟考试系统**：公共基础 / Python 专项 / 标准库 / 综合模拟四种模式
- **学习进度追踪**：环形进度条 + 章节完成度统计，数据自动保存
- **知识点搜索**：支持按关键词快速查找知识点和代码示例
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

## 学习路线建议

| 阶段   | 内容            | 目标                        |
| ---- | ------------- | ------------------------- |
| 基础入门 | 第 1-3 章       | 掌握变量、数据类型、运算符             |
| 程序结构 | 第 4-6 章       | 掌握分支、循环、函数                |
| 核心数据 | 第 7-9 章       | 掌握列表、字典、文件操作              |
| 标准库  | 第 10-12 章     | 掌握 turtle、jieba、pandas 等库 |
| 冲刺阶段 | 第 13 章 + 模拟测验 | 通过公共基础知识和综合模拟考试           |

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

祝你考试顺利！ 🎉
