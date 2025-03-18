安装 Lerna
pnpm add -D lerna
npx lerna init

发布
去cli目录  pnpm link -g
这样本地就能运行    achongQuicktype -V
"bin": {
    "achongQuicktype": "./bin/cli.js"
},

不知道怎么用就
achongQuicktype --help

生成ts类型
achongQuicktype -u https://jsonplaceholder.typicode.com/users/1 -n User -p ./

如果生成的不全，去quickType网站，保存接口的json，直接生成，绝笔字段都全

在packages/hooks调用另一个本地项目libs
pnpm add @achong/libs --workspace

本地私仓
npm install -g verdaccio
启动
verdaccio

npm adduser --registry http://localhost:4873/
502报错解决方式
npm config set noproxy localhost

npm config set registry https://registry.npmjs.org/
npm set registry http://localhost:4873/