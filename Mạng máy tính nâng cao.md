## Ôn lại các kiến thức củ 
### 1. Mô hình **OSI – 7 tầng**

| Số tầng | Tên tầng (EN) | Tên tiếng Việt        | Chức năng chính          |
| ------- | ------------- | --------------------- | ------------------------ |
| 7       | Application   | Tầng Ứng dụng         | Giao diện cho người dùng |
| 6       | Presentation  | Tầng Trình bày        | Mã hóa, nén, định dạng   |
| 5       | Session       | Tầng Phiên            | Quản lý phiên kết nối    |
| 4       | Transport     | Tầng Giao vận         | Truyền dữ liệu tin cậy   |
| 3       | Network       | Tầng Mạng             | Định tuyến, IP           |
| 2       | Data Link     | Tầng Liên kết dữ liệu | Đóng khung, MAC          |
| 1       | Physical      | Tầng Vật lý           | Truyền bit               |
###  2. Mô hình **TCP/IP – 4 tầng**

|Tầng TCP/IP|Gộp từ OSI|Chức năng|
|---|---|---|
|Application|OSI 7–6–5|Dịch vụ mạng|
|Transport|OSI 4|TCP, UDP|
|Internet|OSI 3|IP, ICMP|
|Network Access|OSI 2–1|Ethernet, Wi-Fi|
### 3.Phân loại theo mạng theo **phạm vi địa lý**

| Loại mạng | Phạm vi             | Tốc độ  | Độ trễ     | Chi phí    | Độ tin cậy    | Ví dụ                  |
| --------- | ------------------- | ------- | ---------- | ---------- | ------------- | ---------------------- |
| **PAN**   | Vài mét             | Thấp    | Rất thấp   | Rẻ         | Trung bình    | Bluetooth, NFC         |
| **LAN**   | Phòng / Tòa nhà     | Rất cao | Thấp       | Thấp       | Cao           | Mạng gia đình, công ty |
| **MAN**   | Thành phố           | Cao     | Trung bình | Trung bình | Khá cao       | Mạng đô thị            |
| **WAN**   | Quốc gia / Toàn cầu | Thấp–TB | Cao        | Cao        | Phụ thuộc ISP | Internet               |
### 4. Phân loại theo **mô hình tổ chức**

| Mô hình           | Đặc điểm         | Quản lý | Bảo mật | Khả năng mở rộng | Ví dụ        |
| ----------------- | ---------------- | ------- | ------- | ---------------- | ------------ |
| **Client–Server** | Server trung tâm | Dễ      | Cao     | Tốt              | Web, Mail    |
| **P2P**           | Không server     | Khó     | Thấp    | Kém              | Chia sẻ file |
### 5.Phân loại theo **phương tiện truyền dẫn**

| Loại          | Môi trường      | Tốc độ     | Ổn định    | Bảo mật  | Ví dụ        |
| ------------- | --------------- | ---------- | ---------- | -------- | ------------ |
| **Có dây**    | Cáp đồng, quang | Rất cao    | Rất cao    | Cao      | Ethernet     |
| **Không dây** | Sóng vô tuyến   | Trung bình | Trung bình | Thấp hơn | Wi-Fi, 4G/5G |
### 6.Phân loại theo **kỹ thuật chuyển mạch**

| Loại                      | Cách truyền          | Hiệu suất | Độ linh hoạt | Ứng dụng      |
| ------------------------- | -------------------- | --------- | ------------ | ------------- |
| **Chuyển mạch kênh**      | Đường truyền cố định | Thấp      | Thấp         | Điện thoại cũ |
| **Chuyển mạch gói**       | Chia gói             | Cao       | Cao          | Internet      |
| **Chuyển mạch thông báo** | Gửi toàn bộ          | Thấp      | Thấp         | Ít dùng       |
### 7. Phân loại theo **kiến trúc mạng**

