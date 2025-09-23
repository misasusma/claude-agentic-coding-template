# 🤖 Claude Code Subagent 協作系統

## 系統概述

全功能 Claude Code Subagent 協作系統，採用「主 Agent（PM + 架構師）+ 7個專業化 IC Subagents」模式，整合 VibeCoding 範本驅動開發流程。

## 目錄結構

```
.claude/
├── README.md                    # 本檔案：系統總覽
├── ARCHITECTURE.md              # 架構設計文檔
├── settings.local.json          # Claude Code 本地設定
├── agents/                      # Subagent 配置檔案
│   ├── workflow-template-manager.md      
│   ├── code-quality-specialist.md
│   ├── test-automation-engineer.md
│   ├── e2e-validation-specialist.md
│   ├── security-infrastructure-auditor.md
│   ├── deployment-operations-engineer.md
│   ├── documentation-specialist.md
│   ├── OPTIMIZATION_PLAN.md
│   └── NEW_ARCHITECTURE_SUMMARY.md
├── context/                     # 跨 Agent 上下文共享
│   ├── README.md
│   ├── decisions/               # 主 Agent 技術決策記錄
│   ├── workflow/                # 工作流程管理報告
│   ├── quality/                 # 程式碼品質報告
│   ├── testing/                 # 測試執行報告
│   ├── e2e/                    # E2E 驗證報告
│   ├── security/               # 安全稽核報告
│   ├── deployment/             # 部署維運報告
│   └── docs/                   # 文檔管理報告
├── coordination/               # Agent 協調機制
│   ├── README.md
│   ├── handoffs/               # Agent 間任務交接
│   └── conflicts/              # 衝突解決記錄
└── templates/                  # 標準化範本
    ├── decision-record-template.md
    ├── agent-report-template.md
    ├── handoff-template.md
    └── workflow-integration-template.md    
```

## 系統架構

### 主 Claude Code Agent
**角色**: PM + Tech Lead + Architect
- 專案管理與任務協調
- 系統架構設計與技術決策
- 跨 agent 上下文整合與衝突解決

### 7 個專業化 IC Subagents

1. **workflow-template-manager**: 工作流程範本管理、開發生命週期協調
2. **code-quality-specialist**: 程式碼品質、重構、技術債務、基礎安全
3. **test-automation-engineer**: 單元測試、整合測試、測試基礎設施
4. **e2e-validation-specialist**: 端到端驗證、UI 測試、跨瀏覽器相容性
5. **security-infrastructure-auditor**: 基礎設施安全、依賴安全、合規檢查
6. **deployment-operations-engineer**: 零停機部署、基礎設施管理、系統監控
7. **documentation-specialist**: API 文檔、系統文檔、知識庫維護

## 🎨 VibeCoding 範本整合

完整整合 **VibeCoding_Workflow_Templates** ，提供標準化開發生命週期管理。

### 兩種開發模式
- **Full Process**: 企業級、高風險專案（金流、隱私、合規）
- **MVP Lean**: 快速原型、低風險迭代專案

### 快速啟動
```bash
# 1. 評估專案工作流程
claude code task --agent workflow-template-manager \
  "評估新專案的工作流程需求"

# 2. 查看工作流程報告
cat .claude/context/workflow/workflow-template-manager-report-*.md
```

## 🚀 專案初始化整合 ⭐ 新功能

### 完整整合流程
本系統現在與 **CLAUDE_TEMPLATE_zh-TW.md** 完全整合，提供從專案想法到開發就緒的無縫體驗：

```
CLAUDE_TEMPLATE 偵測 → VibeCoding 7問澄清 → 智能分析 → 整合架構建置 → Agent 協作啟動
```

### 🎯 關鍵特色
- **智能專案分析**: 自動判斷專案類型、複雜度、風險等級
- **VibeCoding 整合**: 7問深度澄清 + 標準化範本驅動開發
- **Linus 開發心法**: 技術債預防 + 品味導向的程式碼品質
- **零衝突整合**: CLAUDE_TEMPLATE 與 .claude 系統完美融合

