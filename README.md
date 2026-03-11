# writer-skill：繁體中文出版社總編輯

> **聲明：**
> - 本專案為自訂的繁體中文潤飾技能
> - 僅做語言層面的潤飾與校訂，不做內容生成、翻譯、程式碼審查
> - 不負責去除 AI 痕跡（請改用 [humanizer-zh](https://github.com/lazyjerry/Humanizer-zh)） 

---

## 專案簡介

writer-skill 讓 AI 助手扮演出版社總編輯，負責繁體中文文章的出版級潤飾。包括錯字修正、標點規範、句子節奏調整和用詞精準度把關，但不改動原文的內容與情節。

適用於：
- 繁體中文文章的校訂與潤飾
- 統一用語、修正標點與節奏

## 安裝

### 方法一：透過 npx 一鍵安裝（推薦）

```bash
npx skills add https://github.com/lazyjerry/writer-skill
```

### 方法二：透過 ai-global 安裝

如果你已安裝 [ai-global](https://github.com/lazyjerry/ai-global)，可以直接執行：

```bash
ai-global add lazyjerry/writer-skill
```

### 方法三：透過 Git 複製

```bash
# 複製到 Claude Code 的 skills 目錄
git clone https://github.com/lazyjerry/writer-skill ~/.claude/skills/writer-skill
```

### 方法四：手動安裝

1. 下載本專案的 ZIP 檔案或複製到本機
2. 將 `writer-skill` 資料夾複製到 Claude Code 的 skills 目錄：
   - **macOS/Linux**: `~/.claude/skills/`
   - **Windows**: `%USERPROFILE%\.claude\skills\`

3. 確保資料夾結構如下：
   ```
   ~/.claude/skills/writer-skill/
   ├── SKILL.md       # 技能定義文件（中文版）
   └── README.md      # 說明文件
   ```

### 驗證安裝

重新啟動 Claude Code 或重新載入 skills 後，在對話中輸入：

```
/writer-skill
```

如果安裝成功，該技能將被啟用。

## 使用

### 基礎用法

在 Claude Code 中，你可以透過以下方式使用 writer-skill：

#### 1. 直接呼叫技能

```
/writer-skill 請幫我校訂以下文字：

[貼上你的文章]
```

#### 2. 在對話中使用

```
請用 writer-skill 潤飾這段文字，保持原意與語氣：

我們的產品在市場上具有關鍵影響力，此外也在不斷演變的產業格局中扮演重要角色。
```

#### 3. 處理檔案內容

```
/writer-skill 請校訂 article.md 檔案中的內容
```

## 校訂範圍與原則

### 最高原則：內容完整性

- 嚴禁改動內容與情節，只做語言層面的修正
- 潤飾而非改寫，不改變原作者的意圖與畫面

### 編輯準則（三級優先序）

#### 第一級：零錯誤與規範化

- 修正錯別字、漏字、衍字
- 「的、得、地」與「在、再」用法
- 使用全形標點
- 嚴格區分逗號「，」與頓號「、」
- 移除非必要表情符號

#### 第二級：流暢易讀與敘事節奏

- 優化句子節奏與長度
- 消除歧義與理順邏輯
- 禁用補充說明式破折號（保留聲音延長用法）

#### 第三級：精準專業

- 精準用詞替換
- 刪除冗詞贅字
- 統一術語與稱謂

## 輸出格式

輸出固定為兩個部分：

### 修正分析報告

以條列式清單呈現所有修改：

- **原文**：他看見了那棟房子、那是他童年的家。
- **修正後**：他看見了那棟房子，那是他童年的家。
- **說明**：前後為兩個獨立子句，應使用逗號「，」而非頓號「、」。

### 完整校訂文稿

僅放置最終完整、乾淨的文本，不包含任何額外註解或說明。

## 操作測試報告

查看完整的操作測試報告與實際 DEMO 效果：

[查看操作測試報告](https://lazyjerry.github.io/libs/try-humanizer-zh/)

報告中包含實際的校訂流程範例，可對照修正分析與完整校訂文稿的輸出結果。

## 檔案說明

- **`SKILL.md`** - 技能定義文件（中文版）
- **`README.md`** - 本說明文件

## 常見使用情境

- 出版前文字總校
- 對外公告、正式文件潤飾
- 文章語氣與節奏修整

## 貢獻

若你有修訂建議或發現規範問題，歡迎提交 Issue 或 Pull Request。

## 授權

本專案僅用於文字潤飾與校訂。
