# 1. Khái niệm

Là một thư viện giúp quản lý global state.

# 2. Keyword

- Redux
- Redux thunk: Hỗ trợ nhiệm vụ đồng bộ data với bên ngoài như call external API
- Redux devtools: Hỗ trợ debug và inspect Redux application dễ dàng hơn
- Redux toolkit (RTK): Được xây dựng dựa trên redux giúp làm đơn giản và ngắn gọn code hơn, chứa đựng các API method và các common dependencies giúp xây dựng các ứng dụng redux dễ dàng hơn. (Code khởi tạo reducer, state, function update state dễ dàng hơn)

# 3. Ưu/nhược điểm

Ưu điểm:

- Chỉ cần 1 lần setup, dễ dàng mở rộng và thêm mới state.
- Hỗ trợ middleware (như redux thunk,...) cho các tính năng đồng bộ data như call external API.
- Hiệu suất được tối ưu hóa sẵn (Performance is optimized **out of the box**)
- Có thể sử dụng redux devtools để xem cách hoạt động và giá trị của các state

Nhược điểm:

- Yêu cầu cần cài đặt thêm pachkage mới -> Gây tăng size của phần mềm.
- Cần thực hiện nhiểu thao tác để setup khởi tạo.

# 4. Các trường hợp nên sử dụng

- Thường sử dụng cho global state trong large app
- Khi có 1 lượng lớn global UI state mà cần **thay đổi thường xuyên** (do redux đã tối ưu cho điều đó): current tabs, complex filters or search, shopping cart,...
- Khi có complex state với các nested object và arrays

# 5. Tài liệu tham khảo

Tham khảo chi tiết:

- [Redux](https://redux.js.org/tutorials/index)
- [Redux thunk](https://redux.js.org/usage/writing-logic-thunks)
- [Redux-toolkit](https://redux-toolkit.js.org/tutorials/overview)
