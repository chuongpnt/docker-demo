# ta bắt đầu từ 1 Image có môi trường Alpint và đã cài sẵn Python phiên bản 3.6
FROM python:3.6-alpine
#a sẽ chuyển đến đường dẫn là /app bên trong Image
WORKDIR /app
# Tạo ra biến môi trường tên là PORT với giá trị 5555
#ENV PORT 5555
#COPY toàn bộ file từ folder ở môi trường gốc (bên ngoài - folder docker-python) và đưa vào trong đường dẫn /app bên trong Image
COPY . .
#cài đặt dependencies, cần cài những thứ gì thì ta đề cập sẵn ở file requirements.txt
RUN pip install -r requirements.txt
#CMD để chỉ command mặc định khi một container được khởi tạo từ Image: ở đây ta sẽ khởi động file app.py
CMD ["python", "app.py"]


#build image dùng :
    # docker build -t learning-docker/python:v1 .
#đổi tên file image để push lên github
    #docker tag learning-docker/python:v1 registry.gitlab.com/chuongpnt/learning-docker
#push lên gitlab
    #docker push registry.gitlab.com/chuongpnt/learning-docker