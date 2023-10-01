---
title: 简介
top: 10

---

这个博客采用了[Cutie](https://github.com/yz-hs/cutie)主题，主题作者的博客：

{% link Yurchiu's Blog, https://yz-hs.github.io/ %}

<!--more-->

在此特别感谢，同时希望大家能给这个主题的仓库点个star，编写的真的非常精美！而且很可爱！

左下角可以听音乐，右边工具栏可以看到最新文章和随机文章，还有动态的文章目录，左边菜单的标签和分类功能还未使用。

建议使用左下角的RSS订阅来及时获取我的文章的更新（当然较大的更新我会发犇犇的awa）

还没来得及更改必要的图片、背景，会尽快做的。

下面是博客的一些语法（留给自己的笔记）

# 语法

## 音乐

### Aplayer

需要安装hexo-tag-aplayer

```sh
npm install --save hexo-tag-aplayer
```

```js
//简单用法
{% aplayer "Caffeine" "Jeff Williams" "caffeine.mp3" "picture.jpg" "lrc:caffeine.txt" %}
```

```js
//直接插入lrc歌词
{% aplayerlrc "title" "author" "url" "autoplay" %}
[00:00.00]lrc here
{% endaplayerlrc %}
```

```js
//完整用法
{% aplayerlist %}
{
    "narrow": false,                          // （可选）播放器袖珍风格
    "autoplay": true,                         // （可选) 自动播放，移动端浏览器暂时不支持此功能
    "mode": "random",                         // （可选）曲目循环类型，有 'random'（随机播放）, 'single' (单曲播放), 'circulation' (循环播放), 'order' (列表播放)， 默认：'circulation' 
    "showlrc": 3,                             // （可选）歌词显示配置项，可选项有：1,2,3
    "mutex": true,                            // （可选）该选项开启时，如果同页面有其他 aplayer 播放，该播放器会暂停
    "theme": "#e6d0b2",	                      // （可选）播放器风格色彩设置，默认：#b7daff
    "preload": "metadata",                    // （可选）音乐文件预载入模式，可选项： 'none' 'metadata' 'auto', 默认: 'auto'
    "listmaxheight": "513px",                 // (可选) 该播放列表的最大长度
    "music": [
        {
            "title": "CoCo",
            "author": "Jeff Williams",
            "url": "caffeine.mp3",
            "pic": "caffeine.jpeg",
            "lrc": "caffeine.txt"
        },
        {
            "title": "アイロニ",
            "author": "鹿乃",
            "url": "irony.mp3",
            "pic": "irony.jpg"
        }
    ]
}
{% endaplayerlist %}
```

### MeingJS

MetingJS 是基于Meting API 的 APlayer 衍生播放器，引入 MetingJS 后，播放器将支持对于 QQ音乐、网易云音乐、虾米、酷狗、百度等平台的音乐播放。

如果想在本插件中使用 MetingJS，请在 Hexo 配置文件 `_config.yml` 中设置：

```yml
aplayer:
  meting: true
```

```html
<!-- 简单示例 (id, server, type)  -->
{% meting "60198" "netease" "playlist" %}

<!-- 进阶示例 -->
{% meting "60198" "netease" "playlist" "autoplay" "mutex:false" "listmaxheight:340px" "preload:none" %}

```

经过测试，theme选项似乎无效



| 参数            |   默认值   | 描述                                                         |
| :-------------- | :--------: | ------------------------------------------------------------ |
| id              |            | 歌曲ID / 歌单ID / 专辑ID / 搜索关键词                        |
| server          |            | platform: `netease`, `tencent`, `kugou`, `xiami`, `baidu` 音乐平台: `网易云`, `QQ音乐`, `酷狗`, `虾米`, `百度` |
| type            |            | ID类型：`song`, `playlist`, `album`, `search`, `artist`      |
| auto            |    可选    | music link, support: `netease`, `tencent`, `xiami`           |
| fixed           |  `false`   | 开启固定模式，固定在左下角                                   |
| mini            |  `false`   | 打开迷你模式                                                 |
| autoplay        |  `false`   | 自动播放                                                     |
| theme           | `#2980b9`  | 主色调（似乎无效）                                           |
| loop            |   `all`    | 列表循环模式：'all', 'one', 'none'                           |
| order           |   `list`   | 列表播放模式：'list', 'random'                               |
| preload         |   `auto`   | 音乐文件预载入模式: 'none', 'metadata', 'auto'               |
| volume          |   `0.7`    | 默认音量, notice that player will remember user setting, default volume will not work after user set volume themselves |
| mutex           |   `true`   | 该选项开启时，如果同页面有其他 aplayer 播放，该播放器会暂停  |
| lrc-type        |    `0`     | lyric type                                                   |
| list-folded     |  `false`   | indicate whether list should folded at first                 |
| list-max-height |  `340px`   | 播放列表的最大长度                                           |
| storage-name    | `metingjs` | localStorage key that store player setting                   |