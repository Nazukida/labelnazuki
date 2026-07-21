# LabelNazuki

现代图像标注工具，替代 LabelImg。基于 Tauri 2 + Svelte 5 构建，轻量、快速、跨平台。

- 主页：https://nazukida.github.io/labelnazuki/
- 下载：https://github.com/Nazukida/labelnazuki/releases/latest

## ver. 1.3.0

- 完善重要样本的标注流程与信息呈现。
- 添加每个不同种类标签的数量，便于查看数据集类别分布。
- 提供 Windows、macOS（Apple Silicon / Intel）和 Linux 安装包。

特别感谢 B 站用户 **@小刘铁定上岸** 提供的反馈与灵感。

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
