# My First Hash
## Challenge's information
- Here's your flag: 8f163b472e2164f66a5cd751098783f9 Psyc! Its encrypted. You think I'd give it to you that easily? Definitely don't look at my code tho -><- (when you find the flag, put it in bctf{} format)
- [my-first-hash.py](https://buckeyectf23-stage1.s3.us-east-2.amazonaws.com/my-first-hash/my-first-hash.py)
## Solution
- Đọc file [python](https://buckeyectf23-stage1.s3.us-east-2.amazonaws.com/my-first-hash/my-first-hash.py), ta thấy rằng đoạn cipher này được mã hoá bằng MD5.
- Sử dụng [tool](https://hashtoolkit.com/) để decrypt và lấy được flag:![](https://hackmd.io/_uploads/SkJ9mynla.png)
- `Flag` là `bctf{orchestra}`
