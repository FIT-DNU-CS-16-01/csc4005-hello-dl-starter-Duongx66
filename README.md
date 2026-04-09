# Report Lab 0 - Hello Deep Learning

## 1. Thiết lập môi trường

Trong bài lab này, tôi đã tiến hành thiết lập môi trường làm việc cho môn học Deep Learning bằng cách sử dụng Anaconda.
Tôi đã tạo một môi trường ảo riêng biệt với tên `csc4005-dl` và sử dụng Python phiên bản 3.10 để đảm bảo tính ổn định và tránh xung đột thư viện với các project khác.

Sau khi tạo môi trường, tôi đã kích hoạt environment và tiến hành cập nhật pip lên phiên bản mới nhất.
Tiếp theo, tôi cài đặt toàn bộ các thư viện cần thiết thông qua file `requirements.txt` được cung cấp trong repo.

---

## 2. Thực hiện kiểm tra môi trường

Sau khi cài đặt xong, tôi đã chạy script:

* `check_env.py`

Mục đích của bước này là kiểm tra xem các thư viện quan trọng (như numpy, torch, matplotlib, v.v.) đã được cài đặt đúng và hoạt động bình thường hay chưa.

Kết quả:

* Hệ thống đã tạo file `outputs/logs/env_check.txt`
* Nội dung file cho thấy môi trường đã được thiết lập thành công, không có lỗi nghiêm trọng.

---

## 3. Chạy pipeline kiểm thử (smoke test)

Tiếp theo, tôi thực hiện chạy script:

* `run_smoke_test.py`

Đây là một pipeline deep learning đơn giản nhằm kiểm tra toàn bộ luồng xử lý từ:

* Load dữ liệu
* Xây dựng model
* Huấn luyện (training)
* Ghi log và lưu kết quả

Kết quả sau khi chạy:

* File log: `outputs/logs/smoke_test_log.txt`
* Biểu đồ loss: `outputs/figures/loss_curve.png`
* Model checkpoint: `outputs/checkpoints/smoke_model.pt`

Điều này chứng tỏ pipeline hoạt động đúng và môi trường đã sẵn sàng cho các bài lab tiếp theo.

---

## 4. Kết quả đạt được

Sau khi hoàn thành các bước, project đã sinh ra đầy đủ các file output theo yêu cầu của đề bài, bao gồm:

* Log kiểm tra môi trường
* Log quá trình train
* Biểu đồ loss
* File model đã huấn luyện

Ngoài ra, repo có thể chạy lại từ đầu mà không gặp lỗi, đảm bảo tính tái lập (reproducibility).

---

## 5. Khó khăn gặp phải và cách xử lý

Trong quá trình thực hiện, tôi gặp một số vấn đề sau:

### ❌ Lỗi thiếu thư viện

* Khi chạy script ban đầu bị lỗi thiếu một số package
* Cách xử lý: chạy lại `pip install -r requirements.txt`

### ❌ Lỗi liên quan đến PyTorch (nếu có)

* Một số trường hợp cài torch bị lỗi do GPU hoặc version không phù hợp
* Cách xử lý: cài bản CPU bằng lệnh:
  `pip install torch torchvision --index-url https://download.pytorch.org/whl/cpu`

### ❌ Lỗi chưa kích hoạt môi trường

* Khi quên `conda activate`, chương trình không nhận đúng thư viện
* Cách xử lý: kích hoạt lại environment trước khi chạy

---

## 6. Kết luận

Qua bài lab này, tôi đã:

* Nắm được cách thiết lập môi trường Deep Learning chuẩn
* Hiểu cách tổ chức project theo cấu trúc chuẩn
* Làm quen với pipeline cơ bản trong Deep Learning
* Biết cách kiểm tra và debug môi trường

Đây là bước nền tảng quan trọng để thực hiện các bài lab nâng cao trong học phần.
