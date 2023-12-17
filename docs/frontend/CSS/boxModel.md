# 1. Box model
Box model là 1 kỹ thuật layout cơ bản trong CSS với 4 thành phần:</br >
 - Margin: Khoảng cách tính từ bên ngoài của phần tử. Đại diện bởi thuộc tính **margin**</br >
 - Border: Đường viền của phần tử. Đại diện bởi thuộc tính **border**</br >
 - Padding: Khoảng cách tính từ bên trong của phần tử. Đại diện bởi thuộc tính **padding**</br >
 - Content: Nội dung trong phần tử. Do đó, không có thuộc tính CSS nào đại diện</br >
 ![Box Model](/assets/image/CSS/box-model.png)
# 2. Box sizing
**box-sizing** là một thuộc tính sẽ giúp bạn có thể tính toán và làm chủ được kích thước của một phần tử dựa vào thuộc tính **width** và **height** đã được thiết lập bên trong. Hay nói cách khác, là bạn sẽ muốn thuộc tính **width** và **height** là kích thước đã bao gồm border và padding.</br >

Hiện tại, **box-sizing** có hỗ trợ một số giá trị như sau:</br >
 - **content-box**: Giá trị mặc định, nghĩa là giá trị width và height chỉ áp dụng cho khu vực nội dung bên trong, không bao gồm padding, border và margin.</br >
 - **border-box**: Khi thiết lập giá trị này, thì width và heigh sẽ bao gồm cho cả phần nội dung, padding và border nhưng không bao gồm margin.</br >
 (Nên sử dụng thuộc tính này cho toàn bộ các phần tử giúp cho các phần tử có kích thước như chúng ta đã khai báo)</br >
 - **padding-box**: Với giá trị này thì width và height chỉ bao gồm cho phần nội dung và padding, không bao gồm border và margin.</br >
 (**padding-box** chỉ có tác dụng với trình duyệt **Firefox**.)
# 3. Keyword, Tài liệu tham khảo