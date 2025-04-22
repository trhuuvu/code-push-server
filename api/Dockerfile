# Sử dụng Node.js LTS làm base image
FROM node:20.9.0

# Thiết lập thư mục làm việc
WORKDIR /app

# Sao chép package.json và package-lock.json (nếu có)
COPY package*.json ./

# Cài đặt dependencies
RUN npm install

# Sao chép source code
COPY . .

# Build ứng dụng
RUN npm run build

# Expose port mặc định
EXPOSE 3000

# Khởi chạy ứng dụng
CMD ["npm", "run", "start:env"]