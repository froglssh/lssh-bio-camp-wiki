# 麗山高中生物營隊與公民科學家知識庫 (LSSH Biology Camp & Citizen Scientist Wiki)

本儲存庫為**臺北市立麗山高級中學 生物科**「生物營隊、野外實察與公民科學家課程」之專屬 LLM 知識庫（LLM Wiki）。  
架構嚴格依據 **Andrej Karpathy LLM Wiki 典範** 設計，具備三層架構（原始來源層、Wiki 知識層、規範與 Schema 層），支援 Obsidian Dataview 結構化檢索與大語言模型（LLM）的 Ingest、Query、Lint 持續增量維護。

## 知識庫架構

```
生物營隊知識庫/
├── index.md        # 全域主索引（Knowledge Map 與多角色入口）
├── log.md          # 時間軸日誌（記錄所有 Ingest、Lint、Update 歷程）
├── wiki-rules.md   # Wiki 規範與 Schema 定義文件
├── SKILL.md        # 麗山高中生物營隊與公民科學家工作助理 Skill
├── sources/        # 原始文件之結構化提煉筆記（含原始檔案本機路徑 file:///）
├── concepts/       # 核心概念、教學法、模組化課程體系、評量規準
├── entities/       # 實察場域、地質地景、特色物種、合作單位、關鍵人物
├── sops/           # 標準作業程序（行政申辦、租車安全、實察踩線、海報發表）
└── chronology/     # 歷屆年表紀實（101~111 學年度全景演進）
```
