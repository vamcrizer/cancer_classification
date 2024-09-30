# Cancer Classification

## Giới Thiệu
Notebook này nhằm mục đích tham khảo cho việc phân loại khối u ung thư thành hai loại: **Lành Tính** và **Ác Tính**.



## Mục Tiêu
- Phân tích dữ liệu để tìm hiểu mối tương quan giữa các đặc trưng và nhãn phân loại.
- Sử dụng heatmap để trực quan hóa mối tương quan giữa các đặc trưng.
- Lựa chọn các đặc trưng có mối tương quan tốt nhất với nhãn.
- Huấn luyện nhiều mô hình học máy và chọn ra mô hình có chỉ số F1 và độ chính xác cao nhất.
- Kiểm tra hiện tượng overfitting bằng cách sử dụng k-folds cross-validation.

## Các Bước Thực Hiện

- Tải dữ liệu khối u ung thư và tiến hành làm sạch dữ liệu.
Dataset: https://www.kaggle.com/datasets/erdemtaha/cancer-data

### 0. Các thư viện cần thiết
```bash
pip install numpy pandas scikit-learn seaborn matplotlib
```
```python
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import warnings
warnings.filterwarnings('ignore')
```


### 1. Khám Phá Dữ Liệu
- Khám phá và phân tích dữ liệu để hiểu cấu trúc và các đặc trưng.

### 2. Phân Tích Tương Quan
- Sử dụng **Seaborn** để tạo heatmap giúp trực quan hóa mối tương quan giữa các đặc trưng: Sau khi khám phá, phát hiện các đặc trưng là biến thể của nhau, ta xử lí bằng cách tính giá trị trung bình các biến thể/
- Cuối cùng lại sử dụng heatmap để lựa chọn đặc trưng cần thiết nhất.

### 3. Kiểm tra ngoại lai

### 4. Tìm kiếm các mô hình tiềm năng phù hợp cho dataset
- Sử dụng hàng loạt mô hình hỗ trợ cho việc phân loại, từ mô hình Logistic Regression đến các mô hình cây.
  
### 5. Tiến hành đánh giá mô hình
- Sử dụng k-folds CV bằng model đã fit, kiểm tra F1 score trên từng fold.

### Lưu ý: Đây chỉ là notebook tham khảo