| Kiến trúc     | Đặc điểm         | Ưu điểm     | Nhược điểm       |
| ------------- | ---------------- | ----------- | ---------------- |
| **Tập trung** | Server trung tâm | Quản lý tốt | Dễ lỗi điểm đơn  |
| **Phân tán**  | Nhiều nút        | Tin cậy cao | Quản lý phức tạp |

## 🌐 WAN (Wide Area Network)

### 📌 Khái niệm

- WAN là mạng truyền dữ liệu trên **phạm vi địa lý rất rộng** (tỉnh, quốc gia, toàn cầu).
- Dùng để **kết nối nhiều mạng LAN ở các vị trí xa nhau**.
---
### 🔗 Đối tượng & mục đích

- Kết nối các **chi nhánh**, **trung tâm**, **mạng LAN độc lập**.
- Cho phép **trao đổi thông tin giữa các mạng ở xa**.
---
### 🏢 Nhà cung cấp dịch vụ
- WAN **phụ thuộc vào các nhà cung cấp dịch vụ viễn thông / Internet (ISP)**.
- Doanh nghiệp thường **thuê dịch vụ WAN**.
---
### 🧵 Phương tiện truyền dẫn
- Sử dụng **nhiều loại liên kết nối tiếp (serial links)**.
- Công nghệ truyền dẫn **đa dạng**, không đơn giản như LAN.
---
### 🧩 Vị trí trong mô hình OSI
- WAN hoạt động chủ yếu ở:
    - **Layer 1 – Physical**
    - **Layer 2 – Data Link*
---

## 🌐 Thiết bị sử dụng trong WAN
### 🔹 Router
- Thiết bị **trung tâm trong WAN**
- Cung cấp các dịch vụ
    - Kết nối Internet
    - Giao tiếp WAN
- Thực hiện **định tuyến và chuyển tiếp gói dữ liệu**
---
### 🔹 WAN Switch
- Switch chuyên dụng cho WAN
- Hỗ trợ truyền:
    - **Thoại**
    - **Video**
    - **Dữ liệu**
- Thường thuộc **hạ tầng nhà cung cấp dịch vụ**
---
### 🔹 Modem
- Thiết bị **giao tiếp giữa mạng WAN và dịch vụ truyền dẫn**
- Các loại phổ biến:
    - **Modem thoại**: giao tiếp dịch vụ truyền thoại
    - **CSU/DSU**: giao tiếp dịch vụ **T1/E1**
    - **TA/NT1**: giao tiếp dịch vụ **ISDN**
📌 _Thi_: Modem = chuyển đổi & giao tiếp dịch vụ WAN
---
### 🔹 Communication Server (Server thông tin liên lạc)
- **Tập trung xử lý các cuộc gọi của người dùng**
- Hỗ trợ truy cập và quản lý kết nối WAN
---
## 📦 Giao thức WAN – Lớp Liên kết dữ liệu

- Giao thức WAN mô tả:
    - **Cách gói dữ liệu được vận chuyển trên đường truyền**
- Hoạt động ở **Layer 2 – Data Link**
- Thiết kế cho:
    - Kết nối **điểm–điểm**
    - **Đa điểm**
    - **Đa truy nhập**
📌 Ví dụ tiêu biểu:

- **Frame Relay**
---
## 🧠 Ghi nhớ nhanh (thi)

> **WAN = Router + WAN Switch + Modem (CSU/DSU, ISDN) + Giao thức L2**
	
## Tỏ chức quản lý và định nghĩa tiêu chuẩn của mạng WAN

- **ITU-T** – **Liên minh Viễn thông Quốc tế – Lĩnh vực Tiêu chuẩn Viễn thông**
- **ISO** – **Tổ chức Tiêu chuẩn hóa Quốc tế**
- **IETF** – **Tổ chức Đặc trách Kỹ thuật Internet**
- **EIA** – **Hiệp hội Công nghiệp Điện tử**
## 🧭 Router trong LAN & WAN
- **Router** vừa dùng để **phân đoạn mạng LAN**, vừa là **thiết bị trung tâm trong mạng WAN**.
- Router có cả **cổng giao tiếp LAN và WAN**.
- Các **kỹ thuật WAN** được sử dụng để **kết nối các router với nhau** qua các liên kết WAN.
- Router giao tiếp với router khác thông qua **đường truyền WAN**.
---
## 🌐 Vai trò của Router
- Là **thiết bị xương sống** của:
    - Mạng **Intranet lớn**
    - Mạng **Internet**
