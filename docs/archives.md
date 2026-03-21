# 📂 归档 (Archives)

<style>
/* ========================================================================
   终极解决方案：专业、简约的时间树归档样式
   ======================================================================== */

/* 1. 整体容器：设定总宽度和左右边距 */
.timeline-container {
    position: relative;
    max-width: 900px;
    margin: 3rem auto;
    padding: 0 1rem;
}

/* 2. 最核心：绘制贯穿整个页面的左侧垂直时间线 */
.timeline-container::after {
    content: '';
    position: absolute;
    width: 2px;
    background-color: #e0e0e0; /* 时间线颜色：简约的灰色 */
    top: 0;
    bottom: 0;
    left: 110px; /* 设定时间线从左侧缩进的距离 */
    margin-left: -1px;
    z-index: 0;
}

/* 3. 时间树单条项目容器 */
.timeline-item {
    position: relative;
    margin-bottom: 2.5rem; /* 单条项目之间的间距 */
    width: 100%;
}

/* 4. 左侧的日期：绝对定位在时间线的左侧 */
.timeline-meta {
    position: absolute;
    left: 0;
    top: 15px;
    width: 100px;
    text-align: right;
    font-size: 0.9rem;
    color: #888;
    font-weight: 500;
}

/* 5. 最关键：破除单行限制，允许日期文字自然换行（防止日期过长撑破布局） */
.timeline-meta .md-ellipsis {
    white-space: normal !important;
    word-break: break-word !important;
    display: block !important;
}

/* 6. 时间线上的“圆点”锚点 */
.timeline-item::after {
    content: '';
    position: absolute;
    width: 16px;
    height: 16px;
    border-radius: 50%;
    background-color: #fff;
    border: 3px solid #e0e0e0; /* 默认灰色边框 */
    top: 15px;
    left: 110px; /* 对齐垂直时间线 */
    margin-left: -8px;
    z-index: 1;
    transition: all 0.3s ease;
}

/* 7. 悬停效果：鼠标划过整个项目时，圆点变蓝 */
.timeline-item:hover::after {
    border-color: #42a5f5; /* 蓝色边框 */
    background-color: #e3f2fd; /* 蓝色淡化背景 */
}

/* 8. 右侧的内容卡片：设定在圆点和线之后 */
.timeline-content {
    position: relative;
    left: 110px; /* 移到线和日期的右侧 */
    width: calc(100% - 130px); /* 占据剩余宽度 */
    padding: 1.2rem 1.8rem;
    background-color: #fff;
    border-radius: 6px;
    border: 1px solid #eee;
    transition: transform 0.2s, box-shadow 0.2s;
}

/* 9. 悬停效果：卡片稍微上浮并增加发光阴影 */
.timeline-item:hover .timeline-content {
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.05);
    border-color: #42a5f5;
}

/* 10. 卡片内的标题样式 */
.timeline-item .timeline-content h3 {
    margin: 0 0 0.5rem 0;
    font-size: 1.2rem;
    font-weight: 700;
    color: #333;
}

/* 11. 卡片内的标题链接：蓝色 + 移除下划线 */
.timeline-item .timeline-content h3 a {
    color: #1976d2 !important;
    text-decoration: none !important;
    transition: color 0.2s;
}
.timeline-item .timeline-content h3 a:hover {
    color: #0d47a1 !important;
}

/* 12. 卡片内的副标题/描述样式 */
.timeline-item .timeline-content p {
    margin: 0;
    font-size: 0.95rem;
    color: #666;
    line-height: 1.6;
}
</style>

<div class="timeline-container">
    
    <div class="timeline-item">
        <div class="timeline-meta">
            <span class="md-ellipsis">2025年<br>12月20日</span>
        </div>
        <div class="timeline-content">
            <h3><a href="20251220_30_gpt/">白嫖 ChatGPT Plus 教程：30秒极速注册方法</a></h3>
            <p>视频的深度文字总结，包含详细的注册步骤、工具推荐和常见问题排查。</p>
        </div>
    </div>

    <div class="timeline-item">
        <div class="timeline-meta">
            <span class="md-ellipsis">2025年<br>11月</span>
        </div>
        <div class="timeline-content">
            <h3><a href="#">如何用 Cursor 打造 AI 工作流：新手指南</a></h3>
            <p>从零开始，手把手教你搭建一套优雅、高效的数字宇宙探索工具。</p>
        </div>
    </div>
    
    <div class="timeline-item">
        <div class="timeline-meta">
            <span class="md-ellipsis">2025年<br>10月</span>
        </div>
        <div class="timeline-content">
            <h3><a href="#">我的第一篇归档文章：Markdown 基础</a></h3>
            <p>优雅地探索数字世界！点击查阅查阅教程！</p>
        </div>
    </div>

    </div>