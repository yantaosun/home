简体中文 

<p>
<strong><h2>9527の主页</h2></strong>
主网站还没有设置起始页一直惦记着，终于完成了。
</p>


原作者[imsyy](https://github.com/imsyy/) 在这，非常感谢🤠


![9527の主页](https://file.unanaos.com/upload/other/WechatIMG276.png)


### Demo

>由于 CDN 缓存原因，查看最新效果可能需要 `Ctrl` + `F5` 强制刷新浏览器缓存

- [9527の主页](https://www.unanaos.com)

### 功能

- [x] 载入动画
- [x] 站点简介
- [x] Hitokoto 一言
- [x] 日期及时间
- [x] 实时天气
- [x] 时光进度条
- [x] 音乐播放器
- [x] 移动端适配

* [ ] 去除 jQuery 依赖
* [ ] VUE 重构

### 天气

由于原天气 API 不稳定，已更换天气 API，现需要前往以下网站获取 key

- 前往 [ROLL](https://www.mxnzp.com/doc/list) 获取 app_id 和 app_secret，用于获取城市信息
- 前往 [和风天气](https://dev.qweather.com/) 获取 key，用于获取天气信息

也可自行更换其他方式

<!-- ### 配置

本项目采用 `json` 文件来配置站点内容，该配置不受版本更新影响，可将自定义配置写入 `setting.json` 以更改页面内容

<details>
<summary>配置说明</summary>

```json
{
    "title": "9527の主页",
    "description": "一个默默无闻的主页",
    "keywords": "9527,个人主页",
    "author": "9527",
    "logo_img": "./img/icon/logo.png",
    "logo_text_1": "unanaos",
    "logo_text_2": .com",
    "github": "unanaos",
    "qq": "1272762009",
    "email": "15910344486@163.com",
    "bilibili": "",
    "telegram": "bottom_user",
    "link_1": [
        "https://blog.unanaos.com/",
        "fa-solid fa-blog",
        "博客"
    ],
    "link_2": [
        "https://drive.unanaos.com/",
        "fa-solid fa-cloud",
        "网盘"
    ],
    "link_3": [
        "https://music.unanaos.com/",
        "fa-solid fa-music",
        "音乐"
    ],
    "link_4": [
        "https://nav.unanaos.com/",
        "fa-solid fa-compass",
        "起始页"
    ],
    "link_5": [
        "https://web.unanaos.com/",
        "fa-solid fa-book-bookmark",
        "网址集"
    ],
    "link_6": [
        "https://lab.unanaos.com/",
        "fa-solid fa-flask",
        "实验室"
    ],
    "Copyright_text": "9527",
    "beian": "蒙ICP备2022001573号"
}
```

</details> -->

### 音乐

>本项目采用了基于 `MetingJS` 的 `Aplayer` 音乐播放器，可实现快速自定义歌单  
>*仅支持 **中国大陆地区**，其他区域请将 [以下内容](https://cdn.jsdelivr.net/gh/imsyy/file/js/music/music-other.js) 替换 `music.js` 以实现音乐播放器的正常使用

更改 `music.js` 的参数即可实现自定义歌单列表

```js
let server = "netease"; //netease: 网易云音乐; tencent: QQ音乐; kugou: 酷狗音乐; xiami: 虾米; kuwo: 酷我
let type = "playlist"; //song: 单曲; playlist: 歌单; album: 唱片
let id = "7452421335"; //封面 ID / 单曲 ID / 歌单 ID
```

### 字体

现采用 `HarmonyOS Sans` 开源字体，采用字体拆分，提升加载速度

<details>
<summary>旧版方式</summary>

>由于本项目引入了中文字体，需要压缩中文字体以提高网页加载速度（ 也可以取消使用中文字体 ）

#### 中文字体去除繁体

- 安装 `Python 3.7` 和 `pip`
- 运行 `pip install fonttools`
- 下载 [sc_unicode.txt](https://gist.githubusercontent.com/imaegoo/d64e5088b723c2e02c40985f55ff12db/raw/5ebd2ce49418c73459a9dfe050483409306a6c1d/sc_unicode.txt)
- 运行 `pyftsubset 字体名称.ttf --unicodes-file=sc_unicode.txt`

#### 字体进一步压缩

- 编译安装 `Google woff2`

```bash
sudo apt-get install -y git g++ make
git clone --recursive https://github.com/google/woff2.git
cd woff2
make clean all
```

- 再压缩字体

```
./woff2_compress ./字体名称.ttf
```

- 最终可对原字体进行缓加载，**先行加载压缩后的字体**

>详细信息可前往 [虹墨空间站](https://www.imaegoo.com/2020/chinese-font-compress/) 查看原文

</details>

### 插件

* [Bootstrap](https://getbootstrap.com/)
* [iziToast](https://izitoast.marcelodolza.com/)
* [Font Awesome](https://fontawesome.com/)
* [jQuery](https://jquery.com/)
* [Aplayer](https://aplayer.js.org/)

### API

* [MetingAPI By 武恩赐](https://api.wuenci.com/meting/api/)
* [小歪 API](https://api.ixiaowai.cn/)
* [和风天气](https://dev.qweather.com/)
* [ROLL](https://www.mxnzp.com/doc/list)
* [Hitokoto 一言](https://hitokoto.cn/)

<a title="SSL" target="_blank" href="https://myssl.com/seal/detail?domain=blog.imsyy.top"><img src="https://img.shields.io/badge/MySSL-安全认证-brightgreen"></a>&nbsp;<a title="CDN" target="_blank" href="https://cdnjs.com/"><img src="https://img.shields.io/badge/CDN-Cloudflare-blue"></a>&nbsp;<a title="Copyright" target="_blank" href="https://unanaos.com/"><img src="https://img.shields.io/badge/CopyRight%20%40%202022%20--%202024-9527-red"></a>
