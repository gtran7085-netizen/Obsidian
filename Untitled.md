
| Hex | Decimal |
| --- | ------- |
| A   | 10      |
| B   | 11      |
| C   | 12      |
| D   | 13      |
| E   | 14      |
| F   | 15      |
Offset là vi trí từ điểm đó đến byte đầu tiên của file
0x10 = 1 × 16¹ + 0 × 16⁰
     = 16
eax, ebx, ecx, edx, esp, ebp, esi và edi

| 32-bit | 16-bit | 8-bit cao trong 16 bit | 8-bit thấp trong 1 bit | Vai Trò                                 |
| ------ | ------ | ---------------------- | ---------------------- | --------------------------------------- |
| EAX    | AX     | AH                     | AL                     | Thanh ghi tính toán chính (accumulator) |
| EBX    | BX     | BH                     | BL                     | Thường dùng làm base address            |
| ECX    | CX     | CH                     | CL                     | Đếm (loop, repeat)                      |
| EDX    | DX     | DH                     | DL                     | Mở rộng phép nhân/chia                  |
| ESP    | SP     |                        |                        | Stack pointer                           |
| EBP    | DP     |                        |                        | Base pointer                            |
| ESI    | SI     |                        |                        | Source inder                            |
| EDI    | DI     |                        |                        | Destination index                       |


| Bit | Tên cờ           | Khi nào = 1        | Ý nghĩa dễ hiểu       |
| --- | ---------------- | ------------------ | --------------------- |
| 0   | Carry Flag       | Có carry / borrow  | Tràn số **không dấu** |
| 2   | Parity Flag      | Số bit 1 là chẵn   | Ít dùng               |
| 4   | Auxiliary Carry  | Carry ở bit 4      | Dùng cho BCD          |
| 6   | Zero Flag        | Kết quả = 0        | Rất quan trọng<br>    |
| 7   | Sign Flag        | Bit cao nhất = 1   | Số âm                 |
| 8   | Trap Flag        | Debug từng lệnh    | Debug                 |
| 9   | Interrupt Enable | Cho phép interrupt | Hệ thống              |
| 10  | Direction Flag   | String đi lùi      | movs, stos            |
| 11  | Overflow Flag    | Tràn số **có dấu** | Rất quan trọng        |

| Lệnh          |                                                            | Ví dụ                                                                  | Nghĩa                                                                                                                                                                                                                                     |     |
| ------------- | ---------------------------------------------------------- | ---------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| MOV           | Di chuyển dữ liệu từ một vị trí sang 1 vị trí khác         | mov eax, [0x403000]                                                    | CPU **đi tới địa chỉ 0x403000**<br>- Lấy **4 byte** ở đó<br>- Gán vào `eax`                                                                                                                                                               |     |
| ADD           | +                                                          | add eax, 42       <br>add eax, ebx      <br>add [ebx], 42              | eax = eax + 42; eax = eax + ebx cộng 42 vào giá trị tại địa chỉ ebx                                                                                                                                                                       |     |
| LEA           | Nạp địa chỉ, không lấy giá trị                             | lea ebx,[0x403000]                                                     | đưa địa chỉ 0x403000 vào EBX                                                                                                                                                                                                              |     |
| SUB           | -                                                          | sub eax, 64h                                                           | ; eax = eax - 0x64 (100)                                                                                                                                                                                                                  |     |
| INC           | +1                                                         |                                                                        |                                                                                                                                                                                                                                           |     |
| DEC           | -1                                                         |                                                                        |                                                                                                                                                                                                                                           |     |
| MUL           | x                                                          | mov eax, [ebp-4]<br>imul eax, [ebp-8]<br>mov [ebp-12], eax             | int c = a * b;<br>                                                                                                                                                                                                                        |     |
| DIV           | /                                                          | mov eax, [ebp-4]<br>cdq<br>idiv dword ptr [ebp-8]<br>mov [ebp-12], eax | int c = a / b;<br>                                                                                                                                                                                                                        |     |
| NOT           | Đảo bit                                                    | not eax                                                                | - `1 → 0`<br>- `0 → 1`                                                                                                                                                                                                                    |     |
| AND           | dùng để mask bit và check flag(1 and 1 = 1 còn lại bằng 0) | and bl, cl<br>                                                         | bl = 0000 0101 (5)<br>cl = 0000 0110 (6)<br>----------------<br>bl = 0000 0100 (4)<br>                                                                                                                                                    |     |
| OR            | bật bit(ít nhất 1bit thì là 1)                             |                                                                        |                                                                                                                                                                                                                                           |     |
| XOR           | giống nhau thì bằng chính nó còn khác nhau thì bằng 1      | xor eax, eax<br>                                                       |                                                                                                                                                                                                                                           |     |
| SHL(SHIFT)    | dịch trái bit                                              | shl al, 2<br>                                                          | al = 0000 0100 (4)<br>shl 2 → 0001 0000 (16)<br>                                                                                                                                                                                          |     |
| SHR           | dịch phải bit                                              | shr eax, 1<br>                                                         | eax = 0000 0100                   shr 1 → 0000 0010                                                                                                                                                                                       |     |
| ROL / ROR<br> | xoay bit                                                   | rol al, 2<br>                                                          | al = 0100 0100 (0x44)<br>rol 2 → 0001 0001 (0x11)<br>                                                                                                                                                                                     |     |
| CMP           | so sánh                                                    |                                                                        |                                                                                                                                                                                                                                           |     |
| TEST          | kiểm tra bit                                               |                                                                        |                                                                                                                                                                                                                                           |     |
| PUSH          | đưa giá trị vào đỉnh stack                                 |                                                                        | - Nó giảm giá trị của con trỏ Stack (**ESP**) đi 4 đơn vị (trong hệ 32-bit). Việc giảm này là để "dành chỗ" vì Stack phát triển ngược từ địa chỉ cao xuống địa chỉ thấp.<br>    <br>- Nó sao chép giá trị vào vị trí mà ESP đang trỏ tới. |     |
| POP           | lấy giá trị từ đỉnh stack và lưu vào nơi khác              |                                                                        | - Nó sao chép giá trị tại vị trí mà **ESP** đang trỏ tới vào đích (destination).<br>    <br>- Nó tăng giá trị của ESP lên 4 đơn vị để "xóa bỏ" logic giá trị đó khỏi ngăn xếp.                                                            |     |
|               |                                                            |                                                                        |                                                                                                                                                                                                                                           |     |
	Nhóm lệnh JUMP

