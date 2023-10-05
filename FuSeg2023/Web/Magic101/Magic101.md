# Magic 101
## Challenge's Information:
Using your magic get flag asap ! https://magic.fptunisecathon2023.tech/
![](https://hackmd.io/_uploads/H1sDTHzp3.png)
## Solution
- Trang web này chỉ có 1 function duy nhất có thể thao tác được là `try` với 2 param để nhập input là `Page Title` và `<p> Dũng sĩ diệt gays!</p>` dùng để render ra 1 trang web có title và content theo input của mình. Trong đó `Page Title` chỉ có tác dụng là đặt title cho trang web đc render sau khi mình nhập input và bấm `Try!` còn `<p> Dũng sĩ diệt gays!</p>` sẽ là nơi mình vứt payload vào để exploit.
![](https://hackmd.io/_uploads/BkJZABM6h.png)
- Ban đầu mình nghĩ bài này là lỗi ssti do cũng vừa làm chall `Baby Injection`. Vì vậy mình đã thử một vài payload SSTI Python-Jinja2 mà mình kiếm được trên `PayloadsAllTheThings` nhưng kết quả chỉ toàn là `noooooooooooooo :)))` hoặc là 1 vài payload đơn giản như `{{7*7}}` sẽ bị filter 1 cặp `{}` và in ra là `{7*7}`.
![](https://hackmd.io/_uploads/BJPJZLM6n.png)
![](https://hackmd.io/_uploads/SJceZUGTn.png)
- BTC cung cấp 1 hint khá quan trong đó là lỗi `Python str.format` cũng như cần tập trung vào hàm `secret_function`. Dựa theo hint đó và một vài gợi ý đến từ author của challenge này, mình đã mò đc ra Write-Up của một bài tương tự:https://ctftime.org/writeup/27904
- Với hướng dẫn của Write-Up trên, mình có được payload hoàn chỉnh là `{self.__init__.__globals__[secret_function].__code__.co_consts}` và có đc flag:
![](https://hackmd.io/_uploads/SJinXIGp3.png)
- Flag cuối cùng là `FUSec{Br3h_1mA0_ni3C_g4Ys}`




