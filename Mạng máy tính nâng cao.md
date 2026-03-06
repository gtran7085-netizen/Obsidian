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

# 🌐 CHƯƠNG 1:ĐỊNH TUYẾN
## 1. Tổng quan về định tuyến (Routing)
- **Định nghĩa:** Là chức năng của Router giúp xác định đường đi tối ưu cho các gói tin từ nguồn tới đích thông qua hệ thống mạng.
- **Cơ chế hoạt động:** * Router dựa vào **Destination IP** (địa chỉ đích) trong gói tin.
    - Tra cứu **Routing Table** (bảng định tuyến) để quyết định hướng chuyển tiếp.
    - Mỗi dòng trong bảng thể hiện: `Mạng đích` + `Interface (cổng ra)` hoặc `Next-hop (địa chỉ router kế tiếp)`.
---
## 2. Phân loại định tuyến
### Theo cách thức cấu hình:
- **Định tuyến tĩnh (Static Route):** Người quản trị mạng trực tiếp cấu hình thủ công.
- **Định tuyến động (Dynamic Route):** Router sử dụng các giao thức (RIP, OSPF, EIGRP...) để tự động trao đổi và cập nhật thông tin.
### Theo cơ chế hoạt động:

|**Loại**|**Đặc điểm chính**|
|---|---|
|**Distance-vector**|Gửi định kỳ toàn bộ bảng định tuyến cho láng giềng. Nhìn mạng qua con mắt của láng giềng.|
|**Link-state**|Trao đổi gói tin trạng thái đường liên kết (**LSA**), xây dựng **Topology Database**, dùng thuật toán **SPF (Dijkstra)**.|
|**Classfull**|Không quảng bá Subnet mask kèm theo (ví dụ: RIPv1).|
|**Classless**|Có quảng bá Subnet mask, hỗ trợ kỹ thuật **VLSM** (ví dụ: RIPv2, OSPF, EIGRP).|

---
## 3. Các tham số lựa chọn đường đi
Để chọn ra đường đi tốt nhất, Router dựa vào:
- **Metric:** Giá trị dùng để chọn đường tốt nhất trong **cùng một giao thức**. Đường có Metric **thấp nhất** sẽ được ưu tiên.
- **AD (Administrative Distance):** Giá trị quy ước về độ tin cậy của giao thức. Khi học cùng một mạng từ nhiều giao thức khác nhau, Router chọn giao thức có **AD nhỏ nhất**.

> [!INFO] **Chỉ số AD mặc định:**
> 
> - Directly Connected: 0
>     
> - Static Route: 1
>     
> - EIGRP: 90
>     
> - OSPF: 110
>     
> - RIP: 120
>     

---
## 4. Cấu hình định tuyến tĩnh và mặc định
### Tuyến tĩnh (Static Route)
Cú pháp:
`ip route <mạng-đích> <subnet-mask> {next-hop | interface} [distance]`
### Tuyến mặc định (Default Route)
- Nằm ở cuối bảng định tuyến, dùng khi không tìm thấy đích cụ thể trong bảng.
- Cực kỳ hữu dụng cho các mạng **"Stub Network"** hướng ra Internet.
- Cú pháp: `ip route 0.0.0.0 0.0.0.0 <next-hop/interface>`
---
## 5. Giao thức RIP (Routing Information Protocol)
- **Đặc điểm:** Thuộc loại Distance-vector.
- **Metric:** Tính theo **Hop count** (số bước nhảy).
    - Tối đa là **15**.
    - Giá trị **16** được coi là Unreachable (không thể tới).
- **AD mặc định:** 120.
- **RIPv2:** Bản cải tiến hỗ trợ Classless, VLSM, gửi cập nhật qua Multicast `224.0.0.9` và hỗ trợ chứng thực (Plain text/MD5).
---
## 6. Giao thức OSPF (Open Shortest Path First)
- **Đặc điểm:** Thuộc loại Link-state, dùng thuật toán **SPF** để tính toán.
- **Metric:** Gọi là **Cost**, tính dựa trên băng thông: $Cost = \frac{10^8}{Bandwidth}$.
- **AD mặc định:** 110.
- **Cơ chế:** * Chia mạng thành các **Area**, trong đó **Area 0** (Backbone) là bắt buộc.
    - Trong mạng đa truy cập (Ethernet), bầu chọn **DR** (Router đại diện) và **BDR** (Router dự phòng).
