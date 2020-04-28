# build stage
FROM node:13-alpine as build-stage
WORKDIR /app
COPY . .
RUN npm install 
RUN npm run build

# production stage
#project Vue hoặc React là dạng full frontend, không có tí backend nào, chúng chỉ được chạy trên trình duyệt. Mà khi ra tới trình duyệt, thì thứ trình duyệt hiểu chỉ là HTML, CSS, JS
#Project VueJS hay ReactJS khi chạy sẽ cần một webserver để có thể chạy được nó, và Nginx ở đây chính là webserver
FROM nginx:1.17-alpine as production-stage
#copy all file khi build ở trong local  sang folder của webserver
COPY --from=build-stage /app/dist /usr/share/nginx/html
# CMD khởi động Nginx
CMD ["nginx", "-g", "daemon off;"]