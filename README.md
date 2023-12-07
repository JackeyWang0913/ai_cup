# 文字辨識模型訓練項目

## 專案介紹
這個項目是關於使用機器學習模型進行文本識別，專注於醫療文件文本的分類和整理。它使用了 EleutherAI 的 Pythia 模型（可選用 70m-deduped 或 160m-deduped 版本）進行訓練，以實現高效的文字處理。

## 資料集
專案使用了兩個資料集：
1. 訓練集：`opendid_set1.tsv`
2. 驗證集：`opendid_valid.tsv`

這些資料集包含了用於訓練和驗證模型的醫療文字資料。

## 在 Google Colab 上開發
建議在 Google Colab 上進行專案的開發和測試，因為它提供了免費的 GPU 支援，這對於深度學習專案非常有用。以下是一些在 Colab 上開發的步驟：

1. 確保您有一個 Google 帳號，以便使用 Colab 服務。
2. 您可以直接在 Colab 中複製您的 GitHub 倉庫，或從 GitHub 匯入 Jupyter 筆記本。
3. 在 Colab 中安裝所需相依性：
   『`python
   !pip install -r requirements.txt
   ```
4. 在 Colab 中，您可以透過修改筆記本設定來啟用 GPU 支援。在「編輯」 -> 「筆記型電腦設定」中選擇「GPU」作為硬體加速器。
5. 考慮使用 Google Drive 來儲存和管理資料集和模型，因為 Colab 會話結束後，執行環境會重設。
6. 您的 Colab 筆記本將保存在 Google Drive 中，可以輕鬆與他人分享。

## 安裝指南
首先克隆倉庫到本地環境或 Colab：
『`bash
git clone https://github.com/yourusername/yourprojectname.git
cd yourprojectname
```
然後安裝所需的依賴：
『`bash
pip install -r requirements.txt
```

## 使用說明
要訓練模型，請運行：
『`bash
python train_model.py --model EleutherAI/pythia-70m-deduped --batch_size <your_batch_size>
```
您可以選擇不同的模型和批次大小。

如果您已經有了訓練好的模型，可以使用 `loading model.ipynb` 來載入和套用模型。

## 輸出
模型訓練完成後，會產生一個 `answer.txt` 文件，包含模型對驗證集的預測結果。

## 貢獻
如果您想為這個專案貢獻程式碼或想法，請閱讀 `CONTRIBUTING.md`。

