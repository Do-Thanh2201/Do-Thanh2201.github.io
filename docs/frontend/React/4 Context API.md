# 1. Khái niệm

Context: Cách mà component cha gửi các thông tin (data, prop) xuống cho các component con mà không cần truyền rõ ràng qua các component con trung gian -> Tránh Prop Drilling

# 2. Keyword

createContext: Tạo context

- SomeContext.Provider: Bọc các component con, xác định các giá trị cần truyền / lưu trữ trong context.
- SomeContext.Consumer: Một cách cũ (trước khi useContext ra đời) để các component con đọc các giá trị được truyền trong context.
- useContext(): Cách mới đơn giản hơn để các component con đọc các giá trị được truyền trong context.

# 3. Ưu/nhược điểm

Ưu điểm:

- Được xây dựng bên trong React
- Set up a singe context dễ dàng

Nhược điểm:

- Khi thêm 1 phần state vào ứng dụng, có thể sẽ phải tạo 1 context mới từ đầu
- Tối ưu hóa hiệu suất phức tạp
- Chỉ sử dụng được React devtools để xem state và component

# 4. Các trường hợp nên sử dụng

- Thường sử dụng cho global state trong small app
- Khi cần share value mà **không thay đổi thường xuyên**: Color thêm, preferred language, authenticated user,...
- Khi cần giải quyết vấn đề đơn giản prop drilling
- Khi cần quản lý state ở local sub-tree của app: Không dùng global state toàn app mà chỉ dùng ở 1 nhánh con trong app

# 5. Tài liệu tham khảo

Tham khảo chi tiết:

- [Context Hooks](https://react.dev/reference/react/hooks#context-hooks)
- [Create Context](https://react.dev/reference/react/createContext)
- [Use Context](https://react.dev/reference/react/useContext)
