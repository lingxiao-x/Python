# 贡献指南

感谢你对本项目的关注！本项目是一个面向计算机二级 Python 考试的交互式学习平台，欢迎任何形式的贡献。

## 如何贡献

### 报告问题

如果你发现了题目错误、代码示例有误，或者界面显示有问题：

1. 先查看现有的 [Issues](https://github.com/lingxiao-x/Python/issues)，确认是否已有人报告
2. 如果没有，点击 **New issue** 创建新问题
3. 标题简洁明了，描述清楚问题内容
4. 如果是界面问题，尽量附上截图

### 提交题目或知识点

如果你希望补充新的题目或完善知识点：

- 直接修改 `index.html` 文件中的 `quizData` 或 `knowledgeBase` 对象
- 确保题目格式与现有题目一致
- 提交 Pull Request 时说明补充的内容

### 改进界面或功能

- 本项目为纯前端单文件，修改 `index.html` 即可
- 保持响应式设计，确保在手机、平板、桌面都能正常使用
- 尽量保持单文件部署的特性，避免引入额外依赖

## 提交规范

### Pull Request 流程

1. Fork 本仓库
2. 创建你的功能分支 (`git checkout -b feature/你的功能`)
3. 提交你的修改 (`git commit -m '添加: 某个功能'`)
4. 推送到你的 Fork (`git push origin feature/你的功能`)
5. 在 GitHub 上创建 Pull Request

### 提交信息格式

- `修复:` 修复某个 bug
- `添加:` 添加新功能或内容
- `更新:` 更新现有内容
- `优化:` 改进代码或界面

## 开发注意事项

- 本项目使用纯 HTML + CSS + JavaScript，无构建工具
- 数据全部内嵌在 `index.html` 中，方便离线使用
- 修改后可以直接双击 `index.html` 在浏览器中测试
- 确保没有 JavaScript 语法错误（特别是字符串中的引号转义）

## 行为准则

参与本项目即表示你同意遵守我们的 [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)。

## 疑问或建议

有任何疑问或建议，欢迎通过 [Issues](https://github.com/lingxiao-x/Python/issues) 或 [Discussions](https://github.com/lingxiao-x/Python/discussions) 交流。
