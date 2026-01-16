1. Mục tiêu
Lab này cung cấp các kiến thức cơ bản về xử lý ảnh kỹ thuật số bằng hai thư viện phổ biến nhất trong Python là Pillow (PIL) và OpenCV.
- Cách đọc, hiển thị và lưu trữ ảnh.
- Thao tác với mảng điểm ảnh (pixel arrays).
- Các kỹ thuật biến đổi ảnh cơ bản: lật (flipping), cắt (cropping) và thay đổi màu sắc.
- Hiểu sự khác biệt về không gian màu (RGB vs BGR) giữa Pillow và OpenCV.

2. Công cụ sử dụng
Ngôn ngữ: Python 3.x
Thư viện chính:
- PIL (Pillow): Thư viện thân thiện để xử lý các đối tượng ảnh.
- cv2 (OpenCV): Thư viện mạnh mẽ cho thị giác máy tính, xử lý ảnh dưới dạng mảng đa chiều.
- numpy: Quản lý và tính toán trên ma trận điểm ảnh.
- matplotlib: Hiển thị hình ảnh trực quan trong môi trường Notebook.

3. Nội dung thực hiện
Phần 1: Xử lý ảnh bằng Pillow (2.2.1_basic_image_manipulation_PIL.ipynb)
- Load & Explore: Sử dụng Image.open() để đọc ảnh và truy vấn các thuộc tính như kích thước (size), định dạng (format) và chế độ màu (mode).

Biến đổi ảnh:
- Chuyển đổi sang ảnh xám (Grayscale) bằng ImageOps.grayscale().
- Tách và hiển thị các kênh màu đơn lẻ (Red, Green, Blue).

Thao tác hình học:
- Lật ảnh dọc (flip) và lật ảnh ngang (mirror) bằng thư viện ImageOps.
- Cắt ảnh (Cropping) bằng phương thức crop().
- Can thiệp Pixel: Chuyển ảnh sang mảng NumPy để thay đổi giá trị màu tại các tọa độ cụ thể.

Phần 2: Xử lý ảnh bằng OpenCV (2.2.2_basic_image_manipulation_open_CV.ipynb)
- Cơ chế màu BGR: Tìm hiểu lý do tại sao OpenCV mặc định dùng BGR và cách dùng cv2.cvtColor() để chuyển sang RGB trước khi hiển thị bằng Matplotlib.
- Thao tác mảng (Slicing): * Sử dụng kỹ thuật cắt mảng (indexing) của Python để cắt ảnh thay vì dùng hàm chuyên dụng.
- Trích xuất các kênh màu bằng cách gán các giá trị kênh khác về 0 trên mảng NumPy.

Biến đổi hình học:
- Sử dụng cv2.flip() với các tham số 0 (dọc), 1 (ngang) và -1 (cả hai).
- Vẽ lên ảnh: Hướng dẫn cách vẽ các hình cơ bản (đường thẳng, hình chữ nhật) trực tiếp lên mảng ảnh.

4. Kết quả đạt được
- Phân biệt rõ ràng cách quản lý dữ liệu ảnh giữa Pillow (Object-based) và OpenCV (Array-based).
- Biết cách xử lý lỗi phổ biến khi đọc sai đường dẫn ảnh hoặc hiển thị sai hệ màu.
- Thành thạo việc sao chép ảnh (copy) để tránh hiện tượng Aliasing (thay đổi trên bản sao làm ảnh hưởng bản gốc).
- Có khả năng thực hiện các bước tiền xử lý dữ liệu ảnh cơ bản cho các bài toán Deep Learning/Computer Vision sau này.

5. Hướng dẫn cài đặt
Để chạy được các file notebook này, bạn cần cài đặt các thư viện sau:

- Bash
- pip install pillow opencv-python numpy matplotlib