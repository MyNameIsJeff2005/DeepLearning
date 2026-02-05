CÂU TRẢ LỜI PHẦN 1:


# So sánh 3 mô hình:

- Mất mát: Tăng số nút (từ 4 lên 8) làm mất mát giảm hơn vì mô hình có khả năng

  học các mẫu phức tạp hơn. Thêm lớp ẩn thứ hai (8-6) giúp mô hình sâu hơn,

  có thể học được các biểu diễn phức tạp hơn.
- Độ chính xác: Mô hình với nhiều nút hơn thường có độ chính xác cao hơn trên

  dữ liệu kiểm tra (nếu không overfitting). Mô hình (2-8-6-1) có thể hiệu quả

  nhất vì nó có tiềm năng học được ranh giới phân loại tốt hơn.
- Tại sao: Với dữ liệu không tuyến tính (vòng tròn/vành đai), những mô hình

  sâu hơn (nhiều lớp ẩn) và rộng hơn (nhiều nút) có thể xấp xỉ được các hàm

  phức tạp tốt hơn.

CÂU TRẢ LỜI PHẦN 2:

## So sánh Loss Function và Optimizer:

1. **BCEWithLogitsLoss vs BCELoss:**

   - Khác biệt: BCEWithLogitsLoss kết hợp Sigmoid vào trong loss function, trong khi

     BCELoss kỳ vọng đầu ra đã được sigmoid. Về mặt toán học, hai cách này tương

     đương nhưng BCEWithLogitsLoss số học ổn định hơn (tránh log(0) hoặc log(1)

     khi sigmoid cho 0 hoặc 1).
   - Mất mát: Giá trị số có thể khác nhau vì scale khác nhau, nhưng độ chính xác

     thường tương tự.
   - Độ chính xác: Nên tương tự nhau vì đều là phân loại nhị phân.
2. **SGD vs Adam:**

   - SGD (Stochastic Gradient Descent) là optimizer đơn giản hơn, cập nhật gradient

     một cách tuyến tính với learning rate cố định.
   - Adam là optimizer tiên tiến hơn, tự điều chỉnh learning rate cho từng tham số

     dựa trên gradient trước đó (có "momentum").
   - SGD mất mát giảm chậm hơn hoặc có thể không giảm đều so với Adam.
   - Độ chính xác cuối cùng của SGD thường thấp hơn Adam.
   - Nguyên nhân: Adam hội tụ nhanh hơn và tìm được điểm tối ưu tốt hơn.

   CÂU TRẢ LỜI PHẦN 3:

   ### Quan sát đồ thị mất mát:


   1. - Mô hình 2-8-1 (8 nút) và 2-4-1 (Adam) giảm nhanh nhất vì Adam optimizer

        hội tụ nhanh. Mô hình 2-8-1 giảm mau hơn 2-4-1 vì có khả năng học tốt hơn.
   2. **Mô hình nào giảm chậm nhất?**

      - Mô hình 2-4-1 với SGD optimizer giảm chậm nhất. SGD là optimizer đơn giản

        hơn, không có adaptive learning rate như Adam.
   3. **Có dao động không?**

      - Mô hình với SGD thường có dao động hơn vì SGD update gradient một cách

        "ngẫu nhiên" hơn, không mịn như Adam.
      - Mô hình 2-4-1 (Adam) và 2-8-1 (Adam) mịn hơn vì Adam có cơ chế làm mền

        gradient updates.
   4. **Kết luận:**

      - Adam optimizer tốt hơn SGD cho bài toán này.
      - Mô hình rộng hơn (8 nút) học tốt hơn mô hình hẹp (4 nút).
      - Đồ thị cho thấy tầm quan trọng của cả cấu trúc mô hình và lựa chọn optimizer.
