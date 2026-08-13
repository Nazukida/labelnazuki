# LabelNazuki

现代图像标注工具，替代 LabelImg。基于 Tauri 2 + Svelte 5 构建，轻量、快速、跨平台。

- 主页：https://nazukida.github.io/labelnazuki/
- 下载：https://github.com/Nazukida/labelnazuki/releases/latest

## ver. 1.4.0

- 新增可选的 SAM 辅助标注：通过前景点、背景点或框选提示快速生成目标轮廓。
- 支持按需下载推理运行时和多种 SAM 模型，不安装模型也不影响原有标注流程。
- 完善困难样本标记与信息呈现，并分别统计各类别标签数量。
- 修复切换图片时类别名丢失导致幽灵标签等问题。
- 提供 Windows、macOS（Apple Silicon / Intel）和 Linux x64 安装包。

感谢所有用户的反馈与建议。

## 主要特性

- **多种标注类型**：矩形框、多边形、旋转框、关键点
- **多格式支持**：PASCAL VOC XML、YOLO TXT、COCO JSON、CreateML JSON
- **高性能画布**：自定义 Canvas 2D 引擎，流畅缩放和平移
- **完整 Undo/Redo**：100 步历史记录
- **自动保存**：标注变化后自动保存，切换图片前自动保存
- **自定义快捷键**：所有操作可自定义快捷键并检测冲突
- **中英双语**：默认中文，可切换英文
- **大目录支持**：虚拟滚动文件列表，可处理大量图片

## 系统要求

- Windows 10+
- macOS 12+
- Linux（Ubuntu 20.04+）
- 推荐分辨率 1280 × 800 以上

## 安装包

| 平台 | 架构 | 格式 |
| --- | --- | --- |
| Windows | x64 | `.exe`、`.msi` |
| macOS | Apple Silicon | `.dmg` |
| macOS | Intel | `.dmg` |
| Linux | x64 | `.deb`、`.AppImage` |

请前往 [Releases](https://github.com/Nazukida/labelnazuki/releases/latest) 下载最新版本。
