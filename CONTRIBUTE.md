# stsdb 文档

## 文档编写

> 安装依赖 

```
npm run install
```

> 开始写文档

```
npm run docs
```

## 文档部署

```
npm run docs:deploy
```

vuepress 文档 [https://vuepress.vuejs.org/zh/](https://vuepress.vuejs.org/zh/)

```
.
├── CONTRIBUTE.md
├── README.md  // 生成首页配置
├── config  // 配置文档目录
├── deploy.sh  // 部署脚本
├── guide   // guide 文档
├── package.json
├── vuepress
└── zh      // 中文文档
    ├── README.md // 中文 guide 
    ├── config   // 中文 config 文档
    └── guide   // 中文 guide 文档
```

## 如何新增文档目录？

- 在跟目录创建文件夹
`mkdir api`

- 在中文目录`zh`创建文件夹
`mkdir ./zh/api`

- 添加配置到`.vuepress/config.js`中的`nav`下面
```
'/': {
  nav: [
    {
      text: 'Api',
      link: '/api/',
    }
  ]
},
'/zh/': {
  nav: [
    {
      text: 'Api',
      link: '/zh/api/',
    }
  ],
}
```
