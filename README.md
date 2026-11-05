# Analog-IC-Design-Lab
Thư viện thiết kế các cổng logic cơ bản (Standard Cells) phục vụ cho Môn học Thiết kế Vi mạch.

## 1. Giới thiệu chung
Repository này lưu trữ toàn bộ dữ liệu thiết kế sơ đồ nguyên lý (schematic), thiết kế vật lý (layout), ký hiệu đóng gói (symbol) và các môi trường kiểm tra (testbench) cho một thư viện cell.

## 2. Danh mục các mạch đã thiết kế

**Các cổng logic cơ bản (Logic Gates):**
* `INV`: Cổng NOT (Inverter)
* `AND2`, `NAND2`: Cổng AND và NAND 2 ngõ vào
* `OR2`, `NOR2`: Cổng OR và NOR 2 ngõ vào
* `XOR`, `XOR2`: Cổng logic loại trừ

**Các khối tuần tự và mạch chức năng khác:**
* `DFF`: D Flip-Flop
* `TG_sch`: Cổng truyền (Transmission Gate)
* `nmos_char_sch`: Mạch khảo sát đặc tuyến transistor NMOS

**Môi trường mô phỏng (Testbenches):**
* `tb_cmos_gates`: Testbench tổng hợp cho các cổng CMOS
* `testbench_fa1bit`: Testbench cho bộ cộng toàn phần 1 bit (Full Adder)
* Các folder testbench và cấu hình riêng lẻ đi kèm từng mạch (ví dụ: `nand2_tb`, `or2_config`,...).

## 3. Cấu trúc thư mục tiêu chuẩn
Bên trong mỗi folder mạch chính (ví dụ: `DFF`, `INV`, `NAND2`), dữ liệu được tổ chức thành các block con:
* **schematic/**: Chứa bản vẽ sơ đồ mạch nguyên lý.
* **layout/**: Chứa bản vẽ thiết kế hình học vật lý của mạch.
* **symbol/**: Ký hiệu của mạch để tái sử dụng trong các bản vẽ lớn hơn ở mức phân cấp (hierarchical design).
* **av_extracted/** / **constraint/**: Dữ liệu trích xuất ký sinh và các ràng buộc thiết kế.
