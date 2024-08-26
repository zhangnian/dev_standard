# Commit规范

### 为什么要制定Commit规范

一个好的 Commit Message 至关重要：

- 可以使自己或者其他开发人员能够**清晰地知道每个 commit 的变更内容**，方便快速浏览变更历史，比如可以直接略过文档类型或者格式化类型的代码变更。

- 可以基于这些 Commit Message **进行过滤查找**，比如只查找某个版本新增的功能：git log --oneline --grep "^feat|^fix|^perf"。

- 可以基于规范化的 Commit Message **生成 Change Log**。

- 可以依据某些类型的 Commit Message **触发构建或者发布流程**，比如当 type 类型为 feat、fix 时我们才触发 CI 流程。

总结来说，一个好的 Commit Message 规范可以使 Commit Message 的可读性更好，并且可以实现自动化。



### 规范格式

#### 格式为：**type: description**

type表示本次commit的类型，有以下几种常用类型：

- - feat：新增功能

  - fix：修复bug

  - perf：改进性能

  - style：格式化代码
  - test：测试用例相关代码
  - docs：文档类的更新

  - refactor：重构代码或其他不好归类的类型

- description表示具体的说明

#### 示例

- 新增了用户登录功能代码

  > feat: 用户登录

- 修复了某个bug

  > fix：修复了xxx的bug

- 优化部分代码

  > refactor: 优化了xxx的逻辑