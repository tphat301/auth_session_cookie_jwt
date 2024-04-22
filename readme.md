## Authentication (xác thực) là gì?

- Authentication là một cơ chế xác thực người dùng, kiểm tra xem người dùng đang truy cập vào hệ thống có phải là một người dùng hợp lệ hay không.
- VD: Khi người dùng vào một website nào đó. Chúng ta muốn kiểm soát được thông tin người dùng (họ là ai? và họ được phép truy cập vào nguồn tài nguyên nào?) bắt buộc chúng ta phải dùng authentication.

## Authorization (ủy quyền) là gì?

- Authorization là một quá trình cấp cho người dùng quyền truy cập vào một tài nguyên nào đó.
- VD: Muốn cho người dùng được bình luận Blog trên website. Nhưng lại không được phép cập nhập hay chỉnh sửa trang cá nhân của người dùng khác

## Session

- Dữ liệu được lưu trữ phía máy chủ nên tính bảo mật rất cao
  VD: Mỗi user đều có một session id mỗi lượt request gửi lên server thì chỉ gửi session id và các thông tin như (username, password,...) của user sẽ không bị lộ. Sau khi nhận được request phía user thì máy chủ sẽ phản hồi lại thông qua request header và trả về các thông tin của người dùng.

- Do dữ liệu được lưu trữ phía máy chủ nên rất khó bị đánh cắp hay chỉnh sửa
- Thời gian tồn tại của Session: tồn tại trong suốt quá trình làm việc và có sẵn ở trình duyệt cho đến khi đóng trình duyệt
- Do phải lưu dữ liệu ở phía máy chủ nên rất dễ dẫn đến việc hao tổn tài nguyên phía máy chủ

## Cookie:

- Dữ liệu được lưu trữ ở phía trình duyệt người dùng nên tính bảo mật không cao (dữ liệu rất dễ bị đánh cắp)
- Dữ liệu chỉ mất đi khi hết thời hạn cookie
- Thời gian tồn tại cookie: tối đa 400 ngày đối với Chrome và 7 ngày đối với Safari

## Hiểu về JSON Web Token (JWT)

- Jwt là một chuẩn mở (RFC 7519) giúp truyền tải thông tin dưới dạng JSON.
- Ở đây có một lưu ý là: Tất cả các JWT đều là token, nhưng không phải tất cả các token đều là JWT.
- Token là gì ?
- Token là một chuỗi ký tự được tạo ra để đại diện cho một đối tượng
- VD: access token, refresh token,...
- Một chuỗi JWT cấu trúc gồm ba phần, mỗi phần được phân tách bởi dấu chấm (.): Header, Payload và Signature.
