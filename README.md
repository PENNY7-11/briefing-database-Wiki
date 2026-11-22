# 台灣早餐店營養學與熱量控制指南 (Breakfast Nutrition Wiki)

[![GitHub Repo](https://img.shields.io/badge/GitHub-breakfast__wiki-blue?logo=github)](https://github.com/PENNY7-11/breakfast_wiki)
[![LLM Wiki Architecture](https://img.shields.io/badge/Architecture-Karpathy_LLM_Wiki-orange)](#架構說明)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> 針對每天習慣在傳統早餐店外食的大學生與久坐上班族，建立一套結構化的營養知識庫。本專案借鑑 Andrej Karpathy 的 **LLM Wiki** 核心架構，將散亂的早餐熱量數據、營養素知識與健康搭配原則進行 Ingest（攝取）、歸納與交叉連結，以此作為**唯一真實來源（Single Source of Truth, SSOT）**，並支援自動轉譯生成初學者互動式教學 HTML 簡報。

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
├── README.md               # 專案說明文件
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
└── assets/                 # 【多媒體與簡報層】圖片素材（供後續 HTML 簡報渲染）
    └── images/
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

本專案對應遠端倉庫：`https://github.com/PENNY7-11/breakfast_wiki`

若欲將本地檔案同步至 GitHub，可於專案目錄執行：

```bash
git init
git remote add origin https://github.com/PENNY7-11/breakfast_wiki.git
git branch -M main
git add .
git commit -m "feat: complete initial ingestion of 5 raw docs, wiki architecture, and AGENTS.md"
git push -u origin main
```
