<h2 style="text-align: center">Bài tập JS</h2>

##### #1 - Viết hàm isPrime(n) để kiểm tra n có phải là số nguyên tố không?

-   Số nguyên tố là số chỉ chia hết cho 1 và chính nó.
-   Trả về true nếu là số nguyên tố, ngược lại trả về false.
-   Ví dụ:
    -   isPrime(3) --> true
    -   isPrime(4) --> false
    -   isPrime(11) --> true

##### #2 - Viết hàm isPerfectNumber(n) để kiểm tra n có phải là số hoàn hảo hay không?

-   Số hoàn hảo là số mà tổng của tất cả ước số (không tính chính nó, tức từ 1 đến n - 1) bằng chính nó.
-   Trả về true nếu đúng, ngược lại trả về false
-   Ví dụ: 6 = 1 + 2 + 3 (6 là một số hoàn hảo)

> _**Gợi ý:**_ _không nhất thiết phải chạy tới (n - 1) để tìm ra tất cả các ước số của n_

##### #3 - Viết hàm countURLs(str) để đếm số lượng URLs có trong câu.

-   URL có định dạng: protocol://domain.com/path-name
-   URL có thể bắt đầu bằng protocol như: http, https, ws hoặc wss
-   Domain có thể là .com, .com.vn hoặc .vn
-   Phần tên domain phải có ít nhất 3 ký tự, như abc.com, chứ ab.com là không hợp lệ
-   Trả về số lượng URLs tìm thấy trong câu.

##### #4 - Viết hàm getDisplayedAddress(address) để ghép chuỗi từ các thuộc tính của object address thành một chuỗi address hoàn chỉnh

-   Chuỗi trả về có dạng: "address.number address.street, address.ward, address.district, address.city"
-   Lưu ý object address không phải lúc nào cũng có đầy đủ các thông tin trên.

-   Ví dụ:

```js
getDisplayedAddress({
    number: 666,
    street: '3/2',
    ward: 'Ward 11',
    district: '10 District',
    city: 'HCMC',
});
// should return '666 3/2, Ward 11, 10 District, HCMC'

getDisplayedAddress({
    street: '3/2',
    district: '10 District',
});
// should return 'Nguyen Cong Tru, 10 District'
```

##### #5 - Viết hàm fillPath(path, params) để thay thế các chuỗi params trong path bằng các giá trị tương ứng trong object params.

```js
fillPath('/products/:productId', { productId: 123 }); // '/products/123'
fillPath('/categories/:categoryId/products/:productId', {
    categoryId: 1,
    productId: 2,
});
// should return '/categories/1/products/2'

fillPath('/categories/:categoryId/products/:productId', { productId: 2 });
// should return '/categories/:categoryId/products/2'
```

##### #6 - Viết hàm hasTruthy(arr) để kiểm tra xem trong mảng arr có giá trị truthy không?

```js
hasTruthy([]); // false
hasTruthy([false, '']); // false
hasTruthy([false, 123]); // true
```

##### #7 - Viết hàm hasStudent(studentList, studentId) để kiểm tra trong mảng studentList có student nào có id là studentId không?

```js
const studentList = [
    { id: 1, name: 'Nguyễn Văn Tèo' },
    { id: 2, name: 'Lê Thị Tủn' },
];
hasStudent(studentList, 1); // true
hasStudent(studentList, 3); // false
```

##### #8 - Viết hàm hasFreeShip(productList, price) để kiểm tra xem có product nào freeship và giá nhỏ hơn price không?

```js
const productList = [
    { id: 1, name: 'Iphone 16', isFreeShip: false, price: 10200500 },
    { id: 2, name: 'Iphone 16 Pro Max', isFreeShip: true, price: 1500000 },
];
hasF;
```

##### #9 - Viết hàm findProductHavingFreeShip(productList) để tìm ra sản phẩm đầu tiên có free ship.

```js
const productList = [
    { id: 1, name: 'IPhone 5', isFreeShip: false },
    { id: 2, name: 'IPhone X', isFreeShip: true },
    { id: 3, name: 'IPhone 12 Pro', isFreeShip: true },
];
findProductHavingFreeShip(productList);
// { id: 2, name: 'IPhone X', isFreeShip: true }
```

##### #10 - Viết hàm generateNumberInRange(a, b) để tạo ra một mảng các số từ a đến b (có bao gồm a và b)

```js
generateNumberInRange(1, 5); // [1, 2, 3, 4, 5]
generateNumberInRange(5, 7); // [5, 6, 7]
generateNumberInRange(7, 5); // []
```

##### #11 - Viết hàm findAllStudents(studentList) để tìm ra tất cả student có điểm toán nhỏ hơn 5

```js
const studentList = [
    { id: 1, name: 'Alice', math: 9 },
    { id: 2, name: 'Bob', math: 4 },
    { id: 3, name: 'John', math: 0 },
];
findAllStudents(studentList);
// should return the following array:
// [
// { id: 2, name: 'Bob', math: 4 },
// { id: 3, name: 'John', math: 0 },
// ]
```

##### #12 - Viết hàm findAllIphones(productList) để tìm ra tất cả các product có tên chứa chữ iphone (ko phân biệt hoa thường) và vẫn còn hàng trong kho (amount > 0)

```js
const productList = [
    { id: 1, name: 'Luxury IPhone X', amount: 1 },
    { id: 2, name: 'Super Cool iphone 16 Pro', amount: 0 },
    { id: 3, name: 'iphone 20 Pro', amount: 2 },
];
findAllIphones(productList);
// should return the following list:
// [
// { id: 1, name: 'Luxury IPhone X', amount: 1 },
// { id: 3, name: 'iphone 20 Pro', amount: 2 },
// ];
```

##### #13 - Viết hàm calcCartTotal(cartItemList) để tính tổng tiền của giỏ hàng.

```js
const cartItemList = [
    { id: 1, product: { id: 1, price: 50000 }, quantity: 1 },
    { id: 2, product: { id: 2, price: 100000 }, quantity: 2 },
];
calcCartTotal(cartItemList); // 250000 = 50 x 1 + 100000 x 2
```

##### #14 - Viết hàm removeStudentById(studentList, studentId) để remove student có id là studentId ra khỏi mảng studentList và trả về mảng mới.

```js
const studentList = [
    { id: 1, name: 'Alice' },
    { id: 2, name: 'Bob' },
];
removeStudentById(studentList, 1);
// should return:
// [
// { id: 2, name: 'Bob' },
// ]
removeStudentById(studentList, 3);
// should return:
// [
// { id: 1, name: 'Alice' },
// { id: 2, name: 'Bob' },
// ]
```
