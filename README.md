# 🌿 Vi-TCM AI Assistant: Hệ Thống Hỗ Trợ Quyết Định Lâm Sàng Dựa Trên Tô Pô Học

[![Hugging Face Space](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Backend%20AI-yellow)](https://huggingface.co/spaces/YOUR_USERNAME/vitcm-ai-engine)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Frontend%20GUI-blue)](https://YOUR_USERNAME.github.io/vitcm-platform/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

**Vi-TCM AI Assistant** là một nền tảng hỗ trợ quyết định lâm sàng (CDSS) tiên tiến, ứng dụng Phân tích Dữ liệu Tô pô (Topological Data Analysis - TDA) để định lượng sự hiệp đồng của các vị thuốc trong Y học cổ truyền Việt Nam.

Dự án này là sản phẩm thực thi hóa từ nghiên cứu: *"Knowledge-Driven Topological Data Analysis in Traditional Medicine: A Macroscopic Synergy Approach"*.

---

## 🚀 Tính năng chính cho Bác sĩ & Nhà nghiên cứu

- **Cơ sở dữ liệu dược liệu số:** Truy cập hơn 700 vị thuốc từ Dược điển Việt Nam với các thuộc tính Tính vị (Nature/Flavor) và Quy kinh (Meridian Tropism) đã được chuẩn hóa.
- **Phân tích hiệp đồng (Synergy Score):** Sử dụng thuật toán AI để tính toán điểm số hiệp đồng dựa trên độ phức tạp hình học của mạng lưới dược lý.
- **Trực quan hóa đường cong Betti (Betti Curves):** Cung cấp bằng chứng khoa học về các "vòng lặp hiệp đồng" (Synergistic Loops - $H_1$) giúp bác sĩ hiểu rõ cơ chế tác động đa mục tiêu của bài thuốc.
- **Hỗ trợ kê đơn:** Giao diện kéo-thả trực quan giúp bác sĩ thử nghiệm các tổ hợp thuốc và nhận phản hồi ngay lập tức về hiệu quả cấu trúc của bài thuốc đó.

---

## 🧠 Kiến trúc hệ thống

Hệ thống được thiết kế theo mô hình Microservices hiện đại:

1.  **AI Backend (Hugging Face Spaces):** - Xây dựng trên nền tảng **FastAPI**.
    - Sử dụng thư viện **Giotto-TDA** để tính toán Persistent Homology thời gian thực.
    - Xử lý không gian vector Euclidean từ thuộc tính dược liệu.
2.  **Frontend Dashboard (GitHub Pages):**
    - Giao diện người dùng (GUI) tinh gọn, phản hồi nhanh.
    - Trực quan hóa dữ liệu bằng **Chart.js**.
    - Kết nối an toàn qua API tới máy chủ AI.

---

## 🛠 Hướng dẫn cài đặt & Triển khai

### 1. Cấu hình Backend (Hugging Face)
- Đảm bảo tệp `curated_tm_features.pkl` đã được tải lên không gian làm việc.
- Cài đặt các thư viện cần thiết:
  ```bash
  pip install fastapi uvicorn giotto-tda pandas scikit-learn
