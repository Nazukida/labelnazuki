# LabelNazuki

现代图像标注工具，替代 LabelImg。基于 Tauri 2 + Svelte 5 构建，轻量、快速、跨平台。

- 主页：https://nazukida.github.io/labelnazuki/
- 下载：https://github.com/Nazukida/labelnazuki/releases/latest

## ver. 1.4.5

- 修复未等自动保存完成就切换图片时，标注丢失或被写到下一张图的问题。
- 修复 classes.txt 中存在空行时类别编号前移，导致标注对应到错误类别的问题。
- 修复图片与标签分开存放时，文件列表把所有图片显示为未标注的问题。
- 支持单独指定 classes.txt 位置，多个数据集可共用同一份类别表。
- 新增关闭当前项目；切换数据集时不再残留上一个项目的类别。
- 关键点标记大小与形状（圆形 / 实心点 / 方形 / 菱形 / 十字）可调。
- 新增关键点连线，支持手动连接与按类别自动连线，四种格式均可无损保存。
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