- Hoạt động tại **Lớp 3 – Network (mô hình OSI)**.
- Thực hiện **chuyển gói dữ liệu dựa trên địa chỉ mạng (IP)**.
---
## ⚙️ Chức năng chính của Router
### 1️⃣ Chọn đường đi tốt nhất (Path Selection
- Xác định **tuyến đường tối ưu** để gửi gói dữ liệu.
### 2️⃣ Chuyển mạch gói dữ liệu (Packet Switching)
- Chuyển tiếp gói tin từ cổng vào sang cổng ra phù hợp.
---
## 🗺️ Bảng định tuyến
- Mỗi router phải:
    - **Xây dựng bảng định tuyến**
    - **Trao đổi thông tin định tuyến** với các router khác
- Bảng định tuyến là cơ sở để router:
    - Chọn đường đi
    - Chuyển tiếp gói dữ liệu
---
## 🧠 Ghi nhớ nhanh (thi)
> **Router = Layer 3 + Chọn đường + Chuyển gói + Bảng định tuyến**
## 🌐 Hệ thống mạng được cấu hình đúng
- **Địa chỉ nhất quán** từ đầu cuối đến đầu cuối
- **Cấu trúc địa chỉ phản ánh cấu trúc mạng**
- **Chọn đường đi tốt nhất**
- Hỗ trợ **định tuyến tĩnh và động**
- Thực hiện **chuyển mạch gói dữ liệu**
## 🌐 WAN, OSI và vai trò của Router (Tóm gọn)
- **WAN khác LAN chủ yếu ở Lớp 1 (Vật lý) và Lớp 2 (Liên kết dữ liệu)**.
- Các lớp còn lại của mô hình OSI **vẫn tồn tại trong WAN**, nhưng **chuẩn & giao thức L1–L2 khác LAN**.
---
### 🔌 Lớp Vật lý trong WAN
- Mô tả giao tiếp giữa
    - **DTE** (Data Terminal Equipment): thiết bị người dùng (router)
    - **DCE** (Data Circuit-Terminating Equipment): thiết bị nhà cung cấp dịch vụ
- DCE thường là:
    - **Modem**
    - **CSU/DSU**
---
### 🧭 Router trong LAN & WAN
- Router hoạt động ở **Lớp 3 – Network** (định tuyến).
- Router có thể là:
    - Thiết bị **LAN**
    - Thiết bị **WAN**
    - **Thiết bị trung gian giữa LAN và WAN**
    - Hoặc **LAN & WAN cùng lúc**

---
### ⚙️ Vai trò của Router trong WAN
- Router **vẫn thực hiện định tuyến ở Lớp 3**, giống như trong mạng LAN.
- Tuy nhiên, **định tuyến không phải là nhiệm vụ chính yếu trong WAN**.
- Khi kết nối các mạng WAN, router chủ yếu:
  - **Cung cấp kết nối giữa các mạng WAN**
  - **Làm trung gian giữa các chuẩn Vật lý (L1) và Liên kết dữ liệu (L2) khác nhau**
  - **Chuyển đổi luồng bit và kiểu đóng gói L2**

- Ví dụ:
  - **ISDN (PPP) ↔ T1 (Frame Relay)**  
  - Router chuyển đổi **dịch vụ truyền dẫn** và **kiểu đóng gói** tương ứng.
## 🌐 Chuẩn & giao thức WAN theo mô hình OSI

### 🔌 Lớp Vật lý (Layer 1)
- **EIA/TIA-232, EIA/TIA-449**
- **V.24, V.35**
- **X.21**
- **EIA-530**
- **ISDN**
- **T1, T3**
- **E1, E3**
- **xDSL**
- **SONET**: OC-3, OC-12, OC-48, OC-192
---
### 🔗 Lớp Liên kết dữ liệu (Layer 2)
- **HDLC**
- **Frame Relay**
- **PPP**
- **SDLC**
- **SLIP**
- **X.25**
- **ATM**
- **LAPB**
- **LAPD**
- **LAPF**

