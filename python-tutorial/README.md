# Lập trình Python cơ bản

Tổng hợp kiến thức cơ bản về Python

## Biến(Variables) trong Python

Trong Python, biến là một khái niệm cơ bản và quan trọng nhất. Biến là một vùng nhớ được dành riêng cho lưu trữ dữ liệu, và có thể được gán, truy cập và sử dụng lại trong chương trình của bạn. 

Các biến trong Python không cần phải được khai báo trước khi sử dụng. Khi bạn gán một giá trị cho biến, Python sẽ tự động xác định kiểu dữ liệu của biến dựa trên giá trị đó, và bạn có thể sử dụng biến đó trong toàn bộ chương trình của bạn. 

Ví dụ, dưới đây là cách khai báo một biến trong Python:
```python
a = 10           # biến a có kiểu số nguyên và giá trị là 10
b = 3.14         # biến b có kiểu số thực và giá trị là 3.14
c = 'Hello'      # biến c có kiểu chuỗi và giá trị là 'Hello'
```

Bạn có thể sử dụng biến trong các biểu thức và câu lệnh của Python, ví dụ:
```python
print(a + b)    # kết quả sẽ là 13.14
print(c * 3)    # kết quả sẽ là 'HelloHelloHello'
```

Bạn cũng có thể thay đổi giá trị của biến bất cứ lúc nào trong chương trình của mình, ví dụ:
```python
a = 20           # thay đổi giá trị của a sang 20
print(a + b)    # kết quả sẽ là 23.14
```

## Định dạng chuỗi(String formatting) trong Python

String formatting trong Python là cách sử dụng để tạo ra chuỗi kết hợp các giá trị biến vào trong chuỗi. String formatting cho phép nhúng các giá trị biến vào trong chuỗi một cách nhanh chóng và dễ dàng. 

Có nhiều cách để sử dụng string formatting trong Python. Bạn có thể sử dụng cú pháp %, .format(), hoặc sử dụng f-string. Dưới đây là ví dụ cách sử dụng các cách này:

Ví dụ sử dụng cú pháp `%`
```python
name = "Trung"
age = 27
print("My name is %s and I'm %d years old." % (name, age))
```

Ví dụ sử dụng phương thức `format()`
```python
name = "Trung"
age = 27
print("My name is {} and I'm {} years old.".format(name, age))
```

Ví dụ sử dụng `f-string`
```python
name = "Trung"
age = 27
print(f"My name is {name} and I'm {age} years old.")
```

Cả ba cách đều cho kết quả là:
```python
My name is Trung and I'm 27 years old.
```

## Nhập dữ liệu từ màn hình console

Trong Python, để lấy input từ người dùng, ta sử dụng hàm input() để lấy chuỗi nhập từ bàn phím:

Ví dụ:
```python
name = input("Nhập tên của bạn: ")
print("Xin chào " + name + "!")
```

Khi chạy chương trình, ta sẽ nhìn thấy một dòng chuỗi xuất hiện, hướng dẫn người dùng nhập vào tên của họ.

Sau khi người dùng hoàn thành nhập liệu và nhấn phím 'Enter', giá trị vừa nhập sẽ được trả về và gán vào biến name. Tiếp theo, chương trình sẽ in ra lời chào với tên người dùng.

Giá trị người dùng nhập đều ở kiểu dữ liệu String, nếu người dùng muốn sử dụng giá trị đó ở kiểu Integer thì cần phải cast dữ liệu từ String thành Integer
```python
ageString = input("Nhập tuổi của bạn: ")
age = int(ageString)
print(f"Tuổi của bạn là {age}")
```

## List và một số thao tác cơ bản với List

Trong Python, list là một kiểu dữ liệu dùng để lưu trữ một tập hợp các phần tử có thứ tự. Dưới đây là một số thao tác phổ biến với list trong Python:

Khởi tạo list:
```python
my_list = []                           # List rỗng
my_list = [1, 2, 3]                     # List chứa các số nguyên
my_list = ['apple', 'banana', 'orange'] # List chứa các chuỗi
```

Truy cập phần tử trong list:
```python
my_list = [1, 2, 3, 4, 5]
print(my_list[0])     # Output: 1
print(my_list[2])     # Output: 3
print(my_list[-1])    # Output: 5 (truy cập từ cuối list)
```

Thay đổi giá trị phần tử trong list:
```python
my_list = [1, 2, 3]
my_list[0] = 4
print(my_list)    # Output: [4, 2, 3]
```

Độ dài của list:
```python
my_list = [1, 2, 3, 4, 5]
length = len(my_list)
print(length)    # Output: 5
```

Thêm phần tử vào list:
```python
my_list = [1, 2, 3]
my_list.append(4)      # Thêm phần tử 4 vào cuối list
my_list.insert(1, 5)   # Thêm phần tử 5 vào vị trí index 1
print(my_list)         # Output: [1, 5, 2, 3, 4]
```

Xóa phần tử khỏi list:
```python
my_list = [1, 2, 3, 4, 5]
del my_list[2]         # Xóa phần tử có index 2 (giá trị 3)
my_list.remove(4)      # Xóa phần tử có giá trị 4
print(my_list)         # Output: [1, 2, 5]
```

Slicing (trích xuất một phần của list):
```python
my_list = [1, 2, 3, 4, 5]
sublist = my_list[1:4]      # Trích xuất các phần tử từ index 1 đến index 3
print(sublist)             # Output: [2, 3, 4]
```

Kiểm tra sự có mặt của phần tử trong list:
```python
my_list = [1, 2, 3, 4, 5]
print(3 in my_list)        # Output: True
print(6 in my_list)        # Output: False
```

Sắp xếp list:
```python
my_list = [3, 1, 4, 2, 5]
my_list.sort()             # Sắp xếp tăng dần
print(my_list)             # Output
```

## Tuple và một số thao tác cơ bản với Tuple

Trong Python, tuple là một kiểu dữ liệu tương tự như list, nhưng không thể thay đổi sau khi khởi tạo (immutable). Dưới đây là một số thao tác phổ biến với tuple trong Python:

Khởi tạo tuple:
```python
my_tuple = ()                            # Tuple rỗng
my_tuple = ('abc',)                       # Tuple có một phần tử
my_tuple = (1, 2, 3)                      # Tuple chứa các số nguyên
my_tuple = ('apple', 'banana', 'orange')  # Tuple chứa các chuỗi
```

Truy cập phần tử trong tuple:
```python
my_tuple = (1, 2, 3, 4, 5)
print(my_tuple[0])     # Output: 1
print(my_tuple[2])     # Output: 3
print(my_tuple[-1])    # Output: 5 (truy cập từ cuối tuple)
```

Độ dài của tuple:
```python
my_tuple = (1, 2, 3, 4, 5)
length = len(my_tuple)
print(length)    # Output: 5
```

Slicing (trích xuất một phần của tuple):
```python
my_tuple = (1, 2, 3, 4, 5)
subtuple = my_tuple[1:4]      # Trích xuất các phần tử từ index 1 đến index 3
print(subtuple)              # Output: (2, 3, 4)
```

