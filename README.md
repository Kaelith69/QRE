<div align="center">
  <picture>
    <img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=250&section=header&text=Dynamic%20Resume%20Builder&fontSize=60&animation=fadeIn" alt="Dynamic Resume Builder Banner">
  </picture>
  
  <br/>
  
  **A lightweight, client-side generator for building visually striking, dynamically-balanced resumes with live preview and PDF export.**
  
  <br/>

  [![Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)](#)
  [![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](#)
  [![Version](https://img.shields.io/badge/Version-1.0.0-orange?style=flat-square)](#)
</div>

<br/>

## 🎯 What It Does

- **Real-Time Live Preview**: Edit your resume payload in a structured UI and instantly see updates reflected in a live canvas.
- **Dynamic Masonry Layouts**: Utilizes advanced CSS multi-column flows (`column-count`, `box-decoration-break: clone`) to seamlessly pack content and perfectly balance unequal column heights.
- **Multiple Aesthetic Templates**: Choose from over 10 distinct, highly-stylized templates (e.g., Dashboard, Comic, Art-Info, Minimalist).
- **Client-Side Rendering**: Operates entirely in the browser using raw HTML/CSS/JS with zero server-side dependencies.
- **One-Click PDF Export**: Generates pixel-perfect PDFs ready for ATS parsing and printing using native browser print capabilities.

## 💡 Why It Exists

- **Eliminates Layout Wrestling**: Traditional Word or LaTeX templates easily break when sections are uneven. This builder autonomously flows variable-length content without causing massive trailing white spaces.
- **Data-Driven Architecture**: Decouples the underlying data (Experience, Education, Projects) from the visual presentation, allowing instant theme switching without re-entering data.
- **Zero-Dependency Simplicity**: Removes the friction of Node.js toolchains or heavy JS frameworks. It runs directly from the file system.

## 🏗️ Architecture & Dataflow

<div align="center">
  <img src="https://mermaid.ink/svg/Z3JhcGggVEQKICAgIEFbVXNlciBJbnRlcmZhY2VdIC0tPnxVcGRhdGVzfCBCKFN0YXRlIE1hbmFnZXIpCiAgICBCIC0tPnxKU09OIFBheWxvYWR8IEN7VGVtcGxhdGUgRW5naW5lfQogICAgQyAtLT58UmVuZGVyc3wgRFtMaXZlIENhbnZhcyBET01dCiAgICBFW1RoZW1lIENvbnRyb2xzXSAtLT58Q1NTIFZhcmlhYmxlc3wgRAogICAgRCAtLi0+fHdpbmRvdy5wcmludHwgRigoUERGIEV4cG9ydCkp" alt="Architecture Diagram">
</div>

<div align="center">
  <img src="https://mermaid.ink/svg/c2VxdWVuY2VEaWFncmFtCiAgICBwYXJ0aWNpcGFudCBVIGFzIFVzZXIKICAgIHBhcnRpY2lwYW50IFVJIGFzIEZvcm0gSW5wdXRzCiAgICBwYXJ0aWNpcGFudCBTIGFzIFN0YXRlIChKUykKICAgIHBhcnRpY2lwYW50IEMgYXMgQ2FudmFzIFJlbmRlcmVyCiAgICAKICAgIFUtPj5VSTogRW50ZXJzIEV4cGVyaWVuY2UgRGF0YQogICAgVUktPj5TOiBVcGRhdGVzIFN0YXRlIE9iamVjdAogICAgUy0+PkM6IFRyaWdnZXJzIHJlbmRlclByZXZpZXcoKQogICAgQy0+PkM6IFNlbGVjdHMgVGVtcGxhdGUgSFRNTCBzdHJpbmcKICAgIEMtPj5DOiBNYXBzIFN0YXRlIHRvIEhUTUwKICAgIEMtLT4+VTogRGlzcGxheXMgVXBkYXRlZCBSZXN1bWUgVmlldw==" alt="Dataflow Sequence Diagram">
</div>

## 🛠️ Tech Stack

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)

## ⚙️ Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/dynamic-resume-builder.git

# Navigate to the project directory
cd dynamic-resume-builder

# Run the project locally (No installation required)
# Just open the HTML file in any modern browser
start dynamic_resume_builder_3.html
```

## 📜 License

MIT License

Copyright (c) 2026

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
