### **1\. Chuỗi giá trị dữ liệu DIKW cho MoMo-Lite**

* **Data (Dữ liệu thô):** Các bản ghi giao dịch chưa qua xử lý thu thập từ ứng dụng. Ví dụ: `{ "user_id": 102, "amount": 45000, "category": "coffee", "timestamp": 1700000000 }`.  
* **Information (Thông tin):** Dữ liệu thô được gom nhóm, phân loại và gán ngữ cảnh thời gian. Ví dụ: "Tổng chi tiêu tháng 10/2026 cho danh mục 'Ăn uống' là 3.500.000 VNĐ."  
* **Knowledge (Tri thức):** Áp dụng quy tắc kiểm soát và so sánh với hạn mức ngân sách. Ví dụ: "Chi tiêu ăn uống đạt 80% hạn mức khi mới qua tuần 2, kích hoạt cảnh báo quá mức."  
* **Wisdom (Trí tuệ):** Phân tích xu hướng dài hạn để đưa ra tư vấn tài chính. Ví dụ: "Gợi ý giảm 15% chi tiêu cà phê ngoài hàng để chuyển 500.000 VNĐ/tháng vào quỹ tiết kiệm tự động."

### **2\. Các module Input / Process / Output tương ứng**

* **Tầng Data:**  
  * Input: Thao tác chuyển tiền hoặc thanh toán của người dùng.  
  * Process: Thu thập, đóng gói dữ liệu JSON/Byte và mã hóa.  
  * Output: File log giao dịch thô lưu trên Storage.  
* **Tầng Information:**  
  * Input: Dữ liệu giao dịch thô từ Storage.  
  * Process: Truy vấn, lọc, tính tổng và gom nhóm theo danh mục hoặc thời gian.  
  * Output: Báo cáo hoặc biểu đồ chi tiêu trên giao diện ứng dụng.  
* **Tầng Knowledge:**  
  * Input: Báo cáo chi tiêu kết hợp hạn mức ngân sách đã cài đặt.  
  * Process: Thuật toán so sánh ngưỡng và phát hiện bất thường.  
  * Output: Thông báo push hoặc alert cảnh báo vượt hạn mức.  
* **Tầng Wisdom:**  
  * Input: Lịch sử chi tiêu nhiều tháng và mô hình dự báo tài chính.  
  * Process: Thuật toán phân tích xu hướng chi tiêu dài hạn.  
  * Output: Kế hoạch tiết kiệm cá nhân hóa và gợi ý phân bổ dòng tiền.

