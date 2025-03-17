# achong Monorepo

这是一个使用 pnpm 管理的 monorepo，包含 achong CLI 工具和相关包。

## 项目结构

```
achong-monorepo/
├── packages/
│   └── achong/          # achong CLI 工具
│       ├── bin/         # CLI 入口点
│       ├── src/         # 源代码
│       └── package.json # 包配置
├── package.json         # 根配置
└── pnpm-workspace.yaml  # pnpm 工作区配置
```

## 开始使用

### 安装依赖

```bash
pnpm install
```

### 构建所有包

```bash
pnpm build
```

### 开发模式

```bash
pnpm dev
```

## 使用 achong CLI

安装后，你可以通过以下方式使用 achong：

```bash
# 在本地开发时使用
pnpm --filter achong start -- generate --url https://jsonplaceholder.typicode.com/users --name User

# 或者将 achong 链接到全局使用
cd packages/achong
pnpm link --global
achong generate --url https://jsonplaceholder.typicode.com/users --name User
```

## 发布包

我们使用 [changesets](https://github.com/changesets/changesets) 来管理包的版本和发布。

创建一个新的变更集：

```bash
pnpm changeset
```

发布包：

```bash
pnpm publish-packages
```

## 许可证

MIT