Kiểm tra sự có mặt của phần tử trong tuple:
```python
my_tuple = (1, 2, 3, 4, 5)
print(3 in my_tuple)        # Output: True
print(6 in my_tuple)        # Output: False
```

Gộp tuple:
```python
tuple1 = (1, 2, 3)
tuple2 = (4, 5, 6)
merged_tuple = tuple1 + tuple2
print(merged_tuple)   
```

Unpacking tuple:
```python
my_tuple = (1, 2, 3)
a, b, c = my_tuple
print(a)                   # Output: 1
print(b)                   # Output: 2
print(c)                   # Output: 3 
```

Sử dụng tuple như một key trong dictionary:
```python
my_dict = {('John', 25): 'Student', ('Jane', 30): 'Teacher'}
print(my_dict[('John', 25)])   # Output: 'Student'
```

## Set và một số thao tác cơ bản với set

Trong Python, set là một kiểu dữ liệu dùng để lưu trữ một tập hợp các phần tử duy nhất và không có thứ tự. Dưới đây là một số thao tác phổ biến với set trong Python:

Khởi tạo set:
```python
my_set = set()                          # Set rỗng
my_set = {1, 2, 3}                       # Set chứa các số nguyên
my_set = {'apple', 'banana', 'orange'}   # Set chứa các chuỗi
```

Thêm phần tử vào set:
```python
my_set = {1, 2, 3}
my_set.add(4)               # Thêm phần tử 4 vào set
print(my_set)               # Output: {1, 2, 3, 4}
```

Xóa phần tử khỏi set:
```python
my_set = {1, 2, 3, 4, 5}
my_set.remove(3)            # Xóa phần tử có giá trị 3
print(my_set)               # Output: {1, 2, 4, 5}
```

Kiểm tra sự có mặt của phần tử trong set:
```python
my_set = {1, 2, 3, 4, 5}
print(3 in my_set)          # Output: True
print(6 in my_set)          # Output: False
```

Độ dài của set:
```python
my_set = {1, 2, 3, 4, 5}
length = len(my_set)
print(length)               # Output: 5
```

Gộp hai set:
```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
merged_set = set1.union(set2)
print(merged_set)           # Output: {1, 2, 3, 4, 5}
```

Giao của hai set:
```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
intersection_set = set1.intersection(set2)
print(intersection_set)     # Output: {3}
```

Phần tử khác nhau giữa hai set:
```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
difference_set = set1.difference(set2)
print(difference_set)       # Output: {1, 2}
```

Kiểm tra set con và set cha:
```python
set1 = {1, 2, 3}
set2 = {1, 2, 3, 4, 5}
print(set1.issubset(set2))  # Output: True
print(set2.issuperset(set1))# Output: True
```

Xóa toàn bộ phần tử trong set:
```python
my_set = {1, 2, 3, 4, 5}
my_set.clear()
print(my_set)              # Output: set()
```

## Boolean trong Python

Trong Python, boolean là một kiểu dữ liệu logic đơn giản chỉ có hai giá trị: True (đúng) và False (sai). Boolean thường được sử dụng trong các biểu thức điều kiện, vòng lặp, và các phép toán logic. Dưới đây là một số điểm cơ bản về boolean trong Python:

### Khai báo biến boolean:
```python
x = True
y = False
```

### Kết quả của các phép so sánh và phép toán logic:

#### Phép so sánh: Trả về giá trị boolean True hoặc False.
```python
a = 5
b = 3
print(a > b)     # Output: True
print(a == b)    # Output: False
```

#### Phép toán logic: Kết quả của các phép toán logic là giá trị boolean True hoặc False.
```python
p = True
q = False
print(p and q)   # Output: False (Phép AND)
print(p or q)    # Output: True (Phép OR)
print(not p)     # Output: False (Phép NOT)
```

#### Kết quả của các phép so sánh và phép toán logic có thể được gán trực tiếp vào biến boolean:
```python
a = 5
b = 3
c = (a > b)        # Gán kết quả của phép so sánh vào biến c
print(c)           # Output: True
```

#### Sử dụng boolean trong câu lệnh điều kiện:
```python
x = 10
if x > 5:
    print("x lớn hơn 5")   # Output: x lớn hơn 5
else:
    print("x không lớn hơn 5")
```

#### Sử dụng boolean trong vòng lặp:
```python
i = 0
while i < 5:
    print(i)
    i += 1
```

#### Sử dụng boolean trong hàm điều kiện:
```python
def is_even(n):
    return n % 2 == 0

print(is_even(4))    # Output: True
print(is_even(7))    # Output: False
```

Boolean rất quan trọng trong việc kiểm tra và quyết định điều kiện trong lập trình, giúp thực hiện các phân nhánh và kiểm soát luồng chương trình.

## Cấu trúc rẽ nhánh `if` trong Python

Câu lệnh `if` trong Python được sử dụng để thực hiện các câu lệnh khác nhau dựa trên một điều kiện logic. Nếu điều kiện là đúng (True), các câu lệnh bên trong khối `if` sẽ được thực hiện. Nếu điều kiện là sai (False), các câu lệnh bên trong khối `if` sẽ được bỏ qua và chương trình sẽ tiếp tục thực hiện các câu lệnh tiếp theo sau khối `if`.

Cú pháp của câu lệnh `if` trong Python như sau:
```python
if condition:
    # Các câu lệnh được thực hiện nếu condition là đúng
else:
    # Các câu lệnh được thực hiện nếu condition là sai
```

`condition` là biểu thức logic đưa ra điều kiện cần kiểm tra. Nếu giá trị của `condition` là True, khối `if` sẽ được thực thi. Nếu `condition` là False, chương trình sẽ bỏ qua khối `if` và thực hiện các câu lệnh tiếp theo sau khối `if`.

Câu lệnh `else` là tùy chọn và chỉ được sử dụng khi bạn muốn xử lý một khối câu lệnh khác khi điều kiện là sai.

Ví dụ đơn giản về câu lệnh `if`:
```python
x = 10

if x > 5:
    print("x lớn hơn 5")   # Nếu x > 5, câu lệnh này được thực hiện
else:
    print("x không lớn hơn 5")   # Nếu x <= 5, câu lệnh này được thực hiện
```

Output sẽ là:
```python
x lớn hơn 5
```

Trong ví dụ này, nếu x lớn hơn 5, câu lệnh `print("x lớn hơn 5")` sẽ được thực thi. Ngược lại, nếu x không lớn hơn 5, câu lệnh `print("x không lớn hơn 5")` sẽ được thực thi.

## Từ khóa `in` trong Python

Trong Python, từ khóa `in` được sử dụng trong một số tình huống khác nhau:

### Phép toán kiểm tra thành viên (Membership Operators):

