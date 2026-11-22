# 知識庫時間軸日誌 (Knowledge Base Log)

本檔案為 append-only 格式之活動記錄，記錄所有文獻歸檔 (ingest)、深入探討與綜述 (query/synthesize)、結構體檢 (lint) 與簡報生成 (presentation) 的操作軌跡。

---

## [2026-11-22] init | 知識庫系統初始化
* 建立專案規範指南 `AGENTS.md`，定義 Karpathy LLM Wiki 運作哲學、Obsidian 雙向連結語法與 Frontmatter 規範。
* 設定主題為「台灣外食族早餐營養學與熱量控制指南」。
* 初始化目錄結構：`raw/papers/`, `wiki/sources/`, `wiki/concepts/`, `wiki/methods/`, `wiki/syntheses/`, `wiki/presentations/`。
* 建立目錄索引 `wiki/index.md` 與首批預備核心概念/方法詞庫。

## [2026-11-22] ingest | 你早餐吃對了嗎？由鄧雯心醫師來公開地雷早餐大破解！
* 來源文件：`raw/papers/你早餐吃對了嗎？由鄧雯心醫師來公開地雷早餐大破解！.pdf`
* 新建來源文獻頁面：`wiki/sources/你早餐吃對了嗎-鄧雯心醫師.md`
* 新建核心概念頁面：
  - `wiki/concepts/胰島素阻抗與早餐升糖反應.md`
  - `wiki/concepts/磨粉澱粉與液態糖吸收動力學.md`
  - `wiki/concepts/飽足感指數與食慾激素.md`
  - `wiki/concepts/隱藏油脂與低營養價值脂肪.md`
* 新建實務方法頁面：
  - `wiki/methods/外食族211晨間餐盤實踐法.md`
  - `wiki/methods/水肉菜飯果進食順序法.md`
  - `wiki/methods/常見外食早餐地雷改造SOP.md`
* 更新索引：`wiki/index.md`

## [2026-11-22] batch-ingest | 全數文獻自動依序歸檔完畢 (共 5 份文獻)
* 處理來源 1：`raw/papers/分析市售含糖飲料的含糖量及對健康的影響.pdf`
  - 新建來源頁面：`wiki/sources/市售含糖飲料含糖量及健康影響-秀傳醫學雜誌.md`
  - 新建/更新概念：`wiki/concepts/液態游離糖與脂質新生DNL.md`
  - 新建方法：`wiki/methods/外食早餐飲品降階減糖法.md`
* 處理來源 2：`raw/papers/早餐地雷組合當心！醫曝「就是在吃油」　爆卡還吃不飽.pdf`
  - 新建來源頁面：`wiki/sources/早餐地雷組合當心-許哲源醫師.md`
  - 新建/更新概念：`wiki/concepts/高溫油脂吸附與煎台熱量炸彈.md`
  - 新建方法：`wiki/methods/中式早餐低油避坑與點餐指南.md`
* 處理來源 3：`raw/papers/早餐店熱量最低是它們！吃早午餐熱量比較低？營養師教你3點健康吃法 悠活原力YohoPower.pdf`
  - 新建來源頁面：`wiki/sources/早餐店熱量最低是它們-李依縉營養師.md`
  - 新建方法：`wiki/methods/早午餐Brunch均衡挑選法.md`
* 處理來源 4：`raw/papers/我的餐盤手冊（全穀及未精製雜糧）v2.pdf`
  - 新建來源頁面：`wiki/sources/我的餐盤手冊-國健署.md`
  - 新建方法：`wiki/methods/國健署六口訣外食速算拳掌法.md`
* 處理來源 5：`raw/papers/每日飲食指南手冊.pdf`
  - 新建來源頁面：`wiki/sources/每日飲食指南手冊-國健署.md`
  - 新建/更新概念：`wiki/concepts/全穀雜糧與精製澱粉代謝差異.md`、`wiki/concepts/六大類食物與宏量營養素平衡.md`
* 全面更新目錄總覽：`wiki/index.md`，建立高密度雙向連結網。

## [2026-11-22] presentation | 產出外食早餐指南互動式 HTML 簡報
* 輸出檔案：`wiki/presentations/外食早餐指南簡報.html`
* 整合素材：引用 `assets/images/` 內 15+ 張高解析插畫與貼圖（包含餐盤、漢堡男孩、珍珠奶茶、炸物、三大營養素、水瓶、咖啡等）。
* 涵蓋篇章：
  - Slide 1: 封面與核心主題
  - Slide 2: 現況痛點與「亂吃比不吃更傷身」
  - Slide 3: 血糖風暴與磨粉破壁爆醣機制
  - Slide 4: 飲品殺手 - 果糖與肝臟脂質新生 (DNL)
  - Slide 5: 早餐店吸油真相 - 鐵板麵、蘿蔔糕與燒餅油條
  - Slide 6: 官方標準 - 衛福部三大營養素黃金佔比
  - Slide 7: 隨身量尺 - 國健署餐盤六口訣與拳掌速算法
  - Slide 8: 減脂黃金法則 - 211 餐盤與水肉菜飯果順序
  - Slide 9: 實戰改造 - 6 大典型地雷對照表格
  - Slide 10: 場景攻防 - 超商 500 kcal 盤 vs 中式豆漿店低油點餐
  - Slide 11: 飲品革命 - 四階段降階戒糖法
  - Slide 12: 總結宣言 - 外食早餐 10 秒檢核清單
* 更新索引：`wiki/index.md` 成果專區。

## [2026-11-23] update | 修正 HTML 簡報排版與配圖
* 修改檔案：`wiki/presentations/外食早餐指南簡報.html`
* 修正項目：
  1. Slide 4：移除警示框的 flex 橫向分欄屬性，改為 block 連貫文字排版，修正「100% 果汁陷阱」文字被切成多欄的問題。
  2. Slide 6：將「醣類 (50~60%)」的小圖示更正為代表碳水化合物的 `Carbohydrate.jpg`。
  3. Slide 12：將總結頁右側配圖更換為更具親和力與肯定感的 `animal_quiz_true.png`。
