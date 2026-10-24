# 麗山高中生物營隊與公民科學家 Wiki 規範 (Wiki Rules)

本文件定義本知識庫（LLM Wiki）的體系結構、命名準則、元數據 (YAML Frontmatter) 規範以及 AI 維護工作流。本知識庫嚴格遵循 **Andrej Karpathy LLM Wiki 架構原則**，旨在沉澱麗山高中生物科十餘年累積之「野外實察、解說員培訓、公民科學家課程模組與行動研究」無形資產，實現長期、可累積、高檢索效率的校本智慧管理系統。

---

## 1. 知識庫目錄架構 (Directory Architecture)

Wiki 根目錄位於 `生物營隊知識庫/`，下轄五大專屬維度目錄與系統檔案：

```
生物營隊知識庫/
├── index.md        # 全域主索引（Knowledge Map 與多角色入口）
├── log.md          # 時間軸日誌（記錄所有 Ingest、Lint、Update 歷程）
├── wiki-rules.md   # Wiki 規範與 Schema 定義文件
├── SKILL.md        # 麗山生物營隊與公民科學家工作助理 Skill
├── sources/        # 原始文件之結構化提煉筆記（含原始檔案本機路徑 file:///）
├── concepts/       # 核心概念、模式理論、模組化課程體系、評量規準
├── entities/       # 實察場域、地景生態、物種多樣性、合作單位、關鍵人物
├── sops/           # 標準作業程序（行政申辦、租車安全、實察踩線、海報發表、解說考核）
└── chronology/     # 歷屆年表紀實（101~111 學年度全景演進與歷史對比）
```

---

## 2. YAML Frontmatter 規範 (Dataview Ready)

所有 Markdown 文件頂部必須包含標準 YAML Frontmatter，以確保相容 Obsidian Dataview 插件與大語言模型結構化檢索：

### 2.1 來源筆記 (Source Note)
```yaml
---
type: source
title: "原始文件完整標題"
author: "作者或發布單位"
year: 2026
file_path: "file:///Users/froglssh/Library/CloudStorage/GoogleDrive-frog@lssh.tp.edu.tw/我的雲端硬碟/12生物營隊/..."
tags: [生物營隊, 野外實察, 原始資料, 公民科學家]
created: 2026-10-24
last_modified: 2026-10-24
---
```

### 2.2 概念筆記 (Concept Note)
```yaml
---
type: concept
aliases: [別名1, 別名2]
tags: [核心素養, 課程模組, 解說藝術, 安全防護]
sources: ["`[[來源筆記名稱]]`"]
created: 2026-10-24
last_modified: 2026-10-24
---
```

### 2.3 實體筆記 (Entity Note)
```yaml
---
type: entity
aliases: [英文名稱, 簡稱, 地理編號]
tags: [實察場域, 潮間帶, 高海拔霧林, 合作機構, 人物]
sources: ["`[[來源筆記名稱]]`"]
created: 2026-10-24
last_modified: 2026-10-24
---
```

### 2.4 標準作業程序筆記 (SOP Note)
```yaml
---
type: sop
aliases: [標準流程, 作業手冊]
tags: [SOP, 行政申辦, 租車安全, 成果驗收]
sources: ["`[[來源筆記名稱]]`"]
created: 2026-10-24
last_modified: 2026-10-24
---
```

### 2.5 編年史紀實筆記 (Chronology Note)
```yaml
---
type: chronology
year: 2017
academic_year: 106
aliases: [年度全景, 營隊紀實]
tags: [編年史, 106學年度, 前瞻計畫]
sources: ["`[[來源筆記名稱]]`"]
created: 2026-10-24
last_modified: 2026-10-24
---
```

---

## 3. 雙向連結與語意網絡 (Bi-directional Linking)

1. **嚴格使用雙括號語法**：所有概念、實體、來源與 SOP 的引用必須採用 `[[` 頁面名稱 `]]`。
2. **事實陳述追溯律**：概念或紀實頁面中任何關鍵數據（預算金額、時數、參與人次、得獎項目、路線細流），必須在句尾附上雙向連結引文（如 `[[SRC_行動研究_培訓高中學生擔任生態保育研究志工]]`）。
3. **零孤立頁面 (Zero-Orphan Policy)**：新建立的筆記必須在 `index.md` 註冊，且至少被 1 個以上相關頁面反向連結。

---

## 4. AI 增量維護工作流 (Karpathy Protocol)

### 4.1 Ingest 工作流（攝入新文件）
當使用者提供新的營隊計畫書、學生報告、活動照片或核銷簽呈時：
1. **讀取原始文件**：提取關鍵時間、地點、人名、課程目標、預算與成效數據。
2. **建立 Source Note**：在 `sources/` 建立摘要筆記，包含 `file_path` 超連結與主要發現。
3. **分發更新各知識維度**：
   - 更新或新增 `concepts/` 中的課程主題與教學法。
   - 更新或新增 `entities/` 中的場域物種與單位紀錄。
   - 更新或新增 `chronology/` 中的學年度大事記，保留演進脈絡。
4. **註冊與日誌**：更新 `index.md` 並於 `log.md` 寫入一行標準紀錄：
   `## [YYYY-MM-DD] ingest | 攝入文件標題`。

### 4.2 Query 工作流（精準查詢與合成）
當使用者詢問營隊設計、行政流程或教學經驗時：
1. 先閱讀 `index.md` 鎖定核心主題節點。
2. 進入對應的 `concepts/`、`entities/`、`sops/` 提取高濃度知識。
3. 若為深層問題，透過 `sources/` 溯源比對原始文件真實數據。
4. 合成結構清晰、引用完整的專業解答。

### 4.3 Lint 工作流（知識庫健康檢查）
定期或每次重大更新後執行：
1. 檢查是否存在死連結（指向不存在的 `[[頁面]]`）。
2. 檢查是否有未在 `index.md` 登記的孤立頁面。
3. 檢查 Frontmatter 是否完整合規。
4. 於 `log.md` 寫入：`## [YYYY-MM-DD] lint | 執行知識庫健康檢查，修復 X 處問題`。
