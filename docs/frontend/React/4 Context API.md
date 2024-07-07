# 1. Khái niệm

Context: Cách mà component cha gửi các thông tin (data, prop) xuống cho các component con mà không cần truyền rõ ràng qua các component con trung gian -> Tránh Prop Drilling

# 2. Keyword / Cách sử dụng

createContext: Tạo context

- SomeContext.Provider: Bọc các component con, xác định các giá trị cần truyền / lưu trữ trong context.
- SomeContext.Consumer: Một cách cũ (trước khi useContext ra đời) để các component con đọc các giá trị được truyền trong context.
- useContext(): Cách mới đơn giản hơn để các component con đọc các giá trị được truyền trong context.

# 3. Tài liệu tham khảo

Tham khảo chi tiết:

- [Context Hooks](https://react.dev/reference/react/hooks#context-hooks)
- [Create Context](https://react.dev/reference/react/createContext)
- [Use Context](https://react.dev/reference/react/useContext)
