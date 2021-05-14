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
## 最大公因數gcd 
```C
#include <stdio.h>
int main()
{
	int a,b,ans;
	printf("Enter two integers: \n");
	scanf("%d%d",&a,&b);
	if(a>b){
	for(int i=1;i<=b;i++){
		if(a%i==0&&b%i==0)
		ans=i;
		}
		printf("The greatest common divisor of %d and %d is %d\n",a,b,ans);
		}
		
	else if(a<b){
	for(int i=1;i<=a;i++){
		if(a%i==0&&b%i==0)
		ans=i;
		}
		printf("The greatest common divisor of %d and %d is %d\n",a,b,ans);
		}
		}
```
## 字串長度
```C
#include <stdio.h>
#include <string.h>
int main()
{
	char a[100],b[100];
	scanf("%s %s",&a,&b);
	int lena,lenb;
	lena=strlen(a);//字串a的長度
	lenb=strlen(b);
	if(lena>lenb) printf("1");
	else if(lenb>lena) printf("-1");
	else {printf("%d",strcmp(a,b));}
}
```
## 函數判斷質數
```C
#include <iostream>
using namespace std;
int prime (int n)
{
	int i;
	for(i=2;i<n;i++){
	if(n%i==0)break;
	}
	if(i==n) return 1;
	else return 0;
	
}

int main(){
  int n;cin>>n;
  cout<<"["<<prime(n)<<"]";
  return 0;
}
/* 上方 C++ 的 main 函數 等價於 下方 C 的 main 函數
int main(void){
    int n;
    scanf("%d", &n);
    printf("[%d]", prime(n));
    return 0;
    }
```
## 判斷迴文
```C
#include <stdio.h>
#include <string.h>
char a[10000];
int main()
{
	scanf("%s",&a);
	int i;
	int len;
	len=strlen(a);
	for( i=0;i<(len/2);i++){
		if(a[i] !=a[len-1-i])break;
		}
		if (i==(len/2))printf("YES");
		else printf("NO");
	}
```
## 計算餘數及列印
```C
#include <stdio.h>
int main()
{
int x,y;
scanf("%d%d",&x,&y);
printf("Enter two numbers: ");
printf("The remainder is %d\n",x%y);
}
```
## 判別正方形
```C
#include <stdio.h>
int main()
{
int x,y;
printf("Enter two numbers:  ");
scanf("%d%d",&x,&y);
if(x==y) printf("It is a square ");
else printf("It is not a square ");
}
```
## 將一連串整數相乘
```C
#include <stdio.h>
int main()
{
	int a,ans=1;
	printf("Enter the number of values to be processed: ");
	scanf("%d",&a);
	for(int i=0;i<a;i++)
	{
		printf("Enter a value: ");
		int b;
		scanf("%d",&b);
		ans*=b;
	}
	printf("Product of the %d values is %d",a,ans);
}
```
## 平年月份的天數 
```C
#include <stdio.h>
int main()
{
	int d[13]={0,31,28,31,30,31,30,31,31,30,31,30,31};
	int a;
	scanf("%d",&a);
	printf("%d",d[a]);
}
```
## 兩數平方差
```C
#include <stdio.h>
int main()
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("%d",a*a-b*b);
}
```
## 零錢總額
```C
#include <stdio.h>
int main()
{
	int a,b,c;
	scanf("%d%d%d",&a,&b,&c);
	printf("%d",a*50+b*5+c);
}
```
## 幾日為星期幾 
```C
#include <stdio.h>
int main()
{
	int a;
	scanf("%d",&a);
	printf("%d",(a-1)%7);
	}
```
## 整數二元四則運算 
```C
#include <stdio.h>
int main()
{
	int a,b;char c;
	scanf("%d %c %d",&a,&c,&b);
	if(c=='+')printf("%d",a+b);
	if(c=='-')printf("%d",a-b);
	if(c=='*')printf("%d",a*b);
	if(c=='/')printf("%d",a/b);\
}
```
## 兩數間可被7整除的數
```C
#include <stdio.h>
int main()
{
	int a,b;
	scanf("%d%d",&a,&b);
	for(int i=a;i<=b;i++){
	if(i%7==0)printf("%d ",i);
	}
}
```
## 奇數之和
```C
#include <stdio.h>
int main()
{
	int n,ans=0;
	scanf("%d",&n);
	for(int i=1;i<=n;i++){
		if(i%2!=0)ans+=i;
	}
	printf("%d",ans);
}
```
## 利用自訂函式最大值max與最小值min求出兩者之差
```C
#include<iostream>
using namespace std;
int max(int a,int b,int c,int d)
{
	int max;
	if(a>b && a>c && a>d) max=a;
	else if(b>a && b>c && b>d)max=b;
	else if(c>a && c>b && c>d)max=c;
	else max=d;
	return max;
}
int min(int a,int b,int c,int d)
{
	int min;
	if(a<b && a<c && a<d) min=a;
	else if(b<a && b<c && b<d)min=b;
	else if(c<a && c<b && c<d)min=c;
	else min=d;
	return min;
}
int main(){
  int a,b,c,d;cin>>a>>b>>c>>d;
  cout<<(max(a,b,c,d)-min(a,b,c,d));
  return 0;
}
/* 上方C++ main 函式 等同於 下方 C 的 main 函式
int main(void){
  int a, b, c, d;
  scanf("%d %d %d %d", &a, &b, &c, &d);
  printf("%d",  max(a,b,c,d) - min(a,b,c,d) );
  return 0;
}
```
## 字串中的數字個數 
```C
#include <stdio.h>
int main()
{
	char a[80];
	int ans=0;
	scanf("%s",&a);
	int i=0;
	while (a[i]!='\0'){
		if(a[i]>='0' && a[i]<='9')ans++;
			i++;
		}
		printf("%d",ans);
}
```
## week12
```C
#include <stdio.h>
int a[10000];
int main()
{
	int N,M;
	while( scanf("%d %d",&N,&M)==2){
		for(int i=0;i<N;i++){
			scanf("%d",&a[i]);
			}
			
			
			
			printf("%d %d\n",N,M);
			for(int i=0;i<N;i++){
				printf("%d\n",a[i]);
			}
		}
}
```
## 數字個數
```C
#include <stdio.h>
int main()
{
	int a,ans=0;
	while (scanf("%d",&a)!=EOF)
	{
	ans++;
	}
	printf("%d",ans-1);
}
```
## 剩餘啤酒有幾手又幾瓶
```C
#include <stdio.h>
int main()
{
	int p,d;
	scanf("%d%d",&p,&d);
	
	printf("%d %d",(p-(d*6))/6,p%6);
}
```
## 三數最小
```C
#include <stdio.h>
int main()
{
	int a,b,c;
	scanf("%d%d%d",&a,&b,&c);
	if(a<b && a<c)
	printf("%d\n",a);
	else if(b<a && b<c)
	printf("%d\n",b);
	else printf("%d\n",c);
}
```
## 計算立方值
```C
#include <stdio.h>
int main()
{
	int a,b,c,d,e,f;
	scanf("%d%d%d%d%d%d",&a,&b,&c,&d,&e,&f);
	printf("%d\n%d\n%d\n%d\n%d\n%d\n",a*a*a,b*b*b,c*c*c,d*d*d,e*e*e,f*f*f);
}
```
## 判斷平方數
```C
#include <stdio.h>
int main()
{
	int n,ans=0;
	scanf("%d",&n);
	for(int i=1;i<n;i++){
	if(n==i*i) ans=i;}
	printf("%d",ans);
		
}
```
## 計算質數個數 
```C
#include <stdio.h>
int main()
{
	int a,b,count=0;
	int j;
	scanf("%d %d",&a,&b);
	for(int i=a;i<=b;i++){
		for( j=2;j<i;j++){
			if(i%j==0)break;}
			if(j==i)
			count++;
		}
		printf("%d",count);
	}
```
## 三數組合
```C
#include <stdio.h>
int main()
{
	int a[3],i,j,temp;
	for(i=0;i<3;i++){
		scanf("%d",&a[i]);}
		for(i=0;i<3;i++)
		{
		for(j=i+1;j<3;j++)
		{
		if(a[i]<a[j])
		{
		temp=a[j];
		a[j]=a[i];
		a[i]=temp;
	}
	}
	}
	printf("%d",a[0]*100+a[1]*10+a[2]+1);
}
```
## 找千位數
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	int d=n/1000%10;
	printf("%d",d);
}
```



