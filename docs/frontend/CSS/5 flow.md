# 1. Writing Mode
Là chiều đọc các phần tử của ngôn ngữ<br />

Lưu ý: Có nhiều loại Writing Mode tương ứng với các loại ngôn ngữ khác nhau: Trên xuống dưới, trái qua phải, phải qua trái, dưới lên trên. Ví dụ như tiếng Anh hoặc tiếng Việt thì sẽ hiển thị từ trái qua phải, từ trên xuống dưới

# 2. FLow
Normal Flow, hoặc Flow Layout, là cách mà các phần tử Block và Inline được hiển thị trên trang trước khi có bất kỳ thay đổi nào về bố cục. Flow trong trường hợp này là một tập hợp các yếu tố hoạt động cùng nhau và biết về nhau trong bố cục của bạn. Khi một yếu tố được loại khỏi flow, nó hoạt động độc lập.<br />

Trong normal flow, các phần tử inline được hiển thị theo hướng inline, tức là theo hướng từ trái sang phải tương ứng với cách từ được hiển thị trong một câu theo Writing Mode của tài liệu. Các phần tử block hiển thị liên tiếp nhau, giống như các đoạn văn trong Writing Mode của tài liệu. Vì vậy, trong tiếng Anh, **các phần tử inline** được hiển thị **liên tiếp nhau**, **bắt đầu từ bên trái**, và các phần tử **block bắt đầu từ đầu trang và di chuyển xuống dưới trang**.<br />


# 3. Display
Mô tả cách các phần tử được hiển thị như nào: inline, block, flex,...

# 4. Block and Inline

Với element format theo 1 **block formatting context**:
Trong 1 **block formatting context**, các box model được sắp xếp liên tiếp nhau theo chiều dọc(chế độ **viết ngang**), bắt đầu từ **containing block**. Khoảng cách giữa các box model bên trong 1 **containing block** được xác định bởi thuộc tính **margin**. Và cạnh trái của mỗi box model sẽ tiếp xúc với cạnh trái của **containing block** (Dùng cho **right-to-left** formatting).


Với element format theo 1 **inline formatting context**:
Trong 1 **inline formatting context**, các box model được sắp xếp liên tiếp nhau theo chiều ngang(chế độ **viết ngang**), bắt đầu từ top của **containing block**. Khoảng cách giữa các box model bên trong 1 **containing block** được xác định bởi thuộc tính **horizontal(lề ngang) margins, borders, and padding**. Các box có thể được căn chỉnh theo chiều theo chiều dọc theo các cách khác nhau: đáy hoặc đỉnh của chúng có thể được căn chỉnh, hoặc các đường cơ sở của văn bản bên trong chúng có thể được căn chỉnh. Khu vực **hình chữ nhật** chứa các boxes tạo thành một dòng được gọi là **line box**.


Ví dụ cụ thể, với Writing Mode là tiếng Anh/tiếng Việt, theo chế độ *viết ngang*:
 - Inline Direction: Theo chiều từ trái qua phải
 - Block Direction: Theo chiều từ trên xuống dưới

Ví dụ cụ thể, với Writing Mode là một số ngôn ngữ theo chế độ *viết dọc*:
 - Inline Direction: Theo chiều từ trên xuống dưới
 - Block Direction: Theo chiều từ trái qua phải

# 5. Float
Thuộc tính này là 1 phần của normal flow, **tác động đến các boxes khác** xung quanh nó. Cho phép đặt các phần tử ở đầu hoặc cuối, trái hoạc phải của **containing block** theo chiều của *Inline Direction* với các giá trị:
 - float: none;
 - float: left;
 - float: right;
 - float: inline-start;
 - float: inline-end;

> Lưu ý: Sử dụng float có thể gây ra 1 vài kết quả không mong muốn: Box dùng float vượt ra ngoài container của **containing block**.

# 6. Inline, Vertical Align, Line-Height
## 6.1 vertical alignment
**line box** luôn có chiều cao đủ để chứa tất cả các boxes ở bên trong. Tuy nhiên, ta có thể set chiều cao cho nó cao hơn chiều cao của các phần tử bên trong nó. Khi chiều cao của 1 box B nhỏ hơn chiều cao của **line box** chứa nó, sắp xếp phần tử B theo chiều dọc (vertical alignment) của B bên trong **line box** được xác định bởi thuộc tính **"vertical-align"** (baseline/top/middle/bottom/sub/text-top).
> Property **"vertical-align"** sets **vertical alignment** of an inline, inline-block or table-cell box.

## 6.2 horizontal direction
Khi tổng chiều rộng của tất cả các inline-level boxes nhỏ hơn chiều rộng của *line box* chứa nó, vị trí theo chiều ngang (horizontal alignment) của các boxes bên trong **line box** được xác định bởi thuộc tính *"text-align"* (start/end/center/justify).
The **"text-align"** CSS property sets the **horizontal alignment** of the inline-level content inside a block element or table-cell box. This means it works like vertical-align but in the **horizontal direction**.
> Thuộc tính CSS *line-height* xác định chiều cao của **line box**. Nó thường được sử dụng để đặt khoảng cách giữa các dòng văn bản. Trên **block-level elements**, nó xác định chiều cao tối thiểu của các **line box** trong phần tử. Trên các phần tử inline không được thay thế, nó xác định chiều cao được sử dụng để tính toán chiều cao của **line box**.

## 6.3 Line-Height
Một phần tử inline có 2 chiều cao khác nhau:
 - chiều cao content-area được định nghĩa bởi các chỉ số của font (font-size, font-family).
 - chiều cao line-height, là chiều cao được dùng để tính toán chiều cao của line-box.

# 7. Logical Properties

# 8. Tài liệu tham khảo
[CSS Display Module Level 3](https://www.w3.org/TR/css-display-3/)<br />
[CSS flow layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flow_layout)