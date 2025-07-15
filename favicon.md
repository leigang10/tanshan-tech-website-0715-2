# 网站图标说明

## 需要添加的图标文件

为了完善网站，建议添加以下图标文件到项目根目录：

### 基本图标
- `favicon.ico` - 网站图标（16x16, 32x32像素）
- `favicon-16x16.png` - 16x16像素PNG图标
- `favicon-32x32.png` - 32x32像素PNG图标
- `apple-touch-icon.png` - iOS设备图标（180x180像素）

### 图标要求
1. 使用公司Logo作为图标基础
2. 确保在小尺寸下清晰可辨
3. 建议使用透明背景
4. 文件大小控制在50KB以内

### 添加方法
1. 将图标文件放入项目根目录
2. 在HTML文件的`<head>`部分添加以下代码：

```html
<link rel="icon" type="image/x-icon" href="/favicon.ico">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
```

### 图标生成工具
可以使用以下在线工具生成图标：
- [Favicon.io](https://favicon.io/)
- [RealFaviconGenerator](https://realfavicongenerator.net/)

这些图标将提升网站的专业性和用户体验。 