# Combine
## Challenge's information
- The symmetric crypto algorithm is much more secure, but the problem of key distribution is annoying. Why don't we combine both symmetric and asymmetric algorithm in a crypto system. What a brilliant idea!
https://drive.google.com/drive/folders/17t2v_JqvkxZnjui4PVl4CgkqqXzV_z--?usp=sharing 
## Solution
- Sau khi tải về 2 file `combine.py` và `output.txt`, ta mở ra và biết được cách thức mà challenge tạo ra ra ciphertext bằng cách encrypt flag với thuật toán AES mode ECB và key của thuật toán này đã được encrypt bằng thuật toán RSA. Vì vậy ta cần phải decrypt đc RSA để lấy key và decrypt nốt AES để có được flag
- ![](https://hackmd.io/_uploads/HyJN1xman.png)
```python
#!/usr/bin/env python3

from Crypto.Util.number import getStrongPrime, bytes_to_long
from Crypto.Cipher import AES
from secret import flag, key

def encrypt_message(key, msg):
	BS = 16
	pad = lambda s: s + (BS - len(s) % BS) * chr(BS - len(s) % BS)
	msg = pad(msg).encode()
	cipher = AES.new(key, AES.MODE_ECB)
	ciphertext = cipher.encrypt(msg).hex()
	return ciphertext

def encrypt_key(key):
	nbit = 2048
	p = getStrongPrime(nbit // 2)
	q = getStrongPrime(nbit // 2)
	n = p * q
	e = 3
	m = bytes_to_long(key)
	cipherkey = pow(m, e, n)
	return n, e, cipherkey

ciphertext = encrypt_message(key, flag)
n, e, c = encrypt_key(key)

print('n =', n)
print('e =', e)
print('cipherkey =', c)
print('ciphertext =', ciphertext)


```
- Rất may là thuật toán RSA này chúng ta đã có sẵn được `n`, `e`, và `c` với `c` là `cipherkey`.
![](https://hackmd.io/_uploads/ryM9kgXa3.png)
- Ta thấy `e` khá nhỏ nên có thể thử sử dụng [tool](https://www.dcode.fr/rsa-cipher) để decrypt và lấy được key của thuật toán là `secret#keysummerSuperSecureAyyah`
![](https://hackmd.io/_uploads/S1OGlg7a3.png)
- Sử dụng key vừa lấy được kết hợp với [tool](https://www.devglan.com/online-tools/aes-encryption-decryption) để decrypt thuật toán AES và ta tìm ra được flag của challenge
![](https://hackmd.io/_uploads/r1ZRxeXpn.png)
- Flag là `FUSEC{The_combine_crypto_system_is_really_secure!!!}`
