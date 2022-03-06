# AP325 CH1 - Recursive

[APCS325](https://drive.google.com/drive/folders/10hZCMHH0YgsfguVZCHU7EYiG8qJE5f-m?fbclid=IwAR2MekSJDV7AufzMGRjN05pbPwb93ygqmE-wAtOUDCdseTNwhPVTgPdW9-o) 學習心得：2022/2/1 ~ 2022/2/28

在開始這個章節前，已經會一些簡單的遞迴，像是費氏序列。

但僅限於最簡單的、條件已經列好的

所以這個單元，要學習的是：

* 列出遞迴式

* 運用更有效率的方法，降低時間複雜度

遞迴用不好會很耗時間

像是費式序列，用加法的時間複雜度是 O(n)

array CODE：
~~~cpp
for(int i = 2; i < k; i++) s[i] += s[i-1] + s[i-2];

~~~

但改用遞迴的話，因為會重複呼叫已經算過的數字，浪費時間，時間複雜度暴增為 O(2^n)

遞迴 CODE：
~~~cpp
int f(int n)
{
 if (n <= 2) return 1;
 return f(n-1) + f(n-2);
} 
~~~

但善用遞迴也能有效率的解決問題，也是這章要學的
