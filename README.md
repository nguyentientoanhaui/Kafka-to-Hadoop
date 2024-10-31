Tổng Quan Dự Án
  Dự án này mô phỏng một kịch bản xử lý dữ liệu cho Công ty A, nơi dữ liệu giao dịch bán hàng từ nhiều chi nhánh trên toàn quốc được thu thập và xử lý liên tục. Bằng cách sử dụng Apache NiFi, Apache Kafka và Hadoop HDFS, mục tiêu là xây dựng một pipeline thu thập và lưu trữ dữ liệu hiệu quả theo thời gian thực, hỗ trợ việc ra quyết định kinh doanh thông qua phân tích dữ liệu lớn.

Mục Tiêu Dự Án
  Kịch Bản Mô Phỏng: Mô phỏng việc thu thập dữ liệu giao dịch bán hàng từ các chi nhánh trên toàn quốc, dữ liệu này sẽ được truyền vào Apache Kafka thông qua Apache NiFi và sau đó lưu trữ trên Hadoop HDFS. Thiết lập này cho phép xử lý và lưu trữ dữ liệu liên tục, mang lại thông tin kinh doanh kịp thời.

  Lựa Chọn Bộ Dữ Liệu: Để làm phong phú thêm pipeline, dự án cũng tích hợp dữ liệu chuyến bay theo thời gian thực và lịch sử từ API Aviationstack. Bộ dữ liệu này bao gồm thông tin chuyến bay thiết yếu như mã chuyến bay, hãng hàng không, sân bay khởi hành và đích đến, cùng với các dấu thời gian.

Kiến Trúc Pipeline
Thu Thập Dữ Liệu:
  Phương pháp 1: MongoDB → Kafka → Hadoop
  Phương pháp 2: API (Aviationstack) → Kafka → Hadoop
Xử Lý Chuyển Đổi Dữ Liệu: Dữ liệu thô từ API sẽ được lọc để trích xuất các thông tin quan trọng như:
  Mã chuyến bay, ngày bay, sân bay khởi hành và đến, múi giờ, thời gian cất cánh và tên hãng hàng không.
  Thiết lập này cung cấp một giải pháp xử lý dữ liệu hoàn chỉnh, theo thời gian thực, cho phép thu thập, chuyển đổi và lưu trữ dữ liệu bán hàng và chuyến bay có cấu trúc để phục vụ cho phân tích quy mô lớn.
