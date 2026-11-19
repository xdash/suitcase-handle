# suitcase-handle

拉杆 · Handle Pull —— 用键盘升降行李箱拉杆的小游戏。单文件 HTML（`index.html`），零依赖零构建。

## 玩法

- 拉杆一直在上下滑，**空格（或任意键 / 点屏幕）按一下换向**：这一下往上，下一下往下
- **挑战模式**：把杆停在亮起的黄条里 —— 按中了得 10 分 + 连击加成，连击每多一次多 2 分（封顶 40）；按偏或超时掉一颗心，三颗心掉光结束
- 越玩越难：目标带逐渐变窄（0.13 → 0.05）、拉杆逐渐变快（0.5 → 1.75 / 秒）、限时越来越短（2.8s → 1.25s）
- **随便玩玩**：没有黄条没有分，纯拉杆，按一下升、按一下降

## 细节

- 三段式伸缩拉杆：每跨过一节有「咔」一声，画面微震
- 进入目标带时黄条会立刻变亮，给「可以按了」的视觉反馈
- 三种配色（深夜机场 / 复古皮革 / 像素薄荷），配色与静音偏好存 localStorage
- 最高分存 localStorage
- 音效用 WebAudio 合成（伸杆 / 命中 / 失手 / 结算），零外部音频文件
- 手机可直接点屏幕，自适应横竖屏

线上地址：https://xdash.me/suitcase-handle/ （GitHub Pages，独立 repo `xdash/suitcase-handle`，push main → 自动发布）

## 宝宝模式（`?kid=1`）

同一份文件，加参数即可变成宝宝键盘乐园里的一关：

- 默认「宝宝天空」浅色配色、直接进「随便玩玩」，不掉心不会输
- 拉杆拉到最高：撒星星 + 语音夸一句（读大厅的 `kids_typing_name`，默认「宝贝」）
- 顶部只留 🏠 回家 / 配色 / 声音，提示条「按一下键盘，拉杆就升起来」
- 线上入口：https://xdash.me/kids-typing-games/suitcase-handle/?kid=1

> 宝宝乐园里的那份是**同一文件的副本**：`Sites/xdash-blog/static/kids-typing-games/suitcase-handle/index.html`。改完请两边同步（或先副本比对 sha256）。

## 本地预览

```bash
python3 -m http.server 8000
# 打开 http://localhost:8000
```