---
## 7. Giao thức EIGRP (Enhanced Interior Gateway Routing Protocol)
- **Đặc điểm:** Giao thức lai (Hybrid) của Cisco, hội tụ nhanh, chống lặp vòng bằng thuật toán **DUAL**.
- **Metric:** Tính dựa trên **Bandwidth** và **Delay**.
- **AD mặc định:** 90.
- **Khái niệm quan trọng:**
    - **Successor:** Tuyến đường chính tốt nhất (đưa vào bảng định tuyến).
    - **Feasible Successor:** Tuyến đường dự phòng (lưu trong Topology table).
---
## 8. Phân phối định tuyến (Redistribution)
- **Định nghĩa:** Là quá trình chuyển đổi Metric của giao thức định tuyến này sang giao thức khác.
- **Mục đích:** Giúp các hệ thống mạng chạy nhiều giao thức khác nhau có thể thông tin và trao đổi các tuyến đường với nhau một cách thống nhất.

Câu này thuộc giao thức **Spanning Tree Protocol**, dùng để **ngăn vòng lặp (loop) trong mạng switch Layer 2**.

# CHƯƠNG 2:VLAN
## 1. Các khái niệm cơ bản về Miền (Domain)
- **Collision domain (Miền đụng độ):** Xảy ra khi nhiều máy truyền dữ liệu đồng thời trên mạng chia sẻ, dẫn đến đụng độ và phá hủy gói tin. Switch giúp chia nhỏ miền này.  
- **Broadcast domain (Miền quảng bá):** Gồm tất cả thiết bị có thể nhận được gói tin quảng bá từ một thiết bị khác trong LAN. Theo mặc định, Switch chuyển tiếp gói quảng bá ra tất cả các cổng, trong khi Router giúp chia mạng thành nhiều miền quảng bá độc lập.

## 2. Công nghệ VLAN (Virtual LAN)
- **Định nghĩa:** Là kỹ thuật chia một Switch vật lý thành nhiều Switch luận lý. Mỗi VLAN là một miền quảng bá và một mạng logic riêng biệt (VLAN = broadcast domain = logical network).  
- **Ưu điểm:** Tăng tính bảo mật, linh hoạt trong thay đổi và di chuyển cấu hình, dễ dàng quản lý việc thêm máy trạm.  

- **Phân loại:**  
	- **VLAN tĩnh (Static VLAN):** Gán cổng Switch cố định vào VLAN, đây là loại phổ biến nhất.  
	- **VLAN động (Dynamic VLAN):** Gán VLAN dựa trên địa chỉ MAC của thiết bị thông qua một server quản lý gọi là VMPS.

## 3. Đường Trunk và Chuẩn 802.1Q
- **Đường Trunk:** Là một kết nối vật lý đơn lẻ cho phép lưu thông dữ liệu của nhiều VLAN giữa các Switch hoặc giữa Switch và Router.  
- **Giao thức 802.1Q (dot1q):** Là chuẩn IEEE dùng để nhận dạng các VLAN bằng cách gắn thêm một "thẻ" (tag) vào frame header (cơ chế frame tagging).

## 4. Giao thức VTP (VLAN Trunking Protocol)
- **Mục đích:** Giúp cấu hình VLAN đồng nhất trên toàn hệ thống mạng khi thực hiện thêm, xóa, sửa. 
- **Thông số Revision number:** Đây là số hiệu phiên bản cấu hình; khi có thay đổi, số này tăng lên và các Switch khác sẽ cập nhật theo Switch có số revision cao hơn.  

- **Các chế độ hoạt động (Modes):**  
	- **Server:** Có thể tạo, sửa, xóa VLAN và quảng bá cho các Switch khác.  
	- **Client:** Không được phép thay đổi VLAN cục bộ, chỉ cập nhật theo Server.  
	- **Transparent:** Không cập nhật từ Server nhưng vẫn chuyển tiếp bản tin VTP; có thể tạo VLAN cục bộ nhưng không quảng bá ra ngoài.

