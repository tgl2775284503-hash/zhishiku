# 📂 归档 (Archives)

<style>
/* ========================================================================
   终极解决方案：简约、超紧凑的时间树归档列表（文本化，非卡片式）
   ======================================================================== */

/* 1. 整体页面和标题预设（使其整体更像列表） */
.md-typeset h1 {
    font-size: 2rem !important; /* 减小页面标题字号 */
    margin-bottom: 0.5rem !important; /* 减小底部间距 */
}

/* 2. 整体容器：居中，缩减上下大边距 */
.timeline-container {
    position: relative;
    max-width: 800px; /* 稍微缩窄，使其视觉上更像文本列表 */
    margin: 1rem auto 3rem auto !important; /* 大幅减小页面顶部的间距 */
    padding: 0 1rem;
}

/* 3. 垂直时间线：改细（1px）且颜色更淡，以适配紧凑布局 */
.timeline-container::after {
    content: '';
    position: absolute;
    width: 1px; /* 极细时间线 */
    background-color: #f1f1f1; /* 更淡的灰色线 */
    top: 0;
    bottom: 0;
    left: 100px; /* 缩减左侧缩进，腾出空间 */
    margin-left: -0.5px;
    z-index: 0;
}

/* 4. 时间树单条项目容器：核心 densification 修改 */
.timeline-item {
    position: relative;
    margin-bottom: 0.6rem !important; /* 【关键】：极致缩减单条项目之间的垂直间距 */
    width: 100%;
    display: flex;
    align-items: center; /* 确保日期、圆点、标题在同一水平线上 */
}

/* 5. 左侧的日期：减小字号，设定单行高度 */
.timeline-meta {
    position: absolute;
    left: 0;
    top: 0; /* 对齐标题顶部 */
    width: 90px; /* 缩减宽度 */
    text-align: right;
    font-size: 0.85rem; /* 减小字号到普通文字大小 */
    color: #999;
    font-weight: 500;
    line-height: 1.4 !important;
}
/* ELLIPSIS FIX（保持，防止日期撑破布局） */
.timeline-meta .md-ellipsis {
    white-space: normal !important;
    word-break: break-word !important;
    display: block !important;
}

/* 6. 时间线上的锚点“圆点”：改小（10px） */
.timeline-item::after {
    content: '';
    position: absolute;
    width: 10px; /* 小圆点 */
    height: 10px;
    border-radius: 50%;
    background-color: #f1f1f1; /* 默认颜色 */
    border: 2px solid #ddd;
    top: 0.35rem; /* 对齐标题基线 */
    left: 100px; /* 对齐时间线 */
    margin-left: -5px;
    z-index: 1;
    transition: all 0.3s ease;
}

/* 7. 悬停效果：圆点和线 */
.timeline-item:hover::after {
    border-color: #42a5f5;
    background-color: #e3f2fd;
}

/* 8. 右侧的内容卡片：彻底移除“卡片”背景色、边框和发光阴影！ */
.timeline-content {
    position: relative;
    left: 120px; /* 紧贴时间线 */
    width: calc(100% - 130px); /* 占据剩余全部宽度 */
    padding: 0 !important; /* 核心：【彻底删掉所有 Padding】 */
    background-color: transparent !important; /* 【核心】：彻底移除背景色 */
    border: none !important; /* 【核心】：彻底移除边框 */
    box-shadow: none !important; /* 【核心】：彻底移除发光阴影 */
}

/* 9. 核心修改：减小标题字号，彻底删掉 Padding */
.timeline-item .timeline-content h3 {
    margin: 0 !important; /* 【关键】：彻底删掉标题所有 Margin */
    font-size: 0.95rem !important; /* 【关键】：将标题字号减小到普通文字大小，非标题级别 */
    font-weight: 600;
    color: #444;
    line-height: 1.4 !important;
    padding: 0 !important; /* 【关键】：彻底删掉所有 Padding */
}

/* 10. 标题链接：蓝色 + 移除下划线 */
.timeline-item .timeline-content h3 a {
    color: #1976d2 !important;
    text-decoration: none !important;
    transition: color 0.2s;
}
.timeline-item .timeline-content h3 a:hover {
    color: #0d47a1 !important;
}

/* 11. 悬停项目：整体颜色变暗，提升阅读体验 */
.timeline-item:hover .timeline-content h3 a {
    color: #0d47a1 !important;
}

</style>

<div class="timeline-container">
    
    <div class="timeline-item">
        <div class="timeline-meta">
            <span class="md-ellipsis">2025年<br>12月20日</span>
        </div>
        <div class="timeline-content">
            <h3><a href="20251220_30_gpt/">白嫖 ChatGPT Plus 教程：30秒极速注册方法</a></h3>
            </div>
    </div>

    <div class="timeline-item">
        <div class="timeline-meta">
            <span class="md-ellipsis">2025年<br>11月</span>
        </div>
        <div class="timeline-content">
            <h3><a href="#">如何用 Cursor 打造 AI 工作流：新手指南</a></h3>
        </div>
    </div>
    
    <div class="timeline-item">
        <div class="timeline-meta">
            <span class="md-ellipsis">2025年<br>10月</span>
        </div>
        <div class="timeline-content">
            <h3><a href="#">优雅地探索数字世界！点击查阅查阅教程！</a></h3>
        </div>
    </div>

    <div class="timeline-item">
        <div class="timeline-meta">
            <span class="md-ellipsis">2025年<br>09月</span>
        </div>
        <div class="timeline-content">
            <h3><a href="#">MkDocs Material 主题高级定制技巧：打造专属个人主页</a></h3>
        </div>
    </div>
    
    <div class="timeline-item">
        <div class="timeline-meta">
            <span class="md-ellipsis">2025年<br>08月</span>
        </div>
        <div class="timeline-content">
            <h3><a href="#">GitHub CDN 缓存清理与绕过策略终极指南</a></h3>
        </div>
    </div>
    
    <div class="timeline-item">
        <div class="timeline-meta">
            <span class="md-ellipsis">2025年<br>07月</span>
        </div>
        <div class="timeline-content">
            <h3><a href="#">如何利用 Git 的 Stash 功能保护未完成的代码状态</a></h3>
        </div>
    </div>
    
    <div class="timeline-item">
        <div class="timeline-meta">
            <span class="md-ellipsis">2025年<br>06月</span>
        </div>
        <div class="timeline-content">
            <h3><a href="#">VS Code 必备插件：Local History 的安装与高效使用</a></h3>
        </div>
    </div>
    
    <div class="timeline-item">
        <div class="timeline-meta">
            <span class="md-ellipsis">2025年<br>05月</span>
        </div>
        <div class="timeline-content">
            <h3><a href="#">Markdown 进阶语法：数学公式与图表的高效整合</a></h3>
        </div>
    </div>
    
    </div>