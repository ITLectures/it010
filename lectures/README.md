# IT010 – Tổ chức và Cấu trúc Máy tính
## Chương 2: Biểu diễn thông tin trong máy tính

---

## 📑 Mục lục
1. Thông tin – Dữ liệu – Tín hiệu  
2. Biểu diễn thông tin  
   - Hệ thập phân  
   - Hệ nhị phân  
   - Hệ cơ số 16 (Hexadecimal)  
   - Biểu diễn số nguyên dương  
3. Tính toán trên hệ cơ số 2  
4. Phương pháp biểu diễn bù 2  
5. BCD (Binary Coded Decimal)  
6. Floating Point (Dấu chấm động – IEEE 754)  
7. ASCII (American Standard Code for Information Interchange)  
8. Câu hỏi & Bài tập  

---

## 1. Thông tin – Dữ liệu – Tín hiệu
- **Thông tin**: dữ liệu có ý nghĩa trong ngữ cảnh, giúp giải quyết sự không chắc chắn.  
- **Dữ liệu**: biểu diễn vật lý của thông tin, chưa có ý nghĩa nếu không được xử lý.  
- **Tín hiệu**: đại lượng vật lý thay đổi theo thời gian/không gian.  
  - Liên tục  
  - Rời rạc  
  - Số (đã được lượng tử hóa)  

🔹 Công cụ:  
- **A/D Converter**: Analog → Digital  
- **D/A Converter**: Digital → Analog  

---

## 2. Biểu diễn thông tin

### 2.1 Hệ thập phân
- Sử dụng 10 ký số: `0-9`.  
- Mỗi vị trí có trọng số \(10^i\).  
- Ví dụ:  
  \[
  269 = 2×10^2 + 6×10^1 + 9×10^0
  \]

### 2.2 Hệ nhị phân
- Máy tính chỉ dùng `0` và `1`.  
- Đơn vị: **bit** (binary digit).  
- Quy ước dung lượng:  
  - 1 B = 8 bit  
  - 1 KB = 1024 B  
  - 1 MB = 1024 KB  
  - 1 GB = 1024 MB  
  - 1 TB = 1024 GB  

### 2.3 Biểu diễn số nguyên dương
- Ví dụ:  
  \[
  23 = 2^4 + 2^2 + 2^1 + 2^0 = 10111_2
  \]

### 2.4 Hệ cơ số 16 (Hexadecimal)
- Ký số: `0–9, A–F`  
- Mỗi ký số hex tương ứng với **4 bit**.  
- Ví dụ:  
  \[
  0010\ 1110\ 1001_2 = 0x2E9_{16}
  \]

---

## 3. Tính toán trên hệ cơ số 2
- Quy tắc cộng/trừ giống hệ thập phân.  
- Ví dụ:  
