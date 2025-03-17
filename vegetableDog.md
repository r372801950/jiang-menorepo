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