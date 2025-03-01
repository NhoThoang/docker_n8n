# Self-host n8n dùng Cloudflare Tunnel để public IP mà không cần mở firewall  

## 1. Cài đặt Cloudflare Tunnel  
Đây là link tải và cài đặt Cloudflare Tunnel:  
[Cloudflare Tunnel Setup](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/downloads/)  

![n8n Screenshot](./picture/n8n-screenshot-readme.png)  

---

## 2. Cài đặt Docker và Docker Compose  

### Clone repository  
```sh  
git clone https://github.com/NhoThoang/docker_n8n.git  
```

### Cài đặt Docker  
Bạn có thể cài đặt **Docker Desktop** hoặc dùng **WSL2** trên Windows.  

#### Với Docker Desktop trên Windows  
- Cài đặt Docker Desktop theo hướng dẫn:  
  [Hướng dẫn cài đặt Docker Desktop](https://docs.docker.com/desktop/setup/install/windows-install/)  
- Sau đó, chạy **Docker Desktop**.  

#### Với WSL2 trên Windows  
Di chuyển vào thư mục đã tải về và chạy lệnh cài đặt Docker, Docker Compose:  
```sh  
bash install_docker.sh  
```

---

## 3. Chạy Docker  
Tạo thư mục và cấp quyền:  
```sh  
mkdir -p n8n_data postgres_data && chmod 777 n8n_data  
```

📌 **Lưu ý:**  
- Trong file `.env`, sửa dòng cuối cùng thành **domain của bạn** để các dịch vụ khác có thể gửi trigger vào máy.  

Chạy Docker Compose:  
```sh  
docker compose up -d  
```

### Kiểm tra Docker đã chạy chưa  
```sh  
docker ps -a  
```

Sau đó, truy cập domain của bạn để kiểm tra xem web đã hoạt động chưa.  

---  
### các template các bạn có thể tham khảo tải về để chỉnh sửa 
[template n8n](https://n8n.io/workflows/?utm_source=n8n_app&utm_medium=template_library&utm_instance=http%3A%2F%2F35.238.151.93%3A5678%2F&utm_n8n_version=1.80.5&utm_awc=0)

---
✅ **Nếu thấy hay và giúp ích cho các bạn bạn có thể gửi quà cho mình nhé Thanks!**

<img src="./picture/qr_pay.png" alt="QR Pay" width="100">


