<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nano Banana - Google最新AI图像模型，会听话的设计师</title>
    <style>
        :root {
            --primary-color: #4285f4;
            --secondary-color: #34a853;
            --text-dark: #202124;
            --text-light: #5f6368;
            --bg-light: #f8f9fa;
            --border-color: #dadce0;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            margin: 0;
            padding: 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 100px 0;
            text-align: center;
        }

        .hero h1 {
            font-size: 3em;
            margin-bottom: 20px;
            font-weight: 700;
        }

        .hero .subtitle {
            font-size: 1.3em;
            max-width: 700px;
            margin: 0 auto 40px;
            opacity: 0.95;
        }

        .cta-button {
            display: inline-block;
            background: white;
            color: var(--primary-color);
            padding: 15px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1em;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(0,0,0,0.25);
        }

        .features {
            padding: 80px 0;
            background: var(--bg-light);
        }

        .features h2 {
            text-align: center;
            font-size: 2.5em;
            margin-bottom: 60px;
            color: var(--text-dark);
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
            margin-bottom: 60px;
        }

        .feature-card {
            background: white;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
        }

        .feature-card h3 {
            color: var(--primary-color);
            font-size: 1.5em;
            margin-bottom: 20px;
        }

        .feature-card .icon {
            font-size: 3em;
            margin-bottom: 20px;
        }

        .version-comparison {
            background: white;
            padding: 80px 0;
        }

        .comparison-table {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .version-card {
            padding: 30px;
            border-radius: 12px;
            border: 2px solid var(--border-color);
            transition: all 0.3s ease;
        }

        .version-card:hover {
            border-color: var(--primary-color);
            box-shadow: 0 4px 15px rgba(66, 133, 244, 0.1);
        }

        .version-card h4 {
            font-size: 1.3em;
            margin-bottom: 15px;
        }

        .version-card ul {
            list-style: none;
            padding: 0;
        }

        .version-card ul li {
            padding: 8px 0;
            position: relative;
            padding-left: 25px;
        }

        .version-card ul li:before {
            content: "✓";
            position: absolute;
            left: 0;
            color: var(--secondary-color);
            font-weight: bold;
        }

        .scenarios {
            padding: 80px 0;
            background: var(--bg-light);
        }

        .scenario-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .scenario-card {
            background: white;
            padding: 30px;
            border-radius: 12px;
            text-align: center;
        }

        .scenario-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 20px;
        }

        .how-to-use {
            padding: 80px 0;
            background: white;
        }

        .steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .step {
            text-align: center;
            padding: 30px;
        }

        .step .step-number {
            width: 60px;
            height: 60px;
            background: var(--primary-color);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5em;
            font-weight: bold;
            margin: 0 auto 20px;
        }

        .templates {
            background: #f0f7ff;
            padding: 30px;
            border-radius: 12px;
            margin-top: 40px;
        }

        .template-code {
            background: #e8f0fe;
            padding: 20px;
            border-radius: 8px;
            margin: 15px 0;
            font-family: monospace;
            border-left: 4px solid var(--primary-color);
        }

        .testimonials {
            padding: 80px 0;
            background: var(--bg-light);
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .testimonial-card {
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .testimonial-card .quote {
            font-size: 1.1em;
            font-style: italic;
            margin-bottom: 20px;
            color: var(--text-dark);
        }

        .testimonial-card .author {
            font-weight: 600;
            color: var(--text-light);
        }

        .testimonial-card .source {
            font-size: 0.9em;
            color: var(--primary-color);
        }

        .faq {
            padding: 80px 0;
            background: white;
        }

        .faq-item {
            margin-bottom: 30px;
            padding: 25px;
            background: var(--bg-light);
            border-radius: 12px;
        }

        .faq-item h3 {
            color: var(--primary-color);
            margin-bottom: 15px;
            font-size: 1.2em;
        }

        .videos {
            padding: 80px 0;
            background: var(--bg-light);
        }

        .video-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .video-card {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .video-card:hover {
            transform: translateY(-5px);
        }

        .video-card h4 {
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .video-card .description {
            color: var(--text-light);
            margin-bottom: 20px;
            font-size: 0.95em;
        }

        .video-link {
            display: inline-block;
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease;
        }

        .video-link:hover {
            color: #3367d6;
            text-decoration: underline;
        }

        .footer {
            background: var(--text-dark);
            color: white;
            padding: 50px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 30px;
        }

        .footer-section h4 {
            margin-bottom: 20px;
            font-size: 1.1em;
        }

        .footer-section ul {
            list-style: none;
            padding: 0;
        }

        .footer-section ul li {
            margin-bottom: 10px;
        }

        .footer-section a {
            color: #9aa0a6;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section a:hover {
            color: white;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #5f6368;
            color: #9aa0a6;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2em;
            }

            .hero .subtitle {
                font-size: 1.1em;
            }

            .feature-grid {
                grid-template-columns: 1fr;
            }

            .steps {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Nano Banana - 会听话的AI设计师</h1>
            <p class="subtitle">Google最新AI图像模型，不仅能理解复杂指令，还能保持角色一致性、生成精准文字，像聊天一样轻松修图</p>
            <a href="https://gemini.google.com" class="cta-button">立即免费体验</a>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features">
        <div class="container">
            <h2>三大突破性功能，重新定义AI绘图</h2>

            <div class="feature-grid">
                <!-- Feature 1 -->
                <div class="feature-card">
                    <div class="icon">🎭</div>
                    <h3>角色一致性</h3>
                    <p><strong>告别"换脸"困扰</strong> - 传统AI绘图的最大痛点是换个场景角色就变脸。Nano Banana能够在一系列不同的画面中保持同一个人物或物体的外观特征不变。</p>
                    <br>
                    <p><strong>实际应用：</strong></p>
                    <ul>
                        <li>连环画创作 - 主角不会"变脸"</li>
                        <li>品牌IP设计 - 保持视觉统一</li>
                        <li>故事分镜制作 - 连续剧情创作</li>
                    </ul>
                </div>

                <!-- Feature 2 -->
                <div class="feature-card">
                    <div class="icon">💬</div>
                    <h3>自然语言编辑</h3>
                    <p><strong>零门槛修图</strong> - 不需要复杂的修图技巧，直接用自然语言对话来修改图片。就像和设计师聊天一样简单。</p>
                    <br>
                    <p><strong>示例指令：</strong></p>
                    <ul>
                        <li>"把背景换成海滩"</li>
                        <li>"给人物戴上一顶帽子"</li>
                        <li>"把这件白衬衫换成格子衫"</li>
                    </ul>
                </div>

                <!-- Feature 3 -->
                <div class="feature-card">
                    <div class="icon">✏️</div>
                    <h3>精准文字渲染</h3>
                    <p><strong>告别乱码时代</strong> - 在生成带有文字的图片（如海报、Logo）时，能够生成清晰、准确的拼写，减少了以往AI生成乱码的情况。</p>
                    <br>
                    <p><strong>文字准确性提升：</strong></p>
                    <ul>
                        <li>拼写错误率 &lt; 1%</li>
                        <li>支持多语言文字生成</li>
                        <li>适合商业设计和logo创作</li>
                    </ul>
                </div>
            </div>

            <!-- Additional Features -->
            <div class="feature-grid">
                <!-- Feature 4 -->
                <div class="feature-card">
                    <div class="icon">🖼️</div>
                    <h3>多图融合</h3>
                    <p>可以将两张或多张图片的内容自然地融合在一起，创造全新的视觉效果。上传两张照片，让AI帮你融合产生意想不到的创意。</p>
                </div>

                <!-- Feature 5 -->
                <div class="feature-card">
                    <div class="icon">⚡</div>
                    <h3>极速响应</h3>
                    <p>Gemini 2.5 Flash Image版本主打速度和效率，适合快速生成和日常娱乐使用。响应速度业界领先，创作灵感无需等待。</p>
                </div>

                <!-- Feature 6 -->
                <div class="feature-card">
                    <div class="icon">🧠</div>
                    <h3>强大推理</h3>
                    <p>Gemini 3.0 Pro Image具备更强的逻辑推理能力和世界知识，适合生成复杂的图表、设计稿以及需要高精度的商业用途。</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Version Comparison -->
    <section class="version-comparison">
        <div class="container">
            <h2>选择适合你的版本</h2>

            <div class="comparison-table">
                <!-- Standard Version -->
                <div class="version-card">
                    <h4>🚀 Gemini 2.5 Flash Image</h4>
                    <p style="font-weight: 600; color: var(--secondary-color); margin-bottom: 20px;">标准版 - 快速高效</p>
                    <ul>
                        <li>速度优先，响应极快</li>
                        <li>适合日常创作使用</li>
                        <li>免费版用户可用</li>
                        <li>2025年8月发布</li>
                        <li>基础图像编辑功能</li>
                        <li>文字渲染准确率高</li>
                    </ul>
                </div>

                <!-- Pro Version -->
                <div class="version-card" style="border-color: var(--primary-color);">
                    <h4>⭐ Gemini 3.0 Pro Image</h4>
                    <p style="font-weight: 600; color: var(--primary-color); margin-bottom: 20px;">专业版 - 高质量输出</p>
                    <ul>
                        <li>画质更高，细节更丰富</li>
                        <li>专业级控制能力</li>
                        <li>需要订阅 Gemini Advanced</li>
                        <li>2025年11月发布</li>
                        <li>强大逻辑推理能力</li>
                        <li>适合商业用途</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Use Scenarios -->
    <section class="scenarios">
        <div class="container">
            <h2>看看Nano Banana能为你做什么</h2>

            <div class="scenario-grid">
                <!-- Creative Workers -->
                <div class="scenario-card">
                    <h3>🎨 创意工作者</h3>
                    <p style="font-size: 0.95em; margin-bottom: 20px;">为创意专业人士打造的效率工具</p>
                    <ul style="text-align: left;">
                        <li><strong>设计师：</strong>快速生成设计稿、Logo创意</li>
                        <li><strong>内容创作者：</strong>制作连环画、表情包</li>
                        <li><strong>营销人员：</strong>制作海报、社交媒体素材</li>
                    </ul>
                </div>

                <!-- Regular Users -->
                <div class="scenario-card">
                    <h3>👥 普通用户</h3>
                    <p style="font-size: 0.95em; margin-bottom: 20px;">人人都能用上的创意助手</p>
                    <ul style="text-align: left;">
                        <li>个性化头像生成</li>
                        <li>室内设计预览</li>
                        <li>创意礼物定制</li>
                        <li>社交媒体内容创作</li>
                    </ul>
                </div>

                <!-- Enterprise -->
                <div class="scenario-card">
                    <h3>🏢 企业应用</h3>
                    <p style="font-size: 0.95em; margin-bottom: 20px;">提升团队设计效率</p>
                    <ul style="text-align: left;">
                        <li>产品原型设计</li>
                        <li>品牌视觉统一</li>
                        <li>培训材料制作</li>
                        <li>快速概念验证</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- How to Use -->
    <section class="how-to-use">
        <div class="container">
            <h2>三步开始使用Nano Banana</h2>

            <div class="steps">
                <!-- Step 1 -->
                <div class="step">
                    <div class="step-number">1</div>
                    <h3>访问 Gemini</h3>
                    <p>打开 <a href="https://gemini.google.com" style="color: var(--primary-color);">gemini.google.com</a> 或下载 Google Gemini App</p>
                </div>

                <!-- Step 2 -->
                <div class="step">
                    <div class="step-number">2</div>
                    <h3>输入指令</h3>
                    <p>直接发送绘图指令，系统自动调用最新模型</p>
                </div>

                <!-- Step 3 -->
                <div class="step">
                    <div class="step-number">3</div>
                    <h3>对话调整</h3>
                    <p>在同一个对话窗口中继续修改和优化</p>
                </div>
            </div>

            <!-- Templates -->
            <div class="templates">
                <h3>📝 实用提示词模板</h3>

                <h4 style="margin-top: 30px;">角色设定模板</h4>
                <div class="template-code">
                    生成一个[年龄]岁的[性别]，穿着[服装描述]，戴着[配饰描述]，[风格]风格<br>
                    <small>示例：生成一个穿着红色连帽衫、戴着眼镜的卡通小男孩，背着一个蓝色书包，皮克斯风格</small>
                </div>

                <h4 style="margin-top: 25px;">场景切换模板</h4>
                <div class="template-code">
                    保持这个角色的形象不变，让他/她现在在[地点]，正在做[动作]<br>
                    <small>示例：保持同一个小男孩的角色形象不变，让他现在在图书馆里看书</small>
                </div>

                <h4 style="margin-top: 25px;">文字设计模板</h4>
                <div class="template-code">
                    生成一个[物体类型]，上面写着"[文字内容]"，[风格]风格<br>
                    <small>示例：生成一个霓虹灯招牌，上面写着 "OPEN 24 HOURS"，赛博朋克风格</small>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials">
        <div class="container">
            <h2>用户怎么说</h2>

            <div class="testimonial-grid">
                <!-- Testimonial 1 -->
                <div class="testimonial-card">
                    <p class="quote">"终于能写对字了！以前AI生成海报文字总是乱码，但Nano Banana生成的招牌、Logo文字非常清晰且拼写准确。"</p>
                    <p class="author">— @AI_Creator_2025</p>
                    <p class="source">来源：X/Twitter</p>
                </div>

                <!-- Testimonial 2 -->
                <div class="testimonial-card">
                    <p class="quote">"角色一致性是游戏规则改变者。我可以画连环画了，因为主角不会换个场景就换张脸。Nano Banana解决了AI绘图最大的痛点！"</p>
                    <p class="author">— @ComicArtist_Pro</p>
                    <p class="source">来源：Reddit</p>
                </div>

                <!-- Testimonial 3 -->
                <div class="testimonial-card">
                    <p class="quote">"像聊天一样P图，把Photoshop的门槛降到了零。上传一张自拍，直接发指令'把我手里的水瓶换成红酒，背景换成巴黎'，效果太惊艳了！"</p>
                    <p class="author">— @Design_Lover</p>
                    <p class="source">来源：X/Twitter</p>
                </div>

                <!-- Testimonial 4 -->
                <div class="testimonial-card">
                    <p class="quote">"Nano Banana是市面上最'聪明'的绘图模型，听得懂人话、能写字、能修图。不过也是'最保守'的，很多东西不让画。"</p>
                    <p class="author">— @Tech_Reviewer</p>
                    <p class="source">来源：技术论坛</p>
                </div>

                <!-- Testimonial 5 -->
                <div class="testimonial-card">
                    <p class="quote">"对比Midjourney：Nano Banana强在理解和功能性，Midjourney强在艺术感。如果你追求'按我的要求把活干完'，Nano Banana更好用。"</p>
                    <p class="author">— @Creative_Director</p>
                    <p class="source">来源：设计师社区</p>
                </div>

                <!-- Testimonial 6 -->
                <div class="testimonial-card">
                    <p class="quote">"它的画质是顶级的，但拒绝率也是顶级的。不过一旦你掌握了正确的提示词技巧，创作效率提升巨大！"</p>
                    <p class="author">— @Power_User</p>
                    <p class="source">来源：AI竞技场</p>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ Section -->
    <section class="faq">
        <div class="container">
            <h2>常见问题解答</h2>

            <!-- FAQ 1 -->
            <div class="faq-item">
                <h3>Q: 在哪里可以下载 "Nano Banana" App？</h3>
                <p><strong>A:</strong> 没有独立的App。Nano Banana是Google模型的研发代号，它已经集成在了<strong>Google Gemini</strong>的网页版和手机App中。你只需要使用Gemini，就是在享用它的技术。</p>
            </div>

            <!-- FAQ 2 -->
            <div class="faq-item">
                <h3>Q: 为什么叫 "Nano Banana" 这么奇怪的名字？</h3>
                <p><strong>A:</strong> 这是为了在<strong>LMArena</strong>（一个AI模型竞技场）进行盲测时使用的匿名代号。目的是为了防止评测者因为知道是Google的产品而产生偏见。结果它在盲测中击败了众多对手，这个名字也就火了。</p>
            </div>

            <!-- FAQ 3 -->
            <div class="faq-item">
                <h3>Q: 它是免费的吗？</h3>
                <p><strong>A:</strong> 大部分功能免费。</p>
                <ul>
                    <li><strong>Gemini 2.5 Flash Image</strong>（速度快、标准版）：通常对Gemini免费版用户开放</li>
                    <li><strong>Gemini 3.0 Pro Image</strong>（画质更高、推理更强）：通常需要订阅<strong>Gemini Advanced</strong>会员才能无限制使用最高质量版本</li>
                </ul>
            </div>

            <!-- FAQ 4 -->
            <div class="faq-item">
                <h3>Q: 怎么让AI保持人物长相不变（角色一致性）？</h3>
                <p><strong>A:</strong> 不需要复杂的代码。</p>
                <ol>
                    <li>先生成一张满意的人物图</li>
                    <li>在<strong>同一个对话窗口</strong>中继续输入："保持这个角色的形象，让他/她去海边散步"</li>
                    <li><strong>技巧：</strong>给角色起个名字（例如"生成一个叫Tom的男孩..."），后续对话中直接用名字指代，效果往往更好</li>
                </ol>
            </div>

            <!-- FAQ 5 -->
            <div class="faq-item">
                <h3>Q: 它可以生成带文字的图片吗？</h3>
                <p><strong>A:</strong> 可以，且表现很强。在提示词中明确指出文字内容，建议用引号括起来。例如："生成一个咖啡店招牌，上面写着<strong>'Fresh Coffee'</strong>"。Nano Banana是目前拼写错误率最低的模型之一。</p>
            </div>

            <!-- FAQ 6 -->
            <div class="faq-item">
                <h3>Q: 我可以上传自己的照片让它修改吗？</h3>
                <p><strong>A:</strong> 可以。你可以上传一张照片，然后发送指令："把背景换成雪山"或"把衣服换成红色的"。但请注意，处于隐私保护，它通常<strong>拒绝处理真人的面部识别</strong>（即不能把名人的脸换到你的照片上，也不能深度伪造）。</p>
            </div>

            <!-- FAQ 7 -->
            <div class="faq-item">
                <h3>Q: 为什么它总是拒绝生成我的图片？(Refusals)</h3>
                <p><strong>A:</strong> 这是Nano Banana被吐槽最多的点。Google的<strong>安全过滤器(Safety Filter)</strong>非常严格。</p>
                <p><strong>常见拒绝原因：</strong></p>
                <ul>
                    <li><strong>版权保护：</strong>即使你没提，如果提示词描述的角色太像马里奥或米老鼠，它可能会拒绝</li>
                    <li><strong>真人/公众人物：</strong>涉及真实政治家、明星的生成通常会被拦截</li>
                    <li><strong>NSFW/暴力：</strong>任何擦边球、暴力、血腥内容都会直接触发封锁</li>
                    <li><strong>特定历史场景：</strong>为了避免偏见争议，某些特定种族或历史敏感场景会被"一刀切"地拒绝</li>
                </ul>
            </div>

            <!-- FAQ 8 -->
            <div class="faq-item">
                <h3>Q: 生成的图片有水印吗？可以商用吗？</h3>
                <p><strong>A:</strong></p>
                <ul>
                    <li><strong>水印：</strong>图片像素里嵌入了<strong>SynthID</strong>（人眼不可见的水印），用来标识这是AI生成的图片，防止深度伪造欺诈</li>
                    <li><strong>商用：</strong>根据Google的服务条款，付费版（Gemini Advanced / Enterprise）生成的内容通常拥有商业使用权，但免费版的条款可能会有所变动，建议查看最新的Google Generative AI使用条款</li>
                </ul>
            </div>

            <!-- FAQ 9 -->
            <div class="faq-item">
                <h3>Q: 和Midjourney相比，它差在哪？</h3>
                <p><strong>A:</strong></p>
                <ul>
                    <li><strong>Nano Banana强在：</strong>听得懂复杂指令、能写对字、修改图片方便、速度快</li>
                    <li><strong>Midjourney强在：</strong>艺术感、光影质感、创意构图</li>
                    <li><strong>建议：</strong>如果你追求"像艺术馆里的画"，Midjourney依然是王者；如果你追求"按我的要求把活干完"，Nano Banana更好用</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Video Resources -->
    <section class="videos">
        <div class="container">
            <h2>视频教程与演示</h2>
            <p style="text-align: center; color: var(--text-light); margin-bottom: 40px;">这些视频大多是英文解说，您可以开启YouTube的"自动翻译字幕"功能（设置→字幕→自动翻译→中文）</p>

            <div class="video-grid">
                <!-- Video 1 -->
                <div class="video-card">
                    <h4>🔰 新手入门：Nano Banana Pro上手体验</h4>
                    <p class="description">展示Gemini 3.0 Pro Image的核心功能，从简单的文生图到复杂的图像编辑流程，适合第一次接触该模型的人。</p>
                    <a href="https://www.youtube.com/watch?v=hk6gwiZmSWA" target="_blank" class="video-link">▶️ 观看视频</a>
                </div>

                <!-- Video 2 -->
                <div class="video-card">
                    <h4>💡 20个创意用法演示</h4>
                    <p class="description">展示20种脑洞大开的创意用法。不仅仅是画图，还包括了做PPT素材、产品模型、甚至辅助设计等实用场景。</p>
                    <a href="https://www.youtube.com/watch?v=-tMERzjAvgw" target="_blank" class="video-link">▶️ 观看视频</a>
                </div>

                <!-- Video 3 -->
                <div class="video-card">
                    <h4>🎨 角色一致性深度教程</h4>
                    <p class="description">专注于解决AI绘图最大的痛点——角色一致性。详细演示如何让同一个角色在不同场景中保持长相、衣服不变。</p>
                    <a href="https://www.youtube.com/watch?v=JNJt1OjpX0Y" target="_blank" class="video-link">▶️ 观看视频</a>
                </div>

                <!-- Video 4 -->
                <div class="video-card">
                    <h4>📚 27个案例深度教程</h4>
                    <p class="description">非常硬核的全面教程，包含了27个测试案例。博主将它与开源模型进行了详细对比，演示具体编辑操作。</p>
                    <a href="https://www.youtube.com/watch?v=qPUreQxB8zQ" target="_blank" class="video-link">▶️ 观看视频</a>
                </div>

                <!-- Video 5 -->
                <div class="video-card">
                    <h4>✍️ 文字渲染与平面设计</h4>
                    <p class="description">重点展示Text Rendering能力。演示了如何生成带有清晰、拼写正确文字的Logo和海报，证明商业设计潜力。</p>
                    <a href="https://www.youtube.com/watch?v=WA_VI0kgkXM" target="_blank" class="video-link">▶️ 观看视频</a>
                </div>

                <!-- Video 6 -->
                <div class="video-card">
                    <h4>🔥 5个隐藏功能揭秘</h4>
                    <p class="description">挖掘了一些隐藏的高级功能。比如如何调整宽高比、如何生成信息图表等，帮你发挥Nano Banana的全部潜力。</p>
                    <a href="https://www.youtube.com/watch?v=yLtgwE0_S-Q" target="_blank" class="video-link">▶️ 观看视频</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <!-- About -->
                <div class="footer-section">
                    <h4>关于Nano Banana</h4>
                    <p style="color: #9aa0a6; font-size: 0.95em;">Google DeepMind开发的最新AI图像生成模型，正式名称为Gemini Image系列。Nano Banana是其在LMArena盲测时使用的代号，因表现优异而广为人知。</p>
                </div>

                <!-- Quick Links -->
                <div class="footer-section">
                    <h4>快速链接</h4>
                    <ul>
                        <li><a href="https://gemini.google.com" target="_blank">开始使用</a></li>
                        <li><a href="https://aistudio.google.com" target="_blank">Google AI Studio</a></li>
                        <li><a href="#" target="_blank">开发者文档</a></li>
                        <li><a href="#" target="_blank">更新日志</a></li>
                    </ul>
                </div>

                <!-- Resources -->
                <div class="footer-section">
                    <h4>学习资源</h4>
                    <ul>
                        <li><a href="#" target="_blank">提示词指南</a></li>
                        <li><a href="#" target="_blank">最佳实践</a></li>
                        <li><a href="#" target="_blank">社区论坛</a></li>
                        <li><a href="#" target="_blank">案例展示</a></li>
                    </ul>
                </div>

                <!-- Legal -->
                <div class="footer-section">
                    <h4>法律信息</h4>
                    <ul>
                        <li><a href="#" target="_blank">隐私政策</a></li>
                        <li><a href="#" target="_blank">服务条款</a></li>
                        <li><a href="#" target="_blank">使用指南</a></li>
                        <li><a href="#" target="_blank">安全中心</a></li>
                    </ul>
                </div>
            </div>

            <div class="footer-bottom">
                <p>&copy; 2025 Google DeepMind. Nano Banana是Gemini Image系列的社区昵称。</p>
                <p style="margin-top: 10px; font-size: 0.9em;">最后更新：2025年12月</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Add animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all cards and sections
        document.querySelectorAll('.feature-card, .version-card, .scenario-card, .testimonial-card, .video-card').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
            observer.observe(el);
        });
    </script>
</body>
</html>