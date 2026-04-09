tuLAB 07: PHÂN ĐOẠN ẢNH (IMAGE SEGMENTATION)
Sử dụng máy ảo https://colab.research.google.com/ hoặc Visual Studio Code dạng file Jupiter Notebook (.ipynb) cho bài thực hành.

Kiểm tra xem opencv-python đã được cài chưa, nếu chưa ta cài bằng lệnh !pip…
Để đọc ảnh và hiển thị ảnh, ta dùng matplotlib 
import cv2 as cv
import matplotlib.pyplot as plt
!pip install opencv-python

Sử dụng hình ảnh sau, hoặc hình ảnh nào đó để đọc ảnh, lưu lại cùng folder


Thresholding để phân đoạn ảnh
Otsu algorithm để phân đoạn ảnh vân tay 
Clustering techniques trong phân đoạn ảnh, K-mean clustering
Sử dụng thuật toán Region growing
Sử dụng thuật toán Split and merge để phân đoạn ảnh
Phân đoạn ảnh với Edge-based sigmentation

Yêu cầu nộp Elearning: 
- Đặt tên file theo mẫu: MasoSV_HoTenSV_MaLHP_Lab07.ipynb
- Trong file, phần đầu import đặt tên Sinh viên thay vì plt: 
import matplotlib.pyplot as TenSV 
Theo cách đặt này, đổi các câu lệnh trong code tương ứng đảm bảo code chạy không bị lỗi. 
- Không Nộp các file ảnh input kèm theo, đổi tên code input file ảnh theo mẫu img = cv2.imread('hinh1.jpg') và img2 = cv2.imread('hinh2.jpg').
- Chỉ nộp file nội dung của Lab01 cho tuần 1 (bỏ các kết quả của tuần khác ở file khác) 


LAB 08: NHẬN DIỆN ĐỐI TƯỢNG TRONG VIDEO (VIDEO DETECTION)
Sử dụng máy ảo https://colab.research.google.com/ cho bài thực hành.

Tải một video ngắn (từ 12-20 giây) trên trang: https://pixabay.com/vi/videos/search/l%e1%bb%85%20h%e1%bb%99i/
Yêu cầu có người trong clip, đặt tên video_predetect:

Sử dụng đoạn code sau để nhận dạng đối tượng trong video: 
!pip install imageai
from imageai.Detection import VideoObjectDetection
import os

execution_path = os.getcwd()

detector = VideoObjectDetection()
detector.setModelTypeAsRetinaNet()
detector.setModelPath( os.path.join(execution_path , "retinanet_resnet50_fpn_coco-eeacb38b.pth"))
detector.loadModel()

video_path = detector.detectObjectsFromVideo(input_file_path=os.path.join(execution_path, "video_predetect.mp4"),
                                output_file_path=os.path.join(execution_path, "video_detected")
                                , frames_per_second=5, log_progress=True)
print(video_path)

Tham khảo và tải file: retinanet_resnet50_fpn_coco-eeacb38b.pth trên 
https://github.com/OlafenwaMoses/ImageAI/blob/master/imageai/Detection/VIDEO.md


Yêu cầu nộp Elearning: 
- Đặt tên file đã detect được theo mẫu: MasoSV_HoTenSV_MaLHP_Lab08.mp4




