# Reverse-The-Number


---

### 🔢 **Problem**

Given a number `N`, print its **reverse**. For example:

* Input: `123` → Output: `321`
* Input: `1200` → Output: `21` (leading zeros are dropped)

---

### 🧠 **How the Code Works**

```cpp
int T;
cin >> T;
```

* Reads the number of test cases (how many numbers you want to reverse).

---

```cpp
while (T--) {
    int N, rev = 0;
    cin >> N;
```

* For each test case:

  * `N` is the number to reverse.
  * `rev` will store the reversed number, starting from `0`.

---

```cpp
while (N != 0) {
    rev = rev * 10 + N % 10;
    N /= 10;
}
```

Let’s break this down with an example:
Say `N = 123`

| Iteration | N   | N % 10 | rev                | N / 10 |
| --------- | --- | ------ | ------------------ | ------ |
| 1         | 123 | 3      | 0 \* 10 + 3 = 3    | 12     |
| 2         | 12  | 2      | 3 \* 10 + 2 = 32   | 1      |
| 3         | 1   | 1      | 32 \* 10 + 1 = 321 | 0      |

When `N` becomes 0, loop ends. Now `rev = 321`.

---

```cpp
cout << rev << endl;
```

* Prints the reversed number.

---

### ✅ **Key Notes**

* Leading zeros in the original number (like in `1200`) are **ignored** in output (e.g., becomes `21`).
* Works only for **positive integers** as written.

