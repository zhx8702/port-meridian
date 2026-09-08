# 复现提示词

下面是生成本项目时使用的原始英文需求，可直接交给支持编程和浏览器验证的 AI 工具。它可用于重新生成同类场景；仓库当前实现以 `index.html` 为准。

## 原始提示词

```text
Build a single HTML file that opens in Chrome and shows an animated model train yard in voxel art, using  Three.js   from a CDN and no outside assets. Make it look like an HO-scale layout on a wooden table in a room, seen from the eye height of a person standing at the front edge.Fill the layout with a busy rail scene: a main line loop, a yard, an engine terminal with a turntable, industries, a harbor, a station, a town, and any other areas you think make it interesting.Keep trains running, add machines and vehicles that move, give it a day-night cycle with glowing lights, and put physical controls on the front of the table,such as levers to change train speed and buttons or switches for the lights and other actions, that the viewer can drag and click with the mouse. Make it colorful, detailed, and pretty, and make sure nothing clips through anything else.
```

## 补充实现与验收要点

以下要点整理自本项目的实际交付，作为复现时的补充要求，不属于上面的原始提示词：

```text
将完整应用交付为 index.html，直接用 Chrome 打开即可运行，不需要构建步骤、后端或本地服务器。

从 CDN 加载 Three.js 和 OrbitControls，其余场景几何体、纹理、标牌和声音均在文件内生成。若使用图标，内嵌所需图标并保留许可说明。

列车沿连续闭合线路运行，保持车厢间距和两条线路之间的净空。转盘上的机车随桥面旋转；吊机、车辆和船只的运动范围应避开建筑和铁路。

前侧桌沿的控制杆和开关必须是可交互的三维物体。控制面板与实体控件的状态保持同步，并提供暂停、视角恢复、全屏和小屏幕可用的操作方式。

用真实浏览器验证桌面和手机尺寸，检查画布非空、列车持续运动、控件可点击和拖动、昼夜及灯光切换正常、文字不溢出。检查完整运行线路的列车与场景净空，并修复发现的穿模问题。

提供白天、夜间和移动端截图，以及一段约 30 秒的 MP4 演示，展示列车运行、调速、转盘和昼夜变化。
```

## 复现环境参考

- 浏览器：支持 WebGL 的 Chrome。
- 场景库：Three.js `0.170.0` 与同版本 OrbitControls。
- 网络：打开页面时允许访问 `cdn.jsdelivr.net`。
- 应用结构：原生 HTML、CSS、JavaScript，无项目构建依赖。
- 浏览器验证：可使用 Playwright 或同类浏览器自动化工具。
- 视频导出：可使用浏览器录制工具；本仓库演示采用浏览器逐帧截图和 FFmpeg 合成。

## 获取当前版本

- [在线体验](https://zhx8702.github.io/port-meridian/train/)
- [历史 Release](https://github.com/zhx8702/port-meridian/releases/tag/v1.0.0)
- [查看完整单文件实现](index.html)
