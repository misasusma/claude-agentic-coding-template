# 🚀 完整專案初始化指南

## 📋 總覽

這份指南說明如何使用整合的 **CLAUDE_TEMPLATE_zh-TW.md + VibeCoding 範本 + .claude Subagent 系統** 來完成從專案想法到開發就緒的完整流程。

## 🎯 整合架構優勢

### ✅ 消除的問題
- **需求澄清不一致** → 統一使用 VibeCoding 7問深度澄清
- **資料夾結構衝突** → CLAUDE_TEMPLATE 與 .claude 系統完美整合
- **流程斷點** → 從初始化到交付的無縫銜接
- **手動配置複雜** → workflow-template-manager 智能分析自動配置

### 🚀 增強的功能
- **智能專案分析** → 自動判斷專案類型、複雜度、風險等級
- **完整開發規則** → Linus 開發心法 + 技術債預防 + Agent 協作
- **標準化流程** → VibeCoding 範本驅動的品質 Gate 機制
- **7個專業 Agent** → 全生命週期專業支援

## 🔄 使用流程

### 步驟 1: 放置初始化範本

```bash
# 將 CLAUDE_TEMPLATE_zh-TW.md 放入專案根目錄
cp "Claude Code Starter Template/CLAUDE_TEMPLATE_zh-TW.md" /your/project/path/
```

### 步驟 2: Claude Code 自動偵測

當 Claude Code 偵測到 `<!-- CLAUDE_CODE_PROJECT_TEMPLATE_V2 -->` 標記時：

```
🤖 偵測到專案初始化模板。您想要我設定一個新專案嗎？

選項：
1. ✅ 是 - 開始整合初始化流程
2. ❌ 否 - 稍後再設定

[等待用戶選擇]
```

### 步驟 3: 基礎資訊收集

Claude Code 執行 CLAUDE_TEMPLATE 的基礎問題：

```
🎯 基礎專案資訊：
1. "您的專案名稱是什麼？" → [PROJECT_NAME]
2. "專案的簡要描述？" → [PROJECT_DESCRIPTION]
3. "主要程式語言？" (Python/JavaScript/TypeScript/Java/其他)
4. "是否設定 GitHub 儲存庫？" (是-新增/是-現有/否)
```

### 步驟 4: VibeCoding 7問深度澄清

**workflow-template-manager** 接手執行深度需求澄清：

```
🎯 問題 1: 核心問題定義
"這個專案主要解決什麼問題？請描述目標用戶和他們遇到的痛點。"

🎯 問題 2: 核心功能範圍
"這個專案的核心功能有哪些？請列出 3-5 個最重要的功能。"

🎯 問題 3: 技術偏好和約束
"您對技術選型有什麼偏好或限制？"

🎯 問題 4: 用戶體驗期望
"您希望用戶在使用這個應用時有什麼樣的體驗？"

🎯 問題 5: 規模和性能要求
"預期的用戶規模和性能要求是什麼？"

🎯 問題 6: 時程和資源限制
"專案的時間限制和可用資源是什麼？"

🎯 問題 7: 成功標準定義
"如何衡量這個專案的成功？有什麼具體的指標嗎？"
```

### 步驟 5: AI 分析建議與人類決策 👤

**workflow-template-manager** 提供智能分析建議，**用戶做最終決策**：

```markdown
📊 AI 分析建議：

🤖 建議專案複雜度: [簡易/標準/AI-ML]
   理由: 基於功能範圍和技術需求的分析

🤖 建議工作流程: [Full Process/MVP Lean]
   理由: 基於風險評估和專案特性

🤖 建議資料夾結構: [CLAUDE_TEMPLATE 結構類型]
   理由: 基於專案類型和團隊規模

🤖 風險評估: [高/中/低風險點分析]

👤 請確認您的選擇：
1. 專案複雜度：[用戶選擇：簡易/標準/AI-ML/自訂]
2. 工作流程模式：[用戶選擇：Full Process/MVP Lean/混合]
3. 資料夾結構：[用戶選擇：接受建議/自訂結構]
4. 特殊需求：[用戶補充的任何特殊要求]

⚠️ 重要：系統將等待您的確認後才繼續建置
```

