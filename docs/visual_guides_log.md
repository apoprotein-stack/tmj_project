# 各張衛教圖設計與修改紀錄

## 01｜手術目的

### 衛教目標

讓病人理解手術不是只為了消除關節聲音，而是以減少關節內刺激、改善機械限制、保留可用組織及追蹤功能為主要目標。

### 資訊架構

1. 減少發炎：沖洗與處理滑膜炎，降低關節內刺激。
2. 解除機械限制：鬆解沾黏，改善卡住與滑動受限。
3. 保留可用組織：依病灶選擇盤復位、固定或修補。
4. 評估療效：以疼痛、張口與進食功能追蹤，不以聲音消失作唯一指標。

### 生圖與設計策略

初版中央圖使用幾何線條表達關節與內視鏡，但評估後認為過於抽象，可能被誤認為正式解剖圖。第二版改為顳顎關節矢狀剖面，但仍偏向簡化線稿。最後改用寫實教科書式顳顎關節剖面，並把資訊文字以 HTML/CSS 放在圖像外部。

### 生成提示詞重點

> Create a medically accurate, realistic textbook-style anatomical illustration of the temporomandibular joint in a lateral sagittal section. Show the temporal bone with the articular eminence and mandibular fossa, the zygomatic arch, the external auditory canal, the mandibular condylar process and ramus, the fibrocartilaginous articular disc, the superior and inferior joint spaces, and the joint capsule. Include a slender arthroscope entering from the preauricular lateral side. Use realistic bone and soft-tissue textures, no gore, no text, no labels, no arrows, no invented anatomy.

### 修改歷程

- V1：抽象中央符號；問題是缺乏解剖可信度。
- V2：增加顳骨、髁突、關節盤與內視鏡路徑；仍不夠寫實。
- V3：參考教科書解剖圖生成寫實剖面，並改用「寫實解剖素材＋HTML 資訊卡」的組合方式。
- V4：縮小中央圖片並調整註記，避免底部文字裁切。

## 03｜手術前評估

### 衛教目標

把術前評估轉換為三個病人容易理解的問題：醫師先了解症狀與功能，再用 MRI 看軟組織，使用 CBCT／CT 看骨性結構，最後整合判讀。

### 三個評估面向

- 病史與臨床檢查：疼痛位置、卡住病史、最大張口、下顎偏移、咬合與耳部基準。
- MRI 軟組織評估：關節盤位置與形態、關節積液、開閉口盤髁關係。
- CBCT／CT 骨性評估：骨性退化、骨折或其他骨病灶、硬組織結構。

### 生圖提示詞

臨床檢查：

> Text-free realistic medical textbook illustration, lateral head and jaw examination for temporomandibular joint preoperative assessment. Show a clinician's gloved hands gently measuring maximum mouth opening and observing mandibular deviation. Clean clinical educational style, warm ivory background, no labels, no text, no gore.

MRI：

> Text-free realistic medical textbook illustration of a temporomandibular joint MRI assessment, showing a patient head in an MRI scanner with a clear inset sagittal TMJ MRI-like soft-tissue view where the articular disc and joint effusion are visually distinguishable. No labels, no text, no logos, no gore.

CBCT／CT：

> Text-free realistic medical textbook illustration of CBCT or CT bone assessment for the temporomandibular joint, showing a CT scanner and a clean 3D or cross-sectional bony rendering of the mandibular condyle, temporal bone and articular eminence. Emphasize hard-tissue anatomy and osseous degeneration assessment. No labels, no text.

### 修改歷程

- 將三個檢查放在同一張圖的三欄卡片中，避免病人把 MRI 與 CT 的用途混淆。
- 增加「症狀與檢查＋影像 → 綜合判讀」流程。
- 加入「影像所見必須與臨床症狀相互應證」提醒，避免形成影像決策的錯誤印象。
- 使用不同素材分別呈現臨床檢查、軟組織影像及骨性影像。

## 04｜適應情況與治療界線

### 衛教目標

說明「有症狀」不等於「直接手術」，而是先確認症狀持續、保守治療反應不佳，再進入內視鏡手術評估。

### 流程內容

1. 持續關節症狀：疼痛、卡住、張口受限。
2. 保守治療反應不佳：藥物、物理治療或咬合板後仍未充分改善。
3. 內視鏡手術評估：確認關節內病灶與可能處置範圍。

治療界線另外列出：

- 先排除肌肉痛、牙源性疼痛、耳疾及神經痛。
- 嚴重纖維化、骨強直或明顯骨性限制需另案討論。

### 生圖提示詞重點

症狀：

> Text-free realistic medical textbook-style clinical illustration of a patient with temporomandibular joint symptoms: holding the preauricular jaw area in pain, limited mouth opening and mandibular deviation. Clean educational composition, warm ivory background, no labels, no text, no gore.

保守治療：

> Text-free realistic medical textbook-style educational illustration showing conservative treatment for temporomandibular joint disorder: clinician-guided jaw physical therapy, medication container without readable branding, and a neutral occlusal splint model. No labels, no text, no logos.

內視鏡評估：

> Text-free realistic medical textbook-style anatomical illustration of temporomandibular joint arthroscopy, lateral sagittal section showing temporal bone, articular disc, mandibular condyle, joint capsule and a slender arthroscope entering the upper joint space from the preauricular lateral side. Accurate anatomy, no labels, no text, no gore.

### 修改歷程

- 將流程拆成三張圖卡，讓「適應條件」與「治療界線」分開理解。
- 以淡粉色區塊呈現需另案討論的情況，避免使用強烈紅色造成恐慌。
- 加入「不是所有顳顎關節症狀的通用解決方案」的提醒。

## 05｜內視鏡的檢查範圍

### 衛教目標

讓病人知道內視鏡主要操作與觀察的是上關節腔，並以後方、中央與前方／內外側三個區域說明鏡下檢查範圍。

### 三個觀察區域

1. 後方區域：後隱窩、滑膜狀態、後附著區。
2. 中央滑動區：關節盤上表面、關節窩及關節結節／隆突。
3. 前方及內外側區：前隱窩、側方溝與沾黏範圍。

### 生圖提示詞

> Create a realistic medical textbook anatomical illustration for patient education about temporomandibular joint arthroscopy. Show a lateral sagittal section of the TMJ with temporal bone, articular eminence, articular disc, mandibular condyle, joint capsule and the upper joint space clearly visible. Highlight the upper joint space as the main arthroscopy working space with three subtle distinct color regions arranged from posterior to central to anterior/lateral: posterior recess, central sliding zone over the superior surface of the disc and articular eminence, and anterior plus medial/lateral gutters. Include a slender arthroscope entering laterally through a preauricular portal and a small directional motion cue suggesting dynamic observation during jaw opening and closing. Use high-detail realistic anatomy, no text, no labels, no gore.

### 修改歷程

- 使用寫實顳顎關節剖面取代抽象流程圖。
- 將上關節腔以不同色彩區域呈現，但文字標示放到 HTML 卡片，避免 AI 生成標籤錯誤。
- 加入下顎開閉口的小型動態示意，對應投影片的動態觀察法。
- 在底部補充：實際可見範圍會受到空間狹窄、沾黏與盤變形影響。

## 共通的素材檢查

每次生圖後都檢查：

- 顳骨、髁突、關節盤與外耳道的空間關係。
- 內視鏡是否位於上關節腔，而非穿越骨骼或進入錯誤空間。
- 是否存在多餘文字、錯誤標籤、血腥內容或品牌標誌。
- 是否能在縮小放入衛教版面後仍看出主要解剖關係。
