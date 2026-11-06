# 中文黑体对比 · Chinese Sans Comparison

一个单文件网页，用来并排对比四款常见的中文黑体：

**Noto Sans SC** · **IBM Plex Sans SC** · **苹方 PingFang SC** · **微软雅黑 Microsoft YaHei**

在输入框里打字，四个展示框会同步显示同一段文字，方便直接看出字形、字面大小、标点位置和中英混排的差别。

## 使用方法

- **在线打开**：开启 GitHub Pages 后访问 `https://muinocriz.github.io/chinese-sans-comparison/`
- **本地打开**：下载 `index.html`，双击用浏览器打开即可。不需要安装任何环境，也不需要联网。

## 网页功能

- **一个输入框，四个展示框**：输入的内容实时同步到四款字体。
- **字号和行高滑块**：字号 12–96px，行高 1.0–2.4。
- **预设文本**：
  - **综合**：结构字、一句正文、一行中英数混排加标点，默认显示这一组。
  - **英文数字**：比较拉丁字母和数字的设计。
  - **标点**：比较中文标点的位置和形状。
  - **长段落**：比较正文排版的整体灰度和阅读感。
  - **生僻字**：检查字库覆盖范围。
- **字体加载状态检测**：每个展示框右上角会显示：
  - `✓ 已加载`：显示的确实是该字体。
  - `✗ 本机未安装` / `✗ 未加载`：当前设备上没有这款字体。
- **缺字一眼可见**：每个展示框只调用它自己的字体，缺字时退回宋体（衬线体），不会被其他黑体悄悄顶替，造成“看起来都一样”的错觉。
- **字体内嵌**：Noto Sans SC 和 IBM Plex Sans SC 的 Regular（400）字重直接打包在 `index.html` 里，不依赖 CDN，国内网络也能稳定显示。文件约 8 MB，首次打开需要稍等。
- **自动适配深色模式**：跟随系统的浅色或深色设置。

### 关于苹方和微软雅黑

这两款是苹果和微软的商业字体，授权不允许嵌入网页，所以页面只能调用设备上已安装的字体：

| 设备 | Noto Sans SC | IBM Plex Sans SC | 苹方 | 微软雅黑 |
|---|---|---|---|---|
| Windows | ✓ | ✓ | ✗ | ✓ |
| macOS / iOS | ✓ | ✓ | ✓ | ✗（通常没有） |

要看到四款字体的完整对比，需要在 Windows 和苹果设备上分别打开一次。

## 四款字体的特点

### Noto Sans SC

Google 与 Adobe 联合开发，和 **思源黑体（Source Han Sans）** 是同一套字形，2014 年发布。

- 风格中性规整，字面适中，笔画端点略微收紧，不张扬也不容易出错，是开源中文黑体里的“标准答案”。
- 英文部分来自 Source Sans，小写 g 是双层的。
- 共 7 档字重（Thin – Black），字库覆盖面最全。
- 开源，SIL OFL 授权，可免费商用。

### IBM Plex Sans SC

IBM 企业字体 Plex 家族的简体中文版，中文部分由韩国字体公司 Sandoll 开发，2024 年 12 月发布。

- 笔画收尾平直利落，带有理性、偏工程的气质，和英文 IBM Plex Sans 风格统一。
- 英文和数字字宽较大，小写 g 是单层的，机械感明显。
- 中文标点更紧凑，紧贴前一个字。
- 共 8 档字重（Thin – Bold），约 3 万个字形，常用字足够，生僻字可能缺字。
- 开源，SIL OFL 授权，可免费商用。

### 苹方 PingFang SC

苹果从 2015 年起（OS X El Capitan / iOS 9）在 macOS 和 iOS 上使用的默认中文字体。

- 字面大，中宫开阔，笔画简洁现代。
- 在高分辨率的 Retina 屏幕上显得干净通透，是“苹果感”界面的重要组成部分。
- 共 6 档字重（Ultralight – Semibold）。
- 仅授权在苹果设备上使用。

### 微软雅黑 Microsoft YaHei

微软委托方正设计，从 Windows Vista 开始成为 Windows 默认的中文界面字体。

- 字面大，中宫宽，笔画末端平直。
- 专门针对低分辨率屏幕和 ClearType 渲染优化，小字号下依然清晰。
- 英文部分来自 Segoe UI。
- 共 3 档字重（Light / Regular / Bold）。
- 随 Windows 授权，网页一般只能调用用户本机安装的字体。

## 文件说明

```
index.html          对比网页（已内嵌 Noto Sans SC 和 IBM Plex Sans SC）
licenses/           内嵌字体的开源授权文件
README.md           本说明
```

## 字体授权

- Noto Sans SC：SIL Open Font License 1.1，见 `licenses/NotoSansSC-OFL.txt`。字体文件来自 [Fontsource](https://fontsource.org/fonts/noto-sans-sc)。
- IBM Plex Sans SC：SIL Open Font License 1.1，见 `licenses/IBMPlexSansSC-OFL.txt`。字体文件来自 [IBM/plex](https://github.com/IBM/plex)。
- 苹方、微软雅黑未包含在本项目中，归各自版权方所有。
