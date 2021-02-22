# Docker-compose
- Sử dụng docker-compose để triển khai ứng dụng chạy trên docker. Khi triển khai sản phẩn ứng dụng thì các thành phần của ứng dụng chạy trên các container thì được gọi là các service. Một ứng dụng trên docker có thể gồm nhiều service và các thành phần khác nhau ví dụ như: ổ đĩa, mạng,...
- Thông thường khi tạo docker compose thì chia ra hai file. Một cho database và 1 cho service. Ngoài ra một số file compose dùng để migration data nhưng mà nó cũng tùy thuộc vào từng dự án,
- ## Ví dụ cho database lần lượt sử dụng redis, dynamodb và mysql.
-### sử dụng redis
