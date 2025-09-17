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


---

## 4. Phương pháp biểu diễn bù 2
- Dùng để biểu diễn số có dấu.  
- **Ý tưởng:** bit dấu có trọng số âm.  
- Ưu điểm:  
- Chỉ có 1 số 0 duy nhất.  
- Tính toán trực tiếp trên bit.  

🔹 Ví dụ (8 bit):  
- `-23` = `11101001` (bù 2)  

---

## 5. BCD (Binary Coded Decimal)
- Dùng **4 bit** để biểu diễn 1 chữ số thập phân.  
- Bảng mã:  

| Thập phân | BCD  | Thập phân | BCD  |
|-----------|------|-----------|------|
| 0         | 0000 | 5         | 0101 |
| 1         | 0001 | 6         | 0110 |
| 2         | 0010 | 7         | 0111 |
| 3         | 0011 | 8         | 1000 |
| 4         | 0100 | 9         | 1001 |

- Ví dụ:  
- 25 (thập phân) = `0010 0101` (BCD)  

---

## 6. Floating Point (IEEE 754)

### 6.1 Công thức
\[
B = (-1)^S × (1.F) × 2^{(E - bias)}
\]

- **S**: bit dấu  
- **E**: số mũ (biased exponent)  
- **F**: phần trị số (fraction/mantissa)  

### 6.2 Chuẩn hóa
- Chỉ giữ 1 chữ số khác 0 trước dấu chấm.  
- Ví dụ:  
\[
5.25 = 101.01_2 = 1.0101 × 2^2
\]

### 6.3 Định dạng
- **32 bit (single precision):**  
- S: 1 bit  
- E: 8 bit (bias = 127)  
- F: 23 bit  
- **64 bit (double precision):**  
- S: 1 bit  
- E: 11 bit (bias = 1023)  
- F: 52 bit  

### 6.4 Trường hợp đặc biệt
- `E=255, F=0` → ∞  
- `E=255, F≠0` → NaN  
- `E=0, F≠0` → chưa chuẩn hóa  

---

## 7. ASCII
- Chuẩn mã hóa ký tự 7-bit.  
- Ví dụ:  
- `"LOVE"` = `1001100100111110101101000101`  

---

## 8. Câu hỏi & Bài tập
