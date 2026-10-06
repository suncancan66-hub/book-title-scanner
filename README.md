# 书角 · 书名扫描记录（Book Title Scanner）

用摄像头扫一下书籍封面或书名页，自动识别书名并记进书单。纯前端运行，**无需服务器、无需注册，任何访问者的数据只保存在自己的浏览器里**。

## 功能

- 摄像头拍照 → OCR 自动识别书名（简体中文 / 中文+英文 / English 可切换）
- 手动添加、阅读状态管理（想读 / 在读 / 已读）、备注
- 搜索与状态筛选
- 导出 CSV（Excel 可打开）、导出 / 导入 JSON 备份
- 识别画面保存缩略图

## 在线体验

https://suncancan66-hub.github.io/book-title-scanner/

> 摄像头调用需要 HTTPS，GitHub Pages 自带；首次识别需联网加载识别引擎（约 1.7MB 中文模型）。

## 技术说明

- 纯静态单页应用（HTML + 原生 JS + IndexedDB 本地存储）
- OCR：Tesseract.js v5（WebAssembly，浏览器本地识别，图片不上传）
- 数据：localStorage 设置项 + IndexedDB 书单记录，导出功能可自行备份
- 本地运行版见仓库 `local/` 分支说明（README 待补），网页版为 CDN 资源

## 隐私

页面不收集、不上传任何信息；书单与照片缩略图保存在访问者自己的浏览器中。导出备份文件由用户自行保管。
