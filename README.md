[![OSCS Status](https://www.oscs1024.com/platform/badge/lvhao01/vite-plugin-lvdeploy.svg?size=small)](https://www.oscs1024.com/project/lvhao01/vite-plugin-lvdeploy?ref=badge_small)

<h1 align="center">vite-plugin-lvdeploy</h1>
<p align="center">前端自动化部署方案依赖</p>


## 使用


1. [源码示例](https://blog.csdn.net/weixin_49230250/article/details/125852469?spm=1001.2014.3001.5501)

2. [仓库](https://github.com/lvhao01/vite-plugin-lvdeploy)

3. npm install vite-plugin-lvdeploy

4. vite.config.js中引入import vitePluginLvdeploy from './vite-plugin-lvdeploy'


5. 在plugins中添加并使用 

```javascript
plugins: [
  vue(),
  vitePluginLvdeploy({
    "dev":{
      host:'xxx.xxx.xxx.xxx',//服务器IP
      port:22,//服务器端口
      username:'xxxxxx',//服务器ssh登录用户名
      password:'xxxxxx',//服务器ssh登录密码
      serverpath:'/www/xxxx/xxxx',//服务器web目录 切记不要加/ 当前目录不存在会创建目录并且当前目录所有文件会被清空重新部署前端项目
    },
    "test":{
      host:'xxx.xxx.xxx.xxx',//服务器IP
      port:22,//服务器端口
      username:'xxxxxx',//服务器ssh登录用户名
      password:'xxxxxx',//服务器ssh登录密码
      serverpath:'/www/xxxx/xxxx',//服务器web目录 切记不要加/ 当前目录不存在会创建目录并且当前目录所有文件会被清空重新部署前端项目
    }
    //...其他自定义环境
  }),
]
```
6. npm run build

## 注意
 - 当不输入0时只会打包zip包不会部署
 - serverpath参数路径 会自动检测是否存在不存在会创建目录 若存在会清空当前目录
 - vite.config.js中若未配置 build.outDir（打包文件名夹名称） 将会使用默认值 'dist';

## 预览效果

[图片无法显示请去这里浏览](https://blog.csdn.net/weixin_49230250/article/details/125852469?spm=1001.2014.3001.5501)

开始打包
![avatar][tu1]

选择环境
![avatar][tu2]

开始部署
![avatar][tu3]

服务器查看
![avatar][tu4]





[tu1]:

[tu2]:



[tu3]:


[tu4]:










