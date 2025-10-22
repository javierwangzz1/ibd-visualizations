# IBD Visualizations 项目重组规划

## 项目概述
Wang Lab (复旦大学907实验室) IBD (炎症性肠病) 可视化项目的目录结构重组计划。

**执行日期**: 2025-10-22
**目标**: 创建清晰、规范的项目结构，统一资源路径，便于维护和扩展

---

## 一、当前问题分析

### 1.1 目录结构混乱
- HTML文件散落在根目录 (20+个文件)
- 图片资源分散在 `image/` 和 `images2/` 两个目录
- 视频、图片、文档混合存放
- TIFF源文件与最终资源未分离

### 1.2 资源路径不统一
- 部分文件使用 `./image/`
- 部分文件使用 `image/`
- 部分文件使用 `images2/`
- 存在错误路径: `image/250723/` (实际应为 `image/`)

### 1.3 文件命名不规范
- 存在重复文件: `20250729-waic.html` vs `20250729_waic.html`
- 命名风格不统一: 有些用日期，有些用描述性名称
- 中文文件名存在: `系统2.html`, `炎症性肠病相关致病菌的评估与抗体开发靶点分析.pdf`

---

## 二、新目录结构设计

```
ibd-visualizations/
├── index.html                          # 主入口页面
├── README.md                           # 项目说明
├── PROJECT_REORGANIZATION.md           # 本规划文档
│
├── pages/                              # 所有HTML页面
│   ├── visualizations/                 # 数据可视化页面
│   │   ├── 3d-barplot.html            # 3D柱状图
│   │   ├── 3d-boxplot.html            # 3D点图
│   │   ├── lamina-propria.html        # 固有层工作流程
│   │   └── il10-lung-homeostasis.html # IL10肺稳态
│   │
│   ├── mouse-management/               # 小鼠管理系统
│   │   ├── 2025-06-16.html            # 按日期命名
│   │   ├── 2025-07-04.html
│   │   ├── 2025-07-07.html
│   │   ├── 2025-07-09.html
│   │   ├── 2025-07-19.html
│   │   ├── 2025-07-20.html
│   │   ├── 2025-08-04.html
│   │   ├── 2025-08-26.html
│   │   ├── 2025-09-17.html            # 最新版本
│   │   ├── 2025-09-30.html
│   │   └── mouse-housing.html         # 通用小鼠管理
│   │
│   ├── events/                         # 活动展览
│   │   └── waic-2025-07-29.html       # WAIC展览
│   │
│   └── misc/                           # 其他页面
│       ├── route.html                  # 上海地铁路线
│       └── traffic-system.html         # 交通隐患管理系统
│
├── assets/                             # 所有资源文件
│   ├── images/                         # 图片资源
│   │   ├── slides/                     # 幻灯片图片
│   │   │   ├── version1/               # images2来源的幻灯片
│   │   │   │   ├── Slide1.png
│   │   │   │   ├── Slide2.png
│   │   │   │   ├── Slide3.png
│   │   │   │   ├── Slide4.png
│   │   │   │   ├── Slide5.png
│   │   │   │   └── Slide6.png
│   │   │   └── version2/               # image来源的幻灯片
│   │   │       ├── Slide1.png
│   │   │       ├── Slide2.png
│   │   │       ├── Slide3.png
│   │   │       ├── Slide4.png
│   │   │       ├── Slide5.png
│   │   │       ├── Slide6.png
│   │   │       ├── Slide7.png
│   │   │       └── Slide8.png
│   │   │
│   │   ├── research/                   # 研究相关图片
│   │   │   ├── 250723-1.png
│   │   │   ├── 250723-2.png
│   │   │   └── 250723-3.png
│   │   │
│   │   ├── waic/                       # WAIC展览图片
│   │   │   ├── entrance.jpg            # 入口.jpg
│   │   │   ├── huawei-ascend.jpg       # 升腾.jpg
│   │   │   ├── basement-1.jpg          # 负一楼企业1.jpg
│   │   │   └── basement-2.jpg          # 负一楼企业2.jpg
│   │   │
│   │   ├── route/                      # 路线相关图片
│   │   │   ├── f1.jpg
│   │   │   ├── f2.jpg
│   │   │   ├── f3.jpg
│   │   │   ├── f4.jpg
│   │   │   ├── f5.jpg
│   │   │   ├── f7.jpg
│   │   │   ├── f8.jpg
│   │   │   ├── f9.jpg
│   │   │   └── f10.jpg
│   │   │
│   │   └── wechat/                     # 微信图片
│   │       ├── image-1.jpg             # WeChat79b373...
│   │       └── image-2.jpg             # WeChatb1c7e0...
│   │
│   ├── videos/                         # 视频资源
│   │   ├── waic/                       # WAIC相关视频
│   │   │   ├── amazon.mp4
│   │   │   ├── finai.mp4
│   │   │   ├── kling-ai.mp4            # 可灵AI.mp4
│   │   │   ├── suanfeng.mp4            # 算丰.mp4
│   │   │   ├── tesla.mp4
│   │   │   ├── floor2.mp4              # 二楼.mp4
│   │   │   └── rokid.mp4
│   │   │
│   │   └── route/                      # 路线相关视频
│   │       └── f6.mp4
│   │
│   └── pdfs/                           # PDF文档
│       ├── initial-analysis.pdf        # analysis.pdf
│       └── ibd-pathogen-assessment.pdf # 炎症性肠病...pdf
│
└── archive/                            # 归档文件 (不在web访问中)
    └── source-tiff/                    # 原始TIFF文件
        ├── Slide1.tiff
        ├── Slide2.tiff
        ├── Slide3.tiff
        ├── Slide4.tiff
        ├── Slide5.tiff
        ├── Slide6.tiff
        ├── Slide7.tiff
        └── Slide8.tiff
```