|**Lệnh**|**Ý nghĩa**|**Tên khác (Aliases)**|**Điều kiện Cờ (Flags)**|
|---|---|---|---|
|**`JZ`**|Nhảy nếu bằng 0|`JE` (Nhảy nếu bằng nhau)|$ZF = 1$|
|**`JNZ`**|Nhảy nếu khác 0|`JNE` (Nhảy nếu khác nhau)|$ZF = 0$|
|**`JL`**|Nhảy nếu nhỏ hơn|`JNGE` (Không lớn hơn hoặc bằng)|$SF \neq OF$|
|**`JLE`**|Nhảy nếu nhỏ hơn hoặc bằng|`JNG` (Không lớn hơn)|$ZF = 1$ hoặc $SF \neq OF$|
|**`JG`**|Nhảy nếu lớn hơn|`JNLE` (Không nhỏ hơn hoặc bằng)|$ZF = 0$ và $SF = OF$|
|**`JGE`**|Nhảy nếu lớn hơn hoặc bằng|`JNL` (Không nhỏ hơn)|$SF = OF$|
|**`JC`**|Nhảy nếu có cờ nhớ|`JB` (Nhỏ hơn), `JNAE`|$CF = 1$|
|**`JNC`**|Nhảy nếu không có cờ nhớ|`JNB` (Lớn hơn hoặc bằng), `JAE`|$CF = 0$|




### Di chuyển giá trị từ thanh ghi vào bộ nhớ
- Bạn có thể di chuyển một giá trị từ **thanh ghi** vào **bộ nhớ** bằng cách **đảo vị trí toán hạng**, sao cho:
-**Bên trái** là **địa chỉ bộ nhớ** (đích – destination)
-**Bên phải** là **thanh ghi** (nguồn – source)
VD:mov [0x403000], eax
→Di chuyển **4 byte** trong thanh ghi `eax` vào vùng nhớ bắt đầu tại địa chỉ `0x403000`.
VD: mov [ebx], eax
→ Di chuyển **4 byte** trong `eax` vào địa chỉ bộ nhớ mà `ebx` đang trỏ tới.
### **Ghi hằng số trực tiếp vào bộ nhớ**
Đôi khi bạn sẽ gặp các lệnh như sau:  
Chúng dùng để **ghi một giá trị hằng (constant)** vào bộ nhớ.
- `dword ptr` → ghi **4 byte**
- `word ptr` → ghi **2 byte**
- `[]` → **luôn là bộ nhớ**
