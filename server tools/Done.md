## **download one files**
hiện đang download cả metadata của file vào content ?

phần server tools hiện tại em thấy còn 2 phần chính là

1. **giữ connection để các api dùng lại**
2. **giảm thời gian response khi access folder nữa**

các phần update giao diện
1. **Để not found khi ko tìm thấy file manager** (làm dropdown cho chọn ip)
2. **bấm vào file seleted thì ko hiện nút checked nữa**
3. **ko refresh vs các action cancel, chỉ lưu mới refresh**
![[Pasted image 20240611114347.png]]với ko cần viết kiểu trả về như này nhé, để nó tự động detect kiểu trả về cũng được


![[Pasted image 20240611113830.png]]mấy cái warning này cũng rút gọn bớt theo IDE nó gợi ý ih cho gọn code

thay thế unzipper @lechuhuuha/unzipper thành unzipper bản mới nhất