---

## 三、文件映射关系

### 3.1 HTML文件重命名

| 原文件名 | 新文件名 | 位置 |
|---------|---------|------|
| 3D_Barplot_Fixed_Symbols.html | 3d-barplot.html | pages/visualizations/ |
| 3D_Boxplot_Reference_Legend.html | 3d-boxplot.html | pages/visualizations/ |
| lamina_propria_workflow_visualization.html | lamina-propria.html | pages/visualizations/ |
| il10_lung_homeostasis.html | il10-lung-homeostasis.html | pages/visualizations/ |
| 20250616.html | 2025-06-16.html | pages/mouse-management/ |
| 250704_final.html | 2025-07-04.html | pages/mouse-management/ |
| 250707.html | 2025-07-07.html | pages/mouse-management/ |
| 250709.html | 2025-07-09.html | pages/mouse-management/ |
| 250719.html | 2025-07-19.html | pages/mouse-management/ |
| 250720.html | 2025-07-20.html | pages/mouse-management/ |
| 250804.html | 2025-08-04.html | pages/mouse-management/ |
| 250826.html | 2025-08-26.html | pages/mouse-management/ |
| 250917_updated.html | 2025-09-17.html | pages/mouse-management/ |
| 250930.html | 2025-09-30.html | pages/mouse-management/ |
| mouse_housing_250622_2.html | mouse-housing.html | pages/mouse-management/ |
| 20250729-waic.html (保留此版本) | waic-2025-07-29.html | pages/events/ |
| 20250729_waic.html (删除重复) | - | - |
| route.html | route.html | pages/misc/ |
| 系统2.html | traffic-system.html | pages/misc/ |

### 3.2 资源路径统一规则

所有HTML文件中的资源路径统一使用相对于项目根目录的路径:

**从 pages/visualizations/ 访问资源:**
```html
<!-- 图片 -->
<img src="../../assets/images/research/250723-1.png">

<!-- PDF -->
<a href="../../assets/pdfs/initial-analysis.pdf">
```

**从 pages/mouse-management/ 访问资源:**
```html
<!-- 幻灯片 -->
<img src="../../assets/images/slides/version2/Slide1.png">
```

**从 pages/events/ 访问资源:**
```html
<!-- WAIC视频 -->
<source src="../../assets/videos/waic/amazon.mp4">

<!-- WAIC图片 -->
<img src="../../assets/images/waic/entrance.jpg">
```

---

## 四、执行步骤

### 步骤1: 创建新目录结构
```bash
mkdir -p pages/{visualizations,mouse-management,events,misc}
mkdir -p assets/{images,videos,pdfs}
mkdir -p assets/images/{slides/version1,slides/version2,research,waic,route,wechat}
mkdir -p assets/videos/{waic,route}
mkdir -p archive/source-tiff
```

### 步骤2: 移动和重命名HTML文件
移动所有HTML文件到对应的pages子目录

### 步骤3: 整理和移动资源文件

**图片资源:**
- `image/Slide*.png` → `assets/images/slides/version2/`
- `images2/Slide*.png` → `assets/images/slides/version1/`
- `image/250723-*.png` → `assets/images/research/`
- `image/入口.jpg` 等 → `assets/images/waic/` (重命名为英文)
- `images2/f*.jpg` → `assets/images/route/`
- `WeChat*.jpg` → `assets/images/wechat/` (规范命名)

**视频资源:**
- `image/amazon.mp4` 等WAIC视频 → `assets/videos/waic/`
- `images2/f6.mp4` → `assets/videos/route/`