## 🧱 Router – Cấu trúc bên trong
### 🔹 CPU (Central Processing Unit)
- **Bộ xử lý trung tâm** của router
- Thực hiện:
    - Tính toán **định tuyến**
    - Xử lý **bảng định tuyến**
    - Khởi động hệ thống
    - Điều kiểu cổng giao tiếp
---
### 🔹 RAM
- Bộ nhớ **tạm thời** (mất dữ liệu khi tắt nguồn)
- Lưu **bảng định tuyến (Routing Table)**
- Lưu **bảng ARP**
- Có **vùng bộ nhớ chuyển mạch nhanh**
- Cung cấp **bộ nhớ đệm (buffer) cho gói dữ liệu**
- Duy trì **hàng đợi (queue) cho các gói dữ liệu**
- Lưu **tập tin cấu hình đang chạy (Running Configuration)**
- **Dữ liệu bị xoá** khi router:
    - Khởi động lại
    - Mất điện
- Thông thường là RAM động có thể nâng cấp
- Chia thành 2 phần:
	- Bộ nhớ xử lý chính 
	- Bộ nhớ chia sẽ xuất nhập
📌 _Thi_: RAM = mọi thứ **đang hoạt động**
---
### 🔹 ROM
- Bộ nhớ **chỉ đọc**
- Lưu:
    - **Bootstrap program**
    - **POST** (Power-On Self Test)
    - **Mini IOS**
📌 _Thi_: ROM dùng khi khởi động
---
### 🔹 NVRAM
- Bộ nhớ **không mất dữ liệu khi tắt nguồn**
- Lưu:
    - **Startup configuration**
- NVRAM có thể là bộ nhớ riêng với Flash hoặc được tích hợp tùy vào thiết bị
📌 _Thi_: NVRAM = cấu hình khởi động
---
### 🔹 Flash Memory
**Bộ nhớ lưu hệ điều hành**
### 📌 Đặc điểm & chức năng
- Lưu **hệ điều hành IOS**
- Có thể **cập nhật IOS** mà không cần thay chip
- Nội dung **không mất** khi:
    - Khởi động lại
    - Tắt nguồn
- Có thể lưu **nhiều phiên bản IOS**
- Flash là **EPROM** (ROM xoá & lập trình được)
📌 _Thi_: Flash = hệ điều hành router
---
### 🔹 Interface (Cổng mạng)
### 📌 Đặc điểm & chức năng
- Kết nối router vào **hệ thống mạng**
- Thực hiện **nhận và chuyển tiếp gói dữ liệu**
- Có thể:
    - Gắn **trực tiếp trên mainboard**
    - Hoặc dưới dạng **card rời**
📌 _Thi_: Interface = kết nối LAN/WAN
---
### 🔹 Bus hệ thống
- Kết nối và trao đổi dữ liệu giữa:
    - CPU
    - Bộ nhớ
    - Interface
## 🔌 Các cổng giao tiếp trên Router

### 🖧 Cổng giao tiếp LAN
- Cho phép router kết nối vào **môi trường mạng cục bộ (LAN)**  
- Thường là:
  - **Ethernet**
  - **Fast Ethernet**
- Ngoài ra có thể có:
  - **Token Ring**
  - **ATM**
- Có thể:
  - Gắn **cố định trên router**
  - Hoặc dưới dạng **card rời (module)**

---
### 🌐 Cổng giao tiếp WAN
- Cung cấp kết nối thông qua **nhà cung cấp dịch vụ (ISP)**:
  - Kết nối các **chi nhánh ở xa**
  - Kết nối **Internet**
- Các loại cổng phổ biến:
  - **Serial**
  - **ISDN**
  - **CSU (Channel Service Unit) tích hợp**