### 步驟 6: 整合架構建置 (基於用戶決策)

**僅在用戶確認所有選擇後**執行架構建置：

```bash
echo "📋 執行用戶確認的配置："
echo "- 專案複雜度：[用戶選擇]"
echo "- 工作流程模式：[用戶選擇]"
echo "- 資料夾結構：[用戶選擇]"

# 1. 建立 .claude 系統 (固定)
mkdir -p .claude/{agents,context,coordination,templates}
mkdir -p .claude/context/{workflow,decisions,quality,testing,e2e,security,deployment,docs}

# 2. 建立專案結構 (基於用戶確認的選擇)
if [[ "$USER_CHOICE" == "簡易" ]]; then
    mkdir -p {src,tests,docs,output}
elif [[ "$USER_CHOICE" == "標準" ]]; then
    mkdir -p {src,docs,tools,examples,output}
    mkdir -p src/{main,test}
    mkdir -p src/main/{python,resources}
    mkdir -p src/main/python/{core,utils,models,services,api}
elif [[ "$USER_CHOICE" == "AI-ML" ]]; then
    mkdir -p {data,notebooks,models,experiments,src,docs,output}
    mkdir -p data/{raw,processed,external,temp}
else
    echo "執行用戶自訂結構..."
    # 根據用戶具體需求建立
fi

# 3. 生成整合式 CLAUDE.md (包含用戶決策上下文)
# 合併：CLAUDE_TEMPLATE 規則 + VibeCoding 澄清結果 + 用戶確認決策 + Agent 協作規則

# 4. 配置開發環境
git init
git config --local user.name "Claude Code"
git config --local user.email "claude@anthropic.com"

# 5. 初始提交 (包含用戶決策資訊)
git add .
git commit -m "chore(init): integrate CLAUDE_TEMPLATE with user-confirmed configuration

- Project complexity: [用戶選擇]
- Workflow mode: [用戶選擇]
- Folder structure: [用戶選擇]
- Special requirements: [用戶補充]"

# 6. GitHub 設定 (基於用戶選擇)
```

### 步驟 7: 生成初始化報告

**workflow-template-manager** 自動生成完整報告至 `.claude/context/workflow/`：

```markdown
## 🚀 Integrated Project Initialization Report

### 🎯 專案概要 (基於 VibeCoding 7問澄清)
- 專案名稱: [實際專案名稱]
- 核心問題: [問題1回答]
- 目標用戶: [用戶痛點分析]
- 主要功能: [3-5個核心功能]
- 技術約束: [技術偏好和限制]
- 成功標準: [具體指標]

### 📊 分析建議與用戶決策
🤖 **AI 建議**:
- 建議專案複雜度: [AI 分析結果]
- 建議工作流程: [AI 建議模式]
- 風險評估: [AI 風險分析]

👤 **用戶最終決策**:
- 確認專案複雜度: [用戶實際選擇]
- 確認工作流程: [用戶實際選擇]
- 確認資料夾結構: [用戶實際選擇]
- 特殊需求: [用戶補充需求]

### 🏗️ 整合架構設置
- CLAUDE_TEMPLATE 結構: [選擇的結構類型]
- .claude 系統集成: ✅ 已配置 7個專業 Agent
- CLAUDE.md 整合: ✅ 包含完整開發規則和上下文

### 🤖 Agent 協作規劃
- Phase 1 規劃: workflow-template-manager + documentation-specialist
- Phase 2 設計: 主Agent + security-infrastructure-auditor
- Phase 3 開發: code-quality-specialist + test-automation-engineer
- Phase 4 品質: e2e-validation-specialist + deployment-operations-engineer

### 🚀 Next Actions (可立即啟動)
- [✅] 專案就緒，可開始開發工作
- [ ] Phase 1: 需求文檔化 (可啟動 documentation-specialist)
- [ ] 設定專案追蹤機制
- [ ] 配置 VibeCoding 品質 Gate
```

## 🎯 開發階段流程

### Phase 1: 規劃階段

