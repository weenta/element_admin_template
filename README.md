# vue_admin_template
基于`element-ui@2.3 + mockjs + axios`的一款通用后台管理模板  

## start
```bash

    cd vue_admin_template
    git checkout -b single_sidebar origin/single_sidebar
    npm i
    npm start

```

## git分支说明
`default` 二级侧边栏 适用一般业务场景    
`single_sidebar` 一级侧边栏 适用简单业务场景  
`sidebar_topbar` 二级侧边栏+顶部导航栏 适用较复杂业务场景   


## 目录结构
```
- element_adimn
|__build
|__config   
|__src                           主资源目录
|   |__api                       API目录
|   |    |__ config.js              API配置文件
|   |    |__ index.js               API文件
|   |__ assets                   资源目录
|   |    |__ css                   
|   |    |__ images                   
|   |__components                组件目录
|   |__mock                      数据模拟目录
|   |    |__ mockApi.js             mock接口
|   |    |__ mockData.js            mock数据
|   |__ pages                    页面目录
|   |__ router                   路由目录
|   |__ vuex                     vuex目录
|   |__ App.vue                  根组件
|   |__ Layout.vue               主布局文件   
|   |__ Login.vue                登录页             
|   |__ main.js
|__static
...
```
