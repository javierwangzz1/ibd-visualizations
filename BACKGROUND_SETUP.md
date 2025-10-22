# 背景图片设置指南

## 需要的操作

页面背景已配置为使用莫奈印象派画作，但需要您手动保存这两张图片到正确的位置。

## 图片保存步骤

请将您提供的两张图片按以下方式保存：

### 1. 第一张图片（干草堆）
- **文件名**: `haystacks-monet.jpg`
- **保存路径**: `/Users/juewang/Desktop/ibd-visualizations/assets/images/haystacks-monet.jpg`
- **用于**: index.html（主页背景）

### 2. 第二张图片（罂粟花田）
- **文件名**: `poppy-field-monet.jpg`
- **保存路径**: `/Users/juewang/Desktop/ibd-visualizations/assets/images/poppy-field-monet.jpg`
- **用于**: animal-room-videos.html（视频页背景）

## 保存方法

1. 在聊天中找到您发送的两张图片
2. 右键点击每张图片 → "另存为..."
3. 保存到上述指定的路径和文件名
4. 确保 `assets/images/` 目录已存在

## CSS 配置说明

两个页面的背景已经配置完成：

### index.html (主页)
```css
body {
  background-image: url('assets/images/haystacks-monet.jpg');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  background-repeat: no-repeat;
}
/* 半透明白色覆盖层，让文字更清晰 */
body::before {
  background: rgba(255, 255, 255, 0.85);
}
```

### animal-room-videos.html (视频页)
```css
body {
  background-image: url('assets/images/poppy-field-monet.jpg');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  background-repeat: no-repeat;
}
/* 半透明白色覆盖层，让文字更清晰 */
body::before {
  background: rgba(255, 255, 255, 0.88);
}
```

## 完成后

图片保存完成后，页面将自动显示印象派背景：
- 背景图片会固定在视口，不随页面滚动
- 半透明白色覆盖层确保内容清晰可读
- 响应式设计，自动适配不同屏幕尺寸

---

生成时间: 2025-10-23
