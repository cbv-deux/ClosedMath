# ClosedMath · 十三个等级

纯静态中英文网站。双击 `index.html` 可离线运行，页面使用的图片、样式和问卷逻辑均已内嵌。点击顶部中国/英国小国旗可随时切换语言，切换保留当前进度和选项顺序；刷新回到中文并重置答案。

五级同意量表固定语义顺序；其他题目每次问卷首次出现时乱序，此后保持排列。

发布地址：https://cbv-deux.github.io/ClosedMath/

## 发布到 GitHub Pages

1. 把本包的 `index.html`、`closedmath-share.png` 和 `.nojekyll` 上传至 GitHub 仓库根目录。
2. 在仓库 **Settings → Pages**，选择 **Deploy from a branch**，指定对应分支和 **/(root)**，保存。
3. 发布成功后，用 Pages 设置页的 **Visit site** 打开网站。

无需安装依赖、申请数据库或配置密钥。没有访问计数、派别比例、数据上传或浏览器持久化存储；答案只在当前页面内存中，刷新重置。

二维码是作者的微信联系二维码；页面中可直接保存。

## 微信分享缩略图

`index.html` 的 head 中已加入 Open Graph 分享标题、简介、网址与图片声明。分享图片为独立的 `closedmath-share.png`：512×512、白底彩色 ClosedMath Logo。

配置的完整图片网址：https://cbv-deux.github.io/ClosedMath/closedmath-share.png

Logo 必须与网页一起提交发布，让微信能够通过公网 HTTPS 地址读取；内嵌在页面里的 Base64 图片不作为此次分享图地址。页面交互仍可离线运行，分享图不参与问卷加载与计分。

这些标签是静态分享信息，不能保证每个微信客户端都采用。更新发布后需在微信中打开正式网址，重新分享并实测；已分享的旧卡片可能保留缓存。若需要通过官方接口主动设置朋友圈图片，需另接微信 JS-SDK 的公众号签名配置，本版本未加入该服务。

将来更换网址时，需要更新 head 中 `og:url`、`og:image`、`og:image:secure_url` 和 canonical；从源项目重新打包则同步修改 `package-static.py` 中的 `site_url`。

分享字段参考：[Open Graph 规范](https://ogp.me/)；[微信 JS-SDK 文档](https://developers.weixin.qq.com/doc/offiaccount/OA_Web_Apps/JS-SDK.html)。

部署步骤参考：[GitHub 官方文档](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)。
