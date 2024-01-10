# 1. Box position
Dùng thuộc tính **position** với CSS thuần để sắp xếp các phần tử.<br />
Thuộc tính **position** có:
 - 5 giá trị chính: static | relative | absolute | fixed | sticky<br />
 - Các thuộc tính có nhiệm vụ căn chỉnh vị trí của element (thuộc tính Helper): top | right | bottom | left | z-index.<br />
 >**Lưu ý**: ác thuộc tính Helper không thể hoạt động nếu như không khai báo thuộc tính position, hoặc với position: static

# 2. Static
Đây là giá trị mặc định
# 3. Relative
Vị trí mới của một element tương quan/ liên hệ tới vị trí mặc định của nó. Tuy nhiên điều này lại không ảnh hưởng đến các box khác (**không thay đổi bố cục xung quanh vị trí đó**.). Điều này cho phép vị trí mới của box có thể chồng lên các box khác<br />
> Với position: relative, chúng ta có thể dễ dàng thay đổi vị trí của chúng. Nhưng cần khai báo để điều chỉnh vị trí của element bằng các thuộc tính **helper**.

Ví dụ:
```CSS
.box-orange {
  position: relative;  // chúng ta có thể di chuyển được element
  background: orange;
  width: 100px;
  height: 100px;
  top: 100px;         // dịch chuyển xuống 100px từ vị trí ban đầu của nó 
  left: 100px;        // dịch chuyển sang phải 100px
}
```

# 4. Absolute
Với **position: absolute**, một element được dịch chuyển tới một vị trí mới **dựa trên ví trí bình thường** của chính nó. Tuy nhiên, position: absolute sẽ dịch chuyển vị trí của nó **tương ứng với thẻ cha của nó** và **thay đổi bố cục xung quanh vị trí đó**.

>Một element được khai báo với thuộc tính **position: absolute** sẽ được **loại bỏ khỏi luồng document (document flow)**. Vị trí mặc định của element sẽ là **điểm bắt đầu (top-left)** của **element cha**. Nếu nó không có bất cứ thẻ cha nào thì thẻ document <html> sẽ là cha của nó.

# 5. Fixed
Một element được khai báo với thuộc tính **position: fixed** sẽ được **loại bỏ khỏi luồng document (document flow)**:
 - Vị trí của chúng CHỈ tương quan với thẻ <html>
 - Chúng không bị ảnh hưởng bới scroll
# 6. Keyword, Tài liệu tham khảo