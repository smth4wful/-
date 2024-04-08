# -шпоры для крипты

1)   16 система в байты
    
    hex_val = "значение"
    print(bytes.fromhex(hex_val))

2)   дешифровка чар
    x = [массив с данными]
    for i in x:
        print(chr(i))


3)    дешифровка бэйс 64
      base64
      import base64
      
      hex_val = "строка"
      byte_val = bytes.fromhex(hex_val)
      print(base64.b64encode(byte_val))



4)    дешифровка long в bytes

    сначала pip install pycryptodome
    
    from Crypto.Util.number import *
    a = 11515195063862318899931685488813747395775516287289682636499965282714637259206269
    print(long_to_bytes(a))


5)  xor для строк
    
    1.pip install pwntools
    
    2.from pwn import xor

      given = "label"
      print(xor(given,ключ))


  xor только для двух переменных одновременно(нужно делать выражения)
  
6) Расширенный алгоритм Евклида
  def extended_euclidean(a, b):
    if b == 0:
        return (a, 1, 0)
    else:
        (g, x, y) = extended_euclidean(b, a % b)
        return (g, y, x - (a // b) * y)

a, b = int(input("Введите два числа: ")), int(input())
(g, x, y) = extended_euclidean(abs(a), abs(b))
print("Наибольший общий делитель:", g)
print("Дополнительные коэффициенты:", x, y)

7) Если задание похоже на 11 ≡ x mod 6, то
   for i in range(100):
    if i % 6 == 11 % 6:
        print(i)
