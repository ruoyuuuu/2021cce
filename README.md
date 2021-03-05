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