- Hiện nay, **đa số cổng WAN là cổng Serial**

---

### ⚙️ Cổng quản lý (Management Ports)
- Bao gồm:
  - **Console**
  - **AUX (Auxiliary)**
- Chức năng:
  - **Thiết lập cấu hình router**
  - **Giám sát hoạt động**
  - **Xử lý sự cố**
- ⚠️ **Không dùng để truyền dữ liệu mạng**
- Thông thường:
  - **Cổng Console** được dùng nhiều nhất
  - Không phải router nào cũng có **cổng AUX**
# 🔧 Cisco IOS
## 🔧 Dịch vụ mạng do Cisco IOS cung cấp
- **Định tuyến và chuyển mạch** dữ liệu
- **Bảo mật và kiểm soát truy cập** tài nguyên mạng
- **Mở rộng và quản lý hệ thống mạng**
---
## 🔧 Cisco IOS & truy cập CLI (Tóm tắt)
- **Cisco IOS** sử dụng **giao diện dòng lệnh (CLI)** qua môi trường console
- IOS là **nền tảng chung**, nhưng **hành vi cụ thể khác nhau** tùy từng thiết bị Cisco.
### 🔑 Các cách truy cập CLI của router
1. **Console**
    - Kết nối trực tiếp PC/terminal → cổng Console
    - **Không cần cấu hình trước**
2. **AUX**
    - Qua modem quay số hoặc null modem
    - **Không cần cấu hình trước**
3. **Telnet**
    - Truy cập từ xa qua mạng
    - **Yêu cầu cấu hình trước**:
        - Router có **IP**
        - Cấu hình **VTY**
        - Đặt **mật khẩu**
---
## 🖥️ Cisco IOS – CLI
- **CLI của Cisco IOS có cấu trúc phân cấp**
    - Muốn cấu hình gì phải vào **đúng chế độ** tương ứng
    - Mỗi chế độ có:
        - **Dấu nhắc riêng**
        - **Tập lệnh riêng**
- **EXEC** là trình thông dịch lệnh của IOS  
    → Lệnh nhập vào được **thực thi ngay**
---
## 🔐 Hai chế độ EXEC
### 1️⃣ User EXEC
- Chỉ cho phép:
    - Xem thông tin cơ bản
- **Không cho phép thay đổi cấu hình**
- Dấu nhắc: `>`
---
### 2️⃣ Privileged EXEC
- Cho phép:
    - Thực thi **tất cả các lệnh**
    - Cấu hình và quản lý router
- Có thể:
    - Đặt **mật khẩu**
    - Cấu hình **userID**
- Dấu nhắc: `#`
- Từ chế độ này có thể vào:
    - **Global Configuration**
    - Các chế độ cấu hình khác
---
## 🔄 Chuyển chế độ
- Dùng lệnh **`enable`** để chuyển:
    - `>` → `#`
- Nếu có cấu hình bảo mật:
    - Router sẽ yêu cầu **mật khẩu**
    - Mật khẩu **không hiển thị khi nhập**
---
## 🔧 Cisco IOS – Tóm tắt trọng tâm
- **Cisco cung cấp nhiều loại IOS** cho các **thiết bị mạng khác nhau**, nhằm:
    - Phù hợp với **loại thiết bị**
    - Phù hợp với **dung lượng bộ nhớ**
    - Phù hợp với **nhu cầu người dùng**
- Dù có nhiều phiên bản IOS, **cấu trúc lệnh CLI cơ bản là giống nhau**  
    → Kỹ năng cấu hình và xử lý sự cố **áp dụng cho nhiều thiết bị Cisco**
---
## 🏷️ Cấu trúc tên Cisco IOS (3 phần)
1. **Loại thiết bị** sử dụng IOS
2. **Các đặc tính / tính năng** của IOS
3. **Vị trí chạy IOS & dạng nén / không nén**
---
## 🧰 Công cụ & kiểm tra IOS
- **Cisco Software Advisor**
    - Giúp **chọn phiên bản IOS phù hợp** với nhu cầu và phần cứng
