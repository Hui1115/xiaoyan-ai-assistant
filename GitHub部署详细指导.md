# GitHub Pages 部署详细操作指导
## 📋 前置准备

### 需要准备：
- GitHub账号（如果没有请先注册：https://github.com）
- 你的项目文件：`index.html` 和 `logo.png`

---

## 🚀 第一步：创建GitHub仓库

### 1.1 登录GitHub
- 访问：https://github.com
- 登录你的账号

### 1.2 创建新仓库
1. 点击右上角的 `+` 按钮
2. 选择 `New repository`
3. 填写仓库信息：
   - **Repository name**：`xiaoyan-ai-assistant`（或你喜欢的名字）
   - **Description**：`晓研 - AI让调研更简单`
   - **Public/Private**：选择 `Public`（免费，GitHub Pages需要公开仓库）
   - **Add a README file**：可以勾选
   - **Add .gitignore**：不需要
   - **Choose a license**：可选

4. 点击 `Create repository`

---

## 📁 第二步：上传项目文件

### 2.1 方案A：网页直接上传（推荐新手）

1. 在新创建的仓库页面，点击 `Add file` → `Upload files`
2. 拖拽或选择你的文件：
   - 选择 `index.html`
   - 选择 `logo.png`
3. 填写提交信息：
   - `Add files via upload`
4. 点击 `Commit changes`

### 2.2 方案B：使用Git命令（推荐熟悉Git的用户）

如果你电脑上有Git，可以使用命令行：

```bash
# 进入项目目录
cd "/Users/wanghui/Desktop/AICoding 晓研/晓研-20261126-07_副本"

# 初始化Git仓库
git init

# 添加远程仓库（替换YOUR_USERNAME为你的GitHub用户名）
git remote add origin https://github.com/YOUR_USERNAME/xiaoyan-ai-assistant.git

# 添加所有文件
git add index.html logo.png

# 提交文件
git commit -m "初始提交：晓研AI助手首页"

# 推送到GitHub
git branch -M main
git push -u origin main
```

---

## ⚙️ 第三步：启用GitHub Pages

### 3.1 进入设置页面
1. 在你的仓库页面，点击 `Settings` 标签
2. 在左侧菜单中找到 `Pages`

### 3.2 配置Pages设置
1. 在 `Source` 部分，选择：
   - **Branch**：`main`
   - **Folder**：`/ (root)`

2. 点击 `Save`

### 3.3 等待部署
- GitHub会开始构建你的网站
- 通常需要1-5分钟完成
- 你可以在Pages页面看到部署状态

---

## 🔗 第四步：获取访问链接

### 4.1 查看部署链接
1. 返回 `Settings` → `Pages` 页面
2. 在顶部会显示你的网站链接，格式为：
   ```
   https://YOUR_USERNAME.github.io/xiaoyan-ai-assistant/
   ```

### 4.2 访问测试
- 点击链接访问你的网站
- 测试所有功能是否正常工作

---

## 🔄 第五步：更新和维护

### 5.1 更新文件
当你需要更新网站时：

#### 网页上传方式：
1. 进入仓库主页
2. 点击需要修改的文件
3. 点击右上角的 `✏️ Edit this file`
4. 修改内容
5. 填写提交信息并提交

#### Git命令方式：
```bash
# 修改文件后
git add .
git commit -m "更新说明"
git push origin main
```

### 5.2 自动重新部署
- 每次你推送代码到main分支
- GitHub Pages会自动重新构建
- 通常1-2分钟后更新生效

---

## 🎯 第六步：优化和进阶设置

### 6.1 自定义域名（可选）
如果你想使用自定义域名：

1. 在 `Settings` → `Pages` 中，在 `Custom domain` 处输入你的域名
2. 在你的域名DNS中添加记录：
   ```
   类型：CNAME
   名称：@
   值：YOUR_USERNAME.github.io
   ```

### 6.2 添加更多页面
如果你想添加其他页面：
1. 在仓库中创建新的HTML文件
2. 在index.html中添加链接指向新页面
3. 访问链接格式：`https://YOUR_USERNAME.github.io/xiaoyan-ai-assistant/页面名称.html`

### 6.3 添加图标
1. 准备一个 `favicon.ico` 文件
2. 上传到仓库根目录
3. 在index.html的`<head>`中添加：
```html
<link rel="icon" type="image/x-icon" href="favicon.ico">
```

---

## ⚠️ 常见问题和解决方案

### Q1: 页面显示404错误
**解决方案：**
- 检查文件名是否正确（大小写敏感）
- 确保文件在仓库根目录
- 等待几分钟让部署完成

### Q2: 图片不显示
**解决方案：**
- 检查图片路径（使用相对路径：`logo.png`）
- 确保图片已成功上传
- 检查图片文件名是否正确

### Q3: 链接不工作
**解决方案：**
- 检查链接是否使用了正确的相对路径
- 确保外部链接以`https://`开头

### Q4: 更新后没有立即生效
**解决方案：**
- 清除浏览器缓存
- 等待2-5分钟让GitHub重新部署
- 检查是否推送到了正确的分支

---

## 🎉 完成后的效果

部署成功后，你将获得：
- ✅ 一个永久免费的网站链接
- ✅ 自动HTTPS加密
- ✅ 全球CDN加速
- ✅ 版本控制和历史记录
- ✅ 简单的更新流程

---

## 📞 需要帮助？

如果在部署过程中遇到问题：
1. 检查GitHub Pages的部署状态
2. 查看仓库的Actions标签页是否有错误
3. 确保仓库是公开的（Private仓库GitHub Pages收费）
4. 可以随时向我寻求帮助！

---

**🎯 恭喜！按照这个指南，你就能成功将晓研AI助手部署到GitHub Pages上了！**
