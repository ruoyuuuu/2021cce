# 2021cce
## 找零錢
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	int coin50 = n/50;
	int coin5 = n%50/5;
	int coin1 = n%5;
	printf("%d=50*", n);
	printf("%d+5*%d+1*%d\n",coin50,coin5,coin1);
```
## 因數個數
```C
#include <stdio.h>
int main()
{
	int n,sum=0;
	scanf("%d",&n);
	for(int i=1;i<=n;i++){
		if(n%i==0)
		sum++;
		}
	printf("%d\n",sum)
} 
```
## 找倍數
```C
#include <stdio.h>
int main()
{
	int a[10],sum=0;
	for(int i=0;i<10;i++){
		scanf("%d",&a[i]);
		if(a[i]%3==0)
		sum++;
	}
	printf("%d\n",sum);

}
```
## 整數轉換為等級
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	if(n>=90)
	printf("A\n");
	else if(80<=n && n<90)
	printf("B\n");
	else if(60<=n && n<80)
	printf("C\n");
	else printf("F\n");
}
```
## 分式化簡
```C
#include <stdio.h>
int main()
{
	int a,b,num=0;
	scanf("%d%d",&a,&b);
	for(int i=1;i<=a;i++){
		if(a%i==0 && b%i==0)
		num=i;
	}
	printf("%d %d\n",a/num,b/num);
	
}
```
## 讀入整數反序列印
```C
#include <stdio.h>
int main()
{
	int a[11];int n=0;
	for(int i=0;i<10;i++){
	scanf("%d",&a[i]);
		if(a[i]==0)
		break;
		n++;
	}
	for(int i=n-1;i>=0;i--){
	printf("%d ",a[i]);
	}
	printf("\n");


}
```
## A的B次方函數
```C
#include <stdio.h>
int MYPOWER(int a, int b)
{
int ans=1;
for(int i=1;i<=b;i++)
	ans=ans*a;
	return ans;
}
int main(void)
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("[%d]",MYPOWER(a,b));
	return 0;
}
```
## 漸增數列相加
```C
#include <stdio.h>
int main()
{
	int n,ans=0;
	scanf("%d",&n);
	for(int i=1;i<n;i++){
		ans+=i*(i+1);
	}
	printf("%d\n",ans);
		


}
```
## 判別正方形
```C
#include <stdio.h>
int main()
{
	int a,b;
	scanf("%d%d",&a,&b);
		printf("Enter two numbers: ");
		if(a==b)
		printf(" It is a square ");
		else
		printf(" It is not a square ");
		}
```

## 第十一題均標與前標計算
```c
#include <stdio.h>
int main()
{
	int N;
	scanf("%d",&N);
	
	int sum=0;
	int a[1000];
	for(int i=0;i<N;i++){
		scanf("%d",&a[i]);
		sum+=a[i];
		}
	float average;
	average=(float)sum/N;
	float r=0;
	float sumTop=0;
	for(int i=0;i<N;i++){
		if(a[i]>=average){
			sumTop+=a[i];
			r++;
			}
		}
	float averageTop;
	averageTop=(float)sumTop/r;
	printf("均標:%.1f\n",average);
	printf("前標:%.1f\n",averageTop);
}

```
## 計算陣列的平方值
```C
#include <stdio.h>
int main()
{
	int n, a[10];
	scanf("%d",&n);
	for(int i=0;i<n;i++){
	scanf("%d",&a[i]);
	printf("%d,",a[i]*a[i]);
	}
	printf("\n");
		
}
```
## 大小寫轉換 
```C
#include <stdio.h>
int main()
{
	char a[10];
	scanf("%s",&a);
	
	for(int i=0;i<=9;i++)
	{
	if(a[i]>='0' && a[i]<='9')printf("%c",a[i]);
	else if (a[i]>='A' && a[i]<= 'Z')printf("%c",a[i]+32);
	else if (a[i]>='a' && a[i]<= 'z')printf("%c",a[i]-32);
	else if(a[i]=='\0') break;
	}
	printf("\n");
	}
```
## 計算幾週與幾天
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	printf("%d %d",n/7,n%7);
	printf("\n");
}
```
## 計程車資計算 
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	if(n<=2000)
	printf("100");
	else if(n>2000)
	printf("%d",(n-2000)/500*5+105);
	printf("\n");
}
```
## 兩數間可被5整除的整數
```C
#include <stdio.h>
int main()
{
	int a,b,temp;
	scanf("%d%d",&a,&b);
	if(a>b)
	{
		temp=a;
		a=b;
		b=temp;
	}
	for(int i=a;i<=b;i++){
		if(i%5==0) printf("%d\n",i);

	}
}
```
## 整數間最大距離
```C
#include <stdio.h>
int main()
{
	int a, b, c;
	scanf("%d%d%d",&a,&b,&c);
	if(a-b>a-c &&a-b>b-c && a-b>c-a &&a-b>c-b && a-b>b-a)
	printf("%d",a-b);
	else if(a-c>a-b &&a-c>b-c && a-c>c-a &&a-c>c-b && a-c>b-a)
	printf("%d",a-c);
	else if(b-c>a-b &&b-c>a-c && b-c>c-a &&b-c>c-b && b-c>b-a)
	printf("%d",b-c);
	else if(c-a>a-b &&c-a>b-c && c-a>a-c &&c-a>c-b && c-a>b-a)
	printf("%d",c-a);
	else if(c-b>a-b &&c-b>b-c && c-b>c-a &&c-b>a-c && c-b>b-a)
	printf("%d",c-b);
	else if(b-a>a-b &&b-a>b-c && b-a>c-a &&b-a>c-b && b-a>a-c)
	printf("%d",b-a);
	printf("\n");
	
}
```
