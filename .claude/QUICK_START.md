# 🚀 快速開始指南

## 立即開始使用 Claude Code Subagent 協作系統

### 第一次使用

#### 1. 評估專案並選擇工作流程
```bash
# 使用 workflow-template-manager 評估專案
claude code task --agent workflow-template-manager \
  "評估新專案的工作流程需求"
```

#### 2. 查看工作流程建議
```bash
cat .claude/context/workflow/workflow-template-manager-report-*.md
```

#### 3. 按建議執行開發流程
根據評估報告執行對應的開發階段。

### 🎯 常用指令

#### 程式碼品質檢查
```bash
claude code task --agent code-quality-specialist \
  "審查專案程式碼品質"
```

#### 執行測試
```bash
claude code task --agent test-automation-engineer \
  "執行單元測試並分析覆蓋率"
```

#### 端到端驗證
```bash
claude code task --agent e2e-validation-specialist \
  "執行端到端測試驗證"
```

#### 安全檢查
```bash
claude code task --agent security-infrastructure-auditor \
  "進行安全漏洞掃描"
```

#### 部署準備
```bash
claude code task --agent deployment-operations-engineer \
  "檢查部署就緒狀態"
```

#### 文檔維護
```bash
claude code task --agent documentation-specialist \
  "更新 API 文檔"
```

### 📊 查看執行結果

```bash
# 查看各類報告
ls .claude/context/quality/      # 程式碼品質報告
ls .claude/context/testing/      # 測試報告
ls .claude/context/e2e/          # E2E 驗證報告
ls .claude/context/security/     # 安全報告
ls .claude/context/deployment/   # 部署報告
ls .claude/context/docs/         # 文檔報告
ls .claude/context/decisions/    # 技術決策記錄
```

### 🔄 工作流程模式

#### Full Process 模式（適用於）
- 企業級應用
- 涉及金流、隱私、合規
- 長期維運需求
- 多團隊協作

#### MVP Lean 模式（適用於）
- 概念驗證或原型
- 快速迭代需求
- 小型功能開發
- 資源受限專案

### 💡 最佳實踐

1. **專案開始時**：先用 workflow-template-manager 評估
2. **開發過程中**：按階段使用對應的 agent
3. **提交代碼前**：執行品質和安全檢查
4. **部署前**：完整的 E2E 驗證
5. **文檔同步**：及時更新技術文檔

### 📚 更多資訊

- [系統架構](./ARCHITECTURE.md) - 了解系統設計
- [Agent 詳細配置](./agents/) - 各 Agent 的詳細設定
- [範本庫](./templates/) - 標準化範本