#### `in`: Kiểm tra xem một giá trị có tồn tại trong một chuỗi, danh sách, tuple, hoặc set hay không. Trả về giá trị boolean True nếu giá trị tồn tại và False nếu không tồn tại.
```python
my_string = "Hello, World!"
print("o" in my_string)       # Output: True
print("abc" in my_string)     # Output: False
```

#### `not in`: Kiểm tra xem một giá trị không tồn tại trong một chuỗi, danh sách, tuple, hoặc set. Trả về giá trị boolean True nếu giá trị không tồn tại và False nếu tồn tại.
```python
my_list = [1, 2, 3, 4, 5]
print(6 not in my_list)       # Output: True
print(3 not in my_list)       # Output: False
```

### Vòng lặp `for`: `in` được sử dụng để lặp qua các phần tử trong một chuỗi, danh sách, tuple, hoặc set.
```python
my_list = [1, 2, 3, 4, 5]
for item in my_list:
    print(item)
```

## Vòng lặp trong Python

Trong Python, có hai loại vòng lặp chính là vòng lặp `for` và vòng lặp `while`, được sử dụng để lặp qua một tập hợp các giá trị hoặc thực hiện một khối lệnh cho đến khi một điều kiện không còn đúng.

### Vòng lặp `for`

Vòng lặp `for` được sử dụng để lặp qua một tập hợp các giá trị cụ thể, chẳng hạn như danh sách, chuỗi, tuple hoặc set. Ví dụ sau minh họa cú pháp và cách sử dụng vòng lặp `for`:
```python
fruits = ["apple", "banana", "orange"]
for fruit in fruits:
    print(fruit)
```

Output sẽ là:
```python
apple
banana
orange
```

Trong ví dụ này, mỗi phần tử trong danh sách `fruits` được gán vào biến `fruit`, và khối lệnh bên trong vòng lặp `for` được thực thi cho mỗi giá trị của `fruit`.

### Vòng lặp `while`

Vòng lặp `while` được sử dụng để thực hiện một khối lệnh cho đến khi một điều kiện không còn đúng. Ví dụ sau minh họa cú pháp và cách sử dụng vòng lặp `while`:
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

Output sẽ là:
```python
0
1
2
3
4
```

Trong ví dụ này, khối lệnh bên trong vòng lặp `while` sẽ được thực hiện cho đến khi `count` không còn nhỏ hơn 5.

Trong cả hai loại vòng lặp, bạn có thể sử dụng các câu lệnh điều kiện như `break` để thoát khỏi vòng lặp hoặc `continue` để bỏ qua các lần lặp hiện tại và tiếp tục vòng lặp tiếp theo.

## List comprehension trong Python

List comprehension là một cú pháp trong Python cho phép tạo nhanh một list mới từ một list hiện có hoặc từ một biểu thức. Nó cung cấp cách ngắn gọn và mạnh mẽ để xử lý và biến đổi các phần tử trong list một cách linh hoạt.

Cú pháp chung của list comprehension như sau:
```python
new_list = [expression for item in iterable if condition]
```

Trong đó:

- `new_list` là list mới được tạo ra.
- `expression` là biểu thức mà bạn muốn áp dụng cho mỗi phần tử trong `iterable` (có thể là biến hoặc biểu thức phức tạp).
- `item` là biến đại diện cho từng phần tử trong `iterable`.
- `iterable` là một tập hợp dữ liệu có thể lặp qua, chẳng hạn như list, tuple hoặc set.
- `if condition` (tùy chọn) là điều kiện để lọc các phần tử. Chỉ những phần tử thoả mãn điều kiện sẽ được chọn vào list mới.

Một số ví dụ về list comprehension

Tạo một list mới bằng cách nhân mỗi phần tử trong list hiện có với 2:
```python
numbers = [1, 2, 3, 4, 5]
new_numbers = [x * 2 for x in numbers]
print(new_numbers)  # Output: [2, 4, 6, 8, 10]
```

Tạo một list mới chứa các số chẵn từ 1 đến 10:
```python
even_numbers = [x for x in range(1, 11) if x % 2 == 0]
print(even_numbers)  # Output: [2, 4, 6, 8, 10]
```

Tạo một list mới chứa các từ độ dài khác nhau từ một list chuỗi:
```python
words = ["hello", "world", "python", "list", "comprehension"]
lengths = [len(word) for word in words]
print(lengths)  # Output: [5, 5, 6, 4, 13]
```

`List comprehension` là một công cụ mạnh mẽ và tiện lợi trong Python, giúp viết mã ngắn gọn và dễ đọc trong việc xử lý list.

## Dictionary trong Python

Dictionary(từ điển) trong Python là một cấu trúc dữ liệu mạnh mẽ được sử dụng để lưu trữ và quản lý các cặp khóa-giá trị không theo thứ tự. Dictionary được xác định bởi cặp dấu ngoặc nhọn `{}` và các cặp khóa-giá trị được phân tách bằng dấu hai chấm `:`

Các đặc điểm chính của dictionary trong Python bao gồm:

- Khóa (key): Là giá trị không thay đổi và phải là duy nhất trong mỗi dictionary. Khóa giúp xác định giá trị tương ứng trong dictionary.
- Giá trị (value): Là giá trị tương ứng với mỗi khóa trong dictionary. Giá trị có thể là bất kỳ kiểu dữ liệu nào, bao gồm số, chuỗi, list, tuple, dictionary, và nhiều hơn nữa.

Dưới đây là một số ví dụ về cách tạo và làm việc với dictionary trong Python:

Tạo dictionary:
```python
person = {"name": "John", "age": 25, "city": "New York"}
```

Truy cập giá trị trong dictionary bằng khóa:
```python
print(person["name"])     # Output: John
print(person["age"])      # Output: 25
```

Thay đổi giá trị trong dictionary:
```python
person["age"] = 26
print(person["age"])      # Output: 26
```

Thêm một cặp khóa-giá trị mới vào dictionary:
```python
person["occupation"] = "Engineer"
print(person)             # Output: {'name': 'John', 'age': 26, 'city': 'New York', 'occupation': 'Engineer'}
```

Xóa một cặp khóa-giá trị trong dictionary bằng khóa:
```python
del person["city"]
print(person)             # Output: {'name': 'John', 'age': 26, 'occupation': 'Engineer'}
```

Duyệt qua các khóa và giá trị trong dictionary bằng vòng lặp:
```python
for key in person:
    print(key, person[key])
```

Output:
```python
name John
age 26
occupation Engineer
```

Dictionary là một cấu trúc dữ liệu mạnh mẽ và linh hoạt trong Python, cho phép lưu trữ, truy cập và thay đổi dữ liệu dễ dàng dựa trên khóa.

##  Destructuring variables

Trong Python, việc destructuring variables là một kỹ thuật cho phép gán giá trị của các phần tử trong một cấu trúc dữ liệu (như tuple, list, dictionary) cho các biến riêng lẻ một cách đồng thời. Điều này giúp truy cập và sử dụng các phần tử của cấu trúc dữ liệu trở nên dễ dàng hơn.

