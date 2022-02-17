# Tìm hiểu Cloudflare Workers

## 1. Cloudflare là gì?

![Cloudflare](https://wiki.tino.org/wp-content/uploads/2019/01/co-nen-su-dung-cloudflare-cho-website-hay-khong.png)

- CloudFlare là dịch vụ DNS trung gian, giúp điều phối lượng truy cập giữa máy chủ và các client qua lớp bảo vệ CloudFlare.

- Cloudflare là một nhà cung cấp cơ sở hạ tầng Internet, với ý tưởng là tăng cường bảo mật, hiệu suất và độ tin cậy của bất kỳ thứ gì được kết nối với Internet. Cloudflar cung cấp hầu hết các tính năng cốt lõi miễn phí và cung cấp cũng như thiết lập đơn giản để cài đặt và sử dụng nó. Cloudflare có cả giao diện người dùng và API để quản lý website của bạn.

- Cloudflare hoạt động trên mô hình Freemium nhưng cung cấp miễn phí hầu hết các tính năng cốt lõi của nó với một số giới hạn.

## 2. Các tính năng của Cloudflare:

- Lưu trữ DNS: DNS chịu trách nhiệm dịch tên miền thành địa chỉ IP, Cloudflare cung cấp dịch vụ lưu trữ DNS để quản lý các bản ghi DNS và các bản ghi Cloudflare có hiệu lực rất nhanh trong hầu hết các trường hợp.

- CDN: Mạng cung cấp nội dung là một dịch vụ lưu trữ trang web của bạn và phục vụ trang web từ máy chủ gần nhất về mặt địa lý, do đó làm tăng tốc độ tải của trang web.

- SSL/TLS: Cloudflare cung cấp SSL miễn phí cho tên miền và các tên miền phụ ký tự đại diện cho cấp 3 trong tên máy chủ miễn phí

- Tường lửa: Giới hạn trong 5 quy tắc Tường lửa Cloudflare cung cấp một cách để chặn lưu lượng truy cập bằng địa chỉ IP, tên máy chủ, các bot đã biết, URI,...

- Page rules: Giới hạn trong 3 quy tắc Page rules cung cấp các chức năng khác nhau như chuyển hướng, ghi lại HTTPS và hơn thế nữa.

- Ứng dụng: Được tạo bởi các nhà phát triển, các ứng dụng Cloudflare cung cấp các chức năng khác nhau chỉ bằng một cú nhấp chuột.

- Analytics: Analytics Cloudflare cung cấp các phân tích đơn giản cho website của bạn

- Domain registrar: Cloudflare cung cấp đăng ký miền với giá bán buôn với Whois redaction miễn phí

- Workers: Các chức năng serverless chạy bằng các ngôn ngữ như JavaScript, C, C ++ và Rust.

## 3. Các ưu điểm

- Cloudflare có một gói miễn phí với hầu hết các tính năng cốt lõi của nó.

- Nó hoạt động như CDN giúp tăng tốc độ tải trang web.

- Cloudflare bảo vệ khỏi các chương trình độc hại và các cuộc tấn công DDoS.

- Nó cung cấp DNS được quản lý với TTL ngắn.

- Nó cung cấp chứng chỉ SSL miễn phí hoàn toàn do Cloudflare quản lý, được gia hạn hàng năm.
- Cloudflare cung cấp các quy tắc chuyển tiếp và các chức năng không cần máy chủ.

- Cloudflare có các phần bổ trợ độc lập khác nhau cho các dịch vụ khác nhau.

- Cloudflare cung cấp dịch vụ đăng ký tên miền.

- Cung cấp API để quản lý hầu hết các dịch vụ.

## 4. Các nhược điểm

- Gói miễn phí có nhiều giới hạn và gói trả phí không hề rẻ.

- Các vùng DNS được quản lý có thể không hữu ích đối với một số người dùng.

- Không thể sử dụng máy chủ Custom Name trong gói miễn phí.

- Chứng chỉ SSL sẽ chỉ được chấp nhận Cloudflare nào đang hoạt động trên miền đó.

- Chứng chỉ SSL chỉ sâu một cấp và được cấp cho sni.cloudflaressl.com với miền của bạn trong trường của SAN.

- Đăng ký miền chưa khả dụng cho tất cả người dùng và đi kèm với TLD giới hạn để đăng ký.
