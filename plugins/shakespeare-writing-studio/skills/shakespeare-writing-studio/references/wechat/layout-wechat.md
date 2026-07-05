# Layout Guidelines / 排版规范(核心)——Word 主交付 + HTML 备份 + QA + 发布说明

This document defines the Word-first layout system, HTML backup, QA flow, and release-note template. Read `wechat-layout-patterns.md` first; this file turns those patterns into concrete Word and HTML settings.

## 一、docx Word-first 排版规范(主交付)
目标:主编打开 Word 看到的就是成品版面;全选粘贴进公众号编辑器后所见即所得。
骨架与助手函数:`scripts/docx_scaffold.js`(R 正文 / B 金句 / A 强调色 / body / secNo /
secTitle / caption / img / quote / divider / makeDoc)。

### 页面与节奏
- A4;页边距 上下 1134 / 左右 1418 DXA(内容宽 16cm,图宽恒为 605px@96dpi)。
- 全文统一 Microsoft YaHei;正文 11pt #333333,行距 line 380,段后 after 260——
  这是阅读稳定性的底盘:**全文只允许这一种正文段样式**,不得混入第二种行距或字号。
- 章节间呼吸:章节编号段 before 480;大图前 before 120、图注后 after 340。
- 大节之间可用 divider(居中「· · ·」,#CCCCCC,before/after 300)最多 2 处。

### 手机阅读流
- 执行前先对照 `wechat-layout-patterns.md` 判断文章属于报道型、拆解型、访谈/人物型或产品/技术型。
- 每段正文 1–3 句,理想长度 38–90 个汉字;超过 120 个汉字必须拆段。
- 连续纯文字不超过 6 段;若超过,插入小标题、引语、图、分隔符或短段转场。
- 连续短句不超过 5 段;短句过密会显得像 AI 断行,用一段解释性长句缓冲。
- 每节开头先给读者一个"为什么读这一节"的入口,再展开材料。
- 每张图前至少有一段铺垫,图后至少有一句收束;图片不能突然出现。
- 首屏目标:标题 + 头图 + 1–2 段冷开场;不要把摘要、目录、作者介绍塞进首屏。

### 层级(自上而下唯一路径)
| 层级 | 样式 |
|---|---|
| 文首大标题 | 16pt(32) bold #111111,line 440,after 360——粘贴时填入公众号标题栏 |
| 蓝色副题行(可选) | 11pt #2A6DF4,after 340 |
| 章节编号 01… | 11pt bold **#2A6DF4** |
| 章节标题 | 14pt(28) bold #111111,after 280 |
| 正文 | 11pt #333333(唯一正文样式) |
| 金句 | 同字号 bold #111111,每节 ≤2 处 |
| 强调色数据 | A():同字号 bold #2A6DF4,全文 ≤4 处,只给关键数字/机制词 |
| 引语块 | 段落底纹 #F7F7F7 + 左边框 3.5pt #D8D8D8(size 28, space 14),缩进左右 280;正文 10.5pt #555,署名 9.5pt #999 |
| 图注 | 9pt #999999 居中,『品牌 · 描述』;网图需署名的写『图:作者 / 平台』 |
| 关于栏 | 9.5pt #888888,段落上边框 0.75pt #EEEEEE space 12,before 400 |

### 图片
- 一律内嵌(ImageRun type:"png"/"jpg"),宽 605px,高按原图比例换算,段落居中;
- 头图紧随大标题;信息图紧随其论证段;两图之间至少隔两段正文;
- 照片 JPEG q85、信息图 PNG;单文件总大小控制在 ≤25MB。
- 图像密度:1000–1600 字文章 2–4 张图;1600–2600 字 4–6 张图;超过 2600 字按章节补图,但连续两屏不能只有图。
- 信息图承担解释或证据功能;氛围图承担首屏、转场或人物/场景感。无明确功能的图删除。
- 图注不写废话:只说明主体、来源、场景或关键判断;不要重复正文小标题。

### 版面自检(排版 QA 清单)
- [ ] 正文只有一种段样式;金句/强调色不超限
- [ ] 图不跨页截断(必要时在图前加空段微调);引语块底纹连续
- [ ] 章节编号连续、颜色一致;divider ≤2
- [ ] 首屏 = 大标题 + 头图 + 冷开场首段,无杂物
- [ ] 手机预览无文字墙:连续纯文字 ≤6 段,连续短句 ≤5 段
- [ ] 每图都有前置铺垫与后置收束,图注不重复正文

## 二、Word → 公众号粘贴流程(写进发布说明)
1. 打开 docx,首行大标题剪切填入公众号「标题」栏;
2. 从头图起 Ctrl/Cmd+A 全选 → 复制 → 粘贴进公众号编辑器,图片随粘贴自动上传;
3. 逐屏预览:个别图被编辑器压糊 → 用包内高清原图手动替换;
4. 填摘要、选封面(cover 图),群发前手机预览一遍。

## 三、HTML 备份模板(article.html,行内样式)
容器:`max-width:677px;margin:0 auto;` 字体栈 `-apple-system,BlinkMacSystemFont,'PingFang SC','Hiragino Sans GB','Microsoft YaHei',sans-serif`;只用 p/strong/img/div。
```html
<p style="font-size:16px;line-height:2.05;letter-spacing:.5px;margin:0 0 24px;">正文,<strong style="color:#111;">金句加粗</strong>。</p>
<p style="font-size:16px;font-weight:700;color:#2A6DF4;margin:46px 0 4px;">01</p>
<p style="font-size:21px;font-weight:700;color:#111;line-height:1.5;margin:0 0 24px;">章节标题</p>
<div style="background:#F7F7F7;border-left:3px solid #D8D8D8;padding:20px 22px;margin:8px 0 28px;">
  <p style="font-size:15px;line-height:1.95;color:#555;margin:0;">"引语"</p>
  <p style="font-size:13px;color:#999;margin:12px 0 0;">—— 署名,头衔</p></div>
<img src="figX.png" style="width:100%;display:block;border-radius:4px;">
<p style="font-size:12px;color:#999;text-align:center;margin:10px 0 30px;letter-spacing:.5px;">品牌 &nbsp;·&nbsp; 图注</p>
<div style="border:1px dashed #B9C4D6;background:#F7FAFF;border-radius:6px;padding:44px 16px;text-align:center;color:#6B7A93;font-size:13.5px;line-height:1.8;">【 占位:__画面__ · 建议尺寸 __ · 直链见发布说明 】</div>
<div style="border-top:1px solid #EEE;padding-top:20px;"><p style="font-size:13.5px;line-height:1.9;color:#888;margin:0;">关于 XX:……<br>官网</p></div>
```
完成后 `python3 scripts/embed_images.py article_src.html article.html`。

## 四、QA 配方
1. 每图渲染/下载后 view 原图;
2. **docx**:`soffice --headless --convert-to pdf x.docx` → `pdftoppm -jpeg -r 70 x.pdf p`
   → 页图拼 contact sheet → view 全页;
3. HTML:playwright 整页截图(viewport 720 宽)→ 切 2–3 段逐段 view。
4. 手机阅读流:按 390px 宽预览逐屏检查,记录文字墙、图片突兀、标题拥挤、图注过长四类问题并修掉。

## 五、发布说明模板(发布说明.txt)
```
《文章名》发布说明
▍主交付:文章名.docx(打开→标题填标题栏→从头图全选复制→粘贴→发布)
▍主标题:… 备选:A… B… C…
▍摘要(≤120字):…
▍图片清单(正文顺序):文件名 / FIG 编号或画面 / 插入位置
▍图片来源与授权(网图逐张):文件名 / 详情页 URL / 协议 / 是否需署名
▍占位替换(如有):位置 / 画面 / 直链或 AI 绘画提示词
▍口径提示:缓冲表述 / 代拟引语待确认 / 占位数字清单
```

## 六、交付包
```
《文章名》-终稿/
├── 文章名.docx        ← 主交付,呈现列表第一位
├── article.html       ← 等价备选(图已内嵌)
├── cover + figX + 网图(高清原图)
├── 发布说明.txt
└── src/(fig html、构建脚本、render.py)
```
外加同名 zip。