**PDF资源:**
- `analysis.pdf` → `assets/pdfs/initial-analysis.pdf`
- `炎症性肠病....pdf` → `assets/pdfs/ibd-pathogen-assessment.pdf`

**归档文件:**
- `Slide*.tiff` → `archive/source-tiff/`

### 步骤4: 更新所有HTML文件中的资源路径

需要更新的路径模式:
- `image/` → `../../assets/images/`
- `images2/` → `../../assets/images/`
- `image/250723/250723-1.png` → `../../assets/images/research/250723-1.png` (修正错误路径)
- PDF链接更新

### 步骤5: 更新index.html

在index.html中添加完整的页面导航:
- 数据可视化板块
- 小鼠管理系统板块
- 活动展览板块
- 其他工具板块

### 步骤6: 清理工作

删除:
- 原 `image/` 目录 (清空后删除)
- 原 `images2/` 目录 (清空后删除)
- 重复文件 `20250729_waic.html`
- 空文件: `image/1`, `images2/1`

---

## 五、资源路径修复清单

### 需要修复的错误路径

**文件**: 250826.html, 250917_updated.html, 250804.html
- `image/250723/250723-1.png` → `assets/images/research/250723-1.png`
- `image/250723/250723-2.png` → `assets/images/research/250723-2.png`
- `image/250723/250723-3.png` → `assets/images/research/250723-3.png`

### 幻灯片版本说明

**Version 1** (来自images2/):
- 6张幻灯片 (Slide1-6)
- 主要用于: 250719.html, 250720.html, 250826.html, 250804.html, 250917_updated.html

**Version 2** (来自image/):
- 8张幻灯片 (Slide1-8)
- 主要用于: 250707.html, 250709.html

---

## 六、index.html 更新方案

### 新增导航结构

```html
<div class="section">
  <h2>🔬 数据可视化</h2>
  <div class="cards">
    <div class="card">
      <h3>3D 柱状图</h3>
      <a href="pages/visualizations/3d-barplot.html">查看</a>
    </div>
    <div class="card">
      <h3>3D 点图</h3>
      <a href="pages/visualizations/3d-boxplot.html">查看</a>
    </div>
    <div class="card">
      <h3>固有层工作流程</h3>
      <a href="pages/visualizations/lamina-propria.html">查看</a>
    </div>
    <div class="card">
      <h3>IL10 肺稳态</h3>
      <a href="pages/visualizations/il10-lung-homeostasis.html">查看</a>
    </div>
  </div>
</div>

<div class="section">
  <h2>🐭 小鼠管理系统</h2>
  <div class="cards">
    <div class="card">
      <h3>2025-09-17 (最新)</h3>
      <a href="pages/mouse-management/2025-09-17.html">查看</a>
    </div>
    <!-- 更多历史版本... -->
  </div>
</div>

<div class="section">
  <h2>🎪 活动展览</h2>
  <div class="cards">
    <div class="card">
      <h3>WAIC 2025</h3>
      <a href="pages/events/waic-2025-07-29.html">查看</a>
    </div>
  </div>
</div>

<div class="section">
  <h2>📚 研究文档</h2>
  <div class="cards">
    <div class="card">
      <h3>初步分析报告</h3>
      <a href="assets/pdfs/initial-analysis.pdf">下载PDF</a>
    </div>
    <div class="card">
      <h3>IBD致病菌评估</h3>
      <a href="assets/pdfs/ibd-pathogen-assessment.pdf">下载PDF</a>
    </div>
  </div>
</div>
```

---

## 七、验证清单

完成重组后需要验证:

- [ ] 所有HTML页面可以正常访问
- [ ] 所有图片资源正确显示
- [ ] 所有视频资源可以播放
- [ ] 所有PDF链接可以下载
- [ ] index.html所有导航链接正常工作
- [ ] 没有404错误
- [ ] 旧目录已清空和删除
- [ ] 浏览器测试 (Chrome, Firefox, Safari)

---

## 八、备份说明

**执行重组前必须备份:**
```bash
# 在项目父目录执行
tar -czf ibd-visualizations-backup-20251022.tar.gz ibd-visualizations/
```

**备份文件位置**: `/Users/juewang/ibd-visualizations-backup-20251022.tar.gz`

---

## 九、优势总结

重组后的优势:
1. ✅ **清晰的模块化结构** - 按功能分类组织
2. ✅ **统一的资源路径** - 所有资源使用规范路径
3. ✅ **规范的命名方式** - 英文命名,连字符分隔
4. ✅ **便于维护扩展** - 新增内容有明确位置
5. ✅ **分离关注点** - 源文件与web资源分离
6. ✅ **版本管理友好** - 清晰的文件组织利于版本控制

---

**文档版本**: v1.0
**创建时间**: 2025-10-22
**维护者**: Wang Lab 907