Dưới đây là một số ví dụ về cách sử dụng destructuring variables trong Python:

Destructuring tuple:
```python
point = (3, 4)
x, y = point
print(x)  # Output: 3
print(y)  # Output: 4
```

Destructuring list:
```python
numbers = [1, 2, 3]
a, b, c = numbers
print(a)  # Output: 1
print(b)  # Output: 2
print(c)  # Output: 3
```

Destructuring dictionary:
```python
person = {"name": "John", "age": 25}
name, age = person.values()
print(name)  # Output: John
print(age)  # Output: 25
```

Destructuring trong vòng lặp:
```python
coordinates = [(1, 2), (3, 4), (5, 6)]
for x, y in coordinates:
    print(f"X: {x}, Y: {y}")
```

Output:
```python
X: 1, Y: 2
X: 3, Y: 4
X: 5, Y: 6
```

Ignoring values:
```python
numbers = [1, 2, 3, 4, 5]
a, _, c, _, e = numbers
print(a)  # Output: 1
print(c)  # Output: 3
print(e)  # Output: 5
# Trong ví dụ này, dấu gạch dưới _ được sử dụng để bỏ qua giá trị không cần thiết.
```

Destructuring variables là một tính năng mạnh mẽ trong Python giúp làm cho mã nguồn dễ đọc hơn và giảm số lượng các câu lệnh gán giá trị. Nó cung cấp một cách thuận tiện để truy cập các phần tử của cấu trúc dữ liệu và gán chúng cho các biến riêng lẻ.

## `*` trong Python

Trong Python, dấu `*`(asterisk) có một số ý nghĩa và sử dụng khác nhau. Dưới đây là một số trường hợp phổ biến mà dấu `*` được sử dụng trong Python:

- Giải nén(unpacking):
  
    Dấu `*` có thể được sử dụng để giải nén các cấu trúc dữ liệu như list, tuple hoặc set thành các phần tử riêng lẻ. Điều này giúp truy cập và sử dụng các phần tử trong cấu trúc dữ liệu dễ dàng hơn.
    ```python
    numbers = [1, 2, 3, 4, 5]
    a, *b, c = numbers
    print(a)  # Output: 1
    print(b)  # Output: [2, 3, 4]
    print(c)  # Output: 5
    ```
    Trong ví dụ này, biến `a` sẽ nhận giá trị đầu tiên, biến `c` sẽ nhận giá trị cuối cùng và biến `b` sẽ nhận tất cả các giá trị còn lại trong list.


- Truyền đối số(arguments):
    
  Dấu `*` có thể được sử dụng để truyền đối số trong một hàm. Khi sử dụng dấu `*`, các đối số được truyền vào sẽ được gom lại thành một tuple.
    ```python
    def my_function(*args):
        for arg in args:
            print(arg)
    
    my_function(1, 2, 3)  # Output: 1 2 3
    ```
    Trong ví dụ này, các đối số 1, 2, 3 được gom lại thành một tuple args và được truyền vào hàm `my_function`


- Truyền đối số laf dictionary(keyword arguments):

    Dấu `*` có thể được sử dụng để truyền đối số là dictionary trong một hàm. Khi sử dụng dấu `*`, các đối số từ điển sẽ được gom lại thành một dictionary.
    ```python
    def my_function(**kwargs):
        for key, value in kwargs.items():
            print(key, value)
    
    my_function(name="John", age=25)  # Output: name John, age 25
    ```
    Trong ví dụ này, các đối số dictionary name="John", age=25 được gom lại thành một dictionary kwargs và được truyền vào hàm `my_function`


- Phép nhân:

    Dấu `*` có thể được sử dụng để nhân số lần lặp của một chuỗi.
    ```python
    word = "Hello"
    repeated_word = word * 3
    print(repeated_word)  # Output: HelloHelloHello
    ```

## Function trong Python

Trong Python, một function(hàm) là một khối mã được đặt tên và thực hiện một tác vụ cụ thể khi được gọi. Hàm giúp tái sử dụng mã, tạo ra các khối mã độc lập và tăng tính tổ chức của chương trình.

Để định nghĩa một hàm trong Python, ta sử dụng cú pháp sau:
```python
def function_name(parameters):
    """Docstring - mô tả chức năng của hàm (tùy chọn)"""
    # Mã thực hiện chức năng của hàm
    return value  # (tùy chọn)
```

Trong đó:

- `function_name` là tên của hàm, nên được đặt theo quy tắc đặt tên biến trong Python.
- `parameters` là danh sách các tham số đầu vào của hàm, được phân tách bằng dấu phẩy (nếu có).
- `Docstring` (tùy chọn) là một chuỗi dùng để mô tả chức năng và cách sử dụng của hàm.
- `Mã` trong khối thực hiện chức năng của hàm.
- `return` (tùy chọn) được sử dụng để trả về giá trị từ hàm.

Dưới đây là một ví dụ đơn giản về một hàm tính tổng hai số:
```python
def add_numbers(a, b):
    """Tính tổng hai số."""
    return a + b

result = add_numbers(2, 3)
print(result)  # Output: 5
```

Trong ví dụ này, hàm `add_numbers` nhận hai tham số `a` và `b`, và trả về tổng của chúng. Khi gọi hàm `add_numbers(2, 3)`, giá trị 2 được gán cho tham số `a` và 3 được gán cho tham số `b`, và kết quả tổng 5 được trả về và gán cho biến `result`.

Hàm có thể có hoặc không có tham số đầu vào và có thể trả về hoặc không trả về giá trị.

## Lambda function trong Python

Lambda function(hàm lambda) trong Python là một loại hàm vô danh(anonymous function) được định nghĩa bằng cú pháp ngắn gọn. Một lambda function có thể chứa một biểu thức duy nhất và không yêu cầu câu lệnh return, nó tự động trả về giá trị của biểu thức đó.

Cú pháp để định nghĩa một lambda function như sau:
```python
lambda arguments: expression
```

Trong đó:
- `arguments` là danh sách các tham số của lambda function, được phân tách bằng dấu phẩy (nếu có).
- `expression` là biểu thức được thực hiện bởi lambda function.

Dưới đây là một ví dụ về cách sử dụng lambda function:
```python
add = lambda x, y: x + y
result = add(2, 3)
print(result)  # Output: 5
```

Trong ví dụ này, lambda function add nhận hai tham số `x` và `y`, và trả về tổng của chúng. Khi gọi lambda function `add(2, 3)`, giá trị 2 được gán cho tham số `x`, 3 được gán cho tham số `y`, và kết quả tổng 5 được trả về và gán cho biến `result`.

Lambda function thường được sử dụng trong các tình huống đơn giản khi chỉ cần một hàm nhỏ gọn và không cần đặt tên cho hàm. Các lambda function thường được sử dụng trong kết hợp với các hàm khác như map(), filter(), reduce(), và cú pháp comprehensions (list comprehensions, dictionary comprehensions) để thực hiện các phép biến đổi dữ liệu và lọc dữ liệu một cách nhanh chóng và gọn nhẹ.

