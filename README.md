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

## 均標與前標計算
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
## week4
```C
#include <stdio.h>
struct DATA{
    int x,y;
}a[3];
struct DATA b={100,200};

int main()
{
    for(int i=0;i<3;i++){
        printf("a[%d]:%d %d\n",i,a[i].x,a[i].y);
    }
    printf("b: %d %d\n",b.x,b.y);

    struct DATA c;
    printf("c: %d %d 像亂碼\n",c.x,c.y);

    c=b;
    printf("c: %d %d\n",c.x,c.y);
}
```
## week4
```C
#include <stdio.h>
struct POINT{
    float x,y,z;
};

struct POINT point[5]={{0,0,0},{1,0,0},{0,1,0},{0,0,1},{1,1,1}};

int main()
{
    struct POINT*p=&point[0];
    printf("%.2f %.2f %.2f\n",p->x,p->y,p->z);

    p++;
    printf("%.2f %.2f %.2f\n",p->x,p->y,p->z);

    p++;
    printf("%.2f %.2f %.2f\n",p->x,p->y,p->z);


}
```
## 除惡務盡 
```C
#include <stdio.h>
int main()
{
	char a[100];
	scanf("%s",&a);
	int i=0;
	while (a[i]!='\0')
	{
	if(a[i]!='2')
	printf("%c",a[i]);
	i++;
	}
	printf("\n");
}
```
## 擲骰統計 
```C
#include <stdio.h>
char a[999];
int main()
{
	char count[7]={0};
	scanf("%s",&a);
	int i=0;
	while( a[i]!='\0')
	{
	count[ a[i]-'0']++;
	i++;
	}
	for(i=1;i<=6;i++){
	printf("%d:%d\n",i,count[i]);
	}
}
```
## 函數找整數的最大數字
```C
#include<iostream>
using namespace std;
int max_digit(int n)
{
int max;
max=n%10;
while(n      >0)
{
if((n%10)>max) max=n%10;
n/=10;
}
return max;
}
int main(){
  int n;cin>>n;
  cout<<"["<<max_digit(n)<<"]";
  return 0;
}
/* 上方C++ 的 main 函數 等價於 下方 C 的 main 函數
int main(void){
  int n;
  scanf("%d", &n);
  printf("[%d]", max_digit(n));
  return 0;
}
*/
```
## 星星等腰三角
```C
#include <stdio.h>
int main()
{
	int n,m=1,t=1;
	scanf("%d",&n);
	for(int i=0;i<n;i++){
		for(int k=n-1;k>=t;k--){
				printf(" ");
				}
			for(int j=1;j<=m;j++){
					printf("*");
					}
			m+=2;
			t++;
			printf("\n");
			}
	}
```
## 分開整數的每個數字 
```C
#include <stdio.h>
int main()
{
	int n,n1,n2,n3,n4,n5;
	scanf("%d",&n);
	n1=(n/10000);
	n=n-n1*10000;
	n2=(n/1000);
	n=n-n2*1000;
	n3=(n/100);
	n=n-n3*100;
	n4=(n/10);
	n5=n-n4*10;
	printf("%d   %d   %d   %d   %d",n1,n2,n3,n4,n5);
	
	}
```
## 字元判別 
```C
#include <stdio.h>
int main()
{
	char n;
	scanf("%c",&n);
	
	if(n>='A'&&n<='Z')printf("U");
	else if(n>='a'&&n<='z')printf("L");
	else if(n>='0'&&n<='9')printf("D");
	else printf("O");
}
```
## 數字之首
```C
#include <stdio.h>
int main()
{
	int n,n1,n2,n3,n4;
	scanf("%d",&n);
	n1=(n/1000);
	n2=(n/100);
	n3=(n/10);
	n4=(n/1);
	printf("%d",n1);
	}
```
## 輸出從0到N的偶數
```C
#include <stdio.h>
int main()
{

	int n;
	scanf("%d",&n);
	for(int i=1;i<=n;i++){
		if(i%2==0)
	printf("%d ",i);
	}
}
```
## 反序數字
```C
#include <stdio.h>
int f(int n)
{
	int p;
	int m=0;
	
	while(n>0)
	{
		p=n%10;
		n=n/10;
		m=p+m*10;
	}
	
	return m;
}

int main()
{
	int n,m;
	scanf("%d",&n);
	printf("%d+%d=%d\n",n ,f(m),n+f(m));
}
```
## 絕對值函數
```C
#include <stdio.h>
int f(int a)
{
	if(a>0)
	return a;
	else return a*(-1);
}

int main(void)
{
	int n;
	scanf("%d",&n);
	printf("[%d]",f(n));
	return 0;
}
```
## N數之和 
```C
#include <stdio.h>
int main()
{
	int n,sum=0,num;
	scanf("%d",&n);
	for(int i=1;i<=n;i++){
		scanf("%d",&num);
		sum+=num;
}
printf("%d\n",sum);
}
```
## 三數極大
```C
#include <stdio.h>
int main()
{
	int a,b,c;
	scanf("%d%d%d",&a,&b,&c);
	if(a>b && a>c)
	printf("%d",a);
	else if(b>a && b>c)
	printf("%d",b);
	else if(c>a && c>b)
	printf("%d",c);
	printf("\n");
}
```
## 計算商數 
```C
#include <stdio.h>
int main()
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("%d",a/b);
	printf("\n");
}
```
## 迴文判斷
```C
#include <stdio.h>
int main()
{
 int a,a1,a2,a3,a4;
 scanf("%d",&a);
 
 a1=a%10;
 a2=a%100/10;
 a3=a%1000/100;
 a4=a/1000;
 
 if(a1==a4&&a2==a3)
 printf("YES\n");
 else printf("NO\n");
 }
```
## 函數反序排列數字
```C
#include <stdio.h>
int f(int n)
{
	int p;
	int m=0;
	
	
	while(n> 0)
{
	p=n%10;
	n=n/10;
	m=p+m*10;
	
}
return m;
}
int main()
{
int n,m;
scanf("%d",&n);
printf("%d\n",f(m));
}
```
## 陣列找出現次數
```C
#include <stdio.h>
int main()
{
	int a[50],i,n,x;
	int count=0;
	for(i=0;i<10;i++)
	{
	scanf("%d",&a[i]);
	if(a[i]==0)
	break;
	}
	scanf("%d",&x);
	n=i;
	for(i=0;i<n;i++)
	{
	if(a[i]==x) count++;
	}
	printf("%d\n",count);
}
```
## 判斷大小
```C
#include <stdio.h>
int f(int a,int b){
if( a<b ) return -1;
else if(a==b) return 0;
else return 1;
}
int main(){
    int a, b;
    scanf("%d %d", &a, &b);
    printf("%d",f(a,b));
    return 0;
}
```
## 計算一列整數的總和
```C
#include <stdio.h>
int main()
{
	int sum=0,a;
	while(a!=999)
	{
	printf("Enter an integer ( 999 to end ): \n");
	scanf("%d",&a);
	sum+=a;}
		printf("The total is: %d",sum-999);
	}
```
## 計算餘數 
```C
#include <stdio.h>
int main()
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("%d",a%b);
}
```
## 整數轉換等級
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	if(n>=90)
	printf("A");
	else if(n< 90 && n>=80)
	printf("B");
	else if(n< 80 && n>=70)
	printf("C");
	else if(n< 70 && n>=60)
	printf("D");
	else printf("F");
}
```
## 計程車資計算
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	if(n<=1500)
	printf("100");
	else if(n> 1500)
	printf("%d",((n-1500)/250)*5+105);
}
```
## 找零錢
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	int a =n/50;
	int b =n%50/10;
	int c =n%50%10/5;
	int d =n%50%10%5/1;
	
	printf("%d=50*%d+10*%d+5*%d+1*%d",n,a,b,c,d);
}
```
