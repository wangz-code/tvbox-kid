## tvbox-kid 基于 [tang99](https://github.com/takagen99/Box)
我不会安卓, 目前基本靠豆包来分析, 鬼知道能不能实现 😛

- ❎ 初步计划,尝试增加儿童保护 音频识别? yolo检测? 还不确定, 如果是 "澳门新 xxx" 直接快进跳过 (未完成)
- ❎ 还有恶心的激活码 如果弹出 xxx扫码激活, 直接隐藏弹窗 真🌶🐔一个吊爬虫还激活

## 运行环境  
jbr-17  java 17
gradle  gradle-7.5

## spider爬虫样例 参考 https://github.com/mymine/CatVodSpider

## 简单看了一下源码
tvbox 本身是一个空壳, 通过加载第三方人编写的jar, jar 包内这实现了爬虫接口,  csp_爬虫类名 
然后进行播放
直接把爬虫文件放在java/com/github/catvod/spider同样的效果


## API 接口概览  java/com/github/catvod/crawler/Spider.java

### 内容获取
- `homeContent(filter)` - 获取首页内容
- `homeVideoContent()` - 获取首页视频内容
- `categoryContent(tid, pg, filter, extend)` - 获取分类内容
- `detailContent(ids)` - 获取详情内容
- `searchContent(key, quick)` - 基础搜索功能
- `searchContent(key, quick, pg)` - 带分页的搜索功能
- `playerContent(flag, id, vipFlags)` - 获取播放内容
- `liveContent(url)` - 获取直播内容

### 工具方法
- `manualVideoCheck()` - 手动检测视频URL
- `isVideoFormat(url)` - 判断URL是否为视频格式
- `proxyLocal(params)` - 本地代理处理

### 资源管理
- `cancelByTag()` - 取消请求
- `destroy()` - 销毁资源

### 静态工具
- `safeDns()` - 获取安全DNS解析器