## Dictionary comprehension

Dictionary comprehension là một cú pháp trong Python cho phép tạo dictionary (từ điển) một cách nhanh chóng và dễ dàng. Nó cho phép bạn xác định một biểu thức và các cặp key-value tương ứng trong một cấu trúc dữ liệu.

Cú pháp chung của dictionary comprehension như sau:
```python
{key_expression: value_expression for element in iterable if condition}
```

Trong đó:
- `key_expression` là biểu thức để xác định key cho mỗi phần tử trong `iterable`.
- `value_expression` là biểu thức để xác định value cho mỗi phần tử trong `iterable`.
- `element` là mỗi phần tử trong `iterable`.
- `iterable` là một cấu trúc dữ liệu có thể lặp qua như list, tuple hoặc set.
- `condition` (tùy chọn) là một biểu thức điều kiện để lọc các phần tử trong `iterable`.

Dưới đây là một ví dụ minh họa về cách sử dụng dictionary comprehension:
```python
numbers = [1, 2, 3, 4, 5]
squared_dict = {num: num ** 2 for num in numbers}
print(squared_dict)  # Output: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

Trong ví dụ này, chúng ta sử dụng dictionary comprehension để tạo một dictionary mới có key là các số trong list numbers và value là bình phương của từng số. Kết quả được lưu trong biến squared_dict.

Dictionary comprehension cung cấp một cách ngắn gọn và rõ ràng để tạo dictionary từ dữ liệu có sẵn. Nó thường được sử dụng để biến đổi dữ liệu từ một cấu trúc dữ liệu sang cấu trúc dữ liệu khác, hoặc để tạo dictionary dựa trên các điều kiện lọc.

## Object-Oriented Programming trong Python

OOP(Object-Oriented Programming) trong Python là một phương pháp lập trình cho phép tổ chức mã thành các đối tượng riêng biệt, mỗi đối tượng có thuộc tính và phương thức riêng. OOP tạo ra một mô hình lập trình dựa trên các khái niệm như lớp (class), đối tượng (object), kế thừa (inheritance), đa hình (polymorphism) và đóng gói (encapsulation).

Trong Python, để định nghĩa một lớp(class), bạn sử dụng từ khóa `class`. Một lớp định nghĩa các thuộc tính (biến) và phương thức (hàm) của đối tượng.

Dưới đây là một ví dụ đơn giản về một lớp Person trong Python:
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        print(f"Hello, my name is {self.name} and I am {self.age} years old.")

# Tạo một đối tượng từ lớp Person
person = Person("John", 25)
person.greet()
# Output: Hello, my name is John and I am 25 years old.
```

Trong ví dụ này:
- Lớp Person có hai thuộc tính là `name` và `age`, được khởi tạo bằng phương thức `__init__`(constructor).
- Phương thức `greet` xuất ra thông tin về tên và tuổi của đối tượng.
- Đối tượng `person` được tạo ra từ lớp `Person` và sử dụng phương thức `greet` để in ra thông tin của nó.

### Phương thức `__str__` 

Phương thức `__str__` được sử dụng để định nghĩa một chuỗi cho một đối tượng. Nó được gọi khi bạn sử dụng hàm `str()` hoặc hàm `print()` để chuyển đối tượng thành chuỗi.
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __str__(self):
        return f"Person(name={self.name}, age={self.age})"

person = Person("John", 25)
print(person)  # Output: Person(name=John, age=25)
```

Trong ví dụ này, phương thức `__str__` trả về một chuỗi biểu diễn của đối tượng Person.

### Phương thức `__repr__`

Phương thức `__repr__` được sử dụng để định nghĩa một biểu diễn chuỗi chính xác của một đối tượng. Nó được gọi khi bạn sử dụng hàm `repr()` để chuyển đối tượng thành chuỗi hoặc khi bạn gọi đối tượng trực tiếp mà không sử dụng hàm `print()`.
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __repr__(self):
        return f"Person(name={self.name}, age={self.age})"

person = Person("John", 25)
print(repr(person))  # Output: Person(name=John, age=25)
```

Trong ví dụ này, phương thức `__repr__` trả về một chuỗi biểu diễn chính xác của đối tượng `Person`.

Phương thức `__str__` và `__repr__` có vai trò quan trọng trong việc debug và hiển thị thông tin về đối tượng trong quá trình phát triển. Tùy thuộc vào mục đích sử dụng, bạn có thể chỉ định cách hiển thị đối tượng của mình thông qua việc định nghĩa phương thức `__str__` và `__repr__` tương ứng.

## `@classmethod` trong Python

`@classmethod` là một decorator trong Python được sử dụng để định nghĩa một phương thức lớp (class method). Phương thức lớp là một phương thức thuộc về lớp chứ không phải thuộc về các đối tượng của lớp đó. Phương thức lớp có thể truy cập và làm việc với các thuộc tính lớp và thực hiện các hoạt động liên quan đến lớp chứ không phải đối tượng.

Để định nghĩa một phương thức lớp, bạn sử dụng decorator @classmethod trước phương thức. Phương thức lớp nhận tham số đầu tiên là cls (viết tắt của class), thể hiện chính của lớp đó.

Dưới đây là một ví dụ minh họa về cách sử dụng @classmethod:
```python
class Person:
    population = 0

    def __init__(self, name):
        self.name = name
        Person.population += 1

    @classmethod
    def get_population(cls):
        return cls.population

# Sử dụng phương thức lớp
print(Person.get_population())  # Output: 0

person1 = Person("John")
print(Person.get_population())  # Output: 1

person2 = Person("Alice")
print(Person.get_population())  # Output: 2
```

Trong ví dụ này, chúng ta có lớp `Person` đại diện cho một người. Thuộc tính `population là một thuộc tính lớp, đếm số lượng đối tượng được tạo ra từ lớp `Person`.

Phương thức `get_population()` là một phương thức lớp được định nghĩa bằng cách sử dụng decorator `@classmethod`. Nó trả về giá trị của thuộc tính `population` của lớp.

Bằng cách sử dụng phương thức lớp `get_population()`, chúng ta có thể truy cập và lấy giá trị của thuộc tính `population` mà không cần tạo đối tượng từ lớp `Person`.

Phương thức lớp là một công cụ hữu ích trong việc làm việc với các thuộc tính lớp và thực hiện các hoạt động liên quan đến lớp mà không cần tạo các đối tượng của lớp đó.

## `@staticmethod` trong Python

`@staticmethod` là một decorator trong Python được sử dụng để định nghĩa một phương thức tĩnh (static method). Phương thức tĩnh là một phương thức không liên kết với bất kỳ đối tượng cụ thể nào của lớp và không có tham số đầu tiên đặc biệt như `self` hoặc `cls`.

Để định nghĩa một phương thức tĩnh, bạn sử dụng decorator `@staticmethod` trước phương thức. Phương thức tĩnh không nhận bất kỳ tham số đầu vào đặc biệt nào (như `self` hoặc `cls`).

Dưới đây là một ví dụ minh họa về cách sử dụng `@staticmethod`:
```python
class MathUtils:
    @staticmethod
    def add(a, b):
        return a + b

    @staticmethod
    def multiply(a, b):
        return a * b