### 立即開始
1. **放置範本**: 將 `CLAUDE_TEMPLATE_zh-TW.md` 放入專案根目錄
2. **自動啟動**: Claude Code 偵測後立即啟動 `workflow-template-manager`
3. **深度澄清**: 回答 VibeCoding 7問，AI 提供建議，人類決策
4. **整合建置**: 基於用戶決策建置專案結構和 CLAUDE.md
5. **Subagent 協作**: 使用明確規範的 7個專業 Agent 進行開發

📖 **完整指南**: [專案初始化指南](./PROJECT_INITIALIZATION_GUIDE.md)

## 🚀 快速上手

**新手必讀**: [🚀 快速開始指南](./QUICK_START.md)

### 常用指令
```bash
# 程式碼品質檢查
claude code task --agent code-quality-specialist "審查程式碼品質"

# 執行測試
claude code task --agent test-automation-engineer "執行測試並分析覆蓋率"

# 端到端驗證
claude code task --agent e2e-validation-specialist "執行 E2E 測試"
```

## 🤝 協作流程

### 典型工作流程
1. **專案評估** - workflow-template-manager 評估選擇模式
2. **需求分析** - 主 Agent 分析使用者需求
3. **任務分派** - 根據專業領域分派 Subagent
4. **並行執行** - 各 Agent 獨立執行專業工作
5. **品質 Gate** - 按 VibeCoding 範本檢查品質
6. **結果整合** - 主 Agent 整合各 Agent 產出
7. **統一交付** - 提供完整解決方案

## 📊 系統優勢

### 核心價值
✅ **消除角色重疊** - 明確專業分工，避免功能衝突
✅ **VibeCoding 整合** - 標準化範本驅動開發流程
✅ **品質內建** - 從規劃到部署的完整 Gate 機制
✅ **強化全局決策** - 架構師整合至主 Agent，獲得完整上下文
✅ **專業化深度** - 7個 Subagent 各司其職，提供最佳實踐

### 使用原則
1. **專案開始時** - 先用 workflow-template-manager 評估
2. **開發過程中** - 按階段使用對應 Agent
3. **提交代碼前** - 執行品質和安全檢查
4. **部署前** - 完整的 E2E 驗證

## 📁 文檔結構

```
.claude/
├── README.md                    # 🏠 本檔：系統總覽
├── QUICK_START.md              # 🚀 快速開始指南
├── ARCHITECTURE.md             # 🏗️ 架構設計文檔
├── agents/                     # 💼 Subagent 配置檔案
│   ├── workflow-template-manager.md      # ⭐ 工作流程管理
│   ├── code-quality-specialist.md        # 🔍 程式碼品質
│   ├── test-automation-engineer.md       # 🧪 測試自動化
│   ├── e2e-validation-specialist.md      # 🌐 端到端驗證
│   ├── security-infrastructure-auditor.md # 🔒 安全稽核
│   ├── deployment-operations-engineer.md  # 🚀 部署維運
│   └── documentation-specialist.md       # 📚 文檔專家
├── context/                    # 📈 跨 Agent 上下文共享
│   ├── workflow/               # 工作流程管理報告
│   ├── decisions/              # 主 Agent 技術決策記錄
│   ├── quality/                # 程式碼品質報告
│   ├── testing/                # 測試執行報告
│   ├── e2e/                   # E2E 驗證報告
│   ├── security/              # 安全稽核報告
│   ├── deployment/            # 部署維運報告
│   └── docs/                  # 文檔管理報告
├── coordination/              # 🤝 Agent 協調機制
│   ├── handoffs/              # Agent 間任務交接
│   └── conflicts/             # 衝突解決記錄
└── templates/                 # 📋 標準化範本
    ├── decision-record-template.md
    ├── agent-report-template.md
    ├── handoff-template.md
    └── workflow-integration-template.md
```

## 📄 相關文檔

- [🚀 快速開始指南](./QUICK_START.md) - 新手必讀，5分鐘上手
- [🏗️ 架構設計](./ARCHITECTURE.md) - 深入了解系統設計
- [💼 Agent 配置](./agents/) - 各 Subagent 詳細設定
- [📋 範本庫](./templates/) - 標準化範本

---

🎆 **充分發揮 Claude Code 原生能力，提供企業級軟體開發協作體驗！**