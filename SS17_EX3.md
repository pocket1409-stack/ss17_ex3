

### Phần 1: Báo cáo phân tích Box Model hiện tại

-   **Phần tử lỗi (`div#lesson-content`):**
    
    -   **Content:**  $840 \times 600\text{ px}$
        
    -   **Padding:**  $10\text{ px}$ (trên/dưới),  $15\text{ px}$ (trái/phải)
        
    -   **Border:**  $1\text{ px}$ (hoặc $2\text{ px}$ tùy cấu hình hiển thị)
        
    -   **Margin:**  $-10\text{ px}$ (trên/dưới), âm ở chiều ngang do bị ép float.
        
-   **Nguyên nhân cốt lõi & Bẫy dữ liệu:**

        

### Phần 2: Thiết kế giải pháp

Điều chỉnh lại thông số tại bảng **Styles** để chia đều không gian mà không bị tràn:

1.  **Khắc phục xung đột chiều rộng và lề âm:**
    
    -   Thay đổi `width` tổng cộng của 2 khối sao cho không vượt quá 100% (ví dụ: chia tỷ lệ `width: 60%` và `width: 38%`).
        
    -   Triệt tiêu toàn bộ các giá trị `margin-right` hoặc `margin-left` dạng âm (`-20px`).
        
2.  **Cấu hình chuẩn Box-Sizing:** Thêm thuộc tính `box-sizing: border-box;` để padding và border nằm gọn trong kích thước width định sẵn, tránh bị phình to vỡ giao diện.
