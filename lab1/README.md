LAB 1: XỬ LÝ ẢNH VỚI THƯ VIỆN PILLOW VÀ OPENCV
1. Mục tiêu
Làm quen với các thao tác cơ bản trên ảnh kỹ thuật số: hiển thị, cắt (cropping), tách kênh màu.
Hiểu sự khác biệt về cấu trúc dữ liệu giữa hai thư viện Pillow (PIL) và OpenCV.
Thực hành chuyển đổi không gian màu (BGR, RGB, Grayscale).

2. Công cụ sử dụng
Ngôn ngữ: Python 3.x
Thư viện: * PIL (Pillow) để xử lý ảnh cơ bản.
- cv2 (OpenCV) để xử lý mảng đa chiều.
- numpy quản lý ma trận điểm ảnh.
- matplotlib hiển thị kết quả trực quan.

3. Nội dung thực hiện
Phần 1: Xử lý ảnh bằng Pillow (PIL)
Load Image: Sử dụng Image.open() để đọc file ảnh và kiểm tra các thuộc tính size, mode.
Transform: Chuyển đổi ảnh màu sang ảnh xám bằng ImageOps.grayscale().
Color Channels: Sử dụng split() để tách 3 kênh màu Red, Green, Blue.
NumPy Integration: Chuyển đối tượng PIL sang mảng NumPy để trích xuất giá trị cường độ pixel tại tọa độ cụ thể.

Phần 2: Xử lý ảnh bằng OpenCV
Cơ chế màu BGR: Đọc ảnh bằng cv2.imread() và thực hiện chuyển đổi sang RGB bằng cv2.cvtColor() để hiển thị đúng màu trên Matplotlib.
Grayscale: Chuyển đổi ảnh màu sang thang độ xám bằng code cv2.COLOR_BGR2GRAY.
Thao tác mảng (Indexing/Slicing): * Cắt lấy nửa trên hoặc nửa bên trái của ảnh.
Trích xuất các kênh màu đơn lẻ bằng cách gán các kênh màu khác về 0.
Lưu trữ: Xuất ảnh sau xử lý ra định dạng .jpg bằng cv2.imwrite().

4. Kết quả đạt được
Nắm vững cách quản lý đường dẫn file bằng module os.
Phân biệt được thứ tự kênh màu: Pillow (RGB) vs OpenCV (BGR).
Hiển thị được ảnh đa dạng: ảnh gốc, ảnh xám, và các ảnh lọc theo kênh màu (Red/Green/Blue channel).

5. Hướng dẫn cài đặt và chạy
Cài đặt môi trường ảo: .venv\Scripts\activate
Cài đặt thư viện:
Bash
pip install opencv-python Pillow matplotlib numpy
Chạy các file Notebook: 2.1.1_Images_with_python_library_PIL.ipynb và 2.1.2_Images_with_python_library_CV.ipynb.