# 🎬 Netflix Churn Prediction - End-to-End MLOps Pipeline on Databricks

## 📌 Giới thiệu dự án
Dự án này cung cấp một quy trình **Data Engineering & Machine Learning (MLOps)** hoàn chỉnh trên nền tảng **Databricks**. Mục tiêu cốt lõi là xây dựng một hệ thống pipeline từ việc nạp dữ liệu thô cho đến lúc huấn luyện thành công mô hình dự đoán tỷ lệ rời bỏ của khách hàng (Churn Prediction) trên nền tảng xem phim trực tuyến.

Dự án sử dụng bộ dữ liệu giả lập (synthetic data) có cấu trúc phức tạp. Dù kết quả dự đoán mang tính chất minh họa quy trình, toàn bộ kiến trúc (architecture) và mã nguồn đều được viết theo tiêu chuẩn production-ready, hoàn toàn có thể tích hợp ngay với dữ liệu kinh doanh thực tế.

## 🚀 Tính năng nổi bật (Key Features)
- **Kiến trúc Medallion (Bronze - Silver - Gold):** Tổ chức, làm sạch và quản lý vòng đời dữ liệu một cách tối ưu bằng Delta Lake.
- **Data Ingestion (Bronze Layer):** Đọc và tự động lưu trữ dữ liệu từ các file CSV thô vào kho dữ liệu thông qua PySpark.
- **Xử lý Mất Cân Bằng Lớp (Class Imbalance):** Triển khai kỹ thuật **Undersampling** nhằm giải quyết triệt để tình trạng chênh lệch dữ liệu (tỷ lệ user churn chỉ khoảng 15%).
- **End-to-End MLOps:** Mô phỏng đầy đủ từ khâu Data Preprocessing, Feature Engineering cho đến Model Training & Logging.

## 🛠️ Công nghệ & Công cụ sử dụng
- **Databricks / Apache Spark:** Xử lý và phân tích dữ liệu lớn.
- **Delta Lake:** Lưu trữ dữ liệu ACID, hỗ trợ time-travel và metadata management.
- **PySpark:** Xây dựng luồng dữ liệu (Data pipelines) hiệu suất cao.
- **Machine Learning:** Huấn luyện mô hình phân loại (Classification Models).

## 📖 Hướng dẫn sử dụng
1. Clone repository này về máy tính của bạn.
2. Import file `Netflix Churn Prediction Model Notebook.ipynb` vào Databricks Workspace.
3. Đảm bảo bạn đã upload tập dữ liệu thô và cấu hình lại đường dẫn gốc (Source Base Path trong Unity Catalog/Volumes) khớp với môi trường của bạn.
4. Chạy từng Cell (Run All) để quan sát luồng chảy của dữ liệu từ file gốc đến khi ra kết quả mô hình.
