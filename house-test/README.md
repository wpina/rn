我们将种子工程与 WBAPP 解耦了。现在可以本地相关 @w/wbapp 版本，可以不用依赖热更新平台的版本了。这保证了线下调试使用的 wbapp 与热更新打包使用的 wbapp 是完全一致的，减少了出错情况下的调试成本。

大家可以选择性的将项目升级为 @w/wbapp 的形式。

## 老项目不升级

不需要做任何改动。但是热更新平台上的 WBAPP 也不会再进行更新，这意味着 APP 8.1.0 以后新增加的接口是不能使用的。

## 老项目要升级

1). 通过以下命令下载 @w/wbapp

```
// 登录/注册。需输入 username  password  email 即可登录/注册
$ npm login —scope=@w —registry=http://cnpm.58v5.cn

// 下载
$ npm install
```

2). 将项目中的改变 wbapp 的方式

```
// 原有引用方式一 
import WBAPP from '../WBAPP';
// 原有引用方式二
import WBAPP from 'wbapp';

// 新的引用方式
import WBAPP from '@w/wbapp';
```

## 新项目

clone 种子工程后，通过以下命令安装依赖包

```
npm install  --registry=http://cnpm.58v5.cn/
```



更详细的开发文档请查看 [本地开发文档](http://rn.58corp.com/react-native/docs/guide-fe-dev.html)

更详细的私有 npm 使用方法请查看 [npm.58v5.cn](http://npm.58v5.cn/)