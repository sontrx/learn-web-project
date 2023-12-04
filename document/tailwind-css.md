# Tailwind CSS
- https://tailwindcss.com/docs
- cài đặt: https://tailwindcss.com/docs/installation/play-cdn

## layout
```css
@media (min-width: 1024px) {
    .container {
        max-width: 1000px;
    }
}
```
### Aspect Ratio: tỉ lệ các khối (block)
### Columns
- chú ý về số phần tử con, nếu không chia hết cho columns thì có thể không hoạt động
### Container
### Box-sizing
- nếu quy định chiều rộng của box là 128px và sau đó, quy định padding 16px, và quy định border 4px thì chiều rộng của box có tăng thêm thành 128 + 16 + 4px không?
- box-border: thì không cộng thêm
- box-content: ngược lại
- thông thường, cách tốt nhất: border-box

### Object-fit
- object fit: cách co giãn của ảnh trong khung khi kích thước gốc của ảnh có tỉ lệ khác với khung
- object position: vị trí của ảnh trong khung

### Overflow
- khi kích thước của các phần tử con lớn hơn phần tử cha, thì ẩn hoặc tạo thanh trượt cho phần nội dung
- thường dùng nhất: overflow-hidden, overflow-scroll (có thể chỉ định thêm chiều x / y)
- https://tailwindcss.com/docs/overflow

### Position
- absolute: tuyệt đối, chỉ định chính xác vị trí của phần tử, thường đi kèm với các thuộc tính như left, right, bottom, top
- absolute: phần tử cha của absolute cần có thuộc tính position, và giá trị của position khác static
fixed: neo vị trí theo các rìa của màn hình
- relative: lấy mốc vị trí là chính bản thân nó
- sticky: gần giống fixed, nhưng hoạt động với croll bar
- top/right/bottom/left
- z-index: thứ tự của phần tử khi nằm chồng lặp lên phần tử khác
