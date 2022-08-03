<div align="center">

[![doocs-md](https://cdn-doocs.oss-cn-shenzhen.aliyuncs.com/gh/doocs/md/images/logo-2.png)](https://github.com/doocs/md)

</div>

<h1 align="center">微信 Markdown 编辑器</h1>

<div align="center">

[![sync status](https://github.com/doocs/md/workflows/Sync/badge.svg)](https://github.com/doocs/md/actions) [![deploy status](https://github.com/doocs/md/workflows/Build%20and%20Deploy/badge.svg)](https://github.com/doocs/md/actions) [![prettier status](https://github.com/doocs/md/workflows/Prettier/badge.svg)](https://github.com/doocs/md/actions) [![users](https://badgen.net/badge/Who's/using/green)](#谁在使用) [![PRs Welcome](https://badgen.net/badge/PRs/welcome/green)](../../pulls)<br> [![github](https://badgen.net/badge/⭐/GitHub/blue)](https://github.com/doocs/md) [![gitee](https://badgen.net/badge/⭐/Gitee/blue)](https://gitee.com/doocs/md) [![license](https://badgen.net/github/license/doocs/md)](./LICENSE) [![release](https://img.shields.io/github/v/release/doocs/md.svg)](../../releases)

</div>

## 项目介绍

> 本项目基于 [wechat-format](https://github.com/lyricat/wechat-format) 进行二次开发，感谢 [lyricat](https://github.com/lyricat) 的创意和贡献！

Markdown 文档自动即时渲染为微信图文，让你不再为微信文章排版而发愁！只要你会基本的 Markdown 语法，就能做出一篇样式简洁而又美观大方的微信图文。

## 在线编辑器地址

- Gitee Pages：https://doocs.gitee.io/md
- GitHub Pages：https://doocs.github.io/md

注：推荐使用 Chrome 浏览器，效果最佳。另外，对于国内（中国）的朋友，访问 [Gitee Pages](https://doocs.gitee.io/md) 速度会相对快一些。

## 为何二次开发

现有的开源微信 Markdown 编辑器，样式繁杂，也不符合我个人的审美需求。在我使用它们进行文章排版的时候，经常还要自己做一些改动，费时费力，因此动手做了二次开发。

欢迎各位朋友随时提交 PR，让这款微信 Markdown 编辑器变得更好！如果你有新的想法，也欢迎在 [Discussions 讨论区](https://github.com/doocs/md/discussions)反馈。

## 功能特性

- [x] 支持自定义 CSS 样式
- [x] 支持 Markdown 所有基础语法
- [x] 支持浅色、暗黑两种主题模式
- [x] 支持 <kbd>Ctrl</kbd> + <kbd>F</kbd> 快速格式化文档
- [x] 支持色盘取色，快速替换文章整体色调
- [x] 支持多图上传，可自定义配置图床
- [x] 支持自定义上传逻辑
- [x] 支持在编辑框右键弹出功能选项卡
- [x] 支持批量转换本地图片为线上图片

## 目前支持哪些图床

| #   | 图床                                            | 使用时是否需要配置                                                         | 备注                                                                                                                   |
| --- | ----------------------------------------------- | -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 1   | 默认                                            | 否                                                                         | -                                                                                                                      |
| 2   | [GitHub](https://github.com)                    | 配置 `Repo`、`Token` 参数                                                  | [如何获取 GitHub token？](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token) |
| 3   | [阿里云](https://www.aliyun.com/product/oss)    | 配置 `AccessKey ID`、`AccessKey Secret`、`Bucket`、`Region` 参数           | [如何使用阿里云 OSS？](https://help.aliyun.com/document_detail/31883.html)                                             |
| 4   | [腾讯云](https://cloud.tencent.com/act/pro/cos) | 配置 `SecretId`、`SecretKey`、`Bucket`、`Region` 参数                      | [如何使用腾讯云 COS？](https://cloud.tencent.com/document/product/436/38484)                                           |
| 5   | [七牛云](https://www.qiniu.com/products/kodo)   | 配置 `AccessKey`、`SecretKey`、`Bucket`、`Domain`、`Region` 参数           | [如何使用七牛云 Kodo？](https://developer.qiniu.com/kodo)                                                              |
| 6   | [MinIO](https://min.io/)                        | 配置 `Endpoint`、`Port`、`UseSSL`、`Bucket`、`AccessKey`、`SecretKey` 参数 | [如何使用 MinIO？](http://docs.minio.org.cn/docs/master/minio-client-complete-guide)                                   |
| 7   | 自定义上传                                      | 是                                                                         | [如何自定义上传？](#自定义上传逻辑)                                                                                    |

![select-and-change-color-theme](https://doocs.oss-cn-shenzhen.aliyuncs.com/img//1606034542281-a8c99fa7-c11e-4e43-98da-e36012f54dc8.gif)

![copy-and-paste](https://doocs.oss-cn-shenzhen.aliyuncs.com/img//1606034542372-59707c83-2caf-4a96-9bb6-c4effaecf731.gif)

![custom](https://doocs.oss-cn-shenzhen.aliyuncs.com/img//1606034542180-4d1c48b1-75f6-4794-95f7-e3b877c2b6a2.gif)

![doocs-md-upload-image](https://doocs.oss-cn-shenzhen.aliyuncs.com/img//1606034542512-0769a336-b9eb-4d58-83c1-29db7b54f71b.gif)

## 注意事项

1. 如果你使用了某些浏览器脚本修改了网页背景色，可能导致渲染后的文章出现背景色分块的现象，详见 [#63](https://github.com/doocs/md/issues/63)。
2. 某些浏览器插件，会对文章样式造成破坏。现象是：复制粘贴到公众号后台文章，点击保存时，样式丢失，详见 [#151](https://github.com/doocs/md/issues/151)。

## 自定义上传逻辑

在工具上没有提供预定义图床的情况下，你只需要自定义上传逻辑即可，这对于例如你不方便使用公共图床，而是使用自己的上传服务时非常有用。

你只需要在给定的函数中更改上传代码即可，为了方便，这个函数提供了可能使用的一些参数：

示例代码：

```js
const { file, util, okCb, errCb } = CUSTOM_ARG;
const param = new FormData();
param.append("file", file);
util.axios
  .post("http://127.0.0.1:9000/upload", param, {
    headers: { "Content-Type": "multipart/form-data" },
  })
  .then((res) => {
    okCb(res.url);
  })
  .catch((err) => {
    errCb(err);
  });

// 提供的可用参数:
// CUSTOM_ARG = {
//   content, // 待上传图片的 base64
//   file, // 待上传图片的 file 对象
//   util: {
//     axios, // axios 实例
//     CryptoJS, // 加密库
//     OSS, // ali-oss
//     COS, // cos-js-sdk-v5
//     Buffer, // buffer-from
//     uuidv4, // uuid
//     qiniu, // qiniu-js
//     tokenTools, // 一些编码转换函数
//     getDir, // 获取 年/月/日 形式的目录
//     getDateFilename, // 根据文件名获取它以 时间戳+uuid 的形式
//   },
//   okCb: resolve, // 重要！上传成功后给此回调传 url 即可
//   errCb: reject, // 上传失败调用的函数
// }
```

如果你创建了适用于其他第三方图床的上传代码，我们非常欢迎你分享它。

## 如何开发和部署

```sh
# 安装依赖
npm i

# 启动开发模式
npm start

# 部署在 /md 目录
npm run build
# 访问 http://127.0.0.1:9000/md

# 部署在根目录
npm run build:h5-netlify
# 访问 http://127.0.0.1:9000/
```

## 快速搭建私有服务

### 方式 1. 使用 npm cli

通过我们的 npm cli 你可以轻易搭建属于自己的微信 Markdown 编辑器。

```sh
# 安装
npm i -g @doocs/md-cli

# 启动
md-cli

# 访问
open http://127.0.0.1:8800/md/

# 启动并指定端口
md-cli port=8899

# 访问
open http://127.0.0.1:8899/md/
```

md-cli 支持以下命令行参数：

- `port` 指定端口号，默认 8800，如果被占用会随机使用一个新端口。
- `spaceId` dcloud 服务空间配置
- `clientSecret` dcloud 服务空间配置

### 方式 2. 使用 Docker 镜像

如果你是 Docker 用户，也可以直接使用一条命令，启动完全属于你的、私有化运行的实例。

```sh
docker run -d -p 8080:80 doocs/md:latest
```

容器运行起来之后，打开浏览器，访问 http://localhost:8080 即可。

关于本项目 Docker 镜像的更多详细信息，可以关注 https://github.com/doocs/docker-md

## 谁在使用

<table>
  <tr>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/RNKDCK2KoyeuMeEs6GUrow">
        <img src="https://fastly.jsdelivr.net/gh/filess/img12@main/2021/05/30/1622376190215-de85712d-d167-4adf-98c8-44f4540b3b5a.png" style="width: 40px;"><br>
        <sub>Doocs开源社区</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/FpGIX9viQR6Z9iSCEPH86g">
        <img src="https://fastly.jsdelivr.net/gh/filess/img17@main/2021/05/30/1622376213480-29314621-97bb-4129-9636-1d5eb955cf67.jpg" style="width: 40px;"><br>
        <sub>掘墓人的小铲子</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/yB3ZH3jmcF_LbzuKmnR9BQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img5@main/2021/05/30/1622376230945-7f633309-64c9-4d30-a6e9-46246b891f81.png" style="width: 40px;"><br>
        <sub>全网重点</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/oc5Z2t9ykbu_Dezjnw5mfQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img7@main/2021/05/30/1622376248105-64954bc0-c016-494d-a6bc-e22862ca9903.png" style="width: 40px;"><br>
        <sub>爱码士的内心独白</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/SFde8OsZ8FzNGMHwpmDtrg">
        <img src="https://fastly.jsdelivr.net/gh/filess/img9@main/2021/05/30/1622376309125-2056ab90-48bf-472a-9662-84b8041eace3.jpg" style="width: 40px;"><br>
        <sub>乐玩nodejs npm工具库</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/7UG24ZugfI5ZnhUpo8vfvQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img17@main/2021/05/30/1622376325266-0974cef0-2599-47c2-a808-5e05f12f6968.jpg" style="width: 40px;"><br>
        <sub>简静慢</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/qefHCmToAdowBz2JwBn_ug">
        <img src="https://fastly.jsdelivr.net/gh/filess/img15@main/2021/05/30/1622376339100-62825d0c-c189-4c9b-8961-af04dcbceed6.jpg" style="width: 40px;"><br>
        <sub>0加1</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/7bfpKACg7HP-PhBrkpM9IQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img0@main/2021/05/30/1622376358002-7950cb87-bb47-48ea-a6bb-2f47bb612a27.png" style="width: 40px;"><br>
        <sub>编程图解</sub>
      </a>
    </td>
  </tr>
  <tr>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/bnlWqzCarDlR4F27HHXNUg">
        <img src="https://fastly.jsdelivr.net/gh/filess/img6@main/2021/05/30/1622376372458-db221d88-b014-4331-98a5-47bc06055b1a.jpg" style="width: 40px;"><br>
        <sub>码云Gitee</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/CVqmcu_OGG8TQO4FViAQ3w">
        <img src="https://fastly.jsdelivr.net/gh/filess/img10@main/2021/05/30/1622376386410-6c603364-5660-42ad-8360-59ced1af49ac.jpg" style="width: 40px;"><br>
        <sub>好酸一柠檬</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/leDCdpvnfk8eZRPRRHwg5w">
        <img src="https://fastly.jsdelivr.net/gh/filess/img9@main/2021/05/30/1622376400386-b7409a18-cfd3-4490-a4b1-f3a38d7cc0ea.png" style="width: 40px;"><br>
        <sub>不知所云Hub</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/c9ZXxQHCrKz1FP1Zbh1S1w">
        <img src="https://fastly.jsdelivr.net/gh/filess/img15@main/2021/05/30/1622376417767-e56e3700-3d69-434b-8711-e432568c4cd7.jpg" style="width: 40px;"><br>
        <sub>会泽百家</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/MV8ch6qlSsamSaBOhWr9kg">
        <img src="https://fastly.jsdelivr.net/gh/filess/img2@main/2021/05/30/1622376434055-690c88cd-6155-470e-a2e1-7ad765443bd1.jpg" style="width: 40px;"><br>
        <sub>平凡而诗意</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/bWPKO-S3TNLsCgzwspHCTg">
        <img src="https://fastly.jsdelivr.net/gh/filess/img3@main/2021/05/30/1622376446363-4ab382c8-58e8-4b76-a4c2-a02855d13bc4.jpg" style="width: 40px;"><br>
        <sub>治恒说说</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/AHHrxu7aIYBpvn3PpVHE_Q">
        <img src="https://fastly.jsdelivr.net/gh/filess/img6@main/2021/05/30/1622376461115-5c402ef3-54d2-437b-b89e-8c815342f03b.jpg" style="width: 40px;"><br>
        <sub>柯宁申的叙事屋</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/6BO977YG5e_4qYxL4oVQJw">
        <img src="https://fastly.jsdelivr.net/gh/filess/img4@main/2021/05/30/1622376477265-591e7c45-5ed1-4557-9ff5-c4744a888319.jpg" style="width: 40px;"><br>
        <sub>我的 Beta 世界</sub>
      </a>
    </td>
  </tr>
  <tr>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/udU2ZICg60HbspgWTQdYpg">
        <img src="https://fastly.jsdelivr.net/gh/filess/img2@main/2021/08/22/1629604090568-c1b0d718-a0ca-4b25-983d-73591bbc5556.png" style="width: 40px;"><br>
        <sub>ApachePulsar</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/fqNxIRxTkn6QEPmi4atW9w">
        <img src="https://fastly.jsdelivr.net/gh/filess/img17@main/2021/05/30/1622376563848-671dbd2e-7b86-460a-b2c4-e2a1e0c5a92d.jpg" style="width: 40px;"><br>
        <sub>生化环材</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/VUlOBFA93eiqZ5ZYGmXzmQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img7@main/2021/05/30/1622376717389-3a6a7a2d-9903-4aa8-9fd7-08ef28b6cbc3.jpg" style="width: 40px;"><br>
        <sub>秀宇笔记</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/UU3cH8LvpO_3aeAkkYvZZQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img4@main/2021/08/22/1629605202587-a69e9e86-5078-4faf-8de1-1f273ee0421d.jpg" style="width: 40px;"><br>
        <sub>IT王小二</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/49wUuhOEYG-OZPbFc6_NrQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img13@main/2021/08/22/1629605348059-33be5c96-3a99-43cf-bf49-e0d2a79e3b53.jpg" style="width: 40px;"><br>
        <sub>小二来碗饭</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/YDUZ0t_spzeqXiE_Idv3OA">
        <img src="https://fastly.jsdelivr.net/gh/filess/img6@main/2021/08/22/1629605468074-9e37a662-29b7-409c-a295-2420e9e82ff2.jpg" style="width: 40px;"><br>
        <sub>青年技术宅</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/oinGHCmer1vNE6Hg2OsH1g">
        <img src="https://fastly.jsdelivr.net/gh/filess/img6@main/2021/08/22/1629605628076-2f06908d-ccdb-44ad-ab2e-06645534dbbc.jpg" style="width: 40px;"><br>
        <sub>路引科研</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/ap_JhwgmfxgqFAIcTF3nKQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img8@main/2021/08/22/1629605991393-9a362483-60ff-4b36-ad4c-901c33d743a4.jpg" style="width: 40px;"><br>
        <sub>凯文有事找你</sub>
      </a>
    </td>
  </tr>
  <tr>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/itkJtMY-1IkZjIn5fWtShw">
        <img src="https://fastly.jsdelivr.net/gh/filess/img16@main/2021/09/01/1630509994812-dea5c24f-fdca-42e0-b6cf-adab8f5ed889.jpg" style="width: 40px;"><br>
        <sub>软件部落库</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/_44Ya309DeQzemXLnJUNdQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img4@main/2021/09/18/1631947087260-320f3919-f9fa-4c25-8fc1-5020b892f338.jpg" style="width: 40px;"><br>
        <sub>网文小密圈</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/k9WbW0zmxl0S2WX2CXQ6cQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img6@main/2021/12/03/1638523595283-d702b1eb-a817-4ecf-8e3d-a63131259fa0.jpg" style="width: 40px;"><br>
        <sub>潇洒哥和黑大帅</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/qFQBBpjUoqdfnmCeOGqRJQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img3@main/2021/12/07/1638868463901-1646dcb8-212e-4179-a81a-14d78ceb551c.jpg" style="width: 40px;"><br>
        <sub>云原生指北</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/i7hTPuuJAtcK9G55tep0Uw">
        <img src="https://fastly.jsdelivr.net/gh/filess/img10@main/2022/01/08/1641608709678-77ffd9a8-1d4f-4401-b4ae-0e16b9b53cb1.jpg" style="width: 40px;"><br>
        <sub>全栈民工</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/14HNDbDIvfDnV7ePEfbyuQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img0@main/2022/01/17/1642383591942-72fefd93-0825-4665-bc52-4612063bfb80.jpg" style="width: 40px;"><br>
        <sub>睡不醒的鲤鱼</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/4QeZsTL84lbN_HO3kCwEwg">
        <img src="https://fastly.jsdelivr.net/gh/filess/img16@main/2022/01/30/1643545315140-74a6b958-e175-44cc-a751-877c8cb997f7.png" style="width: 40px;"><br>
        <sub>Dmego</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/_cNyKqRr8E1ENg9r7IO70Q">
        <img src="https://fastly.jsdelivr.net/gh/filess/img7@main/2022/04/15/1649987014805-5603399b-a3c0-4f28-b569-b08d64e7187a.png" style="width: 40px;"><br>
        <sub>红岸</sub>
      </a>
    </td>
  </tr>
  <tr>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/ekCoyhT-JjbYsysKBgdJzQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img6@main/2022/04/15/1649987014808-6091327c-d2ea-4e9d-9dcc-ce91f18fb2e0.png" style="width: 40px;"><br>
        <sub>HelloCoder</sub>
      </a>
    </td>
    <td align="center" style="width: 60px;">
      <a href="https://mp.weixin.qq.com/s/bnZebWPd5-TgiXgQVUKdaQ">
        <img src="https://fastly.jsdelivr.net/gh/filess/img5@main/2022/07/10/1657466412956-db2d754a-356e-4e4c-a2e9-d78ca2944b80.jpg" style="width: 40px;"><br>
        <sub>前端黑板报</sub>
      </a>
    </td>
  </tr>
</table>

注：如果你使用了本 Markdown 编辑器进行文章排版，并且希望在本项目 README 中展示你的公众号，请到 [#5](https://github.com/doocs/md/discussions/5) 留言。
