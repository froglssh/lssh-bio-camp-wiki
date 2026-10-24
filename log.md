# 知識庫時間軸維護日誌 (Log)

本文件依據 **Andrej Karpathy LLM Wiki 協議**，以追加記錄（Append-only）方式記錄本知識庫的所有 Ingest（資料攝入）、Lint（健康檢查）與重大更新歷程。

---

## [2026-10-24] ingest | 建立生物營隊知識庫初始架構與規範
- 依據 Andrej Karpathy LLM Wiki 典範，建立三層架構：原始來源層 (`sources/`)、知識層 (`concepts/`, `entities/`, `sops/`, `chronology/`) 與規範層 (`wiki-rules.md`, `index.md`, `log.md`, `SKILL.md`)。
- 初始化 GitHub 儲存庫 `froglssh/lssh-bio-camp-wiki`，推送主分支並切換至功能分支 `feat/llm-wiki-architecture-and-content`。

## [2026-10-24] ingest | 攝入《生物營隊活動-野外實察課程全紀錄_102-108》
- 深度提煉 102~108 學年度 328 頁總結報告，建立 `sources/SRC_野外實察課程全紀錄_102-108.md`。
- 梳理北海岸、東北角、宜蘭水鳥、太平山霧林帶、三峽森林等經典實察路線。

## [2026-10-24] ingest | 攝入第19屆行動研究雙特優得獎文檔
- 建立 `sources/SRC_行動研究_培訓高中學生擔任生態保育研究志工.md`。
- 建立 `sources/SRC_行動研究_彈性學習公民科學家課程模組教具說明.md`。
- 提取「翻轉打掃志工」、「五階段 80 小時培訓體系」與「3 套實體講義 + 1 數位光碟」教具架構。

## [2026-10-24] ingest | 攝入教學課程七大模組與歷屆活動手冊全集
- 建立 `sources/SRC_教學課程_七大主題講義全集.md`。
- 建立 `sources/SRC_活動手冊歷屆全景彙編.md`。
- 建立 `sources/SRC_106年度前瞻計畫生物營隊心得報告.md`。
- 建立 `sources/SRC_111年度海洋保育巡查員大手牽小手計畫.md`。
- 建立 `sources/SRC_課後問卷與學生反思彙編.md`。

## [2026-10-24] ingest | 建立九大核心概念與教學法筆記 (Concepts)
- 撰寫 `concepts/公民科學家理念與核心素養.md`。
- 撰寫 `concepts/七大模組化教學課程體系.md`。
- 撰寫 `concepts/五階段長程培訓架構.md`。
- 撰寫 `concepts/自然生態導覽與解說藝術.md`。
- 撰寫 `concepts/生態遊戲教案設計方法.md`。
- 撰寫 `concepts/野外實察安全與風險管理.md`。
- 撰寫 `concepts/高中專題研究與野外採集倫理.md`。
- 撰寫 `concepts/多元評量與反思機制.md`。
- 撰寫 `concepts/行動研究經驗轉化與課綱銜接.md`。

## [2026-10-24] ingest | 建立十大實察場域、機構與人物實體筆記 (Entities)
- 撰寫 `entities/場域_東北角馬岡海蝕平台.md`。
- 撰寫 `entities/場域_北海岸石門老梅與麟山鼻.md`。
- 撰寫 `entities/場域_阿里磅生態農場與八煙聚落.md`。
- 撰寫 `entities/場域_宜蘭時潮塭底與蘭陽溪口濕地.md`。
- 撰寫 `entities/場域_宜蘭雙連埤與福山植物園.md`。
- 撰寫 `entities/場域_太平山與翠峰湖高海拔霧林帶.md`。
- 撰寫 `entities/場域_基隆國立海洋科技博物館與潮境公園.md`。
- 撰寫 `entities/場域_麗山生態池與金面山森林保護區.md`。
- 撰寫 `entities/機構_中研院臨海研究站.md`。
- 撰寫 `entities/人物_麗山生物科教師教學社群.md`。

## [2026-10-24] ingest | 建立六大標準作業程序筆記 (SOPs)
- 撰寫 `sops/SOP_野外實察營隊籌辦全流程.md`。
- 撰寫 `sops/SOP_教育部專案計畫申請與經費核銷.md`。
- 撰寫 `sops/SOP_大客車租賃安全檢核與乘車管理.md`。
- 撰寫 `sops/SOP_野外實察野外急救與安全防護SOP.md`。
- 撰寫 `sops/SOP_小組成果發表會與學術海報製作規範.md`。
- 撰寫 `sops/SOP_生態解說員實地演練與評量規準.md`。

## [2026-10-24] ingest | 建立歷屆演進編年史紀實 (Chronology)
- 撰寫 101~111 學年度八大學期紀實（種子萌芽、海報發表、跨校探究、高海拔突破、前瞻 80 小時、行動研究雙特優、新課綱彈性學習、海保署大手牽小手）。

## [2026-10-24] lint | 執行知識庫全域完整度與雙向連結健康檢查
- 檢查全體 44 篇 Markdown 筆記之 YAML Frontmatter 合規性。
- 檢查 `[[WikiLink]]` 雙向鏈結有效性，落實零孤立頁面政策（Zero-Orphan Policy）。
- 驗證 Obsidian Dataview 結構相容性，知識庫建置圓滿達成。
