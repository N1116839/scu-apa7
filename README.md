# 東吳企管 APA7 中英引用修正

[**下載最新版與安裝說明**](https://github.com/N1116839/scu-apa7/releases/latest)

[**直接下載 scu-apa7.xpi**](https://github.com/N1116839/scu-apa7/releases/latest/download/scu-apa7.xpi)

只需下載 XPI，不用解壓縮，不需另外安裝 CSL；GitHub 的 Source code 不是安裝檔。

## 安裝

1. 適用 Windows、Zotero 10.0.x；目前實機測試版本為 10.0.8。
2. 開啟 Zotero → 工具 → 附加元件，將下載的 XPI 拖入視窗安裝。
3. 關閉 Zotero 全部視窗，再重新開啟。
4. Word → Zotero → Document Preferences，選「東吳企管碩專 APA7 中英混排（修正版）」，按 OK，再按 Refresh。

## 1.0.9 字型更新

外掛以 **12 點**輸出引用（Word 最終字型須依下方設定）：中文與全形標點使用 **標楷體**，英文與數字使用 **Times New Roman**。涵蓋括號式與敘述式引用。

已安裝舊版者：下載同名 XPI → 在 Zotero「工具 → 附加元件」拖入更新 → 關閉全部 Zotero 視窗後重開 → 回到 Word 測試副本按 Refresh。引用字型只處理引用欄位，正文的其他文字仍由 Word 樣式管理。

## Word 請使用欄位（避免書目斜體消失）

在 Word → Zotero → Document Preferences → 進階選項，**取消勾選「引用文獻儲存為書籤」**，使用 Fields（欄位）。保持「東吳企管碩專 APA7 中英混排（修正版）」後按 OK，再按 Refresh。

既有論文若原本使用書籤，先另存副本，再於副本取消該選項，讓 Zotero 轉換既有引用並重新整理；不需逐筆重插。2026-11-08 已在使用者文件副本確認：原書籤模式的書目斜體消失，轉成欄位並重新整理後，書名、期刊名與卷數斜體恢復。僅需與 LibreOffice 協作時才考慮書籤模式；[Zotero 官方也建議 Word 使用欄位](https://www.zotero.org/support/word_processor_plugin_usage#document_preferences)。

## Word 字型設定（重要）

2026-11-08 實機核對補充：Zotero 的 Word 端在插入 RTF 後會還原既有字型，參考文獻還會重新套用 Bibliography 樣式。僅在外掛的 RTF 指定字型，不能保證 Word 最後保留；1.0.9 的原生 RTF 測試未涵蓋此 Word 端步驟。

要讓參考文獻在 Refresh 後維持論文字型，請在 Word 設定一次：

1. 游標點進任一筆參考文獻。
2. 「常用 → 樣式」開啟樣式窗格（Ctrl＋Alt＋Shift＋S），找到目前使用的 **Bibliography／書目／參考書目**，右鍵選「修改」。
3. 左下「格式 → 字型」：**中文字型選標楷體；英文字型選 Times New Roman；字級選 12 點**。
4. 選「僅限此文件」，確定後按 Zotero → Refresh。

內文引用的最終字型同樣受 Word 的 Normal／常規樣式及既有直接字型設定影響；需要時在對應樣式設定同一組中文字型、英文字型與 12 點。書目修改只針對字型與字級，保留文獻個別斜體。

[Zotero 官方字型說明](https://www.zotero.org/support/kb/word_default_font)

## 引用與參考文獻

- 中文全形引文與書目標點；英文半形、三位以上作者 et al.。
- 作者（年份）指出：新增／編輯引用 → 點文獻泡泡 → 勾「敘述式：作者（年份）」，在引用外輸入「指出，……」。單篇文獻可有多位作者，多篇合併引用時此選項停用。
- 中文參考文獻在前、依正體中文筆畫；英文在後、依 A–Z。
- 書目目標版面參照東吳企管碩專範本（字型請設定 Word 書目樣式）：標楷體／Times New Roman、12 點、左右對齊、凸排約 1 公分、單行、段前後各 6 點，保留斜體。

## 狀態與來源

1.0.9 已通過原生引用欄位與 Windows RTF 字型／字級測試，以及原有 31 項格式與啟停回歸；尚待使用者在 Word 實際更新驗證。

此為個人修正版，非學校或 Zotero 官方發行。請先用文件副本測試。已在 Zotero 10.0.8 啟動並通過內建自測；Word 截圖確認中文全形、英文 et al.、中文在前英文在後與斜體。敘述式、完整筆畫順序與精確版面已通過程式或原生 RTF 測試，尚待使用者逐項完成 Word 實測。

CSL 基礎來自 Pulipuli Chen 的中英文 APA7 樣式；原作者與 CC0 宣告保留於樣式內。外掛程式標示 MIT。
