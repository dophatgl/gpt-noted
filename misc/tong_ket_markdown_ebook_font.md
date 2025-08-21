# 📘 Tổng kết: Markdown, HTML, Ebook và Ảnh hưởng của Cỡ chữ

## 1. Markdown cơ bản
- Markdown là **plain text** với cú pháp gọn, dễ đọc/viết.  
- Khi render (trên GitHub, VSCode, Obsidian…) → chuyển thành **HTML**.  
- Hỗ trợ:
  - **Ảnh**: `![](img.png)`
  - **Link**: `[link](url)`
  - **Code, bảng, checklist…**
  - Có thể **nhúng trực tiếp HTML** (ví dụ `<video>`).

👉 Markdown = nhanh viết, dễ đọc, lý tưởng cho tài liệu kỹ thuật, notes, README.  

---

## 2. Markdown vs HTML
- **Markdown**: đơn giản, gọn, đọc raw dễ hiểu.  
- **HTML**: chi tiết, mạnh mẽ, chuẩn gốc web.  
- Markdown thường được **convert sang HTML** để hiển thị.  
- Ưu điểm Markdown: viết nhanh; ưu điểm HTML: kiểm soát mạnh.  

---

## 3. Markdown & Ebook formats (EPUB, MOBI)
- **EPUB**: chuẩn mở, bên trong là HTML + CSS + metadata.  
- **MOBI**: format riêng của Amazon Kindle (đóng hơn, ít linh hoạt).  
- **Markdown thường → HTML → EPUB/MOBI**.  
- **Mất dữ liệu khi convert**:  
  - Markdown → EPUB: thường ổn (text/ảnh/bảng), nhưng layout phức tạp hoặc video có thể không giữ được.  
  - EPUB/MOBI → Markdown: dễ mất định dạng, chỉ giữ text/ảnh.  

👉 Nên dùng **Markdown (source gốc)** → khi cần convert sang EPUB/MOBI/PDF để đọc.  

---

## 4. Cỡ chữ & chất lượng học tập
- **Quá nhỏ** → mỏi mắt, mất tập trung.  
- **Quá to** → giảm tốc độ, mất liền mạch.  
- **Vừa phải (16–18px màn hình / 12pt giấy)** → tối ưu đọc lâu dài.  
- Nguyên tắc **“desirable difficulty”**: hơi nhỏ hơn mức thoải mái một chút → buộc não tập trung hơn → nhớ lâu hơn.  
- Nhưng đừng để quá khó đọc, kẻo phản tác dụng.  

---

## 5. Cỡ chữ khi lập trình
- Code có đặc thù: nhiều ký hiệu nhỏ, cần nhìn nhiều dòng cùng lúc.  
- **Khuyến nghị**:  
  - **11–13pt (13–15px)**: phổ biến cho IDE/terminal.  
  - **13–14pt**: nếu dùng màn hình lớn/4K hoặc hay mỏi mắt.  
- Dùng **monospace font** (Fira Code, JetBrains Mono, Consolas…).  
- Không nên để quá to → mất bối cảnh, phải scroll nhiều.  

👉 Mục tiêu khi code: **giảm mỏi mắt + giữ nhiều dòng trên màn hình + tránh sai sót**.  

---

## 🔑 Kết luận chung
- Markdown mạnh vì **linh hoạt, nhẹ, dễ convert** → nên dùng làm **định dạng gốc để lưu trữ tài liệu**.  
- HTML là **chuẩn hiển thị web**, và là trung gian khi xuất sang EPUB/MOBI.  
- EPUB → thích hợp phát hành/đọc sách; MOBI → riêng cho Kindle.  
- **Cỡ chữ đọc tài liệu**: hơi nhỏ hơn mức thoải mái một chút.  
- **Cỡ chữ lập trình**: vừa phải, ưu tiên giảm mỏi mắt, thường 11–13pt.  
