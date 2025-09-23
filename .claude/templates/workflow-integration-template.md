# VibeCoding 工作流程整合範本

## 檔案命名規範
`workflow-integration-{project-name}-{YYYY-MM-DD}.md`

例如: `workflow-integration-user-auth-system-2025-09-23.md`

---

# 專案工作流程整合規劃

## 專案基本資訊

**專案名稱**: {專案名稱}
**專案類型**: {Web App/API/Mobile App/Desktop App/其他}
**專案規模**: {Small/Medium/Large/Enterprise}
**團隊規模**: {人數} 人
**預期時程**: {週數/月數}
**風險等級**: {Low/Medium/High/Critical}

## 模式選擇分析

### 專案特性評估
- [ ] 涉及金流/支付系統
- [ ] 處理個人隱私資料
- [ ] 需要高可用性 (99.9%+)
- [ ] 跨 3+ 團隊協作
- [ ] 需要長期維運 (2年+)
- [ ] 有法規合規要求
- [ ] 需要規模化擴展

**評估結果**:
- ✅ **Full Process 模式** (完整流程) - 如果有 3+ 項符合
- ✅ **MVP Lean 模式** (快速迭代) - 如果少於 3 項符合

### 選擇的模式
**最終選擇**: {Full Process / MVP Lean}
**選擇理由**: {基於上述評估的具體原因}

## 工作流程階段規劃

### Phase 1: 規劃階段 (Planning)
**目標**: 定義「為何」與「什麼」

#### 使用範本
- [ ] `01_project_brief_and_prd.md` - 專案簡述和產品需求文檔
- [ ] `02_bdd_scenarios_guide.md` - 行為驅動開發場景設計
- [ ] `questions_template.md` - 標準化問題清單

#### 負責 Agent
- **主導**: workflow-template-manager
- **協作**: documentation-specialist (文檔結構化)

#### 交付成果
- [ ] 完整的 PRD 文檔
- [ ] BDD 使用者場景清單
- [ ] 專案範圍和約束定義
- [ ] 成功標準和驗收條件

### Phase 2: 設計階段 (Design)
**目標**: 定義「如何」的藍圖

#### 使用範本
- [ ] `03_architecture_and_design_document.md` - 系統架構設計
- [ ] `04_api_design_specification_template.md` - API 介面設計
- [ ] `01_adr_template.md` - 架構決策記錄
- [ ] `09_class_relationships_template.md` - 類別關係設計

#### 負責 Agent
- **主導**: 主 Claude Code Agent (架構決策)
- **協作**:
  - workflow-template-manager (範本指導)
  - security-infrastructure-auditor (安全設計審查)

#### 交付成果
- [ ] 系統架構文檔
- [ ] API 設計規格書
- [ ] 重要技術決策 ADR 記錄
- [ ] 資料模型和類別設計

### Phase 3: 開發階段 (Development)
**目標**: 精確實現設計藍圖

#### 使用範本
- [ ] `04_module_specification_and_tests.md` - 模組開發規格
- [ ] `06_project_structure_guide.md` - 專案結構組織
- [ ] `08_file_dependencies_template.md` - 檔案依賴管理

#### 負責 Agent
- **協調**: workflow-template-manager
- **執行**:
  - code-quality-specialist (程式碼品質)
  - test-automation-engineer (測試實作)
  - documentation-specialist (技術文檔)

#### 交付成果
- [ ] 模組化的程式碼實作
- [ ] 完整的測試套件
- [ ] 程式碼文檔和註解
- [ ] 開發過程中的決策記錄

### Phase 4: 品質與部署階段 (Quality & Deployment)
**目標**: 確保產品品質和部署就緒

#### 使用範本
- [ ] `05_security_and_readiness_checklists.md` - 安全和就緒檢查
- [ ] 部署檢查清單 (由 deployment-operations-engineer 提供)

#### 負責 Agent
- **協調**: workflow-template-manager
- **執行**:
  - security-infrastructure-auditor (安全檢查)
  - e2e-validation-specialist (端到端驗證)
  - deployment-operations-engineer (部署準備)

#### 交付成果
- [ ] 安全稽核報告
- [ ] E2E 測試驗證報告
- [ ] 部署文檔和程序
- [ ] 監控和告警配置

## Agent 協作流程

### 工作流程協調
```
workflow-template-manager (流程協調)
    ↓
主 Claude Code Agent (架構決策)
    ↓
專業 IC Agents 並行執行
    ↓
workflow-template-manager (品質檢核)
    ↓
統一交付
```

### 交接節點

#### 規劃 → 設計
**觸發條件**: PRD 和 BDD 場景完成
**交接內容**: 業務需求、使用者場景、約束條件
**品質 Gate**: 需求完整性檢查

#### 設計 → 開發
**觸發條件**: 架構設計和 API 規格完成
**交接內容**: 技術架構、介面定義、實作規範
**品質 Gate**: 設計一致性檢查

#### 開發 → 品質
**觸發條件**: 核心功能開發完成
**交接內容**: 程式碼、測試、文檔
**品質 Gate**: 程式碼品質和測試覆蓋率檢查

## 品質 Gate 標準

### Gate 1: 規劃完成
- [ ] PRD 涵蓋所有核心需求
- [ ] BDD 場景可測試和驗證
- [ ] 專案範圍明確定義
- [ ] 風險識別和緩解措施

### Gate 2: 設計完成
- [ ] 架構設計滿足非功能需求
- [ ] API 設計符合最佳實踐
- [ ] 重要技術決策有 ADR 記錄
- [ ] 安全設計通過初步審查

### Gate 3: 開發完成
- [ ] 程式碼品質達到標準
- [ ] 測試覆蓋率 ≥ 80%
- [ ] 技術文檔完整
- [ ] 程式碼審查通過

### Gate 4: 部署就緒
- [ ] 安全檢查清單全部通過
- [ ] E2E 測試驗證成功
- [ ] 部署程序測試完成
- [ ] 監控和告警配置就緒

## 風險管理

### 已識別風險
- **技術風險**: {列出技術相關風險}
- **時程風險**: {列出可能影響時程的因素}
- **品質風險**: {列出品質相關風險}
- **協作風險**: {列出團隊協作風險}

### 緩解措施
- **風險監控**: {監控機制和指標}
- **預警機制**: {早期警告和應對措施}
- **應急計劃**: {風險發生時的應對策略}

## 模式升降級條件

### MVP → Full Process 升級觸發
- [ ] 專案範圍擴大 3 倍以上
- [ ] 團隊規模增加到 5+ 人
- [ ] 發現重大安全或合規需求
- [ ] 需要與外部系統深度整合

### Full Process → MVP 降級適用
- [ ] 專案縮減為概念驗證
- [ ] 資源嚴重受限
- [ ] 時程壓力極大
- [ ] 低風險的獨立功能

## 成功指標

### 過程指標
- **文檔完整度**: {完成百分比}
- **品質 Gate 通過率**: {通過百分比}
- **時程達成率**: {準時交付百分比}

### 結果指標
- **功能完成度**: {需求實現百分比}
- **品質指標**: {錯誤率、效能指標}
- **使用者滿意度**: {驗收測試結果}

---

**建立時間**: {timestamp}
**負責 Agent**: workflow-template-manager
**協作 Agents**: {參與的 agents 清單}
**預期完成**: {預期完成時間}