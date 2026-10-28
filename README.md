# Legge《易經》1882卦爻辭子集：AI影像覆核閱讀版

版本 **0.2.0**；製備日期 **2026-10-28**。整理者：**曲宸宇（Chu, Chen-Yu；GitHub：poplolioi11）**；ORCID：[0009-0003-9738-6914](https://orcid.org/0009-0003-9738-6914)。歷史英文譯者為 **James Legge（理雅各）**，不是本資料集的現代整理者。

## 固定版本與引用

**公開狀態（2026-10-28）：GitHub v0.2.0與Zenodo已正式發布；版本DOI及DataCite狀態已公開讀回為findable。此主分支README與CFF為發布後說明；固定ZIP及tag保留製備時reserved的歷史聲明，不覆寫封存。PACKAGE-SHA256SUMS只驗固定發行包，不套用這兩份後來更新的主分支文件。**

- 固定GitHub發行版：[v0.2.0](https://github.com/poplolioi11/yigua-legge-1882/releases/tag/v0.2.0)。
- 本版DOI：[ 10.5281/zenodo.23723692 ](https://doi.org/10.5281/zenodo.23723692)；全版本DOI：[ 10.5281/zenodo.23585521 ](https://doi.org/10.5281/zenodo.23585521)。
- 此固定包製備時本版DOI為reserved。是否正式發布及登記，請讀公開紀錄；預留號碼不算發布完成。
- 舊版[0.1.1](https://doi.org/10.5281/zenodo.23585522)保留原始檔、tag及署名，不覆寫。

建議資料引用：Chu, Chen-Yu（曲宸宇）. (2026). *Legge's Yî King (1882): Hexagram-Text Subset, AI Image-Collated Reader Edition* (Version 0.2.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.23723692

原書另引：Legge, James, trans. 1882. *The Sacred Books of China: The Texts of Confucianism. Part II. The Yî King*. Sacred Books of the East XVI. Oxford: Clarendon Press. 引用個別段落請附本資料的條目ID、印刷頁與影像連結；例如 `legge-01-line-1`，印刷頁57。CITATION.cff提供引用資訊，不追蹤誰引用。

## 底本、範圍與來源

取文見證為 **Princeton Theological Seminary Library** 藏1882牛津版，InternetArchive識別碼 **sacredbooksofchi16conf**：[館藏／影像](https://archive.org/details/sacredbooksofchi16conf)。目錄的1879為系列記錄；本卷題名頁及copyright-evidence所記1882為本資料版別。

本資料只收 **64卦辭、384爻辭及乾坤各第7段（用九／用六），共450段**，印刷頁57–210的154張影像大字正文。**不是全書**，不收導論、小字注釋、附錄、索引、頁眉、章題或卦圖。頁碼逐條保存；影像位置為印刷頁p對應IA `n(p+33)`，實際來源雜湊與尺寸見影像覆核表。

原始數位文字層是該見證的[IA DjVuXML OCR](https://archive.org/download/sacredbooksofchi16conf/sacredbooksofchi16conf_djvu.xml)，SHA-256為`3e9823f65f22f7679277128649fcc4d1ef53ccf97954d8cb3691e57841022f5b`。只保留範圍內選取片段，不再散布完整OCR或影像。

## 本輪到底校了什麼

2026-10-28另開未見初錄／OCR的影像讀者，逐頁讀完154張影像的指定大字正文，對450段全量對齊，回看差異與高風險項。**全部450條閱讀字串與0.1.1逐字相同**：未發現有足夠影像證據支持改動詞句的差異，不為製造訂正數而改寫原譯。

`legge-1882-image-collation.json`列154頁的影像雜湊／尺寸／定位、450段覆核狀態、9項經正規化後仍須裁定的差異，以及5組尚未解決的印刷／字碼細節。差異主要是引號空白、分段長橫、墨痕及歷史3形羅馬字。Z是已明示的閱讀／搜尋轉寫；Ʒ／Ȝ等近似字不被宣稱為已核定的精確Unicode。self-produced的連字號是編輯保留決策，不稱由單一斷行印面證明其詞彙身分。第65與203頁原印未配對括號照錄，不憑文法補改。

這是 **AI獨立影像讀字與差異覆核**，不是獨立人工雙校、專家覆核、同儕審查、學術定本或測得的準確率。Gemini／Antigravity的兩批有實際模型`gemini-3.8-flash-high`回報；其他使用乾淨Codex子工作階段，要求Sol／Astra，精確底層執行身份與用量未全部由原生介面提供。詳細提示、專用程式及完整私人工作歷程不公開；本包不能完整重跑從影像到初讀的所有步驟。

64卦辭仍保留2026-10-09的歷史稽核檔，當時最初匯入途徑未留存；本輪新核對不會反向捏造早期來源。既有31項OCR校改／邊界紀錄保留為舊版歷史，不冒充本輪新訂正。

## 檔案及文字層

- `legge-1882.json`：閱讀文字、原OCR、頁片段、來源、註記、版本及品質；`text`與`sourceText`不可混用。
- `legge-1882.txt`：直接閱讀的完整450段，導航標題是現代編者metadata。
- `legge-1882.tei.xml`：由同一固定資料衍生，含閱讀層／OCR層／跨頁片段與metadata快照；不是另一份模型重寫稿，也不是完整外交式轉錄。
- `legge-1882-provenance.json`：版本、來源、分層權利、AI使用與歷史校改。
- `legge-1882-image-collation.json`：本輪覆核範圍、差異、影像定位與未解細節。
- `legge-source-audit.json`：2026-10-09歷史卦辭核對，原樣保存。
- `VALIDATION.json`、manifests與SHA256SUMS：結構、往返與固定包完整性證據；不是文本正確認證。

原OCR層保持舊版原狀，包含辨識錯誤。閱讀層沿用已明示的空白／標點間距正規化、斷行接詞、部分羅馬字去音標及3形字轉Z。需要精確字形、字頻、訓詁或引文者應回查原頁及未解紀錄；不把此閱讀層當逐字外交本。

## 權利與機構關係

1882歷史英文譯文為公有領域，本站不增加署名、商用或改作限制。IA項目公開copyright-evidence／NOT_IN_COPYRIGHT（US）為所核來源證據，不是所有司法管轄的法律認證。**CC BY 4.0僅適用於具有著作權且由整理者持有的原創現代說明、metadata及編排**，不重新限制古籍原文。來源影像另有館藏／平台脈絡，只附連結，不含於此包。請求以「yigua.art網站轉譯／曲宸宇（poplolioi11）」保留處理來源，並非對公有領域文字增設條件。詳見LICENSE。

館方已在該IA館藏Notes欄加入舊版DOI連結，明示只是資訊連結，**不代表館方背書、校定、合作或新授權**。本計畫與Princeton無此等機構關係。

## 驗證、更正與版本維護

固定TEIP5 **4.12.0**的官方`tei_all.rng` SHA-256為`b0f115095ead2ccc6933aa3365c6f4a82cba3b2ec7eee7f76bb616d7a63b7e48`；執行安全XML解析、RelaxNG、JSON／TXT／TEI全450段逐字往返，以及錯字／掉爻／錯序／來源更動／重複ID／外部entity負向測試。CFF依官方1.2.0完整schema驗證。**未做Schematron、自訂ODD、人類／專家校訂或完整異文校勘本**。

下載固定ZIP後可用 `shasum -a 256 -c PACKAGE-SHA256SUMS`檢查；checksum只證明固定bytes。公開庫保持[Issues](https://github.com/poplolioi11/yigua-legge-1882/issues)開啟，訂正請提供ID、原頁、影像連結、待改字串、候選與證據。資料／編碼變更另發新版，保留舊版；後來main文件更新不重寫固定發行包。

研究入口：易經英譯、理雅各、漢學史、翻譯研究；I Ching、James Legge、Sinology、translation studies、historical English translation、digital humanities、TEI XML。分類來自本卷與實際檔案，不代表已回答所有研究問題。

## English summary

Prepared by **Chen-Yu Chu** (曲宸宇; GitHub **poplolioi11**), ORCID 0009-0003-9738-6914. This **450-passage subset**, not the entire book, now has complete scoped **AI independent image reading and adjudication** across printed pp. 57–210. All reader strings remain unchanged from v0.1.1. Nine non-equivalent comparison items have explicit dispositions; five grouped typography/encoding details remain unresolved. This is **not human/expert collation, a diplomatic edition, peer review or an accuracy certification**. Public-domain historical text is unrestricted; CC BY 4.0 applies only to copyrightable original modern editorial material. Images, private code, prompts and detailed internal workflow are excluded. Cite the fixed version DOI together with Legge1882, the printed page and passage ID.
