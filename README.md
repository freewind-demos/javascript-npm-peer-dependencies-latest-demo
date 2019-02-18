JavaScript Npm Peer Dependencies "latest" Demo
==============================================

当我们在`peerDependencies`中把某个package声明为`latest`的时候，如：

```
"peerDependencies": {
  "lodash": "latest"
}
```

那么在`dependencies`或者`devDependencies`中，相应的package必须也声明为`latest`才不会报警告。

否则，哪怕写成当前最新的版本号（lodash当前最新版本为`4.17.11`）：

```
"dependencies": {
  "lodash": "4.17.11"
}
```

在进行`npm install`的时候，依然会报警：

```
npm WARN hello requires a peer of lodash@latest but none is installed.
You must install peer dependencies yourself.
```

## 运行

```
npm install
```

然后把package.json中:

```
"dependencies": {
  "lodash": "latest"
}
```

的`latest`改为当前最新版本：<https://www.npmjs.com/package/lodash>

再运行，查看警告。
