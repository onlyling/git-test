# git 工作测试仓库

> 记录、搭建一个体验比较规范的 git 提交方案

## 命名规范

文件夹、文件名 以小写字母、数字组成，多个单词以 `-` 链接。

## 代码格式化

安装 [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) 插件。

## 代码检测

[ESLint](https://github.com/eslint/eslint) 作为基础工具。

TypeScript 依赖 `@typescript-eslint/eslint-plugin`、`@typescript-eslint/parser`。

其他代码格式化依赖 `eslint-plugin-prettier`、`eslint-config-prettier`。

`.eslintrc.js` 中 `rules` 添加自定义规则。

## 代码提交

```
npm run commit

yarn commit
```

通过 `commitizen`、`cz-conventional-changelog` 实现。

参考 [优雅的提交你的 Git Commit Message](https://juejin.im/post/5afc5242f265da0b7f44bee4)

结合 `husky` 提交代码格式化代码，`@commitlint/cli`、`commitlint-config-cz` 配合 `git-cz` 触发 `husky`。

## 更新日志

[点击查看](./CHANGELOG.md)

使用 `standard-version` 生成提交日志、更新版本号。

`conventional-changelog-cli` 没有弄明白怎么更新当前的日志。
