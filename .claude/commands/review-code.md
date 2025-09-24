---
description: Trigger VibeCoding template-based code review with Subagent suggestions
argument-hint: [path] (optional, defaults to current directory)
allowed-tools: Read(/**), Grep(*), Glob(*)
---

# 🔍 VibeCoding Template-Based Code Review

## Analysis Target
Analyzing code at: **$1** (or current directory if not specified)

## 🎯 VibeCoding Template Assessment

Based on the 10 VibeCoding workflow templates, let me analyze your code:

### 📋 Template Categories Being Checked:

#### **🏗️ Architecture & Design Templates**
- `03_architecture_and_design_document.md` → Code structure analysis
- `04_api_design_specification_template.md` → API design compliance
- `06_project_structure_guide.md` → Project organization

#### **🧪 Quality & Testing Templates**
- `04_module_specification_and_tests.md` → Test coverage analysis
- `05_security_and_readiness_checklists.md` → Security assessment

#### **🔍 Code Analysis Templates**
- `08_file_dependencies_template.md` → Dependency relationships
- `09_class_relationships_template.md` → Class structure design

#### **📝 Documentation Templates**
- `01_project_brief_and_prd.md` → Requirements alignment
- `01_adr_template.md` → Architecture decision tracking
- `02_bdd_scenarios_guide.md` → Behavior specification

## 🚦 Analysis Results & Subagent Suggestions

**Based on current code analysis:**

```
📊 VibeCoding Template Review Results:
🎯 分析路徑: $1
🔍 偵測情境: [Code analysis in progress...]

🤖 建議 Subagent 協作:
  🟡 code-quality-specialist - 程式碼重構機會分析
  🔴 security-infrastructure-auditor - 安全合規檢查
  🟢 test-automation-engineer - 測試覆蓋率評估
  📝 documentation-specialist - 文檔同步更新
  🎯 workflow-template-manager - 架構規範審查

❓ 選擇要啟動的 Subagent：
  [1] 🟡 程式碼品質檢查
  [2] 🔴 安全性審查
  [3] 🟢 測試分析
  [4] 📝 文檔更新
  [5] 🎯 架構審查
  [A] 全部啟動
  [N] 跳過建議

請輸入選擇 (1-5, A, 或 N):
```

## 🎛️ 人類主導決策

**Remember: You are the 鋼彈駕駛員 (mech pilot)**
- All suggestions require your explicit approval
- You can mix and match Subagents based on your priorities
- Natural language commands also work ("檢查程式碼品質")

## 🔄 Integration with Current Settings

This review respects your current suggestion mode and VibeCoding template preferences. The analysis is based on the established human-AI collaboration patterns in your `CLAUDE.md` configuration.

**Ready for your command!** 🤖⚔️