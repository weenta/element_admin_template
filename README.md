# element_admin_template
基于`element-ui@2.3 + mockjs`的一款通用后台管理模板  

## start
```bash

    cd ele_admin_template
    npm i
    npm start

```

## git分支说明
`default` 二级侧边栏 适用一般业务场景    
`single_sidebar` 一级侧边栏 适用简单业务场景  
`sidebar_topbar` 二级侧边栏+顶部导航栏 适用较复杂业务场景   

## TODO
single_sidebar 主内容区填充 mockjs


### 目录结构
```
- element_adimn
|__build
|__config   
|__src                           主资源目录
|   |__api                       API目录
|   |    |__ config.js           API配置文件
|   |    |__ index.js            API文件
|   |__components                组件目录
|   |__mock                      数据模拟目录
|   |    |__ mockData.js         模拟数据
|   |    |__ mockApi.js          模拟接口
|   |__ pages                    页面目录
|   |__ router                   路由
|   |__ App.vue  
|   |__ Layout.vue               主布局文件   
|   |__ Login.vue                登录页             
|   |__ main.js
|__static
...
```