## 5. Định tuyến giữa các VLAN (Inter-VLAN Routing)
- Vì các VLAN nằm ở các miền quảng bá khác nhau, chúng cần thiết bị Tầng 3 (Router hoặc Switch Layer 3) để liên lạc.  
- **Router-on-a-stick:** Sử dụng một cổng vật lý của Router chia thành nhiều cổng luận lý (sub-interface), mỗi cổng gán cho một VLAN và một IP tương ứng.  
- **Switch Layer 3 (MSW):** Sử dụng các giao diện ảo SVI (`interface vlan`) để định tuyến giữa các VLAN với tốc độ cao hơn.
## 6. Giao thức STP (Spanning Tree Protocol)
- **Mục đích:** Chống tình trạng lặp vòng (switching loop) trong các sơ đồ mạng có đường kết nối dự phòng bằng cách khóa tạm thời các cổng không cần thiết.  
- **Quy trình bầu chọn:**  
	- **Bầu Root Bridge:** Switch có Bridge-ID (Priority + MAC) thấp nhất.  
	- **Chọn Root Port:** Cổng trên Switch không phải Root có chi phí (cost) thấp nhất đến Root Bridge.  
	- **Chọn Designated Port:** Cổng trên mỗi đoạn mạng có cost thấp nhất đến Root Bridge.  
	- **Cổng còn lại bị khóa (Non-designated port).**  

- **Chi phí (Cost):** Tỷ lệ nghịch với tốc độ kết nối (ví dụ: 100 Mb/s có cost là 19, 1 Gb/s có cost là 4).

# CHƯƠNG 3: ACL
## 1. Giới thiệu về ACL
- **Định nghĩa:** ACL là một danh sách các điều kiện được áp đặt vào các cổng của router để kiểm soát lưu lượng gói tin đi qua nó.  
- **Chức năng:** Router dựa vào ACL để quyết định cho phép (permit) hoặc hủy bỏ (deny) các gói tin dựa trên địa chỉ nguồn, địa chỉ đích, loại giao thức hoặc số hiệu cổng.  
- **Ứng dụng:** Quản lý lưu lượng mạng, hỗ trợ bảo mật cơ bản bằng cách lọc các truy cập không mong muốn.
## 2. Nguyên lý hoạt động của ACL
- **Kiểm tra tuần tự:** Router kiểm tra các điều kiện trong danh sách theo thứ tự từ trên xuống dưới.  
- **Quy tắc khớp lệnh:** Nếu gói tin khớp với một điều kiện nào đó, router thực hiện hành động tương ứng (cho phép/hủy) và ngừng kiểm tra các điều kiện còn lại trong danh sách.  
- **Lệnh cấm ngầm định:** Nếu gói tin không khớp với bất kỳ dòng nào trong ACL, nó sẽ bị hủy bỏ bởi một lệnh **"deny all"** ngầm định ở cuối danh sách. Vì vậy, một ACL hữu dụng phải có ít nhất một lệnh **permit**.  
- **Chiều lưu lượng:** ACL có thể được áp dụng theo hai chiều:  
	- **Inbound (chiều vào):** Lọc gói tin trước khi router thực hiện các bước định tuyến.  
	- **Outbound (chiều ra):** Lọc gói tin sau khi router đã định tuyến và xác định được cổng ra.
