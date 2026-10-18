# 🏗️ Bean 盖楼记

> **一颗 Bean 一颗 Bean，从地基盖到小区。**
> 零基础 Java 后端学习的第一张地图 —— 10 分钟搞清楚六样东西分别管什么、该按什么顺序学。

![License](https://img.shields.io/badge/license-CC%20BY%204.0-34d399)
![Java](https://img.shields.io/badge/JDK-21-orange)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-6DB33F)
![Format](https://img.shields.io/badge/no%20dependencies-single%20HTML-blue)

```
🟦 JavaSE → 🟩 MySQL+Maven → 🟨 JDBC → 🟪 SSM → 🟦 SpringBoot → 🟥 微服务
   地基        材料仓库       接水管    预制零件    一体化套件      盖成小区
```

### ⚡ 先玩这个（不用装任何东西）

<div align="center">


[ HTML 双击打开](https://zhaoyoucai98.github.io/bean-by-bean/index.html)

</div>

一个单文件网页，用盖房子的动画把六个阶段演一遍：散落的砖块 → 仓库自动送货 → 手动插拔水管 → 成堆的 XML → 一键组装 → 多栋房子互联。**零依赖，断网也能看，13 秒自动播一幕。**

> 部署到 GitHub Pages 前，把 `java-backend-roadmap.html` 改名为 `index.html`，上面的在线链接就能用。

---

## 这仓库是不是给你写的？

- [ ] 学完 Java 语法，不知道下一步该学什么
- [ ] 打开 JavaGuide 的目录就头晕 —— 159k star 的那份，光目录就三屏
- [ ] Spring、SpringBoot、MyBatis、微服务这些词都听过，但说不清谁管什么
- [ ] 不知道该装 JDK 8 还是 JDK 21
- [ ] 2026 年了，还在纠结要不要从 SSM 学起
- [ ] 想要一张图能看清全局，而不是一堆散落的教程

命中两条以上，往下看。

---

## 跟 JavaGuide 是什么关系

不是竞品，是**它的前 30 分钟**。

| | JavaGuide | 这个仓库 |
|---|---|---|
| 解决什么 | 面试考点逐个击破 | **先建立全局认知** |
| 颗粒度 | HashMap 扩容机制、TCP 三次握手 | 六个阶段分别管什么 |
| 打开方式 | 159k star 的目录，新手容易劝退 | 一个动画，10 分钟 |
| 读完去哪 | 已经很深了 | **每幕末尾都架桥通到 JavaGuide** |

简单说：**先用故事把地图画出来，再把人送到深水区。**

---

## 六幕

| | 阶段 | 盖房子比喻 | 要学什么 | 权重 |
|---|---|---|---|---|
| ① | [JavaSE](./docs/01-javase.md) | 地基与砖块水泥 | 语法、面向对象、集合、IO、多线程 | **35%** |
| ② | [MySQL + Maven](./docs/02-mysql-maven.md) | 材料仓库 | SQL、索引与事务、Maven 依赖管理 | **20%** |
| ③ | [JDBC](./docs/03-jdbc.md) | 手动接水管 | 连接、PreparedStatement、连接池 | 5% 了解即可 |
| ④ | [SSM](./docs/04-ssm.md) | 预制零件 + 成堆说明书 | Spring IOC / AOP、SpringMVC、MyBatis | 10% 可跳过 |
| ⑤ | [SpringBoot](./docs/05-springboot.md) | 一体化建房套件 | Starter、自动装配、内嵌 Tomcat | **25%** |
| ⑥ | [微服务](./docs/06-microservice.md) | 一栋不够，盖成小区 | Redis、消息队列、Spring Cloud | 5% 找工作再说 |

**注意权重那一列** —— 六幕不是等权重的。JDBC 和 SSM 在 2026 年属于"知道它存在就行"，把时间砸在 JavaSE 和 SpringBoot 上回报高得多。每幕文档里都写清楚了为什么。

---

## 怎么用

**路径 A · 完全零基础**（建议）
先看一遍动画页 → 按 ①→⑥ 顺序读 `docs/` → 每学完一幕做一个小项目，哪怕只是增删改查。

**路径 B · 查漏补缺**
直接翻对应文档，看哪一节的知识点你叫不出名字。

**路径 C · 复习**
只看导图主干，能自己把每个分支展开讲出来才算过关。

导图本体是 [`mindmap.md`](./mindmap.md)，一份 Markdown 缩进大纲 —— **不是图片**。因为图片有三个硬伤：搜不到、改不动一个错字、每次更新要重新导出。缩进大纲能一键渲染成真导图：

```bash
npx markmap-cli mindmap.md -o mindmap.html    # 需要 Node.js
```

不想装 Node 也行，内容贴进 https://markmap.js.org/repl ，或粘贴进 XMind / 幕布 / ProcessOn，都会自动识别层级。

---

## 目录结构

```
.
├── java-backend-roadmap.html   动画演示页（单文件，零依赖）
├── mindmap.md                  导图本体（缩进大纲）
├── docs/
│   ├── 01-javase.md
│   ├── 02-mysql-maven.md
│   ├── 03-jdbc.md
│   ├── 04-ssm.md
│   ├── 05-springboot.md
│   └── 06-microservice.md
└── LICENSE                     CC BY 4.0
```

每篇文档结构统一：**它是什么 → 解决什么问题 → 知识点清单 → 常见坑 → 这一阶段的痛 → 自查清单**。

---

## 几个一定会问的问题

<details>
<summary><b>JDK 装 8 还是 21？</b></summary>

装 **JDK 21**（LTS，长期支持版）。

市面上大量老教程教你装 JDK 8，那是 2014 年的选择。现在主流是 17 / 21，而且 **Spring Boot 3.x 最低要求 JDK 17** —— 装 8 会直接跑不起来。
</details>

<details>
<summary><b>2026 年还要学 SSM 吗？</b></summary>

**XML 配置不用学，IOC 和 AOP 必须学。**

现在没人手写 Spring 的 XML 配置了，全用注解。但 IOC（控制反转）和 AOP（面向切面）是 SpringBoot 的地基 —— 不懂这两个，你只能抄代码，出了错无从下手。

建议学完 SpringBoot 再回头看 IOC/AOP，会豁然开朗。
</details>

<details>
<summary><b>Spring Boot 2.x 和 3.x 有什么区别？</b></summary>

最大的坑：**3.x 起包名从 `javax.*` 改成了 `jakarta.*`**。

照着 2022 年以前的老教程抄代码，import 会一片红。这是新手最常卡住的地方之一。另外 3.x 要求 JDK 17 及以上。
</details>

<details>
<summary><b>学完能找到工作吗？</b></summary>

这个仓库只负责**让你知道该学什么、按什么顺序学**，不负责教到能面试。

学完 ①②⑤ 三块（JavaSE + MySQL + SpringBoot），你就能独立写出能跑的 Web 后台，可以开始投简历了。考点深入请去 [JavaGuide](https://javaguide.cn/)。
</details>

---

## 三条提醒

1. **别跳步。** JavaSE 不牢，后面全学成"抄配置"，报错只能靠猜。
2. **框架是替你写代码的 JavaSE，不是魔法。** 所有框架底下都是基础语法。
3. **遇到报错先读英文堆栈第一行**，答案通常在里面。

---

## 贡献

欢迎提 issue 指出错误、提 PR 补充知识点。补内容时请：

- 用大白话，先说"解决什么问题"，再讲原理
- 一个节点只放一个知识点，别塞长句
- 不确定的内容宁可不写，也不要写错

如果觉得有点用，点个 ⭐ 就行 —— 这是对一个零 star 仓库最大的鼓励。

---

## License

[CC BY 4.0](./LICENSE)：可以自由使用、修改、传播，包括商业用途，**只需注明出处**。

内容基于公开的 Java 技术文档与个人学习整理，不含任何付费课程或书籍的原文。