# Gọi phương thức tĩnh mà không cần tạo đối tượng
sum_result = MathUtils.add(2, 3)
print(sum_result)  # Output: 5

product_result = MathUtils.multiply(4, 5)
print(product_result)  # Output: 20
```

Trong ví dụ này, chúng ta có lớp `MathUtils` chứa hai phương thức tĩnh là `add()` và `multiply()`.

Phương thức tĩnh `add()` nhận hai tham số `a` và `b` và trả về tổng của chúng.

Phương thức tĩnh `multiply()` nhận hai tham số `a` và `b` và trả về tích của chúng.

Bằng cách sử dụng phương thức tĩnh, chúng ta có thể gọi và sử dụng các phương thức này mà không cần tạo đối tượng từ lớp `MathUtils`. Chúng ta gọi các phương thức trực tiếp từ lớp và truyền các đối số tương ứng.

Phương thức tĩnh làm cho mã của bạn trở nên tổ chức hơn và cho phép bạn thực hiện các tính toán và hoạt động độc lập với đối tượng cụ thể nào đó.

## Object-Oriented Programming trong Python(tính kế thừa - Class inheritance)

Kế thừa(class inheritance) là một khái niệm quan trọng trong lập trình hướng đối tượng, cho phép bạn tạo ra các lớp con(subclass) dựa trên các lớp cha(superclass) đã tồn tại. Kế thừa cho phép lớp con sử dụng lại mã của lớp cha và mở rộng hoặc thay đổi chúng nếu cần.

Trong Python, để tạo một lớp con từ một lớp cha, bạn định nghĩa tên lớp con và sau đó đặt tên lớp cha trong dấu ngoặc đơn sau tên lớp con. Khi lớp con được tạo, nó sẽ kế thừa tất cả các thuộc tính và phương thức của lớp cha.

Dưới đây là một ví dụ về kế thừa lớp trong Python:
```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print("The animal makes a sound.")

class Dog(Animal):
    def speak(self):
        print("The dog barks.")

class Cat(Animal):
    def speak(self):
        print("The cat meows.")

# Tạo đối tượng từ lớp con
dog = Dog("Buddy")
dog.speak()  # Output: The dog barks.

# Tạo đối tượng từ lớp con khác
cat = Cat("Whiskers")
cat.speak()  # Output: The cat meows.
```

Một ví dụ khác về tính kế thừa
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def eat(self):
        print('eat eat eat')

class Student(Person):
    def __init__(self, name, age, student_id):
        super().__init__(name, age)
        self.student_id = student_id

    def learn(self):
        print('learn learn learn')
```

Trong ví dụ này, chúng ta có lớp cha `Animal` đại diện cho một con vật. Lớp cha có một phương thức `speak()` để phát ra âm thanh của con vật.

Lớp con `Dog` và `Cat` được tạo từ lớp cha `Animal`. Cả hai lớp con đều có phương thức `speak()`, nhưng mỗi lớp con có một cách riêng để phát ra âm thanh của nó.

Khi chúng ta tạo đối tượng từ lớp con, nó sẽ kế thừa phương thức `speak()` từ lớp cha, nhưng lớp con có thể ghi đè phương thức này để định nghĩa một hành vi khác.

Kế thừa lớp cho phép tái sử dụng mã, tạo ra mối quan hệ `is-a` giữa các lớp và mở rộng hoặc thay đổi chức năng của lớp cha. Bên cạnh đó, Python cũng hỗ trợ việc kế thừa từ nhiều lớp cha thông qua khái niệm `multiple inheritance`(đa kế thừa).

## Type hinting trong python

Type hinting(gợi ý kiểu dữ liệu) là một tính năng trong Python cho phép bạn gắn nhãn kiểu dữ liệu cho các biến, tham số và giá trị trả về của các phương thức và hàm. Type hinting không ảnh hưởng đến việc thực thi chương trình, nhưng nó cung cấp thông tin về kiểu dữ liệu để giúp trong quá trình phát triển, kiểm tra lỗi và làm cho mã nguồn dễ đọc hơn.

Để sử dụng type hinting trong Python, bạn có thể sử dụng cú pháp của Python 3.6+ và thêm các chú thích kiểu dữ liệu bằng cách sử dụng cú pháp : <kiểu dữ liệu> sau tên biến, tham số hoặc giá trị trả về. Ví dụ:
```python
def add(a: int, b: int) -> int:
    return a + b

result: int = add(5, 3)
print(result)  # Output: 8
```

Trong ví dụ này, chúng ta định nghĩa hàm `add()` có hai tham số `a` và `b`, cả hai đều có kiểu dữ liệu là `int`. Chúng ta sử dụng chú thích kiểu dữ liệu để gợi ý rằng hàm này trả về một giá trị kiểu `int`.

Bằng cách sử dụng type hinting, chúng ta có thể đọc và hiểu rõ hơn về kiểu dữ liệu mà hàm mong đợi và trả về. Nó cũng giúp các công cụ kiểm tra lỗi và IDE hiển thị gợi ý kiểu dữ liệu, hỗ trợ bạn trong quá trình phát triển.

Một số loại dữ liệu thường được sử dụng trong type hinting bao gồm `int`, `float`, `bool`, `str`, `list`, `tuple`, `dict`, và cả các lớp được định nghĩa bởi người dùng. Ngoài ra, bạn cũng có thể sử dụng các kiểu dữ liệu tùy chỉnh hoặc kiểu dữ liệu tùy chọn(optional types) bằng cách sử dụng module typing.

Lưu ý rằng type hinting không bắt buộc và không ảnh hưởng đến việc thực thi chương trình. Nó chỉ là một công cụ hữu ích trong quá trình phát triển để tăng tính rõ ràng và dễ đọc của mã nguồn.

Một ví dụ khác sử dụng type hinting trong `class`
```python
class Document:
    def __init__(self, name):
        self.name = name

class Book:
    def __init__(self, name: str):
        self.name = name

    @classmethod
    def create_document(cls, name: str) -> Document:
        return Document(name)

    @classmethod
    def create_book(cls, name: str) -> "Book":
        return cls(name)
```

Trong ví dụ trên có hai phương thức `@classmethod` là `create_document()` và `create_book()`, đối với phương thức `create_document()` gợi ý kiểu trả về là một đối tượng `Document`, do class `Document` được định nghĩa trước đó rồi nên hoàn toàn có thể sử dụng lớp `Document` là gợi ý. Tuy nhiên với phương thức `create_book()` thì gợi ý kiểu trả về là "Book" do thời điểm khai báo phương thức này lớp Book chưa tồn tại nên Python cho phép người dùng sử dụng dấu "" để định nghĩa gợi  kiểu trả về cho những lớp chưa được định nghĩa

