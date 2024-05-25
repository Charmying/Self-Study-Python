# Python 筆記

[Python 入門教學課程](https://www.youtube.com/playlist?list=PL-g0fdC5RMboYEyt6QS2iLb_1m7QcgfHk)



###### <br/>

---

###### <br/>



## 快速開始 <br/> 01_start.py

1. 在 D 槽建立新資料夾 (python)

2. 於 VS Code 的左上方工具列找到檔案 → 開啟資料夾 → 找到 D 槽建立的資料夾 (Python)

3. 新增檔案，主檔名 隨便 (建議英文)，副檔名為 .py

4. 切到終端機 (TERMINAL)

5. 執行 → python 1_start.py → `enter`

- 若要清空 TERMINAL 畫面 → cls `enter`

- 註解：程式碼內打 #，# 後面可任意加寫文字，不會影響程式執行

###### <br/>
###### <br/>
###### <br/>





## 變數 & 資料 & 資料型態 <br/> 02_datatype.py

- 資料：程式中最基本的單位

- 資料型態 (Data type)：資料的分類

- 資料的分類

	- 數字：整數、長整數、浮點數(小數)

	- 字串：任意的文字內容

	- 布林值：表達正確 (True) 或錯誤 (False)，T&F需大寫

	- 可變列表 (List)：有順序、可變動的資料集合，ex. 學生的成績

	- 固定列表 (Tuple)：有順序、不可變動的資料集合

	- 集合 (Set)：無順序的資料集合，ex. 水果

	- 字典：鍵值對 (Key-Value Pair) 的集合， 程式中做資料查詢 (ex. A對應到B)

- 變數 (variable)：可用來存放資料的自訂名稱，可在程式中建立名稱，未來可用自訂名稱代表資料，變數用英文，開頭不可是數字

- 字串：在程式中表達任意的文字，ex. 測試中文 是錯誤的語法，Python 語法為英文，但若想表達中文，用雙引號 (或單引號) 包起來，ex. "測試中文"、"HelloWorld"

	- 雙引號 (或單引號) 中能寫任意文字

###### <br/>
###### <br/>
###### <br/>





## 數字、字串的基本運算 <br/> 03_number-string.py

### 數字

- 基本算術運算：加 (+)、減 (-)、乘 (*)、除 (/)、取餘數 (%)

- 除法詳解：整數除法 (//)、小數除法 (/)

- X 的 Y 次方 ```X ** Y```、開根號 ```X ** 0.5```

### 字串

- 表示法詳解：雙引號 (")、單引號 (')、多行文字

- 重複 & 串接：重複相同文字或串接多個字串

- 索引 & 字元：使用索引 [] 操作字串中的字元

### 數字運算

- ```x = x + 1``` ，左邊 x 為變數，右邊 (x + 1) 要先看

- ```x = x + 1``` 可寫成 ```x += 1```

### 字串運算

```
s = "Hello"
print(s)

→

Hello
```

```
s = "Hell\"o"
print(s)

→

Hell"o
```

#### \"：跳脫

```
s = "Hello" + "World" = "Hello"  "World"
print(s)

→

HelloWorld
```

```
s = "Hello\nWorld"
print(s)

→

Hello
World
```

#### \n：跳行

```
s = """Hello
World"""
print(s)

→

Hello
World
```

##### 單雙引號皆可，前後各 3 個，中間可任意空行 (與跳行相同，兩者皆可使用)

```
s = "Hello" * 3
print(s)

→

HelloHelloHello
```

```
s = "Hello" * 3 + "World"
print(s)

→

HelloHelloHelloWorld
```

### 字串內部字元編號 (索引) 

```
s = "Hello"
print(s[0])

→

H
```

```
s = "Hello"
print(s[2])

→

l
```

##### Hello 中，H 為 0、e 為 1、l 為 2、l 為 3、o 為 4，5 沒有東西

```
s = "Hello"
print(s[1: 4])

→

ell
```

##### ※ 包含開頭，不包含結尾

###### <br/>
###### <br/>
###### <br/>





## 數字、字串的基本運算 <br/> 04_list-tuple.py

### 2 種有序列表型態：List & Tuple

- List (List 的寫法為中括號 [] )

	- 索引基本運用：取得、更新列表中的資料

	- 連續資料處理：串接、取代、連續刪除列表中的資料

	- 取得列表長度：len (列表)

	- 巢狀列表：列表中的資料也是列表

- Tuple ( Tuple 的寫法為小括號 () )

	- 資料不可更動，操作與 List 相同，但資料不可更動

### 有序可變動列表List

```
grades = [12, 60, 15, 70, 90]
print(grades)

→

[12, 60, 15, 70, 90]
```

```
grades = [12, 60, 15, 70, 90]
print(grades[0])

→

12
```

```
grades = [12, 60, 15, 70, 90]
grades[0] = 55
print(grades)

→

[55, 60, 15, 70, 90]
```

```
grades = [12, 60, 15, 70, 90]
print(grades[1: 4])

→

[60, 15, 70]
```

```
grades = [12, 60, 15, 70, 90]
# 連續刪除列表
grades[1: 4] = [] 
print(grades)

→

[12, 90]
```

```
grades = [12, 60, 15, 70, 90]
grades = grades + [12, 33]
print(grades)

→

[12, 60, 15, 70, 90, 12, 33]
```

##### 看到等號先看等號右邊

##### 可輕易做到表的串接

### 槽狀列表

```
data = [[3, 4, 5], [6, 7, 8]]
print(data[0][1])

→

4
```

##### [3, 4, 5] 為第 0 層，[6, 7, 8] 為第 1 層；3 為 0、4 為 1、5 為 2、  6 為 0、7 為 1、8 為 2

```
data=[[3, 4, 5], [6, 7, 8]]
print(data[0][0: 2])

→

[3, 4]
```

```
data = [[3, 4, 5],[6, 7, 8]]
print(data)
data[0][0: 2] = [5, 5, 5]
print(data)

→

[[3, 4, 5], [6, 7, 8]]
[[5, 5, 5, 5], [6, 7, 8]]
```

##### [3, 4, 5] 為第 0 層，[6, 7, 8] 為第 1 層；3 為 0、4 為 1、5 為 2、  6 為 0、7 為 1、8 為 2

#### Tuple 所有操作與 List 相同，但 Tuple 資料不可更動

```
data = (3, 4, 5)
data[0] = 5
print(data)

→

error
```

##### 錯誤：Tuple 的資料不可以變動

###### <br/>
###### <br/>
###### <br/>





## 集合、字典的基本運算 – Set、Dictionary <br/> 05_set-dictionary.py

### 集合

- 基本觀念：一群資料沒有順序性 (列表有順序概念，集合沒有)

- 判斷資料是否存在：使用 in 和 not in 運算符號

	- 交集、聯集：使用 & 和 | 運算符號

		- 交集：取兩個集合中相同的資料

		- 聯集：取兩個集合中的所有資料，但不重複取

	- 差集、反交集：使用 - 和 ^ 運算符號

		- 差集：從A集合中減去和B集合重疊的資料

		- 反交集：取兩個集合中不重疊的資料

- 字串拆解為集合：set (字串)

### 字典

- 基本觀念：鍵值對 (Key-value Pair)，一個索引對一個資料

- key 對應 Value：字典[Key]；字典[Key] = Value

- 判斷資料是否存在：使用 in 和 not in 運算符號

- 刪除鍵值對：使用 del 運算關鍵字

- 從列表建立字典：以列表的資料為基礎來建立字典

### 集合的運算

```
s1 = {3, 4, 5}
print(3 in s1)

→

True
```

##### 檢視 3 有無在集合內，若有為 True，若無為 False

```
s1 = {3, 4, 5}
print(10 in s1)

→

False
```

```
s1 = {3, 4, 5}
print(10 not in s1)

→

True
```

```
s1 = {3, 4, 5}
s2 = {4, 5, 6, 7}
s3 = s1 & s2
print(s3)

→

{4, 5}
```

#### 交集 (&)：取兩個集合中相同的資料

```
s1 = {3, 4, 5}
s2 = {4, 5, 6, 7}
s3 = s1 | s2
print(s3)

→

{3, 4, 5, 6, 7}
```

#### 聯集 (|)：取兩個集合中的所有資料，但不重複取

```
s1 = {3, 4, 5}
s2 = {4, 5, 6, 7}
s3 = s1 - s2
print(s3)

→

{3}
```

#### 差集 (-)：從 s1 中減去和 s2 重疊的資料

```
s1 = {3, 4, 5}
s2 = {4, 5, 6, 7}
s3 = s1 ^ s2
print(s3)

→

{3, 6, 7}
```

#### 反交集 (^)：取兩個集合中不重疊的資料

```
s = set("Hello")
print(s)

→

{'H', 'o', 'e', 'l'}
```

##### 語法為 set (字串)：集合無順序觀念，TERMINAL 顯示順序為隨機，且重複部分不會重複顯示

```
s = set("Hello")

print("H" in s)

→

True
```
```
s = set("Hello")
print("h" in s)

→

False
```

### 字典的運算：Key-value 配對

```
dic = {"apple": "蘋果", "bug": "蟲蟲"}
print(dic["apple"])

→

蘋果
```

```
dic = {"apple": "蘋果", "bug": "蟲蟲"}
dic["apple"] = "小蘋果"
print(dic["apple"])

→

小蘋果
```

```
dic = {"apple": "蘋果", "bug": "蟲蟲"}
print("apple" in dic)

→

True
```

##### 判斷對象為 key 非 value

```
dic = {"apple": "蘋果", "bug": "蟲蟲"}
print(dic)
del dic["apple"]
print(dic)

→

{'apple': '蘋果', 'bug': '蟲蟲'}
{'bug': '蟲蟲'}

```

##### 刪除字典中的鍵值對 (key-value pair)，[] 中只能選 key 不能選 value

### 從列表的資料產生字典

#### 語法：```dic = {x: x * 2 for x in [列表]}```

##### 其中 for in 固定不變

```
dic = {x: x * 2 for x in [3, 4, 5]}
print(dic)

→

{3: 6, 4: 8, 5: 10}
```

###### <br/>
###### <br/>
###### <br/>





## 流程控制：if 判斷式 <br/> 06_condition.py

> 基本語法一

```
if 布林值:
	若布林值為 True，執行命令
```

##### 前面部分為縮排 ```Tab```

> 基本語法二

```
if 布林值:
	若布林值為 True，執行命令
else:
	若布林值為 False，執行命令
```

> 基本語法三

```
if 布林值一:
	若布林值一為 True，執行命令
elif 布林值二:
	若布林值二為 True，執行命令
else:
	若布林值一和二為 False，執行命令
```

##### 布林值一是 True，代表滿足條件，滿足第一個條件跑第一段，第一個條件不滿足就看第二個條件，如果滿足第二個條件跑第二段，若第一個條件和第二個條件都是 False (都不滿足)，才跑第三段

##### elif = else if

> 程式範例

```
x = input("請輸入數字：")   # 基本輸入為字串型態
x = int(x)   # 轉換為整數型態
if x > 200:
	print("大於 200")
elif x > 100:
	print("大於 100，小於 200")
else:
	print("小於 100")
```

##### 以上為 if 語法，至 3.6 版 Python 不支援 switch 語法

##### 用 ```x = input()``` 即可在 TERMINAL 進行輸入

##### 在 TERMINAL 中 input 的數字回到程式中為字串型態，所以需用 x = int(x) 將字串型態轉換為數字型態

> 判斷式

```
if True:
	print("True 執行")
	
→

True 執行
```

```
if False:
	Print("True 執行")

→

(會直接被忽略)
```

```
if True:
	print("True 執行")
else:
	print("False 執行")

→

True 執行
```

```
if False:
	print("True 執行")
else:
	print("False 執行")

→

False 執行
```

```
x = input("請輸入數字：")
x = int(x)
if x > 100:
	print("大於 100")
else:
	print("小於等於 100")

→

請輸入數字：(在 TERMINAL 隨意輸入數字，ex. 200)
大於 100
```

```
x = input("請輸入數字：")
x = int(x)
if x > 100:
	print("大於 100")
else:
	print("小於等於 100")

→

請輸入數字：(在 TERMINAL 隨意輸入數字，ex. 50)
小於等於 100
```

```
x = input("請輸入數字：")
x = int(x)
if x > 200:
	print("大於 200")
elif x > 100:
	print("大於 100，小於等於 200")
else:
	print("小於等於 100")

→

請輸入數字：150
大於 100，小於等於 200
```

```
n1 = int(input("請輸入數字一："))
n2 = int(input("請輸入數字二："))
op = input("請輸入運算：+、-、*、/：")
if op == "+":
	print(n1 + n2)
elif op == "-":
	print(n1 - n2)
elif op == "*":
	print(n1 * n2)
elif op == "/":
	print(n1 / n2)
else:
	print("不支援的運算")

→

請輸入數字一：(在 TERMINAL 隨意輸入數字) enter
↓
請輸入數字二：(在 TERMINAL 隨意輸入數字) enter
↓
請輸入運算：+、-、*、/：(在 TERMINAL 隨意輸入 +、-、*、/ 其一) enter
↓
(自動完成上述運算)
```

##### 程式邏輯：取得第一個數字放在 n1 → 取得第二個數字放在 n2 → 最後取得 +、-、*、/ 中的其中一個放在 op → 判斷式進行判斷是否為 True，若為 True 則跑該段

###### 建議有時間自行重寫練習