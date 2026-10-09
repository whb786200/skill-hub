# Skill Hub 使用指南

> 本文档随每次 Skill 调用自动更新（OTF 机制）

## 一、快速开始

### 查看所有 Skill

对我说：「有什么 skill」或「skill 列表」

→ 返回按分类折叠的 57 个 Skill 索引

### 调用某个 Skill

对我说：「用 XX skill 帮我...」

→ 自动匹配并加载对应 Skill

### 找不到功能时

对我说：「有没有 XX 功能」

→ 触发 `find-skills` 搜索或请用户确认需求

---

## 二、分类说明

| 分类 | 数量 | 说明 |
|------|------|------|
| 🔧 系统工具类 | 5 | meta-skill-bootstrap、skill-hub、ima-skill 等 |
| 📝 公众号运营类 | 11 | aws-wechat-* 系列、social-media-ops 等 |
| 🏗️ 工程知识库类 | 27 | 安全、质量、成本、进度等工程领域 |
| 📊 垂直领域类 | 4 | bamboo-stock、iceberg-os 等 |
| 🔍 百度/文库类 | 3 | 百度文库、网盘相关 |
| ☁️ 其他工具类 | 3 | quark-to-zsxq、ppt-audit-cleaner 等 |

---

## 三、自演进机制说明

### 已具备自演进能力的 Skill

| Skill | 自演进目录 |
|--------|--------------|
| `social-media-ops` | patterns/errors, successes, viral |
| `meta-skill-bootstrap` | 自身即自举引擎 |
| `skill-hub` | patterns/（本文档） |
| `safety-management` | patterns/errors, successes, viral |
| `quality-management` | patterns/errors, successes, viral |
| `cost-management` | patterns/errors, successes, viral |
| `schedule-management` | patterns/errors, successes, viral |

### 自演进工作原理

```
每次执行 Skill
    ↓
OTF 触发：发现重复模式 → 立即记录
    ↓
JIT 收敛：样本足够 → 提炼为模式
    ↓
Bootstrap：模式稳定 → 写入 patterns/ 对应目录
    ↓
下次执行：自动加载 patterns/ 历史经验
```

### 为其他 Skill 注入自演进（模板）

在目标 Skill 的 SKILL.md 末尾追加：

```markdown
---

## Skill 自演进机制（OTF + JIT + Bootstrap）

### 触发条件
- 同一类问题 ≥ 3 次 → 写入 patterns/errors/
- 同一类成功模式 → 写入 patterns/successes/
- 用户反馈 → 提炼可复用要素

### 演进记录格式
## [日期] 模式发现
**触发来源**：<哪次执行>
**核心发现**：<用一句话描述>
**支撑证据**：<案例/数据>
**可复用要素**：<下次怎么做>
**沉淀位置**：patterns/<类别>/
```

并在 Skill 目录下创建：
```
<skill-name>/
  patterns/
    errors/         # 避坑记录
    successes/      # 成功模式
    viral/          # 高频问题
```

---

## 四、Skill 安装后操作

新 Skill 安装后，需手动更新 `skill-hub/SKILL.md` 中的分类索引（后续版本将自动化）。

---

## 五、演进记录（自动更新）

> 以下由 OTF 机制自动维护。

（暂无记录 — 等待首次调用后自动沉淀）
