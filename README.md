# StackOverflow Title Generation

Đây là project sử dụng mô hình học sâu để sinh tiêu đề (title) cho các bài đăng StackOverflow dựa trên phần mô tả và đoạn mã nguồn (code snippet). Hệ thống áp dụng mô hình ngôn ngữ được fine-tune kết hợp với cơ chế tự cải tiến (self-improvement) và post-ranking để cải thiện chất lượng tiêu đề được sinh ra.

## Mục tiêu

Tự động sinh ra tiêu đề ngắn gọn, súc tích và sát nghĩa cho các bài viết kỹ thuật trên StackOverflow — đặc biệt là trong lĩnh vực lập trình, giúp tăng khả năng tìm kiếm và hiểu nội dung.

---

## Cài đặt

Trước khi chạy, bạn cần cài đặt các thư viện cần thiết. Chạy lệnh sau:

``` pip install -r requirements.txt ```
---

## Hướng dẫn sử dụng

### 1. Test mô hình

Nếu bạn chỉ muốn test mô hình đã huấn luyện, chạy:
``` python main.py ```
Giao diện người dùng sẽ mở ra, cho phép bạn nhập mô tả và mã nguồn, chọn ngôn ngữ lập trình, và nhận tiêu đề gợi ý.

---

### 2. Huấn luyện mô hình

Để huấn luyện lại mô hình từ đầu (fine-tune), lần lượt chạy các file sau:
``` 
bash fine_tune1.sh
bash fine_tune2.sh
bash self_improve_finetune.sh
bash test.sh
```
---

## Thư mục dữ liệu

Đảm bảo rằng các file dữ liệu huấn luyện và kiểm thử được đặt đúng đường dẫn như trong script (hoặc bạn có thể tự sửa đường dẫn):

- `./data/train_merged_data.csv`
- `./data/valid_merged_data.csv`

---

## Ghi chú

- Mô hình gốc được sử dụng: `Salesforce/codet5-base`
- Ngôn ngữ hỗ trợ: `C#`, `Java`, `Python`, `JS`