# `import` trong Python

Trong Python, từ khóa `import` được sử dụng để nhập(import) một module hoặc một phần của module vào trong chương trình của bạn. Import cho phép bạn sử dụng mã từ module đã được định nghĩa trước đó hoặc các chức năng, lớp và biến khác mà module cung cấp.

Dưới đây là một số cách sử dụng từ khóa `import` trong Python:

- Import toàn bộ module:
  ```python
  import module_name
  ```

    Ví dụ:
    ```python
    import math
    ```
    Sau khi import module `math`, bạn có thể sử dụng các hàm và hằng số như `math.sin()`, `math.pi` trong chương trình của mình.


- Import một phần của module:
  ```python
  from module_name import item_name
  ```

    Ví dụ:
    ```python
    from math import sqrt
    ```
    Sau khi import `sqrt` từ module `math`, bạn có thể sử dụng `sqrt()` trực tiếp mà không cần sử dụng tên module.


- Import toàn bộ module nhưng sử dụng tên định danh khác:
  ```python
  import module_name as alias_name
  ```

    Ví dụ:
    ```python
    import math as m
    ```
    Sau khi import module `math` và đặt tên định danh là `m`, bạn có thể sử dụng các hàm và hằng số bằng cách gọi `m.sin()`, `m.pi`.


- Import tất cả các thành phần của một module:
  ```python
  from module_name import *
  ```
  
    Ví dụ:
    ```python
    from math import *
    ```
    Lưu ý: Việc sử dụng import * không được khuyến khích trong các chương trình lớn hoặc trong trường hợp có nhiều module có cùng tên thành phần.


Ngoài ra, bạn cũng có thể import module từ các gói (packages) hoặc import các biến, lớp, hàm từ module con bên trong một gói. Cú pháp sử dụng import trong các trường hợp này tương tự như trên.

Import giúp tái sử dụng mã, tăng tính sắp xếp và quản lý mã nguồn trong các dự án lớn. Bằng cách import các module, bạn có thể sử dụng các tính năng và chức năng đã được xây dựng trước đó, tiết kiệm thời gian và công sức trong quá trình lập trình.

## Errors và xử lý Errors trong Python

Trong Python, có hai loại lỗi phổ biến: lỗi cú pháp(syntax errors) và lỗi thực thi(runtime errors). Dưới đây là mô tả về hai loại lỗi này:

- Lỗi cú pháp(Syntax errors): Được xảy ra khi bạn vi phạm cú pháp ngôn ngữ Python. Điều này có thể xảy ra khi bạn viết mã không đúng cú pháp hoặc không đóng các dấu ngoặc, dấu ngoặc vuông, hay dấu nháy đúng cách. Khi gặp lỗi cú pháp, Python sẽ thông báo cho bạn vị trí chính xác của lỗi và loại lỗi mà nó gặp phải. Bạn cần xem xét lại mã nguồn và sửa lỗi cú pháp trước khi chạy chương trình. Ví dụ:
  ```python
  print("Hello, world!"
  ```
  Lỗi cú pháp trong ví dụ trên là việc không đóng dấu ngoặc đơn.


- Lỗi thực thi(Runtime errors): Được xảy ra khi một lỗi xảy ra trong quá trình thực thi chương trình. Các lỗi thực thi có thể bao gồm:
  - Lỗi chia cho 0(ZeroDivisionError): Khi bạn chia một số cho 0.
  - Lỗi tên biến không được định nghĩa(NameError): Khi bạn sử dụng một biến mà không được định nghĩa trước đó.
  - Lỗi truy cập phần tử không tồn tại(IndexError hoặc KeyError): Khi bạn truy cập vào một phần tử không tồn tại trong danh sách hoặc từ điển.
  - Lỗi loại dữ liệu(TypeError): Khi bạn thực hiện các phép toán không hợp lệ giữa các kiểu dữ liệu khác nhau.
  - Và nhiều loại lỗi khác.

  Khi gặp lỗi thực thi, Python sẽ hiển thị traceback(danh sách các lỗi xảy ra) cùng với thông báo lỗi. Bạn cần kiểm tra các thông báo lỗi và traceback để xác định nguyên nhân gây ra lỗi và sửa chúng trong mã nguồn.

### Sử dụng `raise` để ném ra một ngoại lệ

Trong Python, từ khóa `raise` được sử dụng để ném(raise) một ngoại lệ(exception) trong chương trình. Bằng cách sử dụng `raise`, bạn có thể tạo ra và ném các đối tượng ngoại lệ để báo cáo và xử lý các tình huống đặc biệt trong mã Python.
```python
def divide(dividend, divisor):
    if divisor == 0:
        raise ZeroDivisionError("Divisor cannot be 0")
    return dividend / divisor

divide(10, 0)
```

Khi thực hiện chạy đoạn code trên, chương trình sẽ trả về một ngoại lệ như sau:
```python
Traceback (most recent call last):
  File "C:\Users\trunglq\PycharmProjects\HelloWorld\main.py", line 6, in <module>
    divide(10, 0)
  File "C:\Users\trunglq\PycharmProjects\HelloWorld\main.py", line 3, in divide
    raise ZeroDivisionError("Divisor cannot be 0")
ZeroDivisionError: Divisor cannot be 0
```

Để có thể bắt và xử lý được các ngoại lệ trong Python cung cấp một cấu trúc được gọi là `try-except`

### Sử dụng `try-except` để xử lý ngoại lệ

Trong Python, cấu trúc `try-except` được sử dụng để xử lý các ngoại lệ(exceptions) trong chương trình. Bằng cách sử dụng `try-except`, bạn có thể bắt các ngoại lệ xảy ra trong khối mã và thực hiện các xử lý phù hợp để tránh dừng chương trình hoặc hiển thị thông báo lỗi không mong muốn.

Dưới đây là cú pháp của cấu trúc `try-except`:
```python
try:
    # Mã có thể gây ra ngoại lệ
    # ...
except ExceptionType1:
    # Xử lý cho ngoại lệ ExceptionType1
    # ...
except ExceptionType2:
    # Xử lý cho ngoại lệ ExceptionType2
    # ...
except:
    # Xử lý cho các ngoại lệ không xác định trước
    # ...
finally:
    # Khối mã được thực thi luôn, dù có ngoại lệ hay không
    # ...
```

Giải thích chi tiết các phần trong cấu trúc `try-except`:
- Mã trong khối `try` là nơi bạn đặt các dòng mã có thể gây ra ngoại lệ.
- Sau khối `try`, bạn có thể định nghĩa một hoặc nhiều khối `except` để xử lý các loại ngoại lệ khác nhau. Mỗi khối `except` chỉ được thực thi nếu một ngoại lệ có kiểu tương ứng xảy ra trong khối `try`.
- Nếu không xác định kiểu ngoại lệ cụ thể trong khối `except`, bạn có thể sử dụng khối `except` cuối cùng mà không có tên ngoại lệ. Điều này sẽ xử lý bất kỳ ngoại lệ nào không được xác định trước.
- Khối `finally` là tùy chọn và được đặt sau các khối `except`. Mã trong khối `finally` sẽ được thực thi luôn, bất kể có ngoại lệ hay không. Điều này đảm bảo rằng các tài nguyên được giải phóng hoặc các hành động cuối cùng được thực hiện dù có ngoại lệ hay không.