## 3. Các thuật ngữ quan trọng
- **Wildcard mask:** Là một chuỗi 32 bit dùng để xác định phần nào của địa chỉ IP cần được kiểm tra chính xác.  
- **Bit 0:** Phải khớp hoàn toàn với vị trí tương ứng trong địa chỉ IP.  
- **Bit 1:** Bỏ qua, không cần kiểm tra (don't care).
- **Wildcard "host":** Có dạng **0.0.0.0**, dùng để chỉ đích danh một thiết bị duy nhất.  
- **Wildcard "any":** Có dạng **255.255.255.255**, chấp nhận tất cả các địa chỉ IP.
## 4. Phân loại ACL
Dựa trên phạm vi kiểm tra, ACL được chia làm hai loại chính:
### Standard ACL (ACL tiêu chuẩn)
- **Phạm vi:** Chỉ kiểm tra địa chỉ IP nguồn của gói tin.  
- **Số hiệu nhận dạng:** Từ **1 đến 99** (hoặc **1300 đến 1999**).  
- **Vị trí đặt tối ưu:** Nên đặt **gần đích** nhất có thể để tránh việc cấm nhầm lưu lượng đến các mạng khác.
### Extended ACL (ACL mở rộng)
- **Phạm vi:** Kiểm tra linh hoạt hơn, bao gồm: địa chỉ IP nguồn, địa chỉ IP đích, loại giao thức (**TCP, UDP, ICMP,...**) và số hiệu cổng dịch vụ.  
- **Số hiệu nhận dạng:** Từ **100 đến 199** (hoặc **2000 đến 2699**).  
- **Vị trí đặt tối ưu:** Nên đặt **gần nguồn** của lưu lượng muốn cấm để loại bỏ gói tin sớm nhất, giúp tiết kiệm băng thông và tài nguyên hệ thống.
## 5. Named ACL (ACL đặt tên)
- Thay vì dùng con số, **Named ACL** sử dụng một cái tên gợi nhớ để định danh danh sách.  
- **Ưu điểm:** Cho phép người quản trị **xóa hoặc chèn thêm một số dòng điều kiện cụ thể** trong danh sách mà không cần phải xóa đi tạo lại toàn bộ như **Numbered ACL**.
## 6. ACL điều khiển truy cập Telnet
- ACL có thể được áp dụng vào các **cổng ảo vty (line vty)** để kiểm soát những ai được phép truy cập từ xa vào router thông qua giao thức **Telnet**.  
- Lệnh áp dụng trong trường hợp này là **`access-class`** thay vì **`access-group`** như trên cổng vật lý.

Câu hỏi:  
**Trạng thái nào của port chỉ xử lý BPDU nhưng không học MAC và không chuyển tiếp dữ liệu?**

Đáp án đúng: **C. Listening**

---

# 1. Các trạng thái của STP

Trong STP cổ điển (802.1D) port của switch có **5 trạng thái**:

|Trạng thái|Chức năng|
|---|---|
|Disabled|Port tắt|
|Blocking|Chỉ nhận BPDU|
|Listening|Xử lý BPDU nhưng chưa học MAC|
|Learning|Bắt đầu học MAC|
|Forwarding|Chuyển tiếp dữ liệu|

---

# 2. Trạng thái Listening hoạt động như thế nào?

Khi STP đang **tính toán lại topology**, port chuyển sang **Listening**.

Trong trạng thái này:

|Hoạt động|Có hay không|
|---|---|
|Nhận BPDU|✅ Có|
|Gửi BPDU|✅ Có|
|Học MAC|❌ Không|
|Forward frame|❌ Không|

Tức là:

Chỉ dùng để tính toán cây STP

---

# 3. Vì sao cần trạng thái Listening?

Mục đích:

Tránh loop khi mạng đang hội tụ (converging)

Nếu switch cho phép forward ngay lập tức:

Switch A ---- Switch B  
     \        /  
      Switch C

có thể xảy ra:

broadcast storm

---

# 4. Thời gian của trạng thái Listening

Trong STP mặc định:

Listening = 15 giây

Sau đó port chuyển sang:

Learning

---

# 5. Chuỗi trạng thái của một port

Khi một port được bật:

Blocking  
   ↓  
Listening  
   ↓  
Learning  
   ↓  
Forwarding

---

# 6. So sánh Listening và Learning

|Trạng thái|Học MAC|Forward dữ liệu|
|---|---|---|
|Listening|❌|❌|
|Learning|✅|❌|

---

# 7. Tóm tắt câu hỏi

Cổng:

- nhận BPDU ✔
    
- gửi BPDU ✔
    
- không học MAC ❌
    
- không forward dữ liệu ❌
    

➡ trạng thái đó là:

Listening

✅ **Đáp án đúng: C**

<span style="color:red">Đây là chữ màu đỏ</span>
<span style="color:blue">Đây là chữ màu xanh</span>
<span style="color:green">Đây là chữ màu xanh lá</span>