- IOS mới:
    - Có nhiều tính năng hơn
    - → **Yêu cầu nhiều RAM & Flash hơn**
---
## 🔍 Kiểm tra bộ nhớ trước khi cài IOS
### 🔹 Kiểm tra RAM
show version
- Cho biết:
    - **DRAM chính**
    - **DRAM chia sẻ**
    - → Tổng là **RAM thực**
### 🔹 Kiểm tra Flash
show flash
- Cho biết:
    - Tổng dung lượng Flash
    - Dung lượng còn trống
📌 **Bắt buộc kiểm tra RAM & Flash trước khi nâng cấp IOS**
---
# 🔁 Khởi động Router Cisco

## 1️⃣ Các chế độ hoạt động
Router có **3 chế độ hoạt động** khi khởi động:
### 🔹 ROM Monitor (ROMMON)
- **Chế độ cứu hộ / khẩn cấp**
- Chức năng:
    - Bootstrap
    - Kiểm tra phần cứng
- Dùng khi:
    - IOS bị lỗi
    - Mất mật khẩu
    - Router không khởi động bình thường
- ⚠️ Chỉ truy cập qua **cổng Console**
---
### 🔹 Boot ROM
- **IOS tối giản**
- Không đủ chức năng hoạt động bình thường
- Dùng để:
    - Chép IOS mới vào Flash
    - Ví dụ:
        copy tftp flash
- Thường dùng khi IOS trong Flash bị hỏng
---
### 🔹 Cisco IOS
- **Chế độ hoạt động bình thường**
- Router chỉ hoạt động đúng khi:
    - **Chạy được toàn bộ IOS**
- Cách chạy IOS:
    - IOS trong **Flash**
    - **Chép lên RAM rồi chạy**
    - Một số IOS:
	    - **Nén trong Flash**
        - **Giải nén khi chép lên RAM**
---
## 2️⃣ Thanh ghi cấu hình (Configuration Register)
- Quyết định:
    - Boot từ Flash
    - Vào ROMMON
    - Bỏ qua cấu hình
- Xem bằng lệnh:
show version
---
## 3️⃣ Quá trình khởi động Cisco IOS
### 📌 Tổng quan
- Router khởi động theo thứ tự:  
    **Bootstrap → IOS → Startup-config**
- Không tìm thấy cấu hình → **Setup Mode**
---
### ⚙️ Các bước chi tiết
1. **POST**
    - Chạy từ ROM
    - Kiểm tra CPU, bộ nhớ, cổng mạng
2. **Bootstrap**
    - Nằm trong ROM
    - Bắt đầu quá trình tải IOS
3. **Tìm & tải IOS**
    - Từ Flash hoặc mạng (TFTP)
4. **Chạy IOS**
    - IOS được chép vào RAM và bắt đầu hoạt động
5. **Nạp startup-config**
    - Từ NVRAM
    - Không có → vào **Setup Mode**
---
## 🛠️ Setup Mode
- Dùng để:
    - Tạo **cấu hình tối thiểu**
- ❌ Không hỗ trợ cấu hình phức tạp
- Có thể:
    - Nhấn **Ctrl+C** để thoát (các cổng bị shutdown)
- Kết thúc có 3 lựa chọn:
    - `[0]` Vào IOS không lưu cấu hình
    - `[1]` Quay lại setup không lưu
    - `[2]` Lưu cấu hình vào NVRAM và thoát
---
## 💡 Đèn LED trên Router
- LED cổng mạng:
    - **Sáng liên tục** → cổng hoạt động bình thường
    - **Tắt khi đang dùng** → có sự cố
- LED **OK** (gần cổng AUX)
    - Sáng khi router **hoạt động ổn định**
Các câu hỏi làm sai
# Tại sao kỹ thuật VLSM (Variable Length Subnet Masking) lại quan trọng trong việc thiết kế sơ đồ địa chỉ IP hiện nay?

- A. Cho phép chia các subnet có kích thước khác nhau để tối ưu hóa không gian địa chỉ
	- Câu trả lời chính xác
	- VLSM giúp người quản trị phân bổ các subnet phù hợp với số lượng host thực tế, tránh lãng phí địa chỉ.
