### ๐ ๋์๋๋ฆฌ Dictionary

* string substring
* python string compare time compriexity

* [๋ฌธ์์ด] ์ฌ๋ผ์ด์ฑ ๋ณต์ต  

---

> 1. **ํด์ํ์ด๋ธ,  2. ๋์๋๋ฆฌ ๊ธฐ๋ณธ ๋ฌธ๋ฒ, 3. ๋์๋๋ฆฌ ๋ฉ์๋** 



#### (1) ํด์ํ์ด๋ธ

**ํ์ด์ฌ์๋ ๋์๋๋ฆฌ dict ์๋ฃ๊ตฌ์กฐ๊ฐ ๋ด์ฅ ๋์ด ์๋ค.** 

**non-sequence & key value**  

```python
{
"name" : "kt"
"gender" : "male"
"address" : "seoul"
}

# key๋ immutable(๋ณ๊ฒฝ๋ถ๊ฐ๋ฅ)
# ์์๊ฐ ์๋ค. 
```



#### โผ **key : value ๊ฐ ์ ์ฅ๋๋ ์๋ฆฌ๋ ๋ฌด์์ผ๊น? _ ์ผ๋จ ๋ฆฌ์คํธ๐ป๋ฅผ ํ์ฉํ์ฌ key : value๋ฅผ ์ ์ฅํ์.** 

![image-20220803023855768](์๊ณ ๋ฆฌ์ฆ 4DAY.assets/image-20220803023855768.png)



#### โผ ํด์ ํจ์ : ์์ ๊ธธ์ด์ ๋ฐ์ดํฐ๋ฅผ ๊ณ ์  ๊ธธ์ด์ ๋ฐ์ดํฐ๋ก ๋งคํํ๋ ํจ์ 

#### โผ ํด์ : ํด์ ํจ์๋ฅผ ํตํด ์ป์ด์ง ๊ฐ

![image-20220803024037012](์๊ณ ๋ฆฌ์ฆ 4DAY.assets/image-20220803024037012.png)



#### โผ ํด์ ํจ์์ ํด์ ํ์ด๋ธ์ ์ด์ฉํ๊ธฐ ๋๋ฌธ์ ์ฝ์, ์ญ์ , ์์ , ์กฐํ **์ฐ์ฐ์ ์๋๊ฐ ๋ฆฌ์คํธ ๋ณด๋ค ๋น ๋ฅด๋ค.** 

#### โผ (Hash function์ ์ด์ฉํ ์ฐ์  ๊ณ์ฐ์ผ๋ก ๊ฐ์ด ์๋ ์์น๋ฅผ ๋ฐ๋ก ์ ์ ์๊ธฐ ๋๋ฌธ)

---



#### โผ โญ ๋์๋๋ฆฌ ์ฐ์ฐ์ ์๊ฐ ๋ณต์ก๋ = ์ ๋ ๊ธฐ์ตํ๊ธฐ!!!

| ์ฐ์ฐ ์ข๋ฅ   | ๋์๋๋ฆฌ | ๋ฆฌ์คํธ         |
| ----------- | -------- | -------------- |
| get item    | O(1)     | O(1)           |
| insert item | O(1)     | O(1) ๋๋ O(N) |
| update item | O(1)     | O(1)           |
| delete item | O(1)     | O(1) ๋๋ O(N) |
| search item | O(1)     | O(N)           |

**Q. ๋ฆฌ์คํธ ์์ O(1) ๋๋ O(n) ์ผ๊น?** 

= ์ธ์  ๋ฃ๋๋์ ๋ฐ๋ผ ๋ค๋ฅด๊ธฐ ๋๋ฌธ์ด๋ค. 



**Q. ๋์๋๋ฆฌ๋ ์ธ์  ์ฌ์ฉํด์ผ ํ ๊น?**

- ๋ฆฌ์คํธ๋ฅผ ์ฌ์ฉํ๊ธฐ ํ๋  ๊ฒฝ์ฐ (์๊ณ ๋ฆฌ์ฆ)
- ๋ฐ์ดํฐ์ ๋ํ ๋น ๋ฅธ ์ ๊ทผ ํ์์ด ํ์ํ ๊ฒฝ์ฐ  (์๊ณ ๋ฆฌ์ฆ)
- ํ์ค  ์ธ๊ณ์ ๋๋ถ๋ถ์ ๋ฐ์ดํฐ๋ฅผ ๋ค๋ฃฐ ๊ฒฝ์ฐ 



---

### (2) ๋์๋๋ฆฌ ๊ธฐ๋ณธ ๋ฌธ๋ฒ



##### **โผ ์ ์ธ ___ ๋ณ์ = {key1: value1, key2: value2 .....}**

```python
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
print(a)
#์ถ๋ ฅ : {'name': 'su', 'gender': 'f', 'address' : 'Seoul'}
```



##### โผ ๋์๋๋ฆฌ [key] = value

**โญ ๋ด๋ถ์ ํด๋น key๊ฐ ์์ผ๋ฉด ์ฝ์, ์์ผ๋ฉด ์์  (๋ฌด์กฐ๊ฑด ์๊ธฐ)**

