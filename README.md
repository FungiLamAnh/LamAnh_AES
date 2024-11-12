# AES_Mã Hoá
## Đặc điểm cơ bản của AES
* AES là dạng mã hoá đối xứng, sử dụng một khóa chung để mã hóa và giải mã. Khóa này phải được giữ bí mật giữa các bên để bảo mật dữ liệu.
* AES làm việc với các khối dữ liệu có kích thước cố định là 128 bit (16 byte).
* AES hỗ trợ ba kích thước khóa khác nhau là 128, 192 và 256 bit, tương ứng với các phiên bản AES-128, AES-192 và AES-256.
* Số vòng (rounds): Số vòng mã hóa phụ thuộc vào độ dài khóa:
  - 10 vòng cho AES-128
  - 12 vòng cho AES-192
  - 14 vòng cho AES-256
## Nguyên lý hoạt động AES
* Key Expansion (Mở rộng khóa): Mở rộng khóa ban đầu thành nhiều khóa con (round keys) sử dụng trong mỗi vòng.
* Initial Round: Giai đoạn ban đầu chỉ bao gồm bước AddRoundKey.
* Main Rounds: Các vòng chính của AES bao gồm 4 bước chính:
  - SubBytes: Thay thế từng byte của khối dữ liệu bằng một giá trị khác dựa trên một bảng tra cứu (S-box).
  - ShiftRows: Dịch chuyển các hàng của khối dữ liệu theo một số bước cố định để tạo sự phân tán.
  - MixColumns: Trộn các cột của khối dữ liệu bằng các phép toán đại số để tăng sự khuếch tán.
  - AddRoundKey: Kết hợp khóa con (round key) với khối dữ liệu qua phép XOR.
* Final Round: Vòng cuối cùng chỉ bao gồm ba bước: SubBytes, ShiftRows, và AddRoundKey (không có MixColumns).
