# LabelNazuki

现代图像标注工具，替代 LabelImg。基于 Tauri 2 + Svelte 5 构建，轻量、快速、跨平台。

- 主页：https://nazukida.github.io/labelnazuki/
- 下载：https://github.com/Nazukida/labelnazuki/releases/latest

## ver. 1.5.0

- 新增 SAM 3 文字自动标注：输入英文目标名（如 `car, person`）即可一次标出图中所有同类目标，`car=汽车` 可保存为中文类别；支持只标当前图片或批量标注整个数据集（追加写入、可跳过已标注图片、可随时取消）。模型与运行时一键下载，国内默认走镜像，无需配置环境。
- 新增边缘吸附与共边：绘制、移动、缩放矩形框和旋转框时自动贴合相邻框的边（按住 Ctrl 临时关闭）；选中两个框按 G 共边，Shift+G 开关吸附。
- 新增批量修改（Ctrl+B）：按类别、形状筛选，批量改类别、标记 / 取消困难样本、转矩形框或删除，范围可选当前图片或整个数据集。
- 新增 Windows 免安装版（`_portable.zip`）：解压即用，设置与模型保存在程序旁的 data 文件夹。
- 修复旋转框画好后无法调整大小的问题。
- 修复多边形与 SAM 结果无法二次编辑的问题：可拖动顶点、双击边添加顶点、右键删除顶点。
- 修复未选类别时绘制产生无类别标注、YOLO / COCO 类别对应错误、切图时编辑与自动保存的竞态等问题。
- 提供 Windows（安装版 / 免安装版）、macOS（Apple Silicon / Intel）和 Linux x64 安装包。

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
| Windows | x64 | `.exe`、`.msi`、免安装 `.zip` |
| macOS | Apple Silicon | `.dmg` |
| macOS | Intel | `.dmg` |
| Linux | x64 | `.deb`、`.AppImage` |

请前往 [Releases](https://github.com/Nazukida/labelnazuki/releases/latest) 下载最新版本。
