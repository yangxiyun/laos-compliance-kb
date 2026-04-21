# laos-compliance-kb-ingest Skill

ZTL 老挝合规知识库 - Claude Code 摄入技能

---

## 安装步骤

### 第一步：确认 Claude Code 已安装
```bash
claude --version
```

### 第二步：把 SKILL.md 放到正确位置

**Windows：**
```
C:\Users\你的用户名\.claude\skills\laos-kb-ingest\SKILL.md
```

用CMD创建文件夹：
```cmd
mkdir "C:\Users\Dell\.claude\skills\laos-kb-ingest"
```

然后把 SKILL.md 复制进去。

### 第三步：进入知识库目录启动 Claude Code
```cmd
cd D:\laos-wiki
claude
```

### 第四步：测试
在 Claude Code 对话里输入：
```
处理待摄入PDF文件夹里的所有文件
```

---

## 日常使用

### 摄入新文件
1. 把文件放入 `D:\laos-wiki\待摄入\`
2. 在终端运行：
```cmd
cd D:\laos-wiki
claude
```
3. 输入：`请摄入待摄入文件夹里的所有文件`

### 查询知识库
在同一个 Claude Code 会话里直接提问：
```
老挝增值税申报截止日期是什么时候？
```

### 单个文件摄入
```
请摄入这个文件：D:\laos-wiki\待摄入\老挝增值税法.pdf
```

---

## 文件夹结构

```
D:\laos-wiki\
├── laos-compliance-kb\     ← 在这里启动 claude
│   ├── META\
│   ├── 税务\
│   ├── 会计\
│   ├── 工商\
│   ├── 人力资源\
│   └── 业务经验库\
├── 待摄入PDF\              ← 文件放这里
└── 处理完成\               ← 处理完自动移入
```

---

## 与 ingest.js 的区别

| | ingest.js | Claude Code Skill |
|---|---|---|
| 触发方式 | 全自动监控 | 手动执行命令 |
| 智能程度 | 固定逻辑 | AI动态判断 |
| 速率限制 | 容易触发 | 不存在 |
| 维护成本 | 需要调试脚本 | 自动修正 |
| 文件读写 | Node.js API | 直接操作 |
