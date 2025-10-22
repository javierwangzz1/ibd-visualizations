# IBD Visualizations - Wang Lab 907

Wang Lab (Fudan University, Room 907) IBD (Inflammatory Bowel Disease) research visualization portal.

## 🎯 Project Overview

This repository contains interactive visualizations, mouse management systems, and research documentation for B Cell and Immunity research focused on IBD.

**Research Areas**: B Cell / Immunity / IgA / Mucosal Immunity

## 📁 Directory Structure

```
ibd-visualizations/
├── index.html                          # Main portal page
├── README.md                           # This file
├── PROJECT_REORGANIZATION.md           # Reorganization documentation
│
├── pages/                              # All HTML pages
│   ├── visualizations/                 # Data visualization pages
│   │   ├── 3d-barplot.html            # 3D bar plot (microbe analysis)
│   │   ├── 3d-boxplot.html            # 3D dot plot (reference grouped)
│   │   ├── lamina-propria.html        # Cell separation workflow
│   │   └── il10-lung-homeostasis.html # IL10 analysis
│   │
│   ├── mouse-management/               # Mouse housing system
│   │   ├── 2025-09-17.html            # Latest version
│   │   ├── 2025-09-30.html
│   │   ├── 2025-08-26.html
│   │   ├── 2025-08-04.html
│   │   ├── 2025-07-20.html
│   │   ├── 2025-07-19.html
│   │   ├── 2025-07-09.html
│   │   ├── 2025-07-07.html
│   │   ├── 2025-07-04.html
│   │   ├── 2025-06-16.html
│   │   └── mouse-housing.html
│   │
│   ├── events/                         # Event documentation
│   │   └── waic-2025-07-29.html       # WAIC 2025 visit
│   │
│   └── misc/                           # Utility pages
│       ├── route.html                  # Shanghai metro route
│       └── traffic-system.html         # Traffic hazard system
│
├── assets/                             # All resources
│   ├── images/                         # Images
│   │   ├── slides/                     # Presentation slides
│   │   │   ├── version1/               # 6 slides (from images2)
│   │   │   └── version2/               # 8 slides (from image)
│   │   ├── research/                   # Research images
│   │   ├── waic/                       # WAIC event images
│   │   ├── route/                      # Route images
│   │   └── wechat/                     # WeChat images
│   │
│   ├── videos/                         # Videos
│   │   ├── waic/                       # WAIC event videos
│   │   └── route/                      # Route videos
│   │
│   └── pdfs/                           # PDF documents
│       ├── initial-analysis.pdf
│       └── ibd-pathogen-assessment.pdf
│
└── archive/                            # Archived files
    └── source-tiff/                    # Original TIFF files
        ├── Slide1.tiff - Slide8.tiff
```

## 🚀 Getting Started

### Quick Start

1. Open `index.html` in your web browser
2. Navigate to desired section from the main portal
3. All pages are self-contained and work offline

### Deployment

For deployment to a web server:

```bash
# Simply upload the entire directory to your web server
# Ensure directory structure is preserved
# No build process required
```

## 📊 Features

### Data Visualizations
- **3D Interactive Plots**: Plotly-based 3D visualizations
- **Scientific Workflows**: Detailed protocol visualizations
- **Research Analysis**: IBD pathogen and IL10 analysis

### Mouse Management System
- **Genotype Tracking**: Comprehensive mouse genotype database
- **Housing Management**: Visual grid-based housing system
- **Version History**: Historical snapshots from June to September 2025

### Event Documentation
- **WAIC 2025**: World Artificial Intelligence Conference visit
- Multimedia documentation (images + videos)

## 🔧 Technical Details

### Technologies Used
- **HTML5/CSS3**: Modern, responsive design
- **Plotly.js**: Interactive 3D visualizations
- **Vanilla JavaScript**: No framework dependencies
- **Self-contained**: All resources locally hosted

### Browser Compatibility
- Chrome/Edge (recommended)
- Firefox
- Safari

### File Naming Conventions
- HTML pages: lowercase, hyphen-separated (e.g., `3d-barplot.html`)
- Dates: ISO format (e.g., `2025-09-17.html`)
- Assets: descriptive English names

## 📈 Statistics

- **HTML Pages**: 18 pages
- **Total Assets**: 42 files
  - Images: 30+ files
  - Videos: 8 files
  - PDFs: 2 documents

## 🔄 Recent Updates

**2025-10-22** - Major reorganization
- ✅ Restructured entire project for better organization
- ✅ Standardized file naming conventions
- ✅ Unified resource paths
- ✅ Created comprehensive navigation portal
- ✅ Separated source files from web assets

See `PROJECT_REORGANIZATION.md` for detailed reorganization plan and execution steps.

## 📝 Research Interests

- Intestinal B cell responses and mucosal immunity
- IgA antibody secretion and regulatory mechanisms
- Germinal center formation and memory B cell differentiation
- Fc receptor function in plasma cell development
- Immunoglobulin diversity in infection and inflammation

## 📧 Contact

**Wang Lab**
Room 907
Fudan University
B Cell / Immunity / IgA Research

## 📄 License

For research and educational purposes.

---

**Last Updated**: 2025-10-22
**Reorganization**: Completed successfully ✅
