# GPT-6 Demos

使用 GPT-6 制作的交互 demo 集合。每个作品独立存放，当前收录两个可直接用 Chrome 打开的单文件 Three.js 微缩场景。

**[打开作品目录](https://zhx8702.github.io/port-meridian/)**

| 作品 | 在线体验 | 文档与提示词 |
| --- | --- | --- |
| Port Meridian：体素铁路沙盘 | [进入火车沙盘](https://zhx8702.github.io/port-meridian/train/) | [说明](train/README.md) · [提示词](train/PROMPT.md) |
| 一缸小世界：体素鱼缸 | [进入鱼缸](https://zhx8702.github.io/port-meridian/aquarium/) | [说明](aquarium/README.md) · [提示词](aquarium/PROMPT.md) |

## 开发计划

[鱼缸 V2 开发任务](docs/aquarium-v2-tasks.md)：真实养护、生态模拟和新手教程的优先级、依赖与验收标准。当前处于规划阶段，线上鱼缸仍为 V1。

## Port Meridian

木桌上的 HO 比例铁路：运行中的客货列车、港口、小镇、机车转盘、昼夜灯光与实体控制器。

[![Port Meridian 火车沙盘](train/desktop.png)](https://zhx8702.github.io/port-meridian/train/)

## 一缸小世界

房间里的水草鱼缸：18 条彩色小鱼、气泡、水草、沉木和宝箱，支持投喂、调速与昼夜灯光控制。

[![一缸小世界鱼缸](aquarium/desktop.png)](https://zhx8702.github.io/port-meridian/aquarium/)

## 本地打开

```bash
git clone https://github.com/zhx8702/port-meridian.git
```

用 Chrome 打开根目录 `index.html`，从目录进入作品；也可单独打开 `train/index.html` 或 `aquarium/index.html`。

不需要安装依赖、构建或启动服务器。场景使用 CDN 加载固定版本的 Three.js，首次打开需要联网。场景模型、纹理和标签在各自 HTML 内生成；仓库中的 PNG、JPG 和 MP4 仅用于作品预览及文档。

## 目录结构

```text
port-meridian/
  index.html             # GPT-6 Demos 作品目录
  README.md              # 仓库说明
  PROMPT.md              # 提示词索引
  .nojekyll              # GitHub Pages 直接发布静态文件
  train/
    index.html           # 火车完整应用
    README.md
    PROMPT.md
    desktop.png
    night.png
    ...                  # 原有手机截图、演示视频和封面
  aquarium/
    index.html           # 鱼缸完整应用
    README.md
    PROMPT.md
    desktop.png
    night.png
    mobile.png
```

## GitHub Pages

一个仓库对应一个项目站点，但站点可以包含任意多个 HTML 页面和子目录。本仓库从 **`main` 分支的 `/ (root)`** 发布：

- `/port-meridian/`：作品目录。
- `/port-meridian/train/`：火车沙盘。
- `/port-meridian/aquarium/`：鱼缸。

推送到 `main` 后 GitHub Pages 自动重新发布，不需要额外的构建工具或工作流。仓库仍使用 `port-meridian` 这个名称，以保持现有仓库地址和站点根地址稳定；原来根地址上的火车已迁至 `/train/`。

## 添加新 Demo

1. 新建语义明确的英文目录，例如 `terrarium/`。
2. 放入独立的 `index.html`、`README.md`、`PROMPT.md` 和预览图。
3. 在根目录 `index.html` 添加作品条目，更新作品数量，并使用相对路径链接到新作品。
4. 更新本 README 的作品表和根目录 `PROMPT.md` 的索引。
5. 检查首页到作品的跳转、返回目录、桌面与手机渲染，再提交并推送到 `main`。

各作品中的「GPT-6 DEMOS」链接可返回目录。单独下载某个 HTML 时，场景仍能独立运行；返回目录链接需要完整仓库的目录结构。

## 历史版本

[v1.0.0](https://github.com/zhx8702/port-meridian/releases/tag/v1.0.0) 是最初的 Port Meridian 火车作品版本，其标签和 Release 保留。当前 demo 集合以 `main` 分支及上方在线入口为准。
