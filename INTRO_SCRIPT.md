# LabelNazuki — 介绍脚本

> 适用于产品演示、项目展示、README、社交媒体宣传等场景。中英双语版本。

---

## 中文版

### 一句话简介

**LabelNazuki** 是一款新一代的桌面端图像标注工具——比 LabelImg 更快、更好看、功能更强，专为计算机视觉开发者和数据标注团队打造。

### 30 秒电梯演讲

LabelNazuki 是一个开源的、跨平台的图像标注工具。它支持矩形框、多边形、旋转框和关键点四种标注类型，能够导入导出 PASCAL VOC、YOLO、COCO、CreateML 四大主流格式。基于 Tauri 2 和 Rust 构建，安装包仅 5-8MB，内存占用极低，却能流畅处理上万张图片。无论是训练 YOLO 模型、准备 COCO 数据集，还是用 CreateML 在 macOS 上训练，LabelNazuki 都能一站式满足你的标注需求。

### 详细产品介绍

大家好，今天向大家介绍一款我开发的图像标注工具——**LabelNazuki**。

如果你做过目标检测或计算机视觉相关的工作，你一定用过 LabelImg。LabelImg 是一个经典的工具，但它已经很多年没有更新了——界面老旧、功能单一、不支持多边形和关键点标注，而且在大批量图片处理时性能很不理想。

于是我决定自己动手，从零开发了一个现代化的替代品。

**LabelNazuki 的核心亮点：**

1. **四种标注类型，一站搞定**：矩形框、多边形、旋转框、关键点——覆盖了从目标检测到姿态估计的主流标注需求。

2. **四大格式全兼容**：支持 PASCAL VOC XML、YOLO TXT、COCO JSON 和 Apple CreateML JSON。无论你用 PyTorch、Darknet 还是 CreateML，都能无缝对接。

3. **性能极致优化**：采用自研 Canvas 2D 渲染引擎，缩放平移丝滑流畅，60fps 不掉帧。文件列表使用虚拟滚动，即使目录里有上万张图片也不会卡顿。

4. **完善的操作体验**：支持 100 步撤销/重做，自动保存防止数据丢失，自定义快捷键且自带冲突检测，暗色/亮色主题随心切换，中英双语界面。

5. **轻量高效**：基于 Tauri 2 + Rust 构建，安装包 5-8MB，内存占用远低于 Electron 同类产品。跨平台支持 Windows / macOS / Linux。

6. **开源免费**：完全开源，代码托管在 GitHub 上，欢迎 Star、Issue 和 PR。

无论你是独立开发者训练自己的模型，还是团队进行大规模数据标注，LabelNazuki 都能帮你提升效率。

### 功能清单

| 功能 | 说明 |
|------|------|
| 🟦 矩形框标注 | 拖拽绘制，支持移动、缩放、复制 |
| 🟩 多边形标注 | 逐点绘制，支持编辑顶点 |
| 🟨 旋转框标注 | 拖拽绘制，支持旋转调整角度 |
| 🟪 关键点标注 | 点击放置关键点，支持可见性标记 |
| 📂 多格式导入导出 | VOC XML / YOLO TXT / COCO JSON / CreateML JSON |
| ↩️ 撤销/重做 | 100 步历史记录，完整追溯 |
| 💾 自动保存 | 标注变化后自动保存，切图前自动保存 |
| ⌨️ 自定义快捷键 | 所有操作可自定义，冲突自动检测 |
| 🌓 主题切换 | 浅色/深色，跟随系统或手动切换 |
| 🌐 中英双语 | 默认中文，可一键切换英文 |
| 📋 虚拟滚动 | 万级图片流畅浏览 |
| 🖼️ 多格式图片 | JPEG / PNG / BMP / WebP / TIFF |

---

## English Version

### One-Liner

**LabelNazuki** is a next-generation desktop image annotation tool — faster, prettier, and more powerful than LabelImg, built for computer vision developers and data annotation teams.

### 30-Second Elevator Pitch

LabelNazuki is an open-source, cross-platform image annotation tool. It supports four annotation types — bounding boxes, polygons, rotated boxes, and keypoints — and imports/exports four major formats: PASCAL VOC, YOLO, COCO, and CreateML. Built with Tauri 2 and Rust, the installer is only 5-8MB with minimal memory footprint, yet it handles tens of thousands of images smoothly. Whether you're training a YOLO model, preparing a COCO dataset, or using CreateML on macOS, LabelNazuki meets all your annotation needs in one tool.

### Detailed Product Introduction

Hi everyone, today I'd like to introduce **LabelNazuki**, an image annotation tool I've been building.

If you've worked on object detection or computer vision projects, you've probably used LabelImg. It's a classic tool, but it hasn't been updated in years — the UI feels dated, features are limited, there's no support for polygons or keypoints, and it struggles with large image batches.

So I decided to build a modern replacement from the ground up.

**Key highlights of LabelNazuki:**

1. **Four annotation types in one tool**: Bounding boxes, polygons, rotated boxes, and keypoints — covering everything from object detection to pose estimation.

2. **Full format compatibility**: PASCAL VOC XML, YOLO TXT, COCO JSON, and Apple CreateML JSON. Whether you use PyTorch, Darknet, or CreateML, LabelNazuki integrates seamlessly into your workflow.

3. **Blazing-fast performance**: Custom Canvas 2D rendering engine with smooth 60fps zoom and pan. Virtual scrolling file list handles 10,000+ images without lag.

4. **Polished UX**: 100-step undo/redo, auto-save to prevent data loss, fully customizable keyboard shortcuts with conflict detection, light/dark themes, and bilingual Chinese/English interface.

5. **Lightweight and efficient**: Built with Tauri 2 + Rust. Installer size is only 5-8MB, with far lower memory usage than Electron-based alternatives. Cross-platform — Windows, macOS, Linux.

6. **Open source**: Completely open-source, hosted on GitHub. Stars, issues, and PRs are always welcome!

Whether you're a solo developer training your own models, or a team doing large-scale data annotation, LabelNazuki will boost your productivity.

### Feature Checklist

| Feature | Description |
|---------|-------------|
| 🟦 Bounding Box | Drag to draw, move, resize, duplicate |
| 🟩 Polygon | Point-by-point drawing with vertex editing |
| 🟨 Rotated Box | Drag to draw with rotation angle adjustment |
| 🟪 Keypoint | Click to place keypoints with visibility flags |
| 📂 Multi-format I/O | VOC XML / YOLO TXT / COCO JSON / CreateML JSON |
| ↩️ Undo/Redo | 100-step history with full traceability |
| 💾 Auto-Save | Auto-save on changes and before switching images |
| ⌨️ Custom Shortcuts | All actions customizable with conflict detection |
| 🌓 Theme Support | Light/Dark, follows system or manual toggle |
| 🌐 Bilingual | Chinese (default) and English |
| 📋 Virtual Scroll | Smooth browsing for 10,000+ images |
| 🖼️ Image Formats | JPEG / PNG / BMP / WebP / TIFF |
