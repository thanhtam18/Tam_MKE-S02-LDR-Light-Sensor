# Cảm biến ánh sáng quang trở MKE-S02 LDR light sensor

## Giới thiệu

Cảm biến ánh sáng quang trở MKE-S02 LDR light sensor được sử dụng để đo cường độ ánh sáng bằng quang trở LDR (Light Dependent Resistor), thích hợp với các ứng dụng: đo cường độ sáng môi trường, bật tắt đèn tự động,..., cảm biến trả ra giá trị điện áp Analog tuyến tính tương ứng với cường độ ánh sáng của môi trường giúp bạn có thể ghi nhận và xử lý thông tin một cách chính xác nhất, ngoài ra cảm biến còn được bổ sung các thiết kế ổn định, chống nhiễu.

Cảm biến ánh sáng quang trở MKE-S02 LDR light sensor thuộc hệ sinh thái phần cứng Robotics MakerEdu nên có thể sử dụng trực tiếp an toàn với các mạch điều khiển trung tâm ở cả hai mức điện áp 3.3VDC và 5VDC như: Arduino, Raspberry Pi, Jetson Nano, Micro:bit,....với chuẩn kết nối Connector XH2.54 thông dụng.

## Nguyên lý hoạt động

Cảm biến hoạt động dựa trên sự thay đổi điện trở (độ dẫn điện) của quang trở (LDR-Light Dependent Resistor) với cường độ ánh sáng của môi trường, để chuyển giá trị điện trở thành điện áp để có thể đọc bằng bộ chuyển đổi ADC (Analog to Digital Converter) của mạch xử lý ta mắc mạch cầu phân áp như sau:

![image](/image/MKE_S02_LDR_Sensor_01.jpg)

Diễn giải các giá trị:

- VCC: điện áp cấp nguồn cho cảm biến.
- RS: Giá trị điện trở của quang trở (LDR-Light Dependent Resistor).
- R2: Điện trở tạo thành cấu trúc cầu phân áp với RS, có giá trị xác định theo khuyến nghị của nhà sản xuất.
- Vout: Điện áp đầu ra thay đổi theo giá trị của RS.

Ta thấy theo công thức trong hình giá trị Vout sẽ thay đổi theo giá trị của điện trở RS, mà RS sẽ thay đổi theo cường độ ánh sáng của môi trường, khi đó dùng mạch xử lý để đo Vout ta xác định được cường độ ánh sáng môi trường tại thời điểm đo.

## Thông số kỹ thuật

- Điện áp hoạt động: 5VDC
- Chuẩn giao tiếp: Analog
- Điện áp giao tiếp: 0~3.3VDC
- Đo cường độ ánh sáng bằng quang trở (LDR-Light Dependent Resistor)
- Sử dụng trực tiếp an toàn với các board mạch giao tiếp ở cả hai mức điện áp 3.3VDC và 5VDC như: Arduino, Raspberry Pi, Jetson Nano, Micro:bit,....
- Bổ sung thêm các thiết kế ổn định, chống nhiễu.
- Chuẩn kết nối: connector XH2.54 3Pins
- Thuộc hệ sinh thái phần cứng Robotics MakerEdu, tương thích tốt nhất khi sử dụng với các //

## Hình ảnh sản phẩm

![MKE_S01_Ultrasonic](/image/MKE_S02_LDR_Sensor_02.jpg)

![MKE_S01_Ultrasonic](/image/MKE_S02_LDR_Sensor_03.jpg)

## Kích thước sản phẩm

![MKE_S01_Ultrasonic](/image/MKE_S02_LDR_Sensor_04.jpg)

## Các chân tín hiệu

- GND: Chân cấp nguồn âm 0VDC
- 5V: Chân cấp nguồn dương 5VDC
- TRIG: Chân tín hiệu ngõ vào Trigger (Input: 3.3~5VDC)
- ECHO: Chân tín hiệu ngõ ra Echo (Output: 3.3VDC)

## Hướng dẫn sử dụng

### Các thiết bị sử dụng trong bài hướng dẫn:

