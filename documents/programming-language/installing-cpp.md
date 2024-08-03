# Hướng Dẫn Cài Đặt Visual Studio Code Lập Trình C++

**Trong bài viết này mình sẽ giới thiệu đến các bạn một trình biên tập code vừa nhẹ, vừa có giao diện đẹp, lại còn có nhiều tính năng hay, đó chính là Visual Studio Code (vscode). Đồng thời, mình cũng sẽ hướng dẫn các bạn cách cài đặt vscode để code, build, debug một chương trình C++ luôn nhé.**

Để code C++, có rất nhiều IDE, Editor mà ta có thể sử dụng. Một số phổ biến như: Visual Studio, Code::Block hay DevC++, … Tuy nhiên, Visual Studio thì khá nặng, và chiếm nhiều không gian bộ nhớ; Code::Block, DevC++, … thì rất nhẹ và còn đi kèm cả compiler nữa, nhưng giao diện lại hơi “kém sang”.

![VSCode](/assets/pl/vscode.png)


### **Về Visual Studio Code**

Visual Studio Code là một trình biên tập mã được phát triển bởi Microsoft dành cho Windows, Linux và macOS. Nó hỗ trợ chức năng debug, đi kèm với Git, có syntax highlighting, tự hoàn thành mã thông minh, snippets, và cải tiến mã nguồn. Nó cũng cho phép tùy chỉnh, do đó, người dùng có thể thay đổi theme, phím tắt, và các tùy chọn khác. Visual Studio Code miễn phí và là phần mềm mã nguồn mở.

**Lưu ý:** Visual Studio Code không giống Visual Studio IDE

Visual Studio Code rất nhẹ (54 MB với bản dành cho Windows), với yêu cầu phần cứng rất thấp:

* CPU từ 1.6 GHz trở lên
* RAM từ 1 GB
* Có Microsoft .NET Framework 4.5.2


### **Hướng dẫn cài đặt vscode để lập trình C++**


#### **1. Tải và cài đặt vscode**

Các bạn vào trang chủ vscode [link này](https://code.visualstudio.com/), chọn phiên bản phù hợp với thiết bị của các bạn và tải về.

![Download VS Code](/assets/pl/download.png)

Sau khi tải về, tiến hành chạy file cài đặt. Việc cài đặt rất đơn giản, chỉ cần Next – Next – Next là xong.


#### **2. Cài extension C++**

Sau khi cài đặt, vscode sẽ có giao diện như thế này:

![First View](/assets/pl/firstview.png)


Các bạn ấn vào **Extensions** hoặc **Ctrl + Shift + X**, để mở giao diện như hình sau.

![Extension](/assets/pl/extension.png)

Tiếp theo các bạn gõ trên thanh tìm kiếm từ khóa “**C++**”, sau đó chọn extension **C/C++** do **Microsoft** phát hành và ấn **Install** để cài đặt.

![Install C++](/assets/pl/installcpp.png)

### **3. Cài đặt môi trường**

#### **Cài compile: MinGW-w64**

Các bạn vào [link này](https://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/installer/mingw-w64-install.exe/download), chờ khoảng 5 giây, trình biên dịch sẽ tự tải xuống. Sau đó, các bạn hãy tiến hành cài đặt.

![MinGW-w64](/assets/pl/mingw.png)

Lưu ý vị trí lưu compile, các bước sau sẽ cần dùng đến.

![MinGW-w64 Install](/assets/pl/mingw-install.png)

![MinGW-w64 Install](/assets/pl/mingw-installing.png)

Đợi tool tải dữ liệu xong, **Continue**.

![MinGW-w64 Install](/assets/pl/mingw-package.png)

Đến đây, các bạn mark 2 dòng `mingw32-base` và `mingw32-gcc-g++`. Sau đó, **Installation -> Apply Changes**. Rồi tiếp tục chờ ...

![MinGW-w64 Install](/assets/pl/mingw-applying.png)

Đến khi tool tải xong các dữ liệu cần thiết thì **Close** và thoát ra.

#### **Cài biến môi trường**

**Mở của số System**: Chuột phải vào biểu tượng **This PC** -> **Properties**. Hoặc vào **Control Panel** -> **System and Security** -> **System**

Chọn **Advanced system settings** -> **Environment Variables**.

Trong mục **System variables**, chọn **Path** -> **Edit**.

Chọn **New**. Tìm đường dẫn chứa thư mục bin của compile, copy, paste vào rồi nhấn OK.

![Path](/assets/pl/env-var.png)

Đường dẫn của mình là: `C:\Program Files (x86)\mingw-w64\i686-8.1.0-posix-dwarf-rt_v6-rev0\mingw32\bin`

Để kiểm tra đã cài Path thành công hay chưa bạn mở Command Prompt (cmd) và gõ:

```bash
g++ --version
```

Nếu kết quả xuất hiện như hình dưới là bạn đã thành công, nếu không bạn hãy kiểm tra lại nhé.

![g++ version](/assets/pl/gpp-version.png)

### **4. Biên tập và chạy chương trình trên terminal**

Raghu Venkatesh nói: “If you can write “hello world” you can change the world”. Muốn thay đổi thế giới bắt đầu bằng Hello World nhé !

Mở **VSCode** lên. Trên thanh công cụ: **File -> Open Folder** và mở hoặc tạo một thư mục mới (ví dụ Test chẳng hạn), sau đó **Select folder.**

Tạo 1 file `helloworld.cpp` và nhập đoạn code bên dưới vào.

![New file](/assets/pl/helloworld.png)


```cpp
#include <iostream>

using namespace std;

int main()
{
    cout << "Hello World!" << endl;

    return 0;
}
```

#### Cài đặt Code Runner

Code Runner là một extension giúp chúng ta chạy code một cách nhanh chóng và tiện lợi. Để cài đặt Code Runner, bạn làm theo các bước sau:

Mở VSCode, vào Extensions (Ctrl + Shift + X), tìm từ khóa “Code Runner” và cài đặt.

![Code Runner](/assets/pl/coderunner.png)

Sau khi cài đặt xong, bạn có thể chạy code bằng cách nhấn tổ hợp phím Ctrl + Alt + N hoặc nhấn vào biểu tượng Run Code ở góc trên bên phải của cửa sổ.

![Run Code](/assets/pl/runcode.png)

### Kết
Trên đây, mình đã giới thiệu với các bạn về Visual Studio Code và các cài đặt để lập trình C++. Hy vọng bài viết sẽ giúp ích cho các bạn.

```
Science Lab © 2024. Bản quyền thuộc về Science Lab.
```