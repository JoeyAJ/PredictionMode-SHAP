# 線上購買預測｜互動模型展示

公開資料的應用型模型開發與課程展示。研究比較 A/B/C × LR/RF/XGBoost 九組模型；本頁僅示範固定的 B 組 16 特徵 XGBoost，門檻 **0.20**，不宣稱最佳或商用。

## 使用

雙擊 `index.html` 即可離線開啟；不需終端、伺服器或套件。先看可展開的模型圖，再載入範例、改值、看機率與分組 SHAP，最後下載 JSON。可切換繁體中文／한국어，切換保留數值；重設會還原第一個範例。

## 自行部署 GitHub Pages

1. 解壓部署 ZIP。只把 `index.html`、`.nojekyll`、`README.md` 放到你自行建立的公開 GitHub repository 根目錄，不要上傳 ZIP 本身。
2. 在 repository 開啟 **Settings → Pages**。
3. **Build and deployment → Source → Deploy from a branch**。
4. **Branch** 選你放檔案的分支（通常 `main`），資料夾選 **/(root)**，按 **Save**。
5. 等 GitHub 顯示實際網站網址，開啟核對後再把該網址放進報告。本交付未代為建立 repository、推送或發布。

步驟依 [GitHub 官方說明](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) 核對。沒有外部字型、CDN、API 或根目錄資源依賴，可用於 project 子路徑。

## 研究限制與公開內容

頁面是離線展示，不追蹤真實訪客、不上傳輸入。彙總資料不能證明任意預測時點的可用性；機率不是購買保證，SHAP 的 log-odds 歸因不是因果效果或機率百分點。高／中／低是展示等級，不是信心分數。

模型版本 `B-XGB-e1390916a72a`。HTML 內含推論必要的模型參數與四個公開資料範例，部署後可被查看。包內不含 CSV、joblib、訓練工程、論文、私人路徑或內部 QA 截圖。

## 한국어 안내

`index.html`을 더블 클릭하면 오프라인으로 열립니다. 모델 흐름 확인 → 예시 선택 → 값 변경 → 확률과 SHAP 확인 → JSON 저장 순서로 사용하세요. 언어 전환은 수치를 바꾸지 않으며 초기화는 첫 번째 예시를 복원합니다.

GitHub에 세 파일을 루트에 올린 뒤 Settings → Pages → Deploy from a branch에서 해당 브랜치(보통 main)와 /(root)를 선택하고 Save를 누르세요. GitHub가 제공한 실제 URL을 확인한 후 보고서에 넣으세요. 이 파일은 아직 게시되지 않았습니다.

공개 데이터를 활용한 수업용 응용 연구입니다. 임계값은 0.20이며 실시간 추적, 상용 성능, 인과 효과를 검증한 서비스가 아닙니다. 추론 매개변수와 공개 데이터 예시 4개는 HTML 안에 포함되어 공개됩니다.
