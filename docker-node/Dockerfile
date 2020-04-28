#Image đã được build sẵn và chính thức (official) từ team của NodeJS , lấy ở dockerhub
FROM node:13-alpine       
#trong image này, tạo ra cho tôi folder tên là app và chuyển tôi đến đường dẫn /app
WORKDIR /app
#Copy toàn bộ code ở môi trường gốc, tức ở folder docker-node hiện tại vào bên trong Image ở đường dẫn /app
COPY . .
#RUN để chạy một câu lệnh nào đó khi build Docker Image, ở đây ta cần chạy npm install để cài dependencies ,chỉ được chạy 1 lần trong lúc build,
RUN npm install
# CMD sẽ luôn được chạy khi 1 container được khởi tạo từ Image nhé 
CMD ["npm", "start"]





#build image dùng :
    # docker build -t learning-docker/node:v1 .
#Option -t để chỉ là đặt tên Image
#Ở đây là learning-docker/node và gán cho nó tag là v1, ý chỉ đây là phiên bản số 1. Nếu ta không gán tag thì mặc định sẽ được để là latest 
#dấu "chấm" ý bảo là Docker hãy build Image với context (bối cảnh) ở folder hiện tại này cho tôi
#check image dùng:  || xóa image dùng: 
    # docker images    || docker rmi <Mã của Image>
# Copy nhiều file
    # COPY app.js package.json package-lock.json .
# Ở trên ta các bạn có thể copy bao nhiêu file cũng được, phần tử cuối cùng (dấu "chấm") là đích ta muốn copy tới trong Image