#### Arduino:
- [Mạch Vietduino Uno (Arduino Uno Compatible)](https://github.com/makerlabvn/Vietduino-Uno)
- [Mạch MakerEdu Shield for Arduino](https://github.com/makerlabvn/MakerEdu-Shield-for-Arduino)
- [Mạch màn hình LCD1602 I2C Display Module](https://github.com/makerlabvn/MKE-M07-LCD1602-I2C-Display-Module)

#### mBlock:

- [Mạch MakerEdu Creator (Arduino Uno Compatible)](https://github.com/makerlabvn/MakerEdu-Creator)
- [Mạch màn hình LCD1602 I2C Display Module](https://github.com/makerlabvn/MKE-M07-LCD1602-I2C-Display-Module)

#### Micro:bit:

- Mạch Micro:bit V2 hoặc các phiên bản tương thích.
- [Mạch MakerEdu Shield for Micro:bit](https://github.com/makerlabvn/MakerEdu-Shield-for-Microbit)
- [Mạch màn hình LCD1602 I2C Display Module](https://github.com/makerlabvn/MKE-M07-LCD1602-I2C-Display-Module)

### Hướng dẫn sử dụng với Arduino (Code C)
- Tải và cài đặt [phần mềm Arduino tại đây.](https://www.arduino.cc/en/software)
- Trong Tools / Library Manager, tìm và cài đặt bộ thư viện tổng hợp "MAKERLABVN" by MakerLab.vn
- Mở chương trình mẫu tại File / Examples / MAKERLABVN / Sensor / MKE-S01_Ultrasonic hoặc [tải chương trình mẫu tại đây](https://github.com/thanhtam18/Tam_MKE-S02-LDR-Light-Sensor/tree/main/arduino)
- Chọn board là Arduino Uno (mạch Vietduino Uno tương thích với Arduino Uno), chọn đúng cổng COM Port của mạch và tiến hành nạp chương trình.
- Kết nối mạch Vietduino Uno với MakerEdu Shield, kết nối cảm biến tại cổng [D12,13] và màn hình LCD vào cổng [I2C] trên MakerEdu Shield, cấp nguồn qua cổng USB của Vietduino Uno để thấy chương trình hoạt động.

### Hướng dẫn lập trình với mBlock (kéo thả khối)

- Tải và cài đặt phần mềm mBlock 5 ([Windows](https://www.mediafire.com/file/ma55iajd7glwmbo/%255BMakerLab.vn%255D_mBlock_V5.4.3_for_Windows.zip/file) / [Mac Intel](https://www.mediafire.com/file/pjfngy6d7ktb55f/%255BMakerLab.vn%255D_mBlock_V5.4.3_for_Mac_Intel.zip/file) / [Mac M1M2](https://www.mediafire.com/file/mfdkgpgnpa7uv2s/%255BMakerLab.vn%255D_mBlock_V5.4.3_for_Mac_M1M2.zip/file))
- Thêm Device "MakerEdu Creator" by MakerEduVN
- Thêm Extension "Upload Mode Broadcast" by mBlock Official
- Thêm Extension "MakerEdu Hardware" by MakerEduVN
- Mở [chương trình mẫu tại đây](/mBlock5), kết nối MakerEdu Creator với máy tính và nạp chương trình.
- Kết nối cảm biến với cổng [D3,D2] và màn hình LCD vào cổng [I2C] trên MakerEdu Creator, cấp nguồn qua cổng USB của MakerEdu Creator để thấy chương trình hoạt động.


### Hướng dẫn lập trình với Micro:bit (kéo thả khối)

- Khởi động phần mềm MakeCode theo hướng dẫn.
- Cài đặt Extension MakerEdu Hardware trên MadeCode theo đường link sau: [https://github.com/makerlabvn/MakerEdu_Hardware](https://github.com/makerlabvn/MakerEdu_Hardware)
- Mở [chương trình mẫu tại đây](/microbit), kết nối Micro:bit với máy tính và nạp chương trình.
- Kết nối mạch Micro:bit với MakerEdu Shield, kết nối cảm biến tại cổng [P0+P1] và màn hình LCD vào cổng [I2C] trên MakerEdu Shield, cấp nguồn qua cổng USB của MakerEdu Shield để thấy chương trình hoạt động.

## Hỗ trợ và liên hệ:

- Website: [https://www.makerlab.vn/](https://www.makerlab.vn/)
- Facebook: [https://www.facebook.com/makerlabvn](https://www.facebook.com/makerlabvn)

## Nhà phân phối

- Các bạn có thể mua sản phẩm tại các [nhà phân phối của MakerLab](https://www.makerlab.vn/nha-phan-phoi/).
