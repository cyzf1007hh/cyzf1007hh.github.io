# 网站维护

这是独立静态网站，无需安装前端依赖。只发布本目录，不发布上级工作区、PDF 处理库或论文源码。

## 内容位置

- `index.html`：个人介绍、研究方向、论文列表。
- `papers/r2r/index.html`：R2R 标题、作者、单位、完整摘要、方法及结果图。
- `assets/style.css`：响应式布局、颜色、字体与键盘焦点。
- `papers/r2r/r2r-high-resolution.pdf`：高清正文与参考文献，共 10 页，不含补充材料（46.94 MB）。
- `papers/r2r/r2r.pdf`：2.16 MB 正文检索版（10 页，不含补充材料）；照片目标 180 dpi、JPEG quality 85，保留文本与矢量。

## 发布前

1. 确认 GitHub 仓库和最终网址，勿覆盖既有主页。
2. 将两页 canonical、论文页 citation_pdf_url、sitemap.xml 中 URL 设置为最终地址。
3. 首次实际公开时填写 citation_publication_date、citation_online_date 和页面显示日期；采用 `YYYY/MM/DD` 元数据格式。后续修正页面不得重置首次公开日期。
4. 状态保持 Preprint，不添加未经证实的期刊、会议或 arXiv 编号。
5. 若部署在子目录，域名根目录的 robots.txt 才是生效的抓取规则。核对根目录没有阻止本站；子目录 robots.txt 仅为站点独立部署时的配置文件。

## 增加论文

每篇论文创建单独目录和 `index.html`，PDF 放同一目录。每位作者使用一个 citation_author 标签，标题和日期准确填写。摘要直接显示在 HTML 中，避免依赖 JavaScript。更新主页论文链接与 sitemap.xml。

## 素材来源

R2R 图来自用户指定公开论文源码的 figures/：

- fig1_teaser.pdf：主页原始比较图。
- fig2_overview.pdf：论文方法图，转换为 SVG，保持矢量结构。
- qualitative_udisd.pdf、qualitative_classic.pdf：完整定性比较图，保留方法标签与标注。

图片未改变实验内容、颜色或比较条件。中文姓名与身份来自用户提供的信息。未使用简历或企业内部材料；旧站模板作者论文没有纳入本网站。

## Google Scholar

遵循 https://scholar.google.com/intl/en/scholar/inclusion.html 。独立 HTML 页面、完整摘要、同目录直接 PDF、准确引用元数据有助于抓取，但不保证收录。发布后检查两个页面和 PDF 都能在未登录情况下直接访问。

## 本地预览

在此目录运行 `python -m http.server 8766 --bind 127.0.0.1`，访问 http://127.0.0.1:8766/ 。
