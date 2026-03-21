<style>
/* 1. 整体容器：入场淡入上浮动画 */
.hero-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 3rem 1rem 5rem 1rem; /* 增加底部 padding */
    text-align: center;
    animation: fadeIn 1.2s ease-out;
}

/* 2. 头像：上下呼吸悬浮动画 */
.hero-avatar {
    width: 130px;
    height: 130px;
    border-radius: 50%;
    margin-bottom: 2rem;
    box-shadow: 0 0 25px rgba(66, 165, 245, 0.3);
    animation: floatAvatar 3s ease-in-out infinite;
    object-fit: cover;
}

/* 3. 主标题（你的频道名）：流光渐变色文字 */
.hero-title {
    font-size: 3rem; /* 加大字号 */
    font-weight: 800;
    margin-bottom: 1rem;
    background: linear-gradient(120deg, #1976d2, #42a5f5, #00d2ff);
    background-size: 200% 200%;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: gradientShift 5s ease infinite;
}

/* 4. 副标题说明文字 */
.hero-subtitle {
    font-size: 1.1rem;
    color: #666;
    margin-bottom: 3.5rem; /* 增加到按钮的距离 */
    max-width: 600px;
    line-height: 1.8;
}

/* 5. 按钮组容器 */
.hero-buttons {
    display: flex;
    gap: 1.5rem; /* 按钮间距 */
    flex-wrap: wrap;
    justify-content: center;
}

/* 6. 按钮通用样式与悬停动画 */
.hero-btn {
    padding: 0.9rem 2.5rem;
    border-radius: 30px;
    font-weight: 600;
    font-size: 1.05rem;
    text-decoration: none !important;
    transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
    display: flex;
    align-items: center;
    gap: 10px; /* 图标和文字间距 */
}

/* 强调按钮（跳转油管）：红色 + 发光 */
.hero-btn-primary {
    background-color: #ff0000; /* YouTube 经典红 */
    color: white !important;
    box-shadow: 0 5px 20px rgba(255, 0, 0, 0.3);
}
.hero-btn-primary:hover {
    background-color: #cc0000;
    transform: translateY(-5px) scale(1.05); /* 向上浮动更多，并稍微放大 */
    box-shadow: 0 8px 30px rgba(255, 0, 0, 0.5); /* 加强阴影 */
}

/* ================= 动画关键帧定义 ================= */
@keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
}

@keyframes floatAvatar {
    0% { transform: translateY(0px) rotate(0deg); }
    50% { transform: translateY(-15px) rotate(2deg); }
    100% { transform: translateY(0px) rotate(0deg); }
}

@keyframes gradientShift {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}
</style>

<div class="hero-container">
    
    <img src="images/my-avatar.jpg" alt="Avatar" class="hero-avatar">
    
    <h1 class="hero-title">科技小V</h1>
    
    <p class="hero-subtitle">
        你的硬核数字伴侣。<br>
        这里不仅有实用的科技教程、工具分享，还有我 YouTube 视频内容的深度文字总结。陪你一起优雅地探索数字世界！
    </p>
    
    <div class="hero-buttons">
        <a href="https://www.youtube.com/@%E7%A7%91%E6%8A%80%E5%B0%8FV" target="_blank" class="hero-btn hero-btn-primary">
            <svg viewBox="0 0 24 24" width="22" height="22" fill="currentColor" style="color: white;"><path d="M21.582,6.186c-0.23-0.86-0.908-1.538-1.768-1.768C18.254,4,12,4,12,4S5.746,4,4.186,4.418c-0.86,0.23-1.538,0.908-1.768,1.768C2,7.746,2,12,2,12s0,4.254,0.418,5.814c0.23,0.86,0.908,1.538,1.768,1.768C5.746,20,12,20,12,20s6.254,0,7.814-0.418c0.86-0.23,1.538-0.908,1.768-1.768C22,16.254,22,12,22,12S22,7.746,21.582,6.186z M9.996,15.005l0-6.01L15.224,12L9.996,15.005z"/></svg>
            观看最新视频
        </a>
    </div>
    
</div>