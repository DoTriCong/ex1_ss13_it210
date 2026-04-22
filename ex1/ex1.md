Phần 1 - Phân tích: Tại sao thiếu hibernate.dialect lại khiến Hibernate không thể khởi động? 

Thuộc tính nào giúp Hibernate tự động tạo bảng (medicines, prescriptions) từ Java Class?

Vì sao cần hibernate.dialect
Hibernate là ORM, nó phải dịch các thao tác Java thành SQL.
Mỗi hệ quản trị CSDL (MySQL, PostgreSQL…) có cú pháp SQL khác nhau.
Nếu không chỉ định hibernate.dialect, Hibernate không biết dùng cú pháp nào 

-> báo lỗi “Hibernate Dialect must be explicitly set”.

Thuộc tính tạo bảng tự động:

hibernate.hbm2ddl.auto cho phép Hibernate tự động sinh bảng từ Entity.

Các giá trị thường dùng:

update: tự động cập nhật schema theo Entity.

create: tạo mới bảng mỗi lần chạy.

create-drop: tạo bảng khi chạy, xóa khi dừng.

validate: chỉ kiểm tra schema, không tạo.