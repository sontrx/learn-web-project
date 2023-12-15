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

### Flexbox
- flex
- flex basis: quy định kích thước của các phần tử con trong 1 flex box, các giá trị: https://tailwindcss.com/docs/flex-basis
- flex direction: quy định sự sắp xếp của các phần tử con là theo chiều ngang (row) hay dọc (column)
- flex wrap: quy định nếu tổng kích thước của các phần tử con lớn hơn kích thước của phần tử cha, thì sẽ cho xuống dòng hay tràn viền
- flex-1 / flex-initial: quy định phần tử con chiếm bao nhiêu diện tích so với các phần tử còn lại. (flex-grow/flex-shrink)
- order: quy định thứ tự của các phần tử con

grid:
- dùng để chia bố cục giao diện: kiểu lưới
- cạnh tranh với flex

khi nào dùng flex?

flex: justify-content, align-items
grid: justify-items, align-content

### spacing
- padding theo 4 phía: p-0, p-1...
- padding theo phương ngang: px-1, px-2 ...
- padding theo phương dọc: py-1, py-2 ...
- pt-1, pl-1, pr-1, pb-1

margin: tương tự padding

- space-between: khoảng cach giua cac phan tu con

### sizing
- width: w-1/2, w-1/3
- min-width, max-width tương tự
- height: tương tự cách dùng như width

### typography
- các thuộc tính liên quan đến chữ, font chữ, độ đậm nhạt ...

khái niệm:
- đoạn văn bản: paragraph (tương ứng thẻ p)
- 1 đoạn văn bản có nhiều dòng: line
- 1 dòng có nhiều từ: word
- 1 từ có chiều chữ cái: letter
```css

@font-face {
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 300;
  font-display: swap;
  src: url(fonts/Roboto.ttf) format('woff2');
  unicode-range: U+0460-052F, U+1C80-1C88, U+20B4, U+2DE0-2DFF, U+A640-A69F, U+FE2E-FE2F;
}
html {
    font-family: 'Roboto', sans-serif;
}

```
https://fonts.google.com/

#### font
- font-style: normal (bình thường mặc định) / italic (nghiêng)
- font-weight: độ đậm nhạt của chữ, giá trị: 100 -> 900;
- font-size: cỡ chữ, độ to nhỏ. giá trị px
- font-family: ví dụ `font-family: 'Roboto', sans-serif;`
- https://www.w3schools.com/cssref/css3_pr_font-face_rule.php
- letter-spacing: khoảng cách giữa các chữ cái trong câu
- line-clamp: không hiển thị hết các chữ mà chỉ hiển thị n dòng kèm dấu '...'
- line-height: chiều cao dòng
- list-style: hình dấu chấm tròn/ chữ số trước các list-item (thẻ ul -> li, hoặc ol -> li)
- text align: căn lề chữ (trái / phải / giữa / đồng đều)
- text-color: màu
- text-decoration: gạch dưới (gạch trên/ gạch ngang) chữ
- text-transform: in hoa hay in thường chữ
- text-overflow: khi chiều rộng của dòng không đủ để hiển thị hết trọn vẹn 1 từ (word)
- text-indent: canh lề chữ đầu tiên của đoạn văn bản
- vertical-align: nếu chiều cao dòng (line height) lớn quá so với cỡ chữ (font size), thì chữ sẽ nằm ở vị trí nào của dòng: top, bottom, middle
- white-space: quy định việc hiển thị đoạn văn bản khi trong code có nhiều khoảng trắng (dấu cách- space) và có cho xuống dòng chữ không
- word-break: nếu một từ (word) có nhiều chữ cái (letter) quá, hiển thị trên 1 dòng hay cho xuống dòng


### Background
- ảnh nền của một phần tử (các thẻ html)
- background-attachment: thuộc tính CSS quyết định trạng thái cuộn của ảnh background khi tương các với scroll-bar (scroll bar xuất hiện khi nội dung bên trong phần tử vượt quá chiều cao của nó)
- background-clip: quyết định xem phần diện tích chiếm được của background bên trong phần tử text -> content -> padding -> border
- background-color: màu nền của phần tử
- background-position: khi kích thước của ảnh background lớn hơn kích thước của phần tử thì hiển thị vị trí nào của ảnh
- background-repeat: khi kích thước ảnh nhỏ hơn kích thước phần tử (thường là trường hợp nhỏ hơn nhiều lần) thì quyết định xem sẽ hiển thị background như nào
- background-size: điều chỉnh kích thước ảnh cho vừa vặn với kích thước theo 1 chiều (contain) hoặc tất cả các chiều (cover) của phần tử


