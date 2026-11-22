# 台灣早餐店營養學與熱量控制指南 (Breakfast Nutrition Wiki)

[![GitHub Repo](https://img.shields.io/badge/GitHub-briefing--database--Wiki-blue?logo=github)](https://github.com/PENNY7-11/briefing-database-Wiki)
[![LLM Wiki Architecture](https://img.shields.io/badge/Architecture-Karpathy_LLM_Wiki-orange)](#架構說明)
[![Interactive Slides](https://img.shields.io/badge/Slides-slides.html-success)](#-互動教學-html-簡報-slideshtml)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> 針對每天習慣在傳統早餐店外食的大學生與久坐上班族，建立一套結構化的營養知識庫。本專案借鑑 Andrej Karpathy 的 **LLM Wiki** 核心架構，將散亂的早餐熱量數據、營養素知識與健康搭配原則進行 Ingest（攝取）、歸納與交叉連結，以此作為**唯一真實來源（Single Source of Truth, SSOT）**，並由此知識庫自動生成給初學者閱讀的**互動式教學 HTML 簡報 (`slides.html`)**。

---

## 🖥️ 互動教學 HTML 簡報 (`slides.html`)

專案根目錄下附帶獨立、免安裝套件、可直接於任何現代瀏覽器開啟的互動教學簡報 **[slides.html](file:///c:/Users/cutea/OneDrive/桌面/LLM%20Wiki%20Notes/slides.html)**。

### 🌟 簡報亮點功能：
* **逐頁教學引導（共 8 頁）**：遵循「痛點喚醒 $\rightarrow$ 代謝基礎 $\rightarrow$ 地雷拆解 $\rightarrow$ 實戰原則 $\rightarrow$ 互動測驗 $\rightarrow$ 行動清單」教學邏輯。
* **流暢互動操作**：
  * 支援鍵盤 **`&larr;` / `&rarr;` 方向鍵**、`Space`、`PageUp` / `PageDown`、`Home` / `End` 鍵切換。
  * 支援下方按鈕點擊、實時進度條與頁碼顯示。
  * 支援右上角 **全螢幕投影模式 (`⛶`)**。
* **互動隨堂小測驗（第 7 頁）**：內建飲品與主餐改裝即時情境測驗，點擊選項立即彈出對錯標記（`mark_correct.png` / `mark_false.png`）與詳細營養學深度解析。
* **100% 知識來源可追溯**：每頁頁尾皆有專屬標籤，精確標記對應的 `wiki/` 知識庫原始檔名。
* **零破圖保證**：所有插圖與營養素圖卡均嚴格採用 `assets/images/` 實體圖檔渲染。

---

## 🌟 核心理念：為什麼是 LLM Wiki？

傳統 RAG（檢索增強生成）每次提問都是「從零檢索」碎片，沒有累積；而 **LLM Wiki** 則是：
* **持續積累與複利（Compounding）**：新知識會被編織進既有的 Entity（實體）與 Concept（概念）頁面，而非單純堆放檔案。
* **分工明確**：人類擔任**總策展人與架構師**，負責挑選高品質來源並提出好問題；LLM 擔任**維護工程師兼臨床營養顧問**，負責撰寫、交叉引用與健康檢查。
* **IDE 模式**：Obsidian 是檢視與探索的 IDE，Markdown 檔案庫是 Codebase。

---

## 📂 專案目錄結構

```text
LLM Wiki Notes/
├── AGENTS.md               # LLM 知識庫維護憲法與操作指南 (SOP)
├── index.md                # 知識庫總目錄索引 (Content Catalog)
├── log.md                  # 時間軸追加操作日誌 (Append-only Log)
├── README.md               # 專案公開說明文件
├── slides.html             # 【互動教學簡報】免環境依賴、瀏覽器直開 (8頁)
├── raw/                    # 【第一層：不可變真理】原始來源文獻
│   ├── 01_macronutrients_basics.md
│   ├── 02_taiwan_breakfast_categories.md
│   ├── 03_hidden_fat_traps.md
│   ├── 04_beverage_sugar_guide.md
│   └── 05_healthy_combo_formula.md
├── wiki/                   # 【第二層：LLM 維護層】結構化知識庫
│   ├── Concepts/           # 營養學基礎、升糖指數、吸油率、黃金公式
│   ├── Entities/           # 實體庫
│   │   ├── Items/          # 具體餐點（原味蛋餅、豬排蛋吐司、鐵板麵、大冰奶...）
│   │   └── Ingredients/    # 原物料與加工物（台式美乃滋、早餐店奶精、組合肉）
│   ├── Sources/            # raw 資料之結構化摘要
│   └── Syntheses/          # 跨主題綜合指南、外食地雷矩陣、5天減脂輪替菜單
└── assets/                 # 【多媒體與簡報層】圖片素材
    └── images/             # (提供 slides.html 插畫圖示與視覺化元素)
```

---

## 🚀 Ingest 資料清單與對應成果

| 原始來源檔案 (`raw/`) | 主題核心 | 沉澱生成之 Wiki 核心頁面 |
| :--- | :--- | :--- |
| `01_macronutrients_basics.md` | 三大營養素熱量換算與比例原則 | `[[三大巨量營養素與能量代謝]]`、`[[升糖指數與晨間嗜睡]]` |
| `02_taiwan_breakfast_categories.md` | 台式早餐四大類（蛋餅、漢堡吐司、鐵板麵、中式點心）分析 | `[[原味蛋餅]]`、`[[豬排里肌蛋吐司]]`、`[[黑胡椒鐵板麵加蛋]]`、`[[燒餅油條]]` |
| `03_hidden_fat_traps.md` | 早餐店隱形油脂（美乃滋、起酥、吸油率）解析 | `[[台式美乃滋]]`、`[[加工肉品與組合肉]]`、`[[隱形油脂與吸油率機制]]` |
| `04_beverage_sugar_guide.md` | 飲品含糖量、奶精與大冰奶致瀉機制指南 | `[[大冰奶]]`、`[[無糖高纖豆漿]]`、`[[早餐店奶精]]`、`[[大冰奶致瀉機制與反式脂肪]]` |
| `05_healthy_combo_formula.md` | 外食紅綠燈選餐法與 500 大卡黃金公式 | `[[紅綠燈選餐法與外食原則]]`、`[[500大卡黃金早餐公式]]`、`[[外食族早餐四大地雷與避坑指南]]`、`[[大學生與上班族外食5天不重複減脂菜單]]` |

---

## 🚦 外食族三大救命原則（速查）

1. **去醬省 150 卡**：*「老闆，吐司/漢堡完全不要抹沙拉醬（美乃滋）！」*
2. **減油乾烙**：*「老闆，蛋餅少油乾烙，醬油膏分開裝。」*
3. **優質蛋白替換**：*「大冰奶換無糖高纖豆漿或黑咖啡。」*

---

## 🛠️ GitHub 快速同步指令

本專案對應遠端倉庫：`https://github.com/PENNY7-11/briefing-database-Wiki`

若欲將本地檔案同步至 GitHub，可於專案目錄執行：

```bash
git init
git remote add origin https://github.com/PENNY7-11/briefing-database-Wiki.git
git branch -M main
git add .
git commit -m "feat: complete initial ingestion of 5 raw docs, wiki architecture, and slides.html"
git push -u origin main
```
