# 1. Các kiến thức / key word sử dụng

## Hook

Cho phép bạn sử dụng state và các chức năng khác của React mà không cần tạo class. -> Giúp người dùng có thể sử dụng function component thay cho class component

## State và Props; chilrent props

## One way data flows

Data chỉ truyền theo 1 đường từ component cha -> con

## Prop Drilling

Truyền prop qua nhiều components cha -> con dù cho chỉ sử dụng ở component con mà không sử dụng ở component cha

## Side effect react

Các hoạt động / hành vi diễn ra sau khi component render

## Fragment, StrictMode

## useState

Quản lý state -> Re-render component khi state thay đổi

## useEffect

Thực hiện side effect -> Thực hiện sau khi component re-render. -> Thường dùng để kết nối với hệ thống bên ngoài như call API,...</br >

Nguyên lý hoạt động:

- Chạy setup code khi khởi tạo component
- Khi một trong các dependencies thay đổi -> Sau khi component re-render, chạy cleanup code với old props and state sau đó chạy setup code với new props and state.
- Chạy cleanup code chạy 1 lần cuối cùng sau khi component được removed

## useRef()

Refer đến 1 giá trị không cần re-render -> Thường dùng để refer đến 1 DOM

## useReducer()

Dùng khi 1 số state có cùng logic hoặc dùng khi cần update 1 vài state đồng thời: [state, dispatch] = useReducer(reducer, initialArg, init?)

- initialArg: Giá trị khởi tạo state
- init: function khởi tạo giá trị cho state
- reducer (currentState, action): function update state
  -> Khi gọi dispatch(), reducer nhận giá trị action = param truyền vào dispatch(), sau đó thực hiện logic bên trong reducer()

## Lifting state up

Nếu 2 hoặc nhiều component cùng cấp muốn truy cập vào data của component còn lại, ta cần:

- Đưa state đó từ component con lên component cha.
- Sau đó truyền đến các component con cần dùng đến data đó.

## Custom hook

## React-router

Tham khảo chi tiết tại: [Context Hooks]("3 React router.md")

## Context API

## UI state

Các state lưu thông tin của người dùng thao tác như form input, hiển thị các phần tử, giao diện dựa vào hoạt động của người dùng.

## Remote state

Các state lưu data dựa vào fetch() từ server hoặc database.

## Các vị trí sử dụng state:

- Local component: useState(), useReducer(), useRef() -> Local state
- Parent component: useState(), useReducer(), useRef() -> Dùng để truyền data xuống các component con cần nó (Lifting state up)
- Context: Context API + useState() / useReducer() -> Global state (Khuyến cáo dùng cho UI state mà ít thay đổi: Color thêm, authenticate user)
- Thư viện của bên thứ 3: Redux, React query, SWR, Zustand, ... -> Global state (Khuyến cáo dùng cho remote state)
- URL: React router -> Global state, truyền data giữa các page

## Các loại state:

- UI state: Local (useState(), useReducer(), useRef() ); Global state (Context API + useState() / useReducer(); React router; Redux, Zustand, Recoil ....)
- Remote state: Local (fetch + useEffect + useState/useReducer ) ; Global state (Khuyên dùng các tool đặc biệt để xử lý: React query, SWR, RTK query)

# 2. Một số thư viênj hay

- [React Leaflet](https://react-leaflet.js.org/docs/start-introduction/): Thư viện dùng cho map tương tự như google map
