# Legge《易經》1882：卦爻辭子集初錄

版本：0.1.1（2026-10-23）
整理與維護：poplolioi11／一卦 yigua.art

語料版、TEI 編碼版與封存包版：0.1.1，已於 2026-10-23 正式公開。

- 固定發行版：[GitHub v0.1.1](https://github.com/poplolioi11/yigua-legge-1882/releases/tag/v0.1.1)。
- 版本 DOI：[10.5281/zenodo.23585522](https://doi.org/10.5281/zenodo.23585522)，供引用本次固定資料。
- 全版本 DOI：[10.5281/zenodo.23585521](https://doi.org/10.5281/zenodo.23585521)，供介紹持續維護的資料系列。
- [Zenodo 公開紀錄](https://zenodo.org/records/23585522)。兩個 DOI 已查得 DataCite `findable`；公開檔案已下載回讀並核對 SHA-256。這些是發布與傳輸驗證，不是文字準確度或學術審查證明。

版本 0.1.1 只修正來源層兩個章題抽取邊界及公開文件，450 條閱讀正文與 0.1.0 逐字相同；未新增影像校對。固定發行包中的文件保留「製備時 DOI 已預留、尚未發布」的歷史狀態；本段為發布後的主分支說明，不反向改寫封存檔案。

本資料包含 64 條卦辭、384 條爻辭，以及乾、坤各一段附加文字，共 450 條。Legge 將後兩段分別列作乾、坤的第 7 段；本站以「用九／用六」對應。這是印刷頁 57–210 的卦爻辭子集，不是全書，不包含小字注解、導論或附錄。

## 底本與引用

James Legge, trans. *The Sacred Books of China: The Texts of Confucianism. Part II. The Yî King*. *The Sacred Books of the East*, vol. XVI. Oxford: Clarendon Press, 1882.

底本為 [Princeton Theological Seminary Library 藏本之 Internet Archive 掃描](https://archive.org/details/sacredbooksofchi16conf)。新匯入的文字來源是該項目的 [DjVu XML OCR](https://archive.org/download/sacredbooksofchi16conf/sacredbooksofchi16conf_djvu.xml)，不是自行逐字影像轉錄，也未改用其他版次。原始 OCR 完整檔的 SHA-256、下載日期與段落定位見 `legge-1882-provenance.json`。印刷頁 p 對應 IA viewer n(p+33)、一開始計數的 PDF 第 p+34 頁；每條保留所有跨頁連結。

建議資料引用：poplolioi11／一卦 yigua.art 整理，〈Legge《易經》1882 卦爻辭子集：OCR 輔助初錄〉，版本 0.1.1，2026-10-23，https://doi.org/10.5281/zenodo.23585522。引用個別文字時另列 James Legge、1882、印刷頁碼與條目 ID。不虛構正式學術審查或機構背書。

## 來源層、閱讀層與新增標籤

- `sourceText`／`sourceSegments`：從 IA OCR 選出的正文 token。OCR 行內 token 以空格連接，行間與段間保留換行；排除數字段號、章題及小字注解。仍保留 OCR 誤字，不是原刻的外交式轉錄，也不是完整 OCR XML。`sourceSegments` 保留印刷頁邊界。
- `text`：閱讀顯示層。384 爻辭與 2 附加段由此次 OCR 初錄整理；收合空白及標點前空格、合併斷行分字，保留 `long-continued`、`self-produced` 的詞內連字號。定點看圖後的字詞修正另外列入校改表，不覆蓋 OCR 層。羅馬字顯示可簡化重音、斜體及 3 形歷史字母為 Z；不是新翻譯。
- 64 條卦辭的 `text` 完全保留本站原有 `en-legge.ts` 字串及 `legge-source-audit.json` 所記 2026-10-09 原頁校核；該舊資料的最初匯入來源未記錄。此次補充同底本 OCR 層，不能反過來宣稱舊字串最初就是從此次 OCR 匯入。
- `heading` 是本站新增導航標籤，例如 `Line 1 · Nine, undivided`、`Use Nine`，不是 Legge 原刻標題。原爻辭完整的敘述首句仍保存在 `text`，沒有為了介面而刪掉。
- `name`、`title` 是 Legge 羅馬字卦名的簡化顯示；網站另有的英文義名導航標籤不是此古籍正文或 Legge 逐字章題。

## 品質與覆核邊界

此版狀態是 **OCR 輔助結構化初錄，做過 AI 定點影像抽核，未全面逐字影像覆核，也未經獨立人工二校**。範圍完整與文字準確度是兩件事。程式檢查了 450 條結構、卦序、爻序、頁碼、特殊段與輸出一致性；這些檢查不能替代讀字校對。

此次助手為 OpenAI Codex；工作介面未提供可確證的底層模型版本，所以不猜填模型名稱。IA OCR 的引擎及版本未在本次匯入中確定。AI 做來源調查、OCR 段落分類、定點看圖與編輯記錄，固定文字轉換則由程式完成；未宣稱人工校讀。私人助手紀錄與工作腳本不在公開包。

既有初錄開啟並定點檢視 29 張印刷頁影像：58、61、65、75、90、100、108、115、123、125、127、132、133、135、145、150、153、155、158、160、171、188、190、200、203、205、208、209、210。這份清單只表示檢視了選定字句、正文／注解邊界或跨頁續文，不代表這 29 頁每字已覆核。校改表現有 31 項紀錄：9 項抽取邊界調整、22 項閱讀層字詞／標點修正。0.1.1 新增的兩項只移除第 31、52 卦來源層中的純章題段，不提高影像覆核範圍。

原刻第 65 頁第二爻 `admitting (even` 的開括號，以及第 203 頁第六爻 `situation)` 的閉括號不成對；按本次所見原頁保留，未以現代文法猜補。未留下已知無法辨識而被猜填的字；但無疑字標記不等於逐字確定，未抽核部分仍可能有 OCR、標點或字形錯誤。此版不是嚴格保留全部原刻字形與版式的外交式轉錄。

## 檔案與驗證

- `legge-1882.json`：全資料、來源層、閱讀層、頁碼與完整 metadata。
- `legge-1882.txt`：供直接閱讀的閱讀層；導航、來源連結、編輯註與正文分開。
- `legge-1882.tei.xml`：從同一固定 JSON 資料生成的 TEI P5；非另抄一份正文。`ab[@type='reader']` 保存閱讀層，`ab[@type='source-ocr']` 保存 OCR 字串，`ab[@type='source-ocr-segment']` 保存原頁分段，`ref[@type='printed-page']` 保存來源連結。`xenoData` 內嵌完整 provenance JSON 快照。
- `legge-1882-provenance.json`：書目、權利、方法、品質邊界與校改表。
- `legge-source-audit.json`：2026-10-09 的 64 條既有卦辭來源稽核、原頁與字形正規化紀錄；保留原紀錄，不改稱此次新做校對。
- `legge-1882-manifest.json`、`legge-1882-SHA256SUMS`：固定輸出檔案大小與 SHA-256。

TEI 使用固定 [TEI P5 4.12.0 `tei_all.rng`](https://www.tei-c.org/Vault/P5/4.12.0/xml/tei/custom/schema/relaxng/tei_all.rng)，SHA-256：`b0f115095ead2ccc6933aa3365c6f4a82cba3b2ec7eee7f76bb616d7a63b7e48`。本次從已有固定版官方 schema 快取離線驗證並重新計算雜湊；即時下載逾時不被算作成功。schema 不隨此文字包重新授權。

驗證包含安全 XML 解析（禁止 DTD／外部 entity）、TEI Relax NG、450 個 ID 唯一且依序、64×6 爻與 2 特殊段、JSON／TXT／TEI 的正文、OCR、原頁分段、來源連結與 metadata 逐字回讀。使用寬泛 `tei_all` 後另驗本資料契約。未做 Schematron、自訂 ODD、全面異文表或 TEI 機構認證。

## 權利分層

1882 年的歷史英文翻譯屬公有領域；本站不對這些原文附加 CC 限制。IA 原項目 copyright-evidence 的 `NOT_IN_COPYRIGHT` 是美國範圍的來源證據，不等於對全球所有司法管轄區作法律保證。

具有新著作權的本站原創 metadata、編輯說明與編排採 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)，署名 poplolioi11／一卦 yigua.art；不涵蓋也不重新限制古籍公有領域文字。來源影像只提供連結，不在此包重發；收藏機構／影像平台條款另論。

此版沒有匯入 Wikisource 的現代貢獻文字或編排，所以不把它們改標本站 CC BY。若後續改採 Wikisource，須另記固定 revision、貢獻者來源及適用的署名／相同方式分享條件。

## 公開包文件與校驗

本隔離包另附 LICENSE（分層權利）、CITATION.cff（資料集引用）、CONTRIBUTING.md（更正證據）、CHANGELOG.md（版本差異）及 VALIDATION.json（公開驗證摘要）。CFF 的作者欄是現代整理者，歷史英文譯者 James Legge 另於摘要、底本書目及 TEI 責任聲明列明。

在固定發行包的目錄內可使用 `shasum -a 256 -c PACKAGE-SHA256SUMS` 檢查整包位元完整性；`shasum -a 256 -c legge-1882-SHA256SUMS` 檢查六個固定資料／說明輸出。PACKAGE-MANIFEST.json 記錄其餘候選檔的大小與 SHA-256，避免自行校驗循環。主分支的 README 與 CITATION.cff 已於發布後補齊正式 DOI 狀態，不在舊校驗表的驗證對象內；若要驗整包，請下載 v0.1.1 的固定 ZIP，不以主分支文件替換其中檔案。這些校驗值只檢查檔案完整性，不驗讀字準確。官方 TEI schema 的版本、網址及 SHA-256 已列上方；schema 不包含於本包。

這份 README 與校驗表對應製備時固定包；日後 GitHub 主分支的文件若持續更新，不表示舊封存包的校驗值也隨之變更。專用處理與驗收腳本未公開，故本包只宣稱所列的實際回讀與驗證結果，不承諾從原圖完整重跑。

## 更正與後續版本

請經一卦網站提供的聯絡／問題回報入口，附條目 ID、印刷頁、原頁連結、待改字串及理由。後續版本應保留原始 OCR，另更新閱讀層、校改表與校核範圍；有獨立人工覆核時另記實際人員、日期與覆蓋項目，不將 AI 互相比對改稱人工二校。

公開庫的 [Issues](https://github.com/poplolioi11/yigua-legge-1882/issues) 已開啟，可附證據回報；CONTRIBUTING.md 說明所需證據。公開成果包含文字、來源、疑字／訂正成果與驗證摘要；專用處理程式、提示詞、完整助手工作紀錄、工作影像、上游完整 OCR 及網站程式不隨包發布。本包不承諾從原圖完整重跑未公開的處理程序。

## English scholarly abstract

This dataset presents a structured subset of James Legge’s *The Sacred Books of China: The Texts of Confucianism. Part II. The Yî King* (Oxford: Clarendon Press, 1882), volume XVI of *The Sacred Books of the East*. Its witness is the Princeton Theological Seminary Library copy digitized by Internet Archive under the identifier `sacredbooksofchi16conf`. The subset comprises 64 judgments, 384 line passages, and the additional seventh paragraphs of hexagrams 1 and 2, conventionally associated here with “Use Nine” and “Use Six”: 450 passages from printed pages 57–210. It is not the complete book; the introduction, small-print commentaries, appendices, and index are excluded.

The source layer records selected tokens from the witness’s existing DjVu XML OCR, with page-specific segments and a checksum for the complete upstream file. It retains OCR misreadings and is neither a diplomatic transcription nor a facsimile. The separate reader layer normalizes spacing and line-break hyphenation and records targeted corrections. The existing 64 judgment strings are retained unchanged from the site’s earlier reader and its dated source audit. Their original ingestion was not recorded; the present OCR import must not be represented as evidence of that earlier ingestion.

This is an OCR-assisted initial transcription. AI inspected selected phrases, boundaries, or continuations on 29 page images; this does not establish whole-page or whole-text proofreading. No independent human second collation is claimed. Structural validation and JSON/TXT/TEI round trips establish consistency, not textual accuracy. Residual errors may remain. Modern passage headings and the site’s short English navigation glosses are editorial interface metadata, not quotations from Legge’s chapter titles or a new historical translation.

The 1882 historical translation is public-domain material, without additional Creative Commons restrictions imposed by this dataset. CC BY 4.0 applies only to copyrightable original modern metadata, documentation, and arrangement, attributed to poplolioi11 / 一卦 yigua.art. Linked images retain their separate institutional and platform context; they are not redistributed here.

Suggested citation: poplolioi11 / 一卦 yigua.art, ed., “Legge’s *Yî King* (1882): Hexagram-Text Subset, OCR-Assisted Initial Transcription,” version 0.1.1, 23 October 2026, https://doi.org/10.5281/zenodo.23585522. Published on GitHub and Zenodo on 23 October 2026; the version DOI and concept DOI https://doi.org/10.5281/zenodo.23585521 are registered as findable. Use the version DOI for the fixed dataset and the concept DOI for the evolving series. The archived package retains its accurate historical preparation-state statements; this main-branch README and CITATION.cff provide the post-publication update without changing that package or its checksums. Cite individual passages additionally by Legge’s publication, printed page, and dataset ID. Corrections should identify the passage ID, printed page, scan link, proposed reading, and supporting evidence through the repository’s Issues.
