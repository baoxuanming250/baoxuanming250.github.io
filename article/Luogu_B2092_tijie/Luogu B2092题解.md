[toc]

# Luogu B2092题解



原题传送门:[B2092](https://www.luogu.com.cn/problem/B2092)

***
### 分析
---
由于灯是开的，所以如果要将灯关掉，要拉奇数次，也就是这个灯的编号有奇数个因数。所以，我们只要求有奇数个因数的编号即可。

---
### 思路
一般的自然数 $m$ ，都有偶数个因数，因为一个因数必然对应另一个因数 (即 $m=x\times y$ )，因数便成对出现。但如果一个数 $m$ ，可以分为 $m=x\times x$ 的形式，这个数便会比理论少一个因数，于是有奇数个因数。而能分解为 $m=x\times x$ 形式的自然数 $m$，只有完全平方数。所以，我们只要输出完全平方数即可。

***
### Code

```cpp
#include<bits/stdc++.h>
using namespace std;

int main()
{
	int n;
	scanf("%d",&n);
	int a=sqrt(n);//由于求的是完全平方数，只需求是谁的平方即可
	for(int i=1;i<=a;i++)
		printf("%d ",i*i);//输出这个平方数 
	return 0;
}
```