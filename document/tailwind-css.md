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

### Box-sizing
- nếu quy định chiều rộng của box là 128px và sau đó, quy định padding 16px, và quy định border 4px thì chiều rộng của box có tăng thêm thành 128 + 16 + 4px không?
- box-border: thì không cộng thêm
- box-content: ngược lại
- thông thường, cách tốt nhất: border-box
