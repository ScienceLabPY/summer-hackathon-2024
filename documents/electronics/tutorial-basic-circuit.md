### Tài liệu Hướng Dẫn Sử Dụng Wokwi

#### 1. Giới thiệu về Wokwi
Wokwi là một công cụ trực tuyến giúp bạn mô phỏng và thử nghiệm các dự án điện tử ngay trên trình duyệt web. Wokwi hỗ trợ nhiều loại vi điều khiển, cảm biến và các thành phần điện tử khác, giúp bạn tạo và kiểm tra mạch điện mà không cần phải mua linh kiện thực tế.

#### 2. Bắt Đầu với Wokwi

##### 2.1. Đăng Ký và Đăng Nhập
- Truy cập trang web Wokwi: [wokwi.com](https://wokwi.com)
- Đăng ký tài khoản hoặc đăng nhập nếu bạn đã có tài khoản.

##### 2.2. Tạo Dự Án Mới
- Chọn loại vi điều khiển mà bạn muốn sử dụng, ví dụ: Arduino Uno, ESP32, v.v.

![Tạo Dự Án Mới](/assets/wokwi/wokwi.png)

#### 3. Thiết Kế Mạch Điện

⚠️ Chú ý: Không phải tất cả các linh kiện điện tử đều được hỗ trợ trong mô phỏng. Luôn kiểm tra danh sách linh kiện hỗ trợ trước khi bắt đầu dự án.
⚠️ Chú ý: Trình mô phỏng có thể không có cùng bố cục chân như thiết bị vật lý của bạn. Luôn tham khảo tài liệu kỹ thuật của nhà sản xuất!

Trong hướng dẫn này, chúng tôi sử dụng mạch ESP32-S3 để minh họa cho các bước thao tác. Nếu bạn chưa biết, vui lòng xem qua về [ESP32-S3](https://classroom.google.com/c/NzAyMjgzNzM1NTE5/m/NjkxNzYyNDg3NDgz/details).

**Không gian làm việc** của Wokwi:
![Không gian làm việc](/assets/wokwi/workspace.png)

##### 3.1. Thêm Linh Kiện
- Nhấn vào biểu tượng "Add Part" để thêm các linh kiện vào mạch.
- Tìm kiếm và chọn linh kiện cần thiết, ví dụ: LED, điện trở, tụ điện, cảm biến, v.v.

##### 3.2. Kết Nối Linh Kiện
- Kéo và thả linh kiện vào vùng làm việc.
- Kết nối các chân của linh kiện bằng cách kéo dây nối giữa chúng.

![Kết Nối Linh Kiện](/assets/wokwi/interaction.gif)

#### 4. Lập Trình Vi Điều Khiển

⚠️ Chú ý: Bạn sẽ không thể truy cập các cổng ngoại vi thực sự của vi điều khiển trong mô phỏng. Ví dụ: không thể kết nối với cổng USB, kết nối WiFi, Bluetooth hoặc giao tiếp với các thiết bị ngoại vi thực sự.

##### 4.1. Viết Mã
- Chuyển sang tab "Code" để viết mã điều khiển vi điều khiển.
- Sử dụng ngôn ngữ lập trình phù hợp (ví dụ: C++ cho Arduino).

```cpp
// Ví dụ: Chớp tắt LED trên Arduino
int ledPin = 13;

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  digitalWrite(ledPin, HIGH);
  delay(1000);
  digitalWrite(ledPin, LOW);
  delay(1000);
}
```

##### 4.2. Chạy Mô Phỏng
- Nhấn vào nút "Start Simulation" để chạy mô phỏng và kiểm tra hoạt động của mạch.
- Quan sát kết quả mô phỏng trực tiếp trên màn hình.

![Chạy Mô Phỏng](/assets/wokwi/simulation.gif)

#### 5. Một Số Dự Án Mẫu

##### 5.1. Chớp Tắt LED
- **Mạch Điện**: Arduino Uno, 1 LED, 1 điện trở 220Ω.
- **Mã Nguồn**: Xem ví dụ ở trên.

##### 5.2. Đo Nhiệt Độ Bằng Cảm Biến DHT11
- **Mạch Điện**: Arduino Uno, cảm biến DHT11.
- **Mã Nguồn**:

```cpp
#include "DHT.h"

#define DHTPIN 2
#define DHTTYPE DHT11

DHT dht(DHTPIN, DHTTYPE);

void setup() {
  Serial.begin(9600);
  dht.begin();
}

void loop() {
  float h = dht.readHumidity();
  float t = dht.readTemperature();

  Serial.print("Độ ẩm: ");
  Serial.print(h);
  Serial.print("%  Nhiệt độ: ");
  Serial.print(t);
  Serial.println("°C");
  
  delay(2000);
}
```

#### 6. Kết Luận
Wokwi là công cụ mạnh mẽ và dễ sử dụng cho cả người mới bắt đầu và những người có kinh nghiệm trong lĩnh vực điện tử. Hy vọng hướng dẫn này sẽ giúp bạn bắt đầu dễ dàng và tạo ra những dự án thú vị.

Nếu bạn cần thêm thông tin hoặc hỗ trợ, hãy liên hệ với tôi.

```
Science Lab © 2024. Bản quyền thuộc về Science Lab.
```