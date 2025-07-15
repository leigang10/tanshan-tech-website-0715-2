# 北京探山科技有限公司网站部署指南

## 项目概述

这是一个为北京探山科技有限公司开发的静态网站，包含首页和关于我们两个页面。网站采用响应式设计，适配手机和电脑等不同屏幕尺寸。

## 文件结构

```
TSweb_cursor/
├── index.html          # 首页
├── about.html          # 关于我们页面
├── css/
│   └── style.css       # 样式文件
├── js/
│   └── script.js       # JavaScript文件
├── images/             # 图片文件夹
│   └── README.md       # 图片说明文档
└── README.md           # 本部署指南
```

## 部署方法

### 方法一：GitHub Pages（推荐）

#### 步骤1：注册GitHub账号
1. 访问 [GitHub官网](https://github.com)
2. 点击右上角"Sign up"注册账号
3. 完成邮箱验证

#### 步骤2：下载并安装GitHub Desktop
1. 访问 [GitHub Desktop官网](https://desktop.github.com/)
2. 下载并安装GitHub Desktop应用
3. 使用GitHub账号登录

#### 步骤3：创建新仓库
1. 打开GitHub Desktop应用
2. 点击"File" → "New repository"（或按Ctrl+N）
3. 填写仓库信息：
   - Name: `tanshan-tech-website`
   - Description: `北京探山科技有限公司官网`
   - Local path: 选择本地文件夹位置
   - 勾选"Public"
   - 不要勾选"Initialize this repository with a README"
4. 点击"Create repository"

#### 步骤4：添加网站文件
1. 在GitHub Desktop中，点击"Show in Explorer"打开本地文件夹
2. 将整个网站项目文件复制到该文件夹中（包括index.html、about.html、css、js、images等）
3. 回到GitHub Desktop，会看到所有文件都被检测到

#### 步骤5：提交并推送代码
1. 在GitHub Desktop中，在左侧填写提交信息：
   - Summary: `Initial commit - 添加网站文件`
   - Description: `创建北京探山科技有限公司官网`
2. 点击"Commit to main"
3. 点击"Push origin"将代码推送到GitHub

#### 步骤6：启用GitHub Pages
1. 在GitHub Desktop中，点击"Repository" → "View on GitHub"
2. 在GitHub网页中，点击"Settings"标签
3. 左侧菜单找到"Pages"
4. 在"Source"部分，选择"Deploy from a branch"
5. 在"Branch"下拉菜单中选择"main"，文件夹选择"/(root)"
6. 点击"Save"
7. 等待几分钟，GitHub会自动生成网站链接

#### 步骤7：访问网站
- 网站链接格式：`https://你的用户名.github.io/tanshan-tech-website`
- 例如：`https://zhangsan.github.io/tanshan-tech-website`

### GitHub Desktop 使用技巧

#### 后续更新网站内容
1. 在本地文件夹中修改网站文件
2. 回到GitHub Desktop，会看到修改的文件被标记为"Changes"
3. 填写提交信息，点击"Commit to main"
4. 点击"Push origin"推送到GitHub
5. GitHub Pages会自动更新网站内容

#### 查看网站状态
- 在GitHub Desktop中点击"Repository" → "View on GitHub"
- 在GitHub网页的"Settings" → "Pages"中可以看到部署状态
- 绿色勾表示部署成功，可以访问网站

#### 常见问题解决
- 如果推送失败，检查网络连接
- 如果网站无法访问，等待几分钟后重试
- 如果文件没有显示，确保文件已复制到正确的文件夹
- 如果自定义域名冲突，参考"自定义域名冲突解决方案"

#### 域名冲突快速解决
1. **立即解决方案**：暂时使用GitHub提供的免费域名
   - 网站链接：`https://你的用户名.github.io/tanshan-tech-website`
   - 功能完全正常，只是域名不是自定义的

2. **后续解决**：检查您的GitHub账户中其他仓库
   - 在GitHub主页查看所有仓库
   - 找到占用`tanshan.com.cn`的仓库
   - 决定是否要转移域名绑定

### 方法二：Vercel（备选方案）

#### 步骤1：注册Vercel账号
1. 访问 [Vercel官网](https://vercel.com)
2. 点击"Sign Up"注册账号
3. 建议使用GitHub账号登录

#### 步骤2：导入项目
1. 登录后点击"New Project"
2. 选择"Import Git Repository"
3. 选择你的GitHub仓库
4. 点击"Deploy"

#### 步骤3：访问网站
- Vercel会自动生成一个域名
- 格式类似：`https://tanshan-tech-website-xxx.vercel.app`

## 自定义域名设置（可选）

### GitHub Pages设置自定义域名
1. 购买域名（如：www.tanshan.com.cn）
2. 在GitHub仓库的Settings > Pages中
3. 在"Custom domain"输入框中输入你的域名
4. 点击"Save"
5. 在域名提供商处设置DNS解析：
   - 类型：CNAME
   - 主机记录：www
   - 记录值：你的用户名.github.io

### 自定义域名冲突解决方案

#### 方案1：移除其他仓库的域名绑定
1. 找到占用该域名的其他仓库
2. 进入该仓库的Settings > Pages
3. 删除"Custom domain"中的域名
4. 保存设置
5. 重新在当前仓库设置域名

#### 方案2：使用子域名
如果不想影响其他仓库，可以使用子域名：
- 主域名：`www.tanshan.com.cn`（用于其他仓库）
- 子域名：`website.tanshan.com.cn`（用于当前网站）
- 在DNS中添加子域名解析

#### 方案3：使用不同域名
- 使用`tanshan-tech.com.cn`
- 或使用`www.tanshan-tech.com.cn`
- 确保新域名未被占用

#### 方案4：暂时使用GitHub提供的域名
- 使用默认的`你的用户名.github.io/tanshan-tech-website`
- 等域名问题解决后再设置自定义域名

### Vercel设置自定义域名
1. 在Vercel项目页面点击"Settings"
2. 选择"Domains"
3. 添加你的域名
4. 按照提示设置DNS解析

## 内容修改指南

### 修改文字内容
1. 用文本编辑器打开对应的HTML文件
2. 找到需要修改的文字（已用注释标记）
3. 直接修改文字内容
4. 保存文件并重新部署

### 替换图片
1. 准备新的图片文件
2. 将图片重命名为对应的文件名（参考images/README.md）
3. 将图片放入images文件夹
4. 重新部署网站

### 修改联系方式
在`index.html`和`about.html`中找到以下部分进行修改：
```html
<span class="contact-value">（+86）15011531282</span>
<span class="contact-value">lingfei@tanshan.com.cn</span>
```

## 技术说明

### 使用的技术
- HTML5：页面结构
- CSS3：样式和响应式设计
- JavaScript：基础交互功能
- 无后端，纯静态网站

### 浏览器兼容性
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

### 性能优化
- 图片压缩优化
- CSS和JS文件压缩
- 响应式图片加载
- 移动端优化

## 常见问题

### Q: 网站加载速度慢怎么办？
A: 检查图片大小，建议每张图片控制在500KB以内，可以使用在线工具压缩图片。

### Q: 手机上看效果不好？
A: 网站已采用响应式设计，如果仍有问题，请检查浏览器是否为最新版本。

### Q: 如何添加新的页面？
A: 参考现有页面结构创建新的HTML文件，并在导航菜单中添加链接。

### Q: 如何修改网站颜色？
A: 在`css/style.css`文件中修改CSS变量或直接修改颜色值。

## 维护建议

1. **定期更新内容**：保持网站信息的最新性
2. **图片优化**：定期压缩和优化图片
3. **备份代码**：定期备份网站代码
4. **监控访问**：使用Google Analytics等工具监控网站访问情况

## 联系支持

如果在部署过程中遇到问题，可以：
1. 查看GitHub Pages或Vercel的官方文档
2. 在GitHub仓库中提交Issue
3. 联系技术支持

---

**注意**：本网站为静态网站，所有修改都需要重新部署才能生效。 