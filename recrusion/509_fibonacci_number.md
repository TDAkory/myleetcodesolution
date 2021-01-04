# 509\_Fibonacci\_Number

The Fibonacci numbers, commonly denoted F\(n\) form a sequence, called the Fibonacci sequence, such that each number is the sum of the two preceding ones, starting from 0 and 1. That is,

F\(0\) = 0, F\(1\) = 1 F\(n\) = F\(n - 1\) + F\(n - 2\), for n &gt; 1. Given n, calculate F\(n\).

**MySolution:**

```cpp
// c++
class Solution {
public:
    int fib(int n) {
        if (n == 0) return 0;
        if (n == 1) return 1;
        vector<int> res(3, 0);
        res[0] = 0;
        res[1] = 1;
        for (int i = 2; i <= n; i++){
            res[2] = res[1] + res[0];
            res[0] = res[1];
            res[1] = res[2];
        }
        return res[2];
    }
};
```

