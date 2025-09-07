---
marp: true
footer:"
---
<!-- _class: lead -->
<!-- paginate: false -->

<style>
    /* Cover slide (lead): centers content */
    section.lead {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 0 60px;
    }
    
    /* Regular slides: aligns content to top-left */
    section:not(.lead) {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        text-align: left;
        font-size: 25px;
        line-height: 1.3;
        padding: 120px 50px 50px 50px; /* Top, Right, Bottom, Left */
    }
    section:not(.lead) h1 {
        position: absolute;
        top: 30px;
        left: 0;
        right: 0;
        padding: 0 50px;
        border-bottom: 1px solid #ccc;
        border-top: 1px solid #ccc;
        padding-bottom: 10px;
        margin: 0;
    }
</style>

<div style="text-align:center;">

## ĐẠI HỌC QUỐC GIA TP.HCM
### TRƯỜNG ĐH CÔNG NGHỆ THÔNG TIN
#### KHOA KỸ THUẬT MÁY TÍNH

<img src="./ce.png" height="80">  
<img src="./uit.png" height="80"> 

### IT010 – Tổ chức và Cấu trúc Máy tính
</div>

<div style="text-align:center; margin-top:20px;"> 
<b> CBGD</b>: Trương Văn Cương <br>
<b> Email:</b>  cuongtv@uit.edu.vn
</div>

---
<!-- footer:  "**IT010 - Tổ chức & Cấu trúc Máy tính** | ThS Trương Văn Cương" -->

# Thông tin môn học

- Mã môn học: IT010
- Số tín chỉ: 2 (Lý thuyết)
- Khoa: Kỹ thuật Máy tính
- Bộ môn: Thiết kế vi mạch & Phần cứng

---

# Mục tiêu môn học

- Cung cấp kiến thức nền tảng về tổ chức & cấu trúc máy tính
- Hiểu các thành phần chính: CPU, GPU, bộ nhớ, kiến trúc tập lệnh
- Rèn luyện kỹ năng phân tích, đánh giá hiệu suất hệ thống
- Làm quen với lập trình hợp ngữ MIPS trên MARS simulator
- Xây dựng nền tảng cho các môn học tiếp theo (Hệ điều hành, Vi xử lý, Kiến trúc nâng cao)

---

# Chuẩn đầu ra

| CĐRMH | Mô tả CĐRMH (Mục tiêu cụ thể)                                       | Ánh xạ CĐR CTĐT | Cấp độ (NT, KN, TĐ) |
|--------|---------------------------------------------------------------------|------------------|---------------------|
| G2.1   | Nắm vững kiến thức nền tảng về lĩnh vực CNTT (Kiến trúc Máy tính) | LO2              | NT2                |
| G6.1   | Đọc hiểu được tài liệu bằng ngoại ngữ                              | LO6              | KN3                |


---

# Nội dung chính (10 buổi)

| Buổi (3 tiết, tuần) | Nội dung                                 |
|---------------------|------------------------------------------|
| 1                   | Giới thiệu, lịch sử máy tính, các thành phần cơ bản |
| 2                   | Hệ thống số                              |
| 3                   | Đại số Boolean                           |
| 4                   | Mạch số                                  |
| 5                   | Mạch số (tiếp) & Ôn tập giữa kì         |
| 6                   | Hệ thống máy tính                        |
| 7                   | Phân cấp bộ nhớ                          |
| 8                   | Kiến trúc máy tính – ISA                |
| 9                   | Vi kiến trúc                 |
| 10                  | Hiệu suất máy tính & Ôn tập cuối kỳ     |


---

# Đánh giá môn học

| Thành phần | Nội dung                         | Tỉ lệ |
|------------|----------------------------------|-------|
| **A1**     | Quá trình (bài tập, kiểm tra ngắn) | 30%  |
| **A2**     | Giữa kỳ                          | 20%  |
| **A3**     | Cuối kỳ                          | 50%  |
| **A4**     | Thực hành                        | 0%   |

---

# Tài liệu học tập

- **Giáo trình chính**:
    - Đinh Đức Anh Vũ, *Thiết kế luận lý số*
    - Nguyễn Minh Sơn (2023), *Giáo trình Kiến trúc máy tính*
    - Patterson & Hennessy (2013), *Computer Organization and Design*
- **Tham khảo**: Stallings, Abd-El-Barr, Vũ Đức Lung, …
- **Công cụ**: *MARS Simulator*

---

# Quy định học tập

- Dự lớp đầy đủ, xem trước tài liệu
- Tham gia thảo luận, trả lời câu hỏi, làm bài tập trên lớp
- Làm bài tập về nhà đúng hạn
- Chủ động liên hệ giảng viên khi có thắc mắc  