# 可重現工作流程

## 1. 檔案結構

```text
assets/theme2/visual_guides/
├── 01_surgery_purpose.png
├── 03_preoperative_assessment.png
├── 04_indications_and_boundaries.png
├── 05_arthroscopy_scope.png
└── tmj_*.png                  # 寫實解剖與檢查素材

source/visual_guides/
├── 01_surgery_purpose.html
├── 03_preoperative_assessment.html
├── 04_indications_and_boundaries.html
└── 05_arthroscopy_scope.html
```

## 2. 生圖架構

生圖採「先生成無文字醫療素材，再由可控版面承載文字」的架構：

1. 先定義衛教目的、必須呈現的解剖構造與病人可理解的重點。
2. 生成無文字的寫實醫學素材，使用既有顳顎關節寫實圖作為風格與解剖參考。
3. 逐張檢查素材，確認解剖關係、內視鏡路徑與畫面是否適合縮放。
4. 以 HTML/CSS 建立卡片、標題、流程與限制提醒。
5. 使用 Chromium 將 HTML 的 `main` 容器輸出為 PNG。
6. 目視確認文字沒有裁切、圖片沒有錯位，並檢查 PNG 尺寸與模式。

## 3. Prompt 撰寫原則

每個 prompt 建議包含：

- `realistic medical textbook illustration`
- 明確的解剖視角，例如 `lateral sagittal section`
- 必須呈現的構造：temporal bone、articular disc、mandibular condyle、joint capsule、upper joint space
- 影像用途：patient education、clinical educational style
- 視覺限制：`no text, no labels, no arrows with words, no gore, no logos`
- 參考圖用途：只用於解剖風格、構圖或材質參考，不直接複製文字標籤

## 4. HTML 匯出

在具有 Chromium 與 Playwright 的環境中：

```python
from playwright.sync_api import sync_playwright

with sync_playwright() as p:
    browser = p.chromium.launch()
    page = browser.new_page(
        viewport={"width": 1600, "height": 900},
        device_scale_factor=1,
    )
    page.goto("file:///absolute/path/to/guide.html")
    page.wait_for_load_state("networkidle")
    page.locator("main").screenshot(path="/absolute/path/to/guide.png")
    browser.close()
```

若環境沒有預設 Chromium，可改用 `/usr/bin/chromium` 或 Chrome channel。

## 5. 輸出檢查清單

### 內容

- 標題與原始投影片一致。
- 每個數字、區域名稱、影像檢查名稱與醫療限制均正確。
- 不把「可能考慮」寫成「一定需要」。
- 不把示意圖寫成實際手術照片或個案診斷。

### 視覺

- 解剖圖保持清楚且不被卡片裁切。
- 圖片縮小後仍看得到關節盤、髁突與內視鏡大致關係。
- 文字不壓在解剖細節上。
- 重要提醒使用低刺激性的深藍、陶土色或淡粉色區分。

### 技術

- HTML 可在瀏覽器開啟。
- PNG 已成功輸出，且檔案不是空檔或截斷。
- `README.md` 的路徑與實際檔案一致。
- 變更後執行 `git status`、`git diff --check`，再提交。

## 6. 醫療審閱流程建議

此專案的視覺與文字可以供設計、衛教與溝通使用，但正式臨床發布前建議依序由以下人員審閱：

1. 顳顎關節／口腔顎面外科醫師：解剖、術式與適應情況。
2. 影像專業人員或放射科醫師：MRI、CBCT／CT 的表達方式。
3. 臨床衛教或護理人員：病人理解度與用詞。
4. 專案負責人：版本、檔案路徑與發布內容。
