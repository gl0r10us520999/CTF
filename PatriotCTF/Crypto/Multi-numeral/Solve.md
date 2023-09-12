# Multi-numeral
## Challenge's information
- Much numbers, many wows.
https://pctf.competitivecyber.club/files/df392f749d1fb7f25d432c7c68a3deb9/Challenge.txt?token=eyJ1c2VyX2lkIjoyMjkxLCJ0ZWFtX2lkIjo4MjcsImZpbGVfaWQiOjR9.ZQBqkw.UFxe6aeFKZeFOgjlS9wFH3zf8KE
## Solution
- Sau khi tải về file `Challenge.txt`, ta mở ra và nhận được một dãy binary như sau:![](https://hackmd.io/_uploads/ByUroJARn.png)
- Copy tất cả và sử dụng [CyberChef](https://gchq.github.io/CyberChef/) để decode từ binary được dãy số sau `53 53 32 52 53 32 52 69 32 53 53 32 53 50 32 54 69 32 55 52 32 51 51 32 52 68 32 52 56 32 54 52 32 54 54 32 54 51 32 55 65 32 52 50 32 54 54 32 54 50 32 53 52 32 53 50 32 55 53 32 54 53 32 53 54 32 51 57 32 55 53 32 54 52 32 53 55 32 51 49 32 54 57 32 53 65 32 53 56 32 52 57 32 51 49 32 54 54 32 53 49 32 51 68 32 51 68`. 
- Tiếp tục decode dãy số này sử dụng `Magic` và lấy được `Flag`![](https://hackmd.io/_uploads/HyvxTk0R3.png)
- `Flag` là `PCTF{w0w_s0_m4ny_number5}`