# 智能补货原型静态站点

这是智能补货与产销协同系统的可部署静态原型。

## 文件结构

```text
replenishment-prototype/
  index.html
  README.md
  vercel.json
  netlify.toml
  .nojekyll
```

## 本地预览

直接双击 `index.html`，或在当前目录启动一个静态服务：

```bash
python3 -m http.server 8080
```

然后访问：

```text
http://localhost:8080
```

## Vercel 部署

1. 将 `replenishment-prototype` 目录上传到 GitHub/GitLab。
2. 在 Vercel 新建项目。
3. Root Directory 选择 `replenishment-prototype`。
4. Framework Preset 选择 `Other`。
5. Build Command 留空。
6. Output Directory 留空或填写 `.`。

## Netlify 部署

方式一：直接拖拽部署。

1. 打开 Netlify。
2. 选择 Add new site -> Deploy manually。
3. 将整个 `replenishment-prototype` 目录拖进去。

方式二：连接 Git 仓库。

1. Root directory 选择 `replenishment-prototype`。
2. Build command 留空。
3. Publish directory 填写 `.`。

## GitHub Pages 部署

1. 将目录内容提交到仓库。
2. Settings -> Pages。
3. Source 选择对应分支。
4. 如果整个仓库只放这个原型，目录选择 `/root`。
5. 如果放在子目录，可将 `replenishment-prototype` 内容复制到 `docs/` 并选择 `/docs`。

## 更新原型

如果继续修改根目录下的 `smart-replenishment-workbench.html`，需要同步复制到：

```text
replenishment-prototype/index.html
```
