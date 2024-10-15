# Kaggle Competition: [Global Wheat Detection]

## Giới thiệu
Repo này chứa lời giải của tôi cho cuộc thi [Global Wheat Detection](https://www.kaggle.com/competitions/global-wheat-detection/overview). Trong cuộc thi này, người tham dự yêu cầu phải phát hiện các ngọn lúa mỳ từ các bức ảnh chụp lúa mỳ thu thập ở khắp nơi. Bên dưới là cách tôi thực hiện bài toán.
## Dataset
Dữ liệu cho cuộc thi bao gồm:
- **train.zip** và **test.zip**: dữ liệu ảnh lúa mỳ được thu thập khắp nơi dùng cho khi train và test
- **train.csv**: chứa các trường dữ liệu của dữ liệu  huấn luyện lúa mỳ
- **submission.csv**: định dạng file khi nộp kết quả

Thông tin chi tiết về dữ liệu có thể được tìm thấy [tại đây](https://www.kaggle.com/competitions/global-wheat-detection/data).

## Augmentation
Sử dụng một số cách tăng cường dữ liệu sau đây:
- HorizontalFlip
- RandomBrightnessContrast
- Resize

## Model
- Faster RCNN, với backbone Resnet50
- Dùng 5 fold cross validation
- Optimizer: Adam lr: 0.001
- Scheduler: ReduceLROnPlateau, factor 0.1, patience là 5 epoch
- Chạy 15 epoch
- Dùng [Weighted box fusion]() khi vào inference
1. **[Tên notebook 1]**:
   - **Mục đích**: [Mục tiêu của notebook này, ví dụ "Khám phá và phân tích dữ liệu ban đầu"]
   - **Các bước chính**: 
     1. [Tóm tắt các bước thực hiện]
     2. [Tóm tắt các phương pháp phân tích]
   - **Kết quả**: [Những phát hiện hoặc kết luận chính]



## Hướng dẫn sử dụng
Để chạy các notebook, bạn cần thực hiện các bước sau:
1. **Clone repository**: `git clone [link repo]`
2. **Cài đặt dependencies**:
   ```bash
   pip install -r requirements.txt
