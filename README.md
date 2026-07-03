# LabelNazuki

现代图像标注工具，替代 LabelImg。基于 Tauri 2 + Svelte 5 构建，轻量、快速、跨平台。

## 特性

- **多种标注类型**: 矩形框、多边形、旋转框、关键点
- **多格式支持**: PASCAL VOC XML、YOLO TXT、COCO JSON、CreateML JSON
- **高性能画布**: 自定义 Canvas 2D 引擎，60fps 缩放/平移
- **完整 Undo/Redo**: 100 步历史记录，永不丢失工作
- **自动保存**: 标注变化后自动保存，切换图片前自动保存
- **自定义快捷键**: 所有操作可自定义快捷键，冲突检测
- **暗色/亮色主题**: 跟随系统或手动切换
- **中英双语**: 默认中文，可切换英文
- **虚拟滚动文件列表**: 轻松处理 10000+ 图片目录
- **轻量级**: 安装包 ~5-8MB，内存占用低

## 系统要求

- Windows 10+ / macOS 12+ / Linux (Ubuntu 20.04+)
> 暂时不支持mac和linux，因为代码暂时不公开，等我找到构建安装包的方法再说
- 推荐分辨率 1280×800 以上

## 开发

### 前置依赖

- [Node.js](https://nodejs.org/) 18+
- [Rust](https://rustup.rs/) 1.75+
- [Tauri CLI](https://tauri.app/) (`npm install -g @tauri-apps/cli`)

Windows 额外需要：
- Microsoft Visual Studio C++ Build Tools
- WebView2 (Windows 10+ 已内置)

### 安装

```bash
git clone https://github.com/Nazukida/labelnazuki.git
cd labelnazuki
npm install
```

### 开发模式

```bash
npm run tauri dev
```

### 构建安装包

```bash
npm run tauri build
```

构建产物在 `src-tauri/target/release/bundle/` 目录下。

## 快捷键

| 动作 | 默认快捷键 |
|------|-----------|
| 选择工具 | V |
| 矩形框 | W |
| 多边形 | E |
| 旋转框 | R |
| 关键点 | T |
| 下一张图 | D |
| 上一张图 | A |
| 保存 | Ctrl+S |
| 撤销 | Ctrl+Z |
| 重做 | Ctrl+Shift+Z |
| 删除 | Delete |
| 复制 | Ctrl+D |
| 适应窗口 | Ctrl+0 |
| 放大 | Ctrl+= |
| 缩小 | Ctrl+- |
| 切换标签 | L |
| 切换准星 | C |

所有快捷键可在 设置 → 快捷键 中自定义。

## 支持的标注格式

| 格式 | 文件 | 用途 |
|------|------|------|
| PASCAL VOC | 每张图一个 .xml | 目标检测 (经典) |
| YOLO | 每张图一个 .txt + classes.txt | YOLOv5/v8 训练 |
| COCO | 整个目录一个 annotations.json | COCO 格式训练 |
| CreateML | 整个目录一个 JSON | Apple Core ML 训练 |

## 项目结构

```
labelnazuki/
├── src-tauri/          # Rust 后端 (文件系统、图像处理、格式转换)
├── src/                # Svelte 5 前端
│   ├── lib/
│   │   ├── canvas/     # 画布渲染引擎
│   │   ├── components/ # UI 组件
│   │   ├── stores/     # 状态管理
│   │   └── i18n/       # 国际化
│   └── App.svelte      # 主入口
└── package.json
```
