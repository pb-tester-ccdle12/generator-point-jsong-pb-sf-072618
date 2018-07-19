
# The Generator Point

You can think of the generator G as the first point after infinity on the curve. Begin with infinity and add G; the result is G. Add G to this and you get 2G. Add G to this and you get 3G. And so on. If you add G a total of n times (where n is the order of the curve) you will be back at infinity, where you started; the whole curve is a never-ending loop. The order n is how many distinct points are on the curve, or in Bitcoin terms, how many possible private keys there are (plus 1 for the point at infinity). [[Source]](https://bitcoin.stackexchange.com/a/34133)


```python
# Confirgming G is on the curve
p = 2**256 - 2**32 - 977
x = 0x79BE667EF9DCBBAC55A06295CE870B07029BFCDB2DCE28D959F2815B16F81798
y = 0x483ADA7726A3C4655DA4FBFC0E1108A8FD17B448A68554199C47D08FFB10D4B8
print(y**2 % p == (x**3 + 7) % p)
```


```python
# Confirming order of G is n
from ecc import G

n = 0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFEBAAEDCE6AF48A03BBFD25E8CD0364141
print(n*G)
```
