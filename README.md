# Academic Manuscript Guard

將作者與 AI 討論留下的寫作痕跡移出論文正文，保留真正的研究內容、證據與限制。適用於英文及繁體中文稿件。

此專案使用 **meta-writing leakage（元寫作洩漏）** 與 **authoring-process leakage（寫作過程洩漏）** 作為工作描述，並不主張它們是已有共識的正式學術分類。

## 處理什麼

- 命名協商、寫作決策與對話殘留，例如「與作者討論後，我們決定正式命名為……」。
- 不必要的防禦性語氣，例如在目的已知時，以研究實際目的取代對無關目標的否認。
- 正文混入修改說明、給作者的提醒或審稿回覆語氣。

這不是「刪掉所有否定句」的工具。研究限制、負面結果、未驗證的泛化能力、因果推論限制與方法選擇理由都應保留；也不強制刪除第一人稱或章節導讀。

## 安裝

本專案的 Skill 位於 `skills/academic-manuscript-guard`，無 Python 或第三方套件相依性。從專案根目錄執行：

```sh
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R skills/academic-manuscript-guard "${CODEX_HOME:-$HOME/.codex}/skills/"
```

如果目的地已有同名 Skill，先比對再更新，避免覆蓋自己的修改。

## 使用範例

```text
請使用 $academic-manuscript-guard 修改以下論文段落。
去除元寫作洩漏及不必要的防禦性語氣，保留研究限制、數字、引用與原始主張強度。
只輸出修訂後正文；無法確認的術語另列作者備註。
```

```text
Use $academic-manuscript-guard to audit the following manuscript.
List only actionable passages, suggested revisions, and scientific meaning to preserve.
```

也可用於根據已提供研究內容撰稿，完成草稿後檢查正文語氣。這是一套由模型執行的語意編修流程，沒有自動偵測程式或保證性的品質分數。

## 專案內容

- [SKILL.md](skills/academic-manuscript-guard/SKILL.md)：觸發條件、判斷原則、修訂與稽核流程。
- [案例](skills/academic-manuscript-guard/references/examples.md)：應修改與應保留的英中範例。
- [介面設定](skills/academic-manuscript-guard/agents/openai.yaml)：顯示名稱與預設提示詞。

此版本以語意保真為優先；不負責查證論文結果、補充引用或修改文件版面。