- B. Giúp router xử lý các gói tin nhanh hơn bằng cách bỏ qua lớp liên kết dữ liệu
- C. Tự động gán địa chỉ IP cho tất cả các thiết bị trong mạng
- D. Chỉ có tác dụng với các mạng LAN nhỏ sử dụng hub
# Giao thức định tuyến RIPv2 sử dụng địa chỉ nào để gửi thông tin cập nhật định tuyến đến các router láng giềng?
A. 224.0.0.9 (Multicast)
Chính xác!
RIPv2 sử dụng địa chỉ multicast để gửi cập nhật, giúp giảm tải cho các thiết bị không chạy RIP trong cùng mạng.
B.127.0.0.1 (Loopback)
C.224.0.0.5 (Multicast)
D.255.255.255.255 (Broadcast)
# Mục đích chính của giao thức định tuyến OSPF là gì?

A.

Kết nối các thiết bị không cùng chuẩn vật lý ở lớp 1

B.

Chỉ dựa vào số lượng hop để tìm đường đi nhanh nhất

C.

Tự động cấp phát địa chỉ IP cho các máy trạm trong vùng

D.

Xây dựng cây đường đi ngắn nhất dựa trên trạng thái các đường liên kết

Chính xác!

OSPF là giao thức link-state, sử dụng thuật toán Dijkstra để tính toán đường đi tốt nhất dựa trên cấu trúc topo mạng toàn cục.
# Trong thiết kế WAN, thiết bị nào thường được đặt tại phía nhà cung cấp dịch vụ để thực hiện việc chuyển đổi tín hiệu và cung cấp xung nhịp (clocking)?

A.

DCE (Data Circuit-terminating Equipment)

Chính xác!

Thiết bị DCE (như modem hoặc CSU/DSU) chịu trách nhiệm cung cấp tín hiệu xung nhịp để đồng bộ hóa quá trình truyền dữ liệu.

B.

DTE (Data Terminal Equipment)

C.

Switch Workgroup

D.

Hub
# NAT (Network Address Translation) giúp giải quyết vấn đề gì của Internet hiện nay?

A.

Tốc độ tải dữ liệu quá chậm trên các đường truyền cũ

Chưa đúng lắm!

NAT thực chất làm tăng nhẹ độ trễ vì router phải xử lý thay đổi header gói tin, không giúp tăng tốc độ vật lý.

B.

Lỗi vòng lặp định tuyến trong mạng OSPF

C.

Sự không tương thích giữa các loại cáp khác nhau

D.

Sự khan hiếm địa chỉ IPv4 công cộng

Câu trả lời chính xác

NAT cho phép nhiều thiết bị dùng địa chỉ IP nội bộ (private) truy cập Internet thông qua một địa chỉ IP công cộng duy nhất.
# VLAN (Virtual LAN) được sử dụng để giới hạn loại miền (domain) nào trong hạ tầng switch?

A.

Miền xung đột (Collision domain)

B.

Miền quản trị vật lý

C.

Miền quảng bá (Broadcast domain)

Chính xác!

VLAN chia nhỏ switch thành nhiều mạng logic, giúp các gói tin quảng bá chỉ lan truyền trong nội bộ một VLAN thay vì toàn bộ mạng.

D.

Miền định tuyến lớp 4
# Thuật toán nào được sử dụng bởi OSPF để tính toán đường đi ngắn nhất đến các mạng đích?

A.

Spanning Tree (STP)

Chưa đúng lắm!

STP được dùng ở lớp 2 để ngăn chặn vòng lặp trong hệ thống switch, không phải để định tuyến gói tin lớp 3.

B.

DUAL

C.

Dijkstra (SPF)

Câu trả lời chính xác

Thuật toán SPF (Shortest Path First) của Dijkstra xây dựng một cây sơ đồ mạng hoàn chỉnh để tìm đường tối ưu nhất.

D.

Bellman-Ford