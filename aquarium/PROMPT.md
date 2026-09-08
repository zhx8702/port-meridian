# 鱼缸复现提示词

## 原始需求

这个作品源自 [Port Meridian 的铁路提示词](../train/PROMPT.md)。用户要求沿用其单文件、体素微缩景观、持续动画与实体控制器的写法，把火车沙盘改成鱼缸。

下面的英文提示词根据这一需求和实际交付整理，便于复现，不是逐字记录的原始用户输入。

## 整理后的提示词

```text
Build a single HTML file that opens directly in Chrome and shows an animated aquarium in voxel art, using Three.js from a CDN and no outside images, models, or textures. Make it look like a carefully arranged glass aquarium on a wooden cabinet in a room, seen from the eye height of a person standing in front of it.

Fill the aquarium with a colorful underwater garden: schools of small fish, tall aquatic plants, a sandy gravel bed, rocks, a stone arch, driftwood, a small treasure chest, a snail, an air stone, and a filter. Model the room, window, furniture, aquarium glass, and overhead light in the same detailed miniature style.

Keep the fish swimming and moving their tails and fins. Let plants sway, bubbles rise, the water surface ripple, and soft light patterns move across the bottom. Add a day-night cycle with a glowing aquarium lamp. Fish should gather around slowly sinking food when fed. Keep their swimming routes clear of the glass, plants, and hardscape, and keep fish from intersecting each other.

Put physical controls on the front of the wooden cabinet: a slider to change swimming speed, switches for the aquarium light, air bubbles, and day-night cycle, and a feeding button. The viewer must be able to drag and click these three-dimensional controls with the mouse. Keep them synchronized with an accessible compact control bar that works on mobile devices.

Allow dragging to adjust the camera, scrolling or pinching to zoom, and resetting the view. Keep the complete aquarium in frame on desktop and mobile without obscuring its controls. Make it colorful, detailed, peaceful, and pretty, with no build step or local server required.

Verify the result in Chrome at desktop, mobile portrait, and mobile landscape sizes. Check nonblank canvas pixels, animation, physical controls, feeding, fish separation, and visible changes between day, night, and aquarium lighting states.
```

## 当前实现

- [在线体验](https://zhx8702.github.io/port-meridian/aquarium/)
- [完整 HTML](index.html)
- [操作与验证说明](README.md)

当前实现使用 Three.js `0.160.1`，包含 18 条鱼。CDN 库之外的场景内容全部由代码生成。
