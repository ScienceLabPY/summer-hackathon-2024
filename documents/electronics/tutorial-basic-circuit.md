# Hướng dẫn: Mạch điện cơ bản với Fritzing

Tài liệu này cung cấp hướng dẫn chi tiết và minh họa cụ thể để người dùng mới có thể sử dụng phần mềm Fritzing một cách hiệu quả. Mục tiêu là giúp người dùng xây dựng, chỉnh sửa và quản lý các dự án mạch điện tử một cách dễ dàng, từ việc bắt đầu dự án, sắp xếp môi trường làm việc, xây dựng và kết nối mạch điện, đến việc chỉnh sửa thuộc tính và xuất mạch điện dưới các định dạng khác nhau. Tài liệu nhấn mạnh tầm quan trọng của việc lưu dự án thường xuyên và cung cấp các mẹo hữu ích để tối ưu hóa quy trình làm việc trong Fritzing.

### Mục lục:
1. [Bắt đầu dự án mới](#bắt-đầu-dự-án-mới)
2. [Sắp xếp môi trường](#sắp-xếp-môi-trường)
3. [Xây dựng mạch điện](#xây-dựng-mạch-điện)
4. [Chỉnh sửa thuộc tính](#chỉnh-sửa-thuộc-tính)
5. [Xuất mạch điện](#xuất-mạch-điện)

---

#### Bắt đầu dự án mới

Trước khi bắt đầu một dự án trong Fritzing, bạn cần xây dựng một mạch điện thực tế và đảm bảo nó hoạt động đúng cách. Sau đó, bạn sẽ xây dựng lại mạch điện này trong Fritzing.

Bắt đầu bằng cách mở Fritzing, đặt tên và lưu dự án của bạn. Việc lưu dự án ngay từ đầu và thường xuyên trong quá trình làm việc là rất quan trọng vì Fritzing vẫn đang ở giai đoạn Alpha và có thể bị crash.

![Opening Fritzing](https://fritzing.org/assets/uploads/fritzing__png_versions/small_Fritzing_-ac262c919045f26241d180ddb2cd1a4dee94fc645bb427341888e5822b747bea.png)

1. Từ thanh menu Fritzing, chọn File > Save As...
2. Đặt tên và chọn vị trí cho dự án, sau đó nhấp vào Save.

![Save Project](https://fritzing.org/assets/uploads/learning/building_circuit/building_circuit_1_jpg_versions/big_building_circuit_1-ba077c31b7230289c7c73ee8805e52c541f395b2a4898645b1cf76da46376a14.jpg)

---

#### Sắp xếp môi trường

Trước khi bắt đầu làm việc, chúng ta có thể muốn sắp xếp môi trường làm việc theo nhu cầu và sở thích của mình.

1. Từ thanh Menu Fritzing, chọn Window > và đánh dấu các cửa sổ palette mà bạn muốn hiển thị trong môi trường.
2. Kéo & thả các cửa sổ palette vào bất cứ đâu trong môi trường và chú ý cách các cửa sổ sắp xếp lại, kết hợp hoặc nổi.
3. Chọn chế độ xem breadboard trong Navigator, nếu nó chưa được chọn.

![Breadboard View](https://fritzing.org/assets/uploads/learning/building_circuit/building_circuit_2_jpg_versions/big_building_circuit_2-efb2f46d2591c023d0955cbfadbcf611cfd5f647d53ced2e051759e0bbc1083c.jpg)

---

#### Xây dựng mạch điện

Đảm bảo mạch điện của bạn trong thực tế hoạt động đúng cách. Sau đó, xây dựng lại mạch điện của bạn trong Fritzing theo các hướng dẫn sau:

1. Kéo & thả một Arduino từ cửa sổ Parts palette vào Project View.
2. Làm tương tự với breadboard và tất cả các bộ phận khác của mạch điện. Nếu bạn không tìm thấy một phần nào đó trong thư viện, sử dụng Mystery Part (biểu tượng giống dấu hỏi - ?). Mystery Part sẽ cho phép bạn nhanh chóng định nghĩa một phần mới và các đầu nối của nó (thông qua Inspector).
3. Bạn có thể sắp xếp các phần bằng cách chọn, kéo và thả, hoặc sử dụng các chức năng trong thanh menu, dưới mục Part.
4. Để xóa một phần, chỉ cần chọn và nhấn BACKSPACE.
5. Nhấp & kéo đầu nối +5V của Arduino. Điều này sẽ tạo ra một dây nối. Thả dây nối vào một trong các đầu nối của breadboard. Kết nối được xác nhận bởi một vòng tròn hoặc hình vuông màu xanh lá cây nhỏ.

![Wire Connection](https://fritzing.org/assets/uploads/learning/building_circuit/building_circuit_3_jpg_versions/big_building_circuit_3-c18bd67032071e59b43640caa8508ec6659e4caa7b50658eff53c8d3b752b961.jpg)

6. Kết nối tất cả các phần cho đến khi mạch điện trông giống hệt như mạch điện của bạn trong thực tế. Chú ý rằng các đầu nối không kết nối đúng sẽ được tô màu đỏ.
7. Nếu bạn nhấp và giữ trên một đầu nối, Fritzing sẽ làm nổi bật tất cả các đầu nối đồng thế. Điều này thực sự hữu ích nếu bạn muốn xem toàn bộ tập hợp các kết nối gắn liền với kết nối này.
8. Bạn có thể uốn cong dây nối bằng cách thêm các điểm uốn. Chỉ cần kéo chúng ra khỏi dây nối.

![Breadboard View](https://fritzing.org/assets/uploads/learning/building_circuit/building_circuit_4_jpg_versions/big_building_circuit_4-9a4013e895ec59d601585395067a102528de39f14dcabd63df8b6a10974429c8.jpg)

Chọn các tab schematic và pcb để xem hoặc chỉnh sửa mạch điện của bạn trong các chế độ xem này.

---

#### Chỉnh sửa thuộc tính

Bây giờ khi chúng ta đã kết nối tất cả các phần, hãy xem cách chúng ta có thể chỉnh sửa các thuộc tính của từng phần.

1. Chọn bất kỳ phần nào của mạch điện và xem cửa sổ Part Inspector palette.
2. Nhấp vào tên phần và đổi tên nó. Điều này hữu ích khi bạn muốn phân biệt giữa các phần tương tự.
3. Thử thay đổi các thuộc tính khác.

![PCB View](https://fritzing.org/assets/uploads/learning/building_circuit/building_circuit_5_jpg_versions/big_building_circuit_5-f997dc8ecb28eac8d6c7468b531526eaab6b42e6be88eac100d0630da2817bae.jpg)

Bạn cũng có thể thay đổi thuộc tính của các phần trong PCB View. Hình dạng của bảng mạch có thể được thay đổi thành một Arduino shield, một hình chữ nhật có thể thay đổi kích thước hoặc một hình dạng tùy chỉnh.

![Custom Shape](https://fritzing.org/assets/uploads/learning/building_circuit/building_circuit_6_jpg_versions/big_building_circuit_6-bb60e3b4d0bb3467edcf8c80f7468c6cec139ca1886a37c32d38da56584170e6.jpg)

---

#### Xuất mạch điện

Sau khi hoàn thành việc xây dựng mạch điện, lưu dự án của bạn. Bạn có thể muốn xuất mạch điện dưới dạng tệp hình ảnh hoặc PDF.

1. Chọn chế độ xem Project View mong muốn để xuất (breadboard, schematic hoặc pcb).
2. Từ thanh menu Fritzing, chọn File > Export > và định dạng mong muốn.

![Export Format](https://fritzing.org/assets/uploads/learning/building_circuit/building_circuit_7_jpg_versions/big_building_circuit_7-00569767fde7d9f1264a1d7188cf43ec5359c11204ecdec761eb45a818960b63.jpg)

---

Bây giờ khi chúng ta đã đi qua quy trình làm việc cơ bản, hãy tiếp tục và học cách tạo các phần tùy chỉnh và cách thiết kế một PCB.

```
Science Lab © 2021
```
