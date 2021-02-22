# Docker-compose
- Sử dụng docker-compose để triển khai ứng dụng chạy trên docker. Khi triển khai sản phẩn ứng dụng thì các thành phần của ứng dụng chạy trên các container thì được gọi là các service. Một ứng dụng trên docker có thể gồm nhiều service và các thành phần khác nhau ví dụ như: ổ đĩa, mạng,...
- Thông thường khi tạo docker compose thì chia ra hai file. Một cho database và 1 cho service. Ngoài ra một số file compose dùng để migration data nhưng mà nó cũng tùy thuộc vào từng dự án,
- ## Ví dụ cho database lần lượt sử dụng redis, dynamodb và mysql.
### sử dụng redis
![Capture](https://user-images.githubusercontent.com/63154819/108739935-b5604a80-7567-11eb-9d83-10b0b680ee1b.PNG)
- có 4 options là build, command, ports và volume
- tương ứng với các option thì có các ý nghĩa như sau
  - build: chỉ định dockerfile sẽ được tạo ra trong build time. Một container được tạo nên từ 1 image và image được định nghĩa từ dockerfile. Nên rõ ràng build là option đầu tiên mà ta cần quan tâm. build có thể là một path chỉ định dockerfile hoặc có thể là config path đó với các option như context, dockerfile,.. hoặc build có thể đơn gian như: build: ./redis.
    - context: chỉ định đường dẫn chứa dockerfile (hoặc đường dẫn đến git repository chứa docker file chẳng hạn). Nó có thể là đường dẫn tương đối hoặc tuyệt đối. Điều này giúp docker compose dễ dàng quản lý các docker file rải rác trong bộ source của mình.
