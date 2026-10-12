# Bài 2: Khởi chạy Web Server Nginx với Port Mapping

## 1. Khởi chạy container

**Lệnh thực hiện:**

```bash
docker run -d -p 8080:80 --name my-web nginx:alpine
```

**Kết quả:** Container `my-web` được khởi chạy ở chế độ nền và ánh xạ cổng 8080 của máy tính tới cổng 80 của container.

## 2. Kiểm tra container

**Lệnh thực hiện:**

```bash
docker ps
```

**Kết quả:** Container `my-web` có trạng thái `Up` và cổng được ánh xạ là `8080:80`.

## 3. Kiểm tra phản hồi của Web Server

**Lệnh thực hiện:**

```bash
curl.exe http://localhost:8080
```

**Kết quả:** Máy chủ trả về mã HTML của trang mặc định Nginx, chứa nội dung `Welcome to nginx!`.

## 4. Dừng và xóa container

**Lệnh thực hiện:**

```bash
docker stop my-web
docker rm my-web
```

**Kết quả:** Container `my-web` đã được dừng và xóa sau khi kiểm tra.

## 5. Kết luận

Đã thực hành khởi chạy Nginx bằng Docker với image `nginx:alpine`, sử dụng chế độ chạy ngầm, ánh xạ cổng 8080:80, kiểm tra phản hồi HTTP và dọn dẹp container sau khi hoàn thành.