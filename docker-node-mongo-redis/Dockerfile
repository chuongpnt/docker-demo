FROM node:13-alpine

WORKDIR /app

COPY . .

RUN npm install

# Development
CMD ["npm", "run", "dev"]

# Production
# RUN npm install -g pm2
# CMD ["pm2-runtime", "ecosystem.config.js", "--env", "production"]




# tạo ra những folder để lưu lại dữ liệu để khi container có khởi động lại thì dữ liệu của ta vẫn sẽ được lưu lại nhé 
# (việc này tiếng anh gọi là persist data), để làm được việc đó thì ta mount những folder chứa dữ liệu này vào trong container dùng volumes nhé
# tạo  folder .docker . Trong .docker ta tạo folder data, trong data ta tạo 2 folder tên là db (cho mongodb) và redis cho redis