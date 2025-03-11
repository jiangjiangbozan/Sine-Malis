# Sine Malis - A Classical Blogging System  
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)  

> "The Odes serve to stimulate the mind. They may be used for purposes of self-contemplation. They teach the art of sociability. They show how to regulate feelings of resentment."  
> ― *Confucius* on *The Book of Odes* (Shi Jing), from which our name "思无邪" originates  


## 🌿 Project Etymology  
**中文名「思无邪」**（*sī wú xié*）  
> 孔子评《诗经》：「诗三百，一言以蔽之，曰思无邪」（《论语·为政》）  
> *（思想无杂念，心归纯粹）*  

**拉丁名 *Sine Malis***（*Without Evils*）  
> "The soul becomes dyed with the color of its thoughts."  
> ― *Marcus Aurelius*, *Meditations* V.16  
> *（灵魂浸染于所思，故去恶存真）*  


## 📜 Core Features  
### 🏛️ 古典排版系统  
- ✝️ **古腾堡首字母**：每个章节以1455年圣经同款`&nbsp;❦︎`浮雕字母开头（CSS伪元素实现）  
- 📜 **碑铭段落**：罗马石刻风格的`letter-spacing: 0.08em`，模仿青铜铭文的呼吸感  
- 💬 **苏格拉底评论**：嵌套式对话线程（`@回复`语法），支持`> 引用> 深层引用`的辩证结构  

### 📚 典籍化架构  
- 🪑 **卷轴时间轴**：基于`transform: rotate(-2deg)`的羊皮卷展开动画，按`YYYY-MM`归档  
- 📜 **羊皮纸档案**：`background: repeating-linear-gradient`模拟手工纸纤维，`box-shadow`实现做旧卷边  


## 🧩 Philosophical Implementation  
> "Ut pictura poesis" (诗画同源)  
> ― *Horace*, *Ars Poetica*  

| 技术实践               | 古典哲学映射               | 具体实现细节                     |  
|------------------------|--------------------------|------------------------------|  
| **语义化HTML5**        | 西塞罗修辞五艺（Inventio, Dispositio） | 严格使用`<article>`（文章）、`<aside>`（笺注）、`<q>`（直接引语） |  
| **CSS变量系统**        | 亚里士多德四因说（形式因）   | 定义`--golden-ratio: 1.618`、`--parchment-brown: #d2b48c`等32个变量 |  
| **无框架JavaScript**     | 卢克莱修《物性论》原子说     | 仅用`IntersectionObserver`实现懒加载，总代码量<500行（gzip后28KB） |  
| **印刷级CSS**          | 维特鲁威《建筑十书》比例论   | `line-height: 1.5`（黄金分割行高），`hyphens: auto`（西塞罗式断字） |  


## 📜 代码哲学  
> *"Typography is the craft of endowing human language with a durable visual form."*  
> ― *Beatrice Warde*, *The Crystal Goblet*  

```css
/* 典型段落样式（模仿15世纪抄本） */
p {
  text-indent: 2em; /* 悬挂缩进（古罗马誊写传统） */
  margin-block: 1.5em; /* 两倍行高留白（符合Quattrocento书籍标准） */
  letter-spacing: 0.05ch; /* 活字印刷的字符间距 */
  quotes: '“' '”' '‘' '’'; /* 中文引号优先 */
  /* 暗藏《诗经》叠字彩蛋 */
  &:nth-child(3)::before { content: '呦呦'; color: #666; font-size: 0.8em; }
}
```

## 🛠️ 技术栈

📜 标记语言：HTML5 + Microdata（符合Schema.org/Article规范）  
🎨 样式方案：PostCSS + CSS Modules（含20+古籍纹样变量）  
⚡ 交互逻辑：Vanilla JS（无框架） + Web Workers（评论实时预览）  
📚 构建工具：Rollup（Tree Shaking后<150KB，支持IE11+）  

## 📄 License

MIT License

Copyright (c) 2025 Sullivan <sullivan@example.com>

Permission is hereby granted... (完整文本见LICENSE)

特别声明：  
- 保留「思无邪」「Sine Malis」名称的文化溯源声明  
- 商业使用需包含《诗经》与《沉思录》的引用标注  
- 代码修改需保留注释中的古典哲学引用（如// 维吉尔·农事诗III.284）

  
## 🛠️ Installation  
*（遵循赫拉克利特「万物皆流」的克隆哲学）*  
```bash
# 以流动的方式克隆（含完整修订历史）
git clone https://github.com/yourname/sine-malis.git
cd sine-malis

```

（苏格拉底问答式依赖安装）

```bash
# 交互式安装（自动过滤冗余依赖）
npm install --dialectic  # 询问："这个包真的必要吗？—— 苏格拉底"
```

（荷马史诗模式启动）

```bash

# 加载所有寓言路由与诗性日志
npm run start -- --epic  # 日志前缀："Ὠς δ᾽ ἐπὶ σταυροῦ..."（《奥德赛》开头）

```

## 🖋️ Contribute

*（文艺复兴式协作指南）*

1.复刻雅典学院
```bash
git fork  # 在翡冷翠创建你的思想工坊
```

2.分支命名的艺术
以amphora/（希腊双耳瓶）开头，如：
```bash
git checkout -b amphora/comment-threading  # 修复苏格拉底式评论嵌套
```

3.诗意的提交信息
遵循贺拉斯《诗艺》格律：
```bash
git commit -m "fix(scroll): 修正羊皮卷时间轴的维吉尔式断行 📜#《埃涅阿斯纪》VI.847"
```

4.在阿波罗之光中提交
```bash
git push origin amphora/comment-threading
```

5.打开 PR 时，请引用古典文献：

  「吾爱吾师，吾更爱真理」—— 亚里士多德《尼各马可伦理学》