Ví dụ:
```python
try:
    x = 10 / 0  # Gây lỗi chia cho 0
    print("This line will not be executed.")
except ZeroDivisionError:
    print("Cannot divide by zero.")
except Exception as e:
    print("An error occurred:", e)
finally:
    print("Finally block is always executed.")
```

Trong ví dụ trên, chúng ta cố tình chia số 10 cho 0, gây ra lỗi `ZeroDivisionError`. Trong khối `try`, lỗi này sẽ được bắt và được xử lý bằng cách in ra một message lỗi mà người dùng định nghĩa

### Ngoại lệ do người dùng tự định nghĩa

Trong Python, ta có thể tạo ra các ngoại lệ tùy chỉnh(custom exceptions) bằng cách định nghĩa các lớp mới kế thừa từ lớp Exception hoặc các lớp ngoại lệ khác có sẵn trong Python. Điều này cho phép bạn tạo ra các ngoại lệ có ý nghĩa đặc biệt và xử lý chúng một cách tùy chỉnh trong chương trình.

Dưới đây là một ví dụ về việc tạo ra một lớp ngoại lệ tùy chỉnh:
```python
class CustomException(Exception):
    def __init__(self, message):
        self.message = message
        super().__init__(self.message)

try:
    raise CustomException("This is a custom exception.")
except CustomException as e:
    print("Exception caught:", e.message)
```

Trong ví dụ trên, chúng ta định nghĩa một lớp `CustomException` kế thừa từ lớp `Exception`. Lớp này có một phương thức `__init__` để khởi tạo thông báo của ngoại lệ.

Sau đó, chúng ta sử dụng từ khóa `raise` để ném một đối tượng `CustomException` với thông báo tương ứng. Trong khối `except`, chúng ta bắt ngoại lệ `CustomException` và in thông báo lỗi.

## First-class functions

Trong Python, first-class functions(hàm có cấp độ nhất định) đề cập đến việc xem hàm như là một loại đối tượng dữ liệu, nghĩa là hàm có thể được gán cho biến, truyền như tham số cho hàm khác, và được trả về từ một hàm khác. Điều này cho phép xử lý hàm như một đối tượng linh hoạt và tiện lợi trong Python.

Dưới đây là một số ví dụ về first-class functions trong Python:

Gán hàm cho biến:
```python
def greet(name):
    print("Hello, " + name + "!")

hello = greet
hello("Alice")  # Gọi hàm thông qua biến
```

Truyền hàm như tham số cho hàm khác:
```python
def square(x):
    return x ** 2

def process_numbers(numbers, callback):
    for number in numbers:
        result = callback(number)
        print(result)

numbers = [1, 2, 3, 4, 5]
process_numbers(numbers, square)  # Truyền hàm square như một tham số
```

Trả về hàm từ một hàm khác:
```python
def create_multiplier(n):
    def multiplier(x):
        return n * x
    return multiplier

double = create_multiplier(2)  # Trả về hàm multiplier với n = 2
print(double(5))  # Kết quả: 10
```

First-class functions rất hữu ích trong việc xây dựng các hàm cao cấp, như hàm bậc cao(higher-order functions), decorator và xử lý sự kiện(event handling). Chúng cung cấp một cách linh hoạt để làm việc với hàm và tạo ra mã nguồn mạnh mẽ và dễ đọc.

## `nested function` hoặc `inner function`

Trong Python, bạn có thể định nghĩa một hàm bên trong một hàm khác. Được gọi là hàm lồng nhau(nested function) hoặc hàm nội tại(inner function), hàm bên trong có thể truy cập các biến và tham số của hàm ngoài và có phạm vi chỉ tồn tại trong hàm ngoài.

Dưới đây là một ví dụ về việc định nghĩa hàm bên trong hàm trong Python:
```python
def outer_function():
    message = "Hello"

    def inner_function():
        print(message)

    inner_function()

outer_function()  # Kết quả: Hello
```

Trong ví dụ trên, chúng ta định nghĩa hàm `outer_function()`, trong đó có một hàm bên trong được gọi là `inner_function()`. Hàm `inner_function()` có thể truy cập biến `message` trong hàm ngoài và in ra giá trị của nó.

Lưu ý rằng hàm bên trong chỉ có thể được gọi và truy cập trong phạm vi của hàm ngoài. Nếu bạn cố gắng gọi hàm bên trong từ bên ngoài, bạn sẽ gặp lỗi.

Hàm bên trong có thể được sử dụng để tạo ra mã nguồn sạch hơn và giảm tình trạng trùng lặp mã. Nó cũng hữu ích trong việc ẩn các chi tiết triển khai bên trong hàm và giới hạn phạm vi của các biến để tránh xung đột với các biến bên ngoài.

## Decorators trong Python

Decorator trong Python là một cú pháp đặc biệt cho phép bạn bao bọc một hàm hoặc một lớp bằng một hàm khác để mở rộng hoặc thay đổi hành vi của hàm/lớp gốc mà không cần thay đổi mã nguồn của hàm/lớp đó. Decorator cho phép bạn áp dụng chức năng bổ sung hoặc xử lý trước và sau khi hàm/lớp được gọi.

Cú pháp để sử dụng decorator trong Python là sử dụng ký hiệu `@` trước tên decorator, và đặt decorator trực tiếp trước định nghĩa của hàm hoặc lớp.

Dưới đây là một ví dụ đơn giản về việc sử dụng decorator trong Python:
```python
def decorator(func):
    def wrapper():
        print("Before function call")
        func()
        print("After function call")
    return wrapper

@decorator
def say_hello():
    print("Hello, world!")

say_hello()
```

Trong ví dụ trên, chúng ta định nghĩa một decorator là hàm `decorator()`. Hàm này nhận một hàm `func` làm tham số và trả về một hàm mới được gọi là `wrapper()`. `wrapper()` chứa mã để thực hiện xử lý trước và sau khi hàm gốc được gọi.

Sau đó, chúng ta sử dụng decorator bằng cách đặt `@decorator` trước định nghĩa của hàm `say_hello()`. Khi chúng ta gọi `say_hello()`, nó sẽ tự động được bao bọc bởi decorator và mã trong `wrapper()` sẽ được thực thi.

Kết quả của đoạn mã trên sẽ là:
```python
Before function call
Hello, world!
After function call
```

Decorator là một tính năng mạnh mẽ trong Python và được sử dụng rộng rãi trong nhiều tình huống, chẳng hạn như ghi log, đo thời gian thực thi, xử lý ngoại lệ, kiểm tra quyền truy cập, vv.
