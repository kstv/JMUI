# JMUI
    
    JMUI - 为移动而生


## 目录结构

- index.html
    + 示例入口文件
- demo/
    + 示例
- css/
   + jmui.css
- js/
   + jmui.js
- lib/
   + 存放第三方依赖类库，如 zeptojs

- stylus/
    + 存放 .styl 源码

- site/
    + 网站文档


## 代码规范

代码请遵命[AlloyTeam 团队规范](http://alloyteam.github.io/code-guide/#css)

## 构建方式
    
    // 下载源码
    $ git clone https://github.com/AlloyTeam/JMUI.git

    // 切换到目录
    $ cd JMUI

    // 安装依赖
    $ npm install 

    // 生成 JMUI/dist/ 文件夹
    $ grunt dist


    // 如果需要进一步生成 site/ 即文档网站所需的数据，继续执行
    // 1. 根据 config.js 中的配置生成数据到 data/_.js  以及示例到 demo/_.html
    // 2. 根据 site/views/*.ejs 生成静态页面到 site/public/*.html 方便脱离服务器环境访问
    $ grunt site

    // 接着开启文档网站
    $ cd site && grunt nodemon
    // 接着打开浏览器访问 127.0.0.1:7777 或直接执行
    $ grunt open


## 约定

为了方便自动生成文档, 约定如下:

## demo/*.html 包含以下 html 结构即可自动生成文档:

    <section id="组件ID">
        <div class="demo-item">
            <p class="demo-desc">组件描述</p>
            <div class="demo-block">
                组件 html 代码
            </div>
        </div>
        <div class="demo-item">
             <p class="demo-desc">组件描述</p>
            <div class="demo-block">
                组件代码
            </div>
        </div>
    </section>

其中, #组件ID 唯一, .demo-item 可多个

## 下划线开头的文件为自动构建生成，无需手动修改，如 demo/_base-css.html





