# Colab——訓練YOLO-v5

### 本專案旨在訓練[YOLOv5](https://github.com/ultralytics/yolov5)用於檢測是否配戴口罩


### Step 1：Google Drive準備
- 進入[Google Drive](https://drive.google.com/)首頁 ➔ 按下左上角的"新增"

  ![googledrive1](images/google_drive.png)
- 按"更多" ➔ "Google Colaboratory"

  <p align="center">
    <img src="images/google_driveMORE.png" alt="more">
    &nbsp;&nbsp;&nbsp;
    <img src="images/google_driveCOLAB.png" alt="colab">
  </p>

***
### Step 2：Google Colaboratory設定
- 按下"編輯" ➔ "筆記本設定"
  
  ![setting](images/colab_setting.png)

- 將"硬體加速器"從`CPU`改為`T4 GPU`並按下"儲存"
  
  ![selectGPU](images/colab_selectGPU.png)

- 在"程式碼儲存格"輸入```!nvidia-smi```檢查是否成功切換為`T4 GPU`
  
  ![checkGPU](images/colab_checkGPU.png)
***

### Step 3：程式碼實作
- 新增一個"程式碼儲存格"接著輸入：
  ```python
  import os
  from google.colab import drive
  drive.mount('/content/drive')
  ```
  作用：執行掛載指令，將個人的 Google Drive 連接並映射到 Colab 虛擬機的 `/content/drive` 目錄下
