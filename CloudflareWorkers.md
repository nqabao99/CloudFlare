# Tìm hiểu Cloudflare Workers

![Cloudflare](https://blog-cloudflare-com-assets.storage.googleapis.com/2020/07/Workers-handshake-after@2x.png)

## 1. Cloudflare Workers là gì?

- Cloudflare Workers giúp triển khai mã severless ngay lập tức trên toàn cầu, có hiệu suất cao, ổn định và dễ dàng mở rộng.

- Cloudflare Worker mới chỉ support: Javascript, C, C++, Rust.

- Cloudflare Worker chạy trên cùng một mạng đám mây toàn cầu gồm hơn 165 trung tâm dữ liệu cung cấp cho các dịch vụ củ nó. Cloudflare worker là một dịch vụ cung cấp môi trường thực thi JavaScript nhẹ để tăng cường các ứng dụng hiện có hoặc tạo các ứng dụng mới.

![Cloudflare Workers](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/317d6aa0-0c30-462f-b19e-7958375f941b/cloudflare-network-map.jpg)

## 2. Các ưu điểm

- Tự động mở rộng: không cần phải lo lắng về vấn đề cấu hình tự động mở rộng nữa, bao gồm cả cân bằng tải (load balancers), hay trả phí cho tài nguyên không sử dụng. Lưu lượng truy cập được định tuyến tự động và cân bằng tải thông qua hàng ngàn máy chủ của Cloudflare. Các đoạn mã mở rộng dễ dàng mà không cần lo lắng.

- Mạng toàn cầu có hiệu suất cao: mỗi triển khai được thực hiện trên mạng trung tâm dữ liệu chạy trên V8 đã được cô lập. Các đoạn mã được mạng lưới của Cloudflare hỗ trợ, các mạng này thường chỉ cách người dùng có vài mili giây.

- Khởi động 0ms: hầu hết các nền tảng severless cần khởi động nguội (cold start) mỗi khi triển khai hoặc dịch vụ gia tăng trong cộng đồng. Cloudflare Worker có thể chạy đoạn mã ngay lập tức, mà không cần khởi động.

- Giá cả phải chăng: 100 ngàn yêu cầu đầu tiên mỗi ngày đều miễn phí, và gói trả phí có giá chỉ 5$ trên 10 triệu yêu cầu, điều này giúp cho Cloudflare Worker có giá rẻ hơn so với các nền tảng serverless khác.

- Không phải lo bảo trì máy chủ: chúng ta sẽ có thời gian dành cho việc xây dựng do bớt được thời gian cấu hình, không cần VM, không cần máy chủ, và không bao gồm cả việc quản lý. Triển khai thông qua việc sử dụng CLI hoặc giao diện web.

- Tài nguyên tĩnh có hiệu suất động: Khai thác sức mạnh vô song của các máy chủ biên để tạo ra các ảnh, SVG, PDF, hay bất cứ thứ gì mà người dùng cần một cách nhanh chóng, và phân phối chúng cho người dùng nhanh nhất có thể như một dạng tài nguyên tĩnh.

- Lưu trữ biên được tích hợp sẵn: lưu trữ các tài nguyên tĩnh tại máy chủ biên với Workers KV, trên các trung tâm dữ liệu toàn cầu, độ trễ thấp. Truy cập vào tài nguyên, cùng với mã của chúng ta và chuyển đổi chúng thông qua API mạnh mẽ, để chỉnh sửa trang của chúng ta trước khi nó đến được với người dùng.

## 3. Các nhược điểm

- Gói miễn phí có nhiều giới hạn.

- Các vùng DNS được quản lý có thể không hữu ích đối với một số người dùng.

- Không thể sử dụng máy chủ Custom Name trong gói miễn phí.

- Chứng chỉ SSL sẽ chỉ được chấp nhận Cloudflare nào đang hoạt động trên miền đó.

- Chứng chỉ SSL chỉ sâu một cấp và được cấp cho sni.cloudflaressl.com với miền của bạn trong trường của SAN.

- Đăng ký miền chưa khả dụng cho tất cả người dùng và đi kèm với TLD giới hạn để đăng ký.
