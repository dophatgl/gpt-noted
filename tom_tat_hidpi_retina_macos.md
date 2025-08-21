# 📘 Tóm tắt: Hiểu về độ phân giải, Retina và HiDPI trên macOS

## 1. Pixel logic (points) và pixel vật lý

-   **Pixel vật lý**: số điểm ảnh thật trên panel màn hình (VD: MacBook
    Pro 14" có 3024×1964 pixel).\
-   **Pixel logic (points)**: đơn vị ảo macOS dùng để vẽ UI (VD: Default
    là 1512×982).\
-   macOS luôn render ở **gấp đôi pixel logic (2×)** để khớp với pixel
    vật lý → hiển thị sắc nét, không bị răng cưa.

------------------------------------------------------------------------

## 2. Cơ chế HiDPI (Retina scaling)

-   Khi chọn độ phân giải "thấp" (VD: 1512×982), macOS vẫn render ở
    **full 3024×1964** rồi scale xuống → chữ/icon to hơn nhưng **vẫn cực
    kỳ mịn**.\
-   Nếu chọn "native" 3024×1964 (1:1), UI sẽ **rất bé**, trải nghiệm tệ,
    không thêm độ nét nào.

👉 **Hiểu đúng**: chọn độ phân giải logic thấp trên macOS **không lãng
phí** màn hình 3K.

------------------------------------------------------------------------

## 3. Vì sao macOS khác Windows/Linux

-   **macOS**: áp dụng HiDPI 2× như chuẩn bắt buộc, Apple kiểm soát cả
    phần cứng + phần mềm → trải nghiệm đồng bộ, font/icon luôn mượt.\
-   **Windows/Linux**: hỗ trợ nhiều loại màn hình khác nhau → dùng DPI
    scaling linh hoạt (125%, 150%...). Cách này dễ gây mờ nhòe vì không
    đồng nhất giữa font vector và icon bitmap.

------------------------------------------------------------------------

## 4. Màn hình ngoài tối ưu cho MacBook

macOS vẫn áp dụng HiDPI khi xuất ra màn rời. Trải nghiệm tốt hay không
phụ thuộc **mật độ điểm ảnh (PPI)**:

-   **\~220ppi** = chuẩn Retina, mắt người khó phân biệt pixel.\
-   Gợi ý:
    -   **24" 4K (≈185ppi)** → khá mịn, dùng ổn.\
    -   **27" 4K (≈163ppi)** → PPI thấp, chữ/icon có thể hơi mờ.\
    -   **27" 5K (≈218ppi)** → chuẩn Retina, tối ưu (giống iMac/Studio
        Display).\
    -   **32" 6K (≈218ppi)** → chuẩn Retina, high-end.

👉 **Lựa chọn tối ưu nhất**: màn 27" 5K, cân bằng kích thước và độ mịn.

------------------------------------------------------------------------

## 5. Kết luận

-   MacBook 14" 3K (3024×1964) thật ra hiển thị ở \~1.5K logic
    (1512×982), nhưng nhờ HiDPI 2× nên vẫn tận dụng toàn bộ 3K pixel vật
    lý để đem lại trải nghiệm mịn như Retina.\
-   Người dùng không cần ép chạy native resolution.\
-   Để mắt thoải mái, quan trọng nhất là:
    -   **PPI \~220** (màn hình đủ mịn).\
    -   **Kích thước vật lý phù hợp** (14", 24", 27"...).

👉 Do đó, lo lắng rằng "chọn độ phân giải thấp sẽ không tận dụng hết màn
hình" là **hiểu sai**.
