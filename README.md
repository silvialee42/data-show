# Framework-Front-end-Vue3
前端项目基础框架（基于Vue3）

## README更新时间
2021/11/12

## Vue3基础模板更新日志
[CHANGELOG](./CHANGELOG.md)

## 项目启动/使用说明
- 安装项目依赖
```
npm install
```

- 开发环境编译与热加载
```
npm run serve
```

- 生产环境打包与最小化
```
npm run build
```

- 灰度/测试环境编译与热加载
```
npm run stage-serve
```

- 灰度/测试环境打包与最小化
```
npm run stage-build
```

- 自定义脚手架配置
See [Configuration Reference](https://cli.vuejs.org/config/).

## 框架相关知识

- 框架文档Document

See [Document](https://v3.cn.vuejs.org/guide/introduction.html)

- 脚手架Vue Cli

See [Vue Cli](https://cli.vuejs.org/config/)

- 风格指南Style Guide

See [Style Guide](https://v3.cn.vuejs.org/style-guide/#%E8%A7%84%E5%88%99%E7%B1%BB%E5%88%AB)

- 路由Vue Router

See [Vue Router](https://next.router.vuejs.org/zh/guide/)

- 状态管理Vuex

See [Vuex](https://next.vuex.vuejs.org/zh/index.html)

## 规范
### 编程中常见的几种命名方法
- 匈利亚命名法(属性+类型+对象描述)
- camelCase命名法(驼峰式命名)(小驼峰)
- PascalCase命名法(帕斯卡命名)(大驼峰)
- kebab-case(短横线命名)
- UnderScoreCase(下划线命名)

```bash
#举例
sCourseDetail | courseDetail | CourseDetail | course-detail | course_detail
#匈利亚命名法(属性(弱类型动态语言可忽略)+类型(缩写)+对象描述(可忽略))
```

### 资源规范
- 公共资源

```bash
#命名方式 {}可选 默认com前缀 common公共的 缩写com
com{_产品模块}{_功能}{_状态}.图片后缀
1.com_tab_active.png      #公共_功能_状态
2.com_collect.png         #公共_功能_默认
3.com_collect_active.png  #公共_功能_激活状态
4.com_video_play.png      #公共_模块_功能
5.com_video_pause.png     #公共_模块_功能
```
- 页面资源

```bash
#命名方式 {}可选 状态normal与default可省略
场景{_二级场景}_模块{_状态}.图片后缀 
1.center_avatar.png           #场景_模块
2.center_settings_avatar.png  #场景_二级场景_模块
```
```bash
名词解析：
【场景和二级场景】一般指一级页面与二级页面(业务模块)
【模块】一般指页面中的部分区块，也有指背景图。如背景、按钮、icon都是模块
【功能】一般指的是，页面或者模块中，需要操作或点击的某个点，如发现页中的搜索icon
【状态】一般指当前切图的状态区分，像按钮的话，有默认状态、点击时状态、按下状态、不可点击状态等，网页上按钮还有悬停状态
```

<table>
    <caption>功能/操作命名</caption>
    <thead>
    	<th>中文名</th>
        <th>名称</th>
    </thead>
    <tbody>
        <tr>
        	<td>往前</td>
            <td>forward</td>
        </tr>
        <tr>
        	<td>返回</td>
            <td>back</td>
        </tr>
        <tr>
        	<td>关闭</td>
            <td>close</td>
        </tr>
        <tr>
        	<td>添加</td>
            <td>add</td>
        </tr>
        <tr>
        	<td>删除</td>
            <td>delete</td>
        </tr>
        <tr>
        	<td>编辑</td>
            <td>edit</td>
        </tr>
        <tr>
        	<td>查看</td>
            <td>view</td>
        </tr>
        <tr>
        	<td>隐藏</td>
            <td>hide</td>
        </tr>
        <tr>
        	<td>上传</td>
            <td>upload</td>
        </tr>
        <tr>
        	<td>下载</td>
            <td>download</td>
        </tr>
        <tr>
        	<td>收藏</td>
            <td>collect</td>
        </tr>
        <tr>
        	<td>评论</td>
            <td>comment</td>
        </tr>
        <tr>
        	<td>播放</td>
            <td>play</td>
        </tr>
        <tr>
        	<td>暂停</td>
            <td>pause</td>
        </tr>
        <tr>
        	<td>弹出</td>
            <td>pop</td>
        </tr>
        <tr>
        	<td>扫描</td>
            <td>scan</td>
        </tr>
        <tr>
        	<td>搜索</td>
            <td>search</td>
        </tr>
        <tr>
        	<td>设置</td>
            <td>setting</td>
        </tr>
    </tbody>
</table>

<table>
    <caption>状态命名</caption>
    <thead>
    	<th>中文名</th>
        <th>名称</th>
        <th>缩写</th>
    </thead>
    <tbody>
        <tr>
        	<td>默认</td>
            <td>default</td>
            <td>def</td>
        </tr>
        <tr>
        	<td>一般</td>
            <td>normal</td>
            <td>nor</td>
        </tr>
        <tr>
        	<td>选中</td>
            <td>selected</td>
            <td>sel</td>
        </tr>
        <tr>
        	<td>无法点击(不允许状态)</td>
            <td>disabled</td>
            <td>dis</td>
        </tr>
        <tr>
        	<td>点击时(高亮突显状态)</td>
            <td>highlight</td>
            <td>hig</td>
        </tr>
        <tr>
        	<td>悬浮时/点击后(各种激活状态)</td>
            <td>active</td>
            <td>act</td>
        </tr>
        <tr>
        	<td>加载中</td>
            <td>loading</td>
            <td>loa</td>
        </tr>
        <tr>
        	<td>按下</td>
            <td>pressed</td>
            <td>pre</td>
        </tr>
        <tr>
        	<td>滑动</td>
            <td>slide</td>
            <td>sli</td>
        </tr>
    </tbody>
</table>

### HTML规范
**HTML结构指导原则**
- 保持简约
  - 能用简单css实现 就不要额外增加结构体
  - 如无必要或动态JS操作的元素 不要在元素上写行内样式
  - 不必要的(元素挂载的所有东西)属性(未使用 无影响) 不保留
  - 过于庞大的结构体 拆分多个结构体/文件/组件
- 实现复用
  - 同一个结构体 在两个及以上的地方使用到 拆分抽取出来 引入使用
- 实用为王
  - 尽量遵循 HTML 标准和语义，但是不要以牺牲实用性为代价。任何时候都要尽量使用最少的标签并保持最小的复杂度。

**参考文档**
- See [codeguide](https://codeguide.bootcss.com/)
- See [aotu.io](https://guide.aotu.io/docs/html/code.html)

### CSS规范
采用 预处理语言SASS/SCSS + ITCSS设计方法论
- See [sass](https://sass-lang.com/)
- See [sass中文文档](https://www.sass.hk/)
- See [ITCSS](https://speakerdeck.com/dafed/managing-css-projects-with-itcss) (如不能访问 从前端同事那拿ITCSS的PDF)
- 思维导图
    [CSS样式标准V1.0.0](https://www.processon.com/mindmap/61a6efe21efad477b461b581)

### JavaScript规范