**觸發方式**:
```bash
claude code task --agent documentation-specialist \
  "基於專案初始化資訊，建立 PRD 和 BDD 場景文檔"
```

**產出**:
- Project Brief & PRD
- BDD Scenarios
- 需求追蹤矩陣

### Phase 2: 設計階段

**觸發方式**:
```bash
# 架構設計 (主 Agent)
claude code task \
  "基於 PRD 進行系統架構設計，使用 VibeCoding 架構範本"

# 安全審查
claude code task --agent security-infrastructure-auditor \
  "審查架構設計的安全性，參考 VibeCoding 安全檢查清單"
```

**產出**:
- Architecture Document
- API Specification
- Security Assessment

### Phase 3: 開發階段

**觸發方式**:
```bash
# 程式碼品質管理
claude code task --agent code-quality-specialist \
  "基於 VibeCoding 模組規格範本進行程式碼審查"

# 測試實作
claude code task --agent test-automation-engineer \
  "依據 BDD 場景實作自動化測試"
```

**產出**:
- 模組規格實作
- 單元測試和整合測試
- 程式碼品質報告

### Phase 4: 品質與部署

**觸發方式**:
```bash
# E2E 驗證
claude code task --agent e2e-validation-specialist \
  "執行端到端測試，驗證 BDD 場景"

# 部署準備
claude code task --agent deployment-operations-engineer \
  "基於 VibeCoding 就緒檢查清單準備部署"
```

**產出**:
- E2E 測試報告
- 部署就緒評估
- 監控和維運計畫

## 📊 品質 Gate 檢查點

### Gate 1: 規劃完成
```
- [ ] PRD 使用 VibeCoding 範本完成
- [ ] BDD 場景符合測試標準
- [ ] 風險評估通過 workflow-template-manager 審查
```

### Gate 2: 設計完成
```
- [ ] 架構設計使用 VibeCoding ADR 範本記錄
- [ ] API 設計符合 VibeCoding 規格範本
- [ ] security-infrastructure-auditor 安全審查通過
```

### Gate 3: 開發完成
```
- [ ] 模組開發符合 VibeCoding 規格範本
- [ ] code-quality-specialist 品質審查通過
- [ ] test-automation-engineer 測試覆蓋率達標
```

### Gate 4: 部署就緒
```
- [ ] VibeCoding 安全檢查清單全部通過
- [ ] e2e-validation-specialist E2E 驗證成功
- [ ] deployment-operations-engineer 部署準備完成
```

## 🔧 故障排除

### 常見問題

**Q: Claude Code 沒有偵測到模板？**
A: 確認檔案包含 `<!-- CLAUDE_CODE_PROJECT_TEMPLATE_V2 -->` 標記

**Q: VibeCoding 7問流程被跳過？**
A: workflow-template-manager 可能未正確配置，檢查 `.claude/agents/` 目錄

**Q: 資料夾結構與預期不符？**
A: 檢查智能分析結果，可能專案複雜度判斷需要手動調整

**Q: Agent 協作沒有啟動？**
A: 確認 `.claude/context/workflow/` 中有初始化報告生成

### 手動修復

如果自動初始化失敗，可以手動執行：

```bash
# 手動啟動 workflow-template-manager
claude code task --agent workflow-template-manager \
  "執行 CLAUDE_TEMPLATE 整合初始化，請進行 VibeCoding 7問澄清"
```

## 🎯 最佳實踐

### 專案啟動原則
1. **完整澄清** - 不要跳過 VibeCoding 7問
2. **智能分析結果信任** - workflow-template-manager 的判斷基於最佳實踐
3. **階段式開發** - 嚴格按照 4個 Phase 進行
4. **品質 Gate 把關** - 每個 Gate 都要達標才能進入下一階段

### 團隊協作建議
1. **CLAUDE.md 為聖經** - 所有開發規則以此為準
2. **Agent 專業分工** - 讓專業的 Agent 做專業的事
3. **上下文共享** - 充分利用 `.claude/context/` 中的資訊
4. **持續改進** - 定期檢討和優化流程

---

**🎯 這套整合流程確保從專案想法到最終交付的每個環節都有最佳實踐支援，消除了所有衝突和疏失。**