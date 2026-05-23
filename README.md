# 徐景浩个人学术主页

这是一个“简历模式”的个人学术主页，可以直接部署到 GitHub Pages。老师打开你的网址后，可以看到：

- 简历摘要
- 教育背景
- 项目与科研经历
- 荣誉奖项
- 完整简历 PDF
- 后续上传的项目代码入口

当前完整简历文件已放在：

```text
assets/cv.pdf
```

## 第一次使用 GitHub 的推荐流程

### 1. 注册 GitHub 账号

打开：

```text
https://github.com
```

注册账号。你的 GitHub 用户名会决定主页网址，例如用户名是 `xjh050221`，主页仓库名就是：

```text
xjh050221.github.io
```

最终网址就是：

```text
https://xjh050221.github.io
```

### 2. 新建主页仓库

登录 GitHub 后：

1. 右上角点击 `+`
2. 点击 `New repository`
3. Repository name 填：`你的用户名.github.io`
4. 选择 `Public`
5. 不要勾选 `Add a README file`
6. 点击 `Create repository`

GitHub Pages 的个人主页仓库必须使用 `用户名.github.io` 这种名字。

### 3. 上传主页文件

进入刚创建的仓库页面后：

1. 点击 `uploading an existing file`
2. 把本文件夹中的这些内容拖进去：

```text
index.html
styles.css
.nojekyll
.gitignore
README.md
assets/
project-readme-template.md
```

3. 页面底部的 commit message 可以写：

```text
Initial academic homepage
```

4. 点击 `Commit changes`

浏览器上传单个文件一般不能超过 25 MiB。你的简历 PDF 目前远小于这个限制，可以直接上传。

### 4. 打开你的主页

上传后等待 1-5 分钟，打开：

```text
https://你的用户名.github.io
```

如果出现 404：

1. 打开仓库的 `Settings`
2. 左侧点击 `Pages`
3. Source 选择 `Deploy from a branch`
4. Branch 选择 `main` 和 `/root`
5. 点击 `Save`
6. 再等几分钟刷新网址

## 项目代码怎么上传

不要把所有项目代码都塞进主页仓库。推荐每个项目单独建一个仓库，例如：

```text
metro-flood-evacuation
urban-design-rag
tunnel-fire-trajectory-prediction
subway-passenger-flow-system
```

每个项目仓库建议包含：

- `README.md`：项目介绍、运行方式、结果说明
- `requirements.txt` 或 `environment.yml`：Python 环境依赖
- `src/`：主要代码
- `data/`：小样例数据，真实敏感数据不要公开上传
- `docs/`：报告、图片、说明文档

项目代码上传后，把项目仓库网址填回 `index.html` 对应项目卡片里。

例如：

```html
<a href="https://github.com/你的用户名/urban-design-rag">查看代码</a>
```

## 隐私提醒

GitHub Pages 的免费个人主页通常来自公开仓库。公开仓库里的 PDF、手机号、邮箱、微信号、生日等信息，别人只要有链接就可能看到。

如果你想公开给老师看，但不想让个人隐私暴露太多，建议准备一份公开版简历：

- 保留姓名、学校、邮箱、项目、奖项
- 删除手机号、微信号、生日、家庭住址等信息
- 项目数据、API key、密码、导师未公开代码不要上传

## 本地预览

这个站点是纯静态网页，双击 `index.html` 就能打开。

也可以在本目录运行：

```bash
python -m http.server 8000
```

然后访问：

```text
http://localhost:8000
```

## 后续修改

常改的地方都在 `index.html`：

- 修改项目介绍
- 添加 GitHub 项目链接
- 更新论文和奖项
- 更换简历 PDF
- 添加个人照片
