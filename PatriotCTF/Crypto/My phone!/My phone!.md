# My phone!
## Challenge's information
- Some weird triangle man stole my phone, he taunted me by sending me his location but it seems to be encrypted with some odd cipher I've never seen before, could you please help me get my phone back?
- Flag format: PCTF{city_name}
- https://pctf.competitivecyber.club/files/4f511c6fa90972692d1e98b99c40ab0f/cipher.png?token=eyJ1c2VyX2lkIjoyMjkxLCJ0ZWFtX2lkIjo4MjcsImZpbGVfaWQiOjV9.ZQBwpA.rhKQiLaGyQUzRwQkk7tg2RgGkrI
## Solution
- Tải file `cipher.png` về và mở ra, ta thấy trong ảnh là 1 dãy `Bill Cipher-Gravity Fall`![](https://hackmd.io/_uploads/SkXm-gAR3.png)
- Sử dụng [tool](https://www.dcode.fr/gravity-falls-bill-cipher) để decode ra được 1 dãy các từ tiếng anh có ý nghĩa là các con số `FOURSIX.SEVENSIXEIGHT,-NINETWO.ONETWOFOUR`
![](https://hackmd.io/_uploads/rJHhWlAA3.png)
- Nhận thấy đây rất giống kinh-vĩ độ của một nơi nào đó trên thế giới, sử dụng [Google Map](https://maps.google.com/) để tìm kiếm và ra được tên thành phố cần tìm
![](https://hackmd.io/_uploads/By9uGlCR2.png)
- `Flag` là `PCTF{Duluth}`


