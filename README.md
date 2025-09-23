# 🤖 Claude Code 通用專案模板

<!-- TEMPLATE_VERSION: v2.0 -->
<!-- CLAUDE_CODE_PROJECT_TEMPLATE_V2 -->

**一個完整的 Claude Code 專案模板，整合心流友善的 Subagent 協作系統與 VibeCoding 工作流程範本**

## 🎯 **模板特色**

- **🎨 心流友善設計** - 保護開發創造力，智能觸發 Subagent 協作
- **🤖 7個專業 Subagent** - 覆蓋軟體開發生命週期的所有專業領域
- **📚 VibeCoding 範本庫** - 企業級開發流程和品質標準
- **⚡ 即插即用** - 3分鐘快速設定，立即開始高效開發
- **🛡️ 技術債預防** - 內建 Linus 開發心法和品質把關機制

## 🚀 **快速開始**

### 1️⃣ 複製模板
```bash
cp -r claude-service/ your-new-project/
cd your-new-project/
```

### 2️⃣ 設定 API Keys
```bash
# 編輯 .mcp.json 和 .claude/settings.local.json
# 替換 YOUR_BRAVE_API_KEY, YOUR_CONTEXT7_API_KEY 等 placeholders
```

### 3️⃣ 啟動 Claude Code
```bash
claude code
# Claude Code 會自動偵測模板並開始初始化流程
```

### 4️⃣ VibeCoding 7問澄清
回答專案需求問題，獲得 AI 建議，選擇專案結構，自動建置完成！

## 🎨 **三種開發模式**

### 🔥 **心流模式** (預設)
- **觸發**: 說 "快速原型"、"實驗"、"心流"
- **特色**: 完全不打斷，專注創造，忽略品質規範

### 🔄 **整理模式**
- **觸發**: 說 "重構"、"整理"、"優化"
- **特色**: 程式碼品質檢查，結構優化，載入架構範本

### 🛡️ **品質模式**
- **觸發**: 說 "提交"、"部署"、"品質檢查"
- **特色**: 全面品質保證，測試、安全、文檔一條龍服務

## 🤖 **7個專業 Subagent**

| Agent | 專業領域 | 觸發時機 |
|-------|---------|---------|
| **workflow-template-manager** ⭐ | 專案規劃、工作流程管理 | 專案初始化 |
| **code-quality-specialist** 🔍 | 程式碼品質、重構建議 | 整理模式 |
| **test-automation-engineer** 🧪 | 測試自動化、BDD 實作 | 品質模式 |
| **e2e-validation-specialist** 🌐 | 端到端測試、UI 驗證 | 品質模式 |
| **security-infrastructure-auditor** 🔒 | 安全掃描、漏洞分析 | 品質模式 |
| **deployment-operations-engineer** 🚀 | CI/CD、部署策略 | 品質模式 |
| **documentation-specialist** 📚 | API 文檔、技術寫作 | 品質模式 |

## 📁 **專案結構選項**

- **🔹 簡易型** - 原型專案、學習專案、小工具
- **🔹 標準型** - 正式專案、團隊協作、中等複雜度
- **🔹 AI-ML型** - 機器學習、資料科學、AI 應用
- **🔹 客製化** - Claude 基於需求分析建議的專屬結構

## 📚 **文檔資源**

- **📖 [詳細使用指南](TEMPLATE_USAGE_GUIDE.md)** - 完整的模板使用說明
- **🚀 [快速開始](.claude/QUICK_START.md)** - 5分鐘上手指南
- **🏗️ [系統架構](.claude/ARCHITECTURE.md)** - 深入了解設計原理
- **📋 [初始化指南](.claude/PROJECT_INITIALIZATION_GUIDE.md)** - 專案設定詳解

## 🎨 **VibeCoding 範本庫**

內建完整的企業級開發範本：
- 專案簡報與 PRD 範本
- BDD 行為驅動開發指南
- 架構與設計文件範本
- API 設計規格範本
- 模組規格與測試案例
- 安全與就緒檢查清單
- 專案結構指南

## ⚙️ **模板內容結構**

```
📦 Claude Code Universal Template
├── 📄 TEMPLATE_USAGE_GUIDE.md          # 📖 完整使用指南
├── 📄 README.md                        # 🏠 本檔案
├── 📁 Claude Code Starter Template/
│   └── 📄 CLAUDE_TEMPLATE_zh-TW.md     # ⭐ 主初始化模板
├── 📁 .claude/                         # 🤖 Subagent 協作系統
│   ├── 📁 agents/                      # 7個專業 Subagent 配置
│   ├── 📁 context/                     # 上下文管理
│   ├── 📁 coordination/                # 協調機制
│   ├── 📁 templates/                   # 標準化範本
│   └── 📄 settings.local.json          # Claude Code 設定
├── 📁 VibeCoding_Workflow_Templates/   # 🎨 開發範本庫
└── 📄 .mcp.json                        # 🔧 MCP 服務配置
```

## 🌟 **核心優勢**

### ✅ **開發體驗**
- **保護心流** - 創造期完全不打斷，讓靈感自由奔放
- **智能協作** - 在適當時機自動提供專業支援
- **標準化流程** - 企業級品質標準，個人開發效率

### ✅ **技術品質**
- **技術債預防** - Linus 開發心法內建品質 Gate
- **全生命週期** - 從想法到交付的完整支援
- **可複製性** - 每個專案都能享受一致的高品質開發體驗

### ✅ **可擴展性**
- **模組化設計** - 每個組件都可獨立使用或替換
- **範本驅動** - VibeCoding 範本可根據團隊需求客製化
- **多專案適用** - 一次設定，多專案重複使用

## 🚨 **注意事項**

### ⚠️ **使用前必做**
- [ ] 替換 `.mcp.json` 中的 API key placeholders
- [ ] 替換 `.claude/settings.local.json` 中的 API key placeholders
- [ ] 確認 Claude Code 版本支援 MCP 和 Subagent 功能

### ⚠️ **開發建議**
- [ ] 尊重心流模式，不強制品質檢查
- [ ] 在自然檢查點進行品質把關
- [ ] 充分利用各 Subagent 的專業能力

## 📞 **支援與回饋**

- **📋 問題排除**: 查看 [TEMPLATE_USAGE_GUIDE.md](TEMPLATE_USAGE_GUIDE.md#-常見問題排除)
- **📚 進階文檔**: 參考 `.claude/` 目錄下的詳細文檔
- **🔧 客製化**: 根據團隊需求調整 VibeCoding 範本

## 📜 **授權與版本**

- **模板版本**: v2.0
- **更新日期**: 2024-09-23
- **相容性**: Claude Code v1.0+

---

**🎆 開始您的高效率、高品質的 Claude Code 開發之旅！**

> 💡 **提示**: 首次使用建議詳讀 [TEMPLATE_USAGE_GUIDE.md](TEMPLATE_USAGE_GUIDE.md) 以充分發揮模板的強大功能。