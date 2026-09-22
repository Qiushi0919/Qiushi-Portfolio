# 谢秋实作品集

谢秋实的个人主页与项目作品集，包含论文、电子设计竞赛、嵌入式系统项目与独立小项目（Codex Tidy、Boring Notch Focus、AltTab 和 MindMap）。

打开 `index.html` 查看个人主页；`portfolio-cover.html` 为兼容已有链接保留的同内容入口。

页面首次加载会等待关键缩略图；淡入后在后台预载论文、比赛和小项目三个分类的全部缩略图与展开详情媒体。

## 个人简历

`cv/index.html` 提供原版 PDF 预览、直接打开及下载。主站地址为 `https://qiushi0919.cn/cv`；主页和兼容入口的简历链接位于微信、QQ 联系方式行上方，支持中英文切换。

更新简历时替换 `cv/qiushi-xie-cv.pdf`，保持文件名不变，并用 `pypdfium2` 渲染第一页更新 `cv/qiushi-xie-cv.webp`（2.5 倍缩放、WebP quality=92），以兼容移动端浏览器。当前使用用户提供的 2026 年 9 月 PDF，不对原文件重新排版。

网站是静态文件，无需安装依赖或构建。提交 `main` 后由 GitHub Pages 发布；国内站使用服务器 `/opt/qiushi-portfolio-src` 拉取同一提交，将此次变更的入口、语言脚本和 `cv/` 同步到 `/opt/portfolio`。发布前在服务器 Web 根目录之外备份将覆盖的文件。现有 Nginx 静态目录规则自动处理 `/cv` 到 `/cv/`，无需改动其他路由。