```python
# ์ฝ์
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
a["job"] = "Fullstack developer"
print(a)

#์ถ๋ ฅ 
{'name': 'su', 'gender': 'f', 'address' : 'Seoul', 'job' : 'Fullstack developer'}
```

```python
# ์์ 
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
a["name"] = "kyung"
print(a)

#์ถ๋ ฅ 
{'name': 'kyung', 'gender': 'f', 'address' : 'Seoul'}
```



##### โผ ๋์๋๋ฆฌ.pop(key) ์ญ์  

##### ๋ด๋ถ์ ์กด์ฌํ๋ key์ ๋ํ value ์ญ์  ๋ฐ ๋ฐํ, ์กด์ฌํ์ง ์๋ key์ ๋ํด์๋ keyerror ๋ฐ์ 

```python
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
gender = a.pop("gender")

print(a)
print(gender)

#์ถ๋ ฅ 
{'name': 'kyung',  'address' : 'Seoul'}
f
```

```python
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
phone = a.pop("phone")

print(a)
print(phone)

# keyerror ๋ฐ์ 
```



##### โผ ๋์๋๋ฆฌ.pop(key, default) ์ญ์  

##### ๋๋ฒ์งธ ์ธ์๋ก default๊ฐ์ ์ง์ ํ์ฌ keyerror ๋ฐฉ์ง ๊ฐ๋ฅ 

(default  ๊ฐ์ ์ง์ ํด์ฃผ๋ฉด ์ค๊ฐ์ ๋ฉ์ถ๋ ๊ฒ์ ๋ฐฉ์งํด์ค)

```python
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
phone = a.pop("phone", "010-8666-0000")

print(a)
print(phone)

#์ถ๋ ฅ : 
# {'name': 'su', 'gender': 'f', 'address' : 'Seoul'}
# 010-8666-0000
```



##### โผ  key ์ ํด๋นํ๋ value ๋ฐํ 

```python
# ๋์๋๋ฆฌ [key]
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
print(a["name"])

#์ถ๋ ฅ : su
```

#####  

```python
# ๋์๋๋ฆฌ .get(key)
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
print(a.get("name"))
#์ถ๋ ฅ : su
```



##### โผ  ๊ธฐ๋ณธ์ ์ธ ๋์๋๋ฆฌ ์ฌ์ฉ๋ฒ _์กฐํ

```python
# ๋์๋๋ฆฌ [key]
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
pritn(a["phone"])

#keyerror
```

```python
# ์์ ๋์๋๋ฆฌ [key] ์ ๋น๊ตํด๋ณด๊ธฐ 
# ๋์๋๋ฆฌ .get(key)

a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
pritn(a.get["phone"])
#์ถ๋ ฅ : none

a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
print(a.get("phone", "์์"))

#์ถ๋ ฅ : ์์

```



##### ๐โโ๏ธ ๋์๋๋ฆฌ ๊ธฐ๋ณธ ๋ฌธ๋ฒ ์ ๋ฆฌ 

|    **์ ์ธ**     |   **๋ณ์ = {key1: value1, key2: value2 .....}**    |
| :-------------: | :------------------------------------------------: |
| **์ฝ์ / ์์ ** |             **๋์๋๋ฆฌ [key] = value**             |
|    **์ญ์ **     |           **๋์๋๋ฆฌ.pop(key, default)**           |
|    **์กฐํ**     | **๋์๋๋ฆฌ [key]  /  ๋์๋๋ฆฌ .get(key, default)** |



---



### 3. ๋์๋๋ฆฌ ๋ฉ์๋ 

**(1) .keys()** **: ๋์๋๋ฆฌ key๋ชฉ๋ก์ด ๋ด๊ธด dict_keys ๊ฐ์ฒด ๋ฐํ** 

```python

a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
print(a.keys())

# ์ถ๋ ฅ
# dict_keys(['name', 'gender', 'address'])
```

```python
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}

for key in a.keys():
    print(key)

# ์ถ๋ ฅ 
# name
# gender
# address
```

```python
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
for key in a:
    print(key)
    
# ์ถ๋ ฅ 
# name
# gender
# address   
```



**(2) .values() : ๋์๋๋ฆฌ value ๋ชฉ๋ก์ด ๋ด๊ธด dict_values ๊ฐ์ฒด ๋ฐํ** 

```python
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
print(a.values())

# ์ถ๋ ฅ 
# dict_values(['su', 'f', 'Seoul'])
```

```python
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
for value in a.values():
    print(values)
    
# ์ถ๋ ฅ 
# su
# f
# Seoul
```



**(3) .items() : ๋์๋๋ฆฌ์ (key, value) ์ ๋ชฉ๋ก์ด ๊ฐ๊ธด dict_items ๊ฐ์ฒด ๋ฐํ** 

```python
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}
print(a.items())

#์ถ๋ ฅ 
dict_items([('name', 'su'), ('gender', 'f'), ('address', 'Seoul')])
```

```python
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}

for item in a.items():
    print(item)

# ('name', 'su')
# ('gender', 'f')
# ('address', 'Seoul')
```

```python
a = {
    "name" : "su"
    "gender" : "f"
    "address" : "Seoul"
}

for key, value in a.items():
    print(key, value)

# name su
# gender f
# address Seoul
```

