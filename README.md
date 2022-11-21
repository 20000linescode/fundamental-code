# fundamental-code
C语言日常基础
#include<stdio.h>//if的多重语句
int main()
{
	/*int age=55;
	if(age<18) printf("未成年\n");
	else if(age>=18&&age<50) printf("成年\n");
	else if(age>=50&&age<60) printf("壮年\n");
	else  printf("老年\n");
	return 0;*/
}
#include<stdio.h>//
int main()
{
	int a=0,b=1;
	if(a==1)
	if(b==1) printf("hhh\n");
	else
		printf("hha\n");
	return 0;
}
#include<stdio.h>
int main()
{
	int a=1;
	if(a=2) printf("hhh\n");
	return 0;
}
#include<stdio.h>
int main()
{
	int i=0;
	for(i=0;i<=100;i++)
	{
		if(1==i%2) printf("%d ",i);
	}
	return 0; 
}
#include<stdio.h>
int main()
{
	int day=0;

	return 0;
}
#include<stdio.h>
int main()
{
	while(1)
		printf("无敌\n");
	return 0;
}
#include<stdio.h>
int main()
{
    char ch;
	/*while((ch=getchar())!=EOF)
	{	putchar(ch);
	}*/
	ch=getchar();
	printf("%d\n",ch);
	printf("%c\n",ch);
	putchar(ch);
	return 0;
}
#include<stdio.h>//减少空格之类对下一个getchar的影响，使用了一个while循环
int main()
{
	int ret =0;
	int ch=0;
	char password[20]={0};
	printf("请输入密码:>");
	scanf("%s",password);//输入密码，存放在数组password中
	while((ch=getchar())!='\n')
	{
		;
	}
	printf("请确认密码（Y/N）:>");
	ret=getchar();
	if (ret=='Y') printf("确认成功\n");
	else printf("放弃确认\n");
    return 0;
}
#include<stdio.h>//只输出0到9的ASCII码
int main()
{
	int ch=0;
	while((ch=getchar())!=EOF)
	{
		if(ch<'0'||ch>'9')
			continue;
		putchar(ch);
	}
	return 0;
}
}
#include<stdio.h>//for循环里改变变量值产生死循环
int main()
{
	int i=0;
	for(i=1;i<10;i++)
	{
		if(i=5)
			printf("hhh\n");
		printf("aaa\n");
	}
	return 0;
}
#include<stdio.h.>//缺少j=0代码只循环十次
int main()
{
	int i=0,j=0;
	for(;i<10;i++)
	{
		for(;j<10;j++)
			printf("hhh\n");
	}
	return 0;
}
#include<stdio.h>//K=0不执行
int main()
{
	int i=0,k=0;
	for(i=0,k=0;k=1;i++,k++)
	{k++;}
	printf("%d\n",k);
	
	return 0;
}
#include<stdio.h>//死循环
int main()
{
	int i=1;
	do
	{
		if(i==5) continue;
		printf("%d\n",i);
		i++;
	}
	while(i<=10);
		return 0;

}
#include<stdio.h>//计算n的阶乘
int main()
{
	int n,i,sum=1;
	scanf("%d",&n);
	for(i=1;i<=n;i++)
	{
		sum*=i;
	}
	printf("%d\n",sum);
	return 0;
}
#include<stdio.h>//计算1到10的阶乘的和
int main()
{
	int i,j,sum=0;
	int ret=1;
	for(i=1;i<=10;i++)
	{
		ret=1;//每次计算完后将ret重新赋值为1
		for(j=1;j<=i;j++)
		{
			ret=ret*j;
		}
		sum=ret+sum;
	}
	printf("%d\n",sum);
	return 0;
}
#include<stdio.h>//输入一个小写字母，输出一个大写字母，并且输出他的ASCII码值。
int main()
{
	char ch;
	printf("请输入一个小写字母:");

	ch=	getchar();
	if(ch<'a'||ch>'z') 
	{printf("请重新输入\n");}
	else {putchar(ch-32);
	printf(" %d\n",ch-32);}
	return 0;
}
#include<stdio.h>//二分查找法
int main()
{
	int n;
	int arr[]={1,2,3,4,5,6,7,8,9,10};
	int sz=sizeof(arr)/sizeof(arr[0]);//计算数组元数个数
	int left=0,right=sz-1;//赋予左右下标的大小
	//int mid=(left+right)/2;
	printf("输入要查找到的0-10的数:");
	scanf("%d",&n);
	while(left<=right)
  {
	int mid=(left+right)/2;
	if(arr[mid]<n) 
	{
		left=mid+1;
	}
	else if(arr[mid]>n)
	{
		right=mid-1;
	}
	else 
	{
		printf("找到了,下标是:%d\n",mid);
		break;
	}
  }
    if(left>right)
		{
			printf("找不到\n");
	    }
			return 0;
}
#include<stdio.h>
#include<string.h>
int main()
{
	char arr1[]={"Welcome to bit!!!!"};
	char arr2[]={"##################"};
	int left=0;
	int right=strlen(arr1);//sizeof(arr1);
	//printf("%d\n",sizeof(arr1));
	//printf("%d\n",sizeof(arr2));
	//printf不如strlen
    while(left<=right)
	{
		arr2[left++]=arr1[left++];
		arr2[right--]=arr1[right--];
		printf("%s\n",arr2);
	}
	return 0;
}
#include<stdio.h>
#include<string.h>
#include<Windows.h>
#include<stdlib.h>
int main()
{
	char arr1[]={"Welcome to bit!!!!"};
	char arr2[]={"##################"};
	int left=0;
	int right=strlen(arr1);
    while(left<=right)
	{
		arr2[left]=arr1[left];
		arr2[right]=arr1[right];
		printf("%s\n",arr2);
		Sleep(1000);
		system("cls");
		left++;
		right--;
	}
	return 0;
}
#include<stdio.h>
int main()
{
	char password[20]={0};
	int i=0;
	//printf("请输入密码:>");
	for(i=0;i<3;i++)
	{
		printf("请输入密码:>");
		scanf("%s",password);
		if(password=="123456")
	   { 
		   printf("登录成功\n");
		   break;
	   }
		else                  
		{
			printf("密码错误，请重新输入\n");
		}
	}
	if(i==3) printf("密码错误三次，不可继续输入\n");
	return 0;
}
#include<stdio.h>
#include<string.h>
int main()
{
	char password[20]={0};
	int i=0;
	for(i=0;i<3;i++)
	{
		printf("请输入密码:>");
		scanf("%s",password);
		if(strcmp(password,"123456")==0)//若相等则返回0
	   { 
		   printf("登录成功\n");
		   break;
	   }
		else                  
		{
			printf("密码错误，请重新输入\n");
		}
	}
	if(i==3) printf("密码错误三次，不可继续输入\n");
	return 0;
}
#include<stdio.h>//输入三个数并且由大到小排列
int main()
{
	int x,y,z,tmp;
	scanf("%d %d %d",&x,&y,&z);
	if(x<y) 
	{
		tmp=x;
		x=y;
		y=tmp;
	}
	if(x<z)
	{
		tmp=x;
		x=z;
		z=tmp;
	}
	if(y<z)
	{
		tmp=y;
		y=z;
		z=tmp;
	}
    printf("%d,%d,%d",x,y,z);

		return 0;
}
#include<stdio.h>//输出1-100中3的倍数
int main()
{
	int i;
	for(i=1;i<=100;i++)
	{
		if((i%3)==0)
			printf("%d ",i);
	}
	return 0;
}
#include<stdio.h>//求两个数的最大公约数
int main()
{
	int a,b,r=0;
	printf("输入a,b的值:>");
	scanf("%d %d",&a,&b);
	while(a%b) //a%b为真即不等于0，所以输入数字不需要区分大小
	{
		r=a%b;//可以直接改成while(r=a%b)省略这一行
		a=b;
		b=r;
	}
	printf("%d\n",b);
	return 0;
}
#include<stdio.h>//打印1000--2000的闰年
int main()
{
	int year=0;//闰年条件，1.能被4整除并且不能被100整除
	                     //2.能被400整除。只要满足上面两个其中一个即是闰年。
    int count=0;
	for(year=1000;year<=2000;year++)
	{
		if((year%4==0)&&(year%100!=0))
		{	printf("%d ",year);
		  count++;
		}
		else if(year%400==0)
		{
			printf("%d ",year);
			count++;
		}
	}
	printf("\n %d\n",count);
	return 0;
}
#include<stdio.h>
int main()
{
	int year=0;
	int count=0;
	for(year=1000;year<=2000;year++)
	{
		if(((year%4==0)&&(year%100!=0))||year%400==0)
		{   
			printf("%d ",year);
		    count++;
		}
	}
printf("\n %d\n",count);
        return 0;
}
#include<stdio.h>//求100-200中的素数，并且打印出来，计算其总个数。
int main()
{
	int i=0,j=0,count=0;
	for(i=100;i<=200;i++)
	{
		for(j=2;j<i;j++)
		{
			if(i%j==0)
			break;
		}
	    if(i==j)
		{
			printf("%d ",i);
			count++;
		}
	}
			printf("\n %d\n",count);

	return 0;
}
#include<stdio.h>//依然是求素数，改进了算法,使用了开平方减少运算量。
#include<math.h>
int main()
{
	int i=0,j=0,count=0;
	for(i=100;i<=200;i++)
	{
		for(j=2;j<=sqrt(i);j++)
		{
			if(i%j==0)
			break;
		}
	    if(j>sqrt(i))
		{
			printf("%d ",i);
			count++;
		}
	}
			printf("\n %d\n",count);

	return 0;
}
#include<stdio.h>//依然是求素数，改进了算法,使用了开平方减少运算量并且偶数不可能是素数使用了i+=2。
#include<math.h>
int main()
{
	int i=0,j=0,count=0;
	for(i=101;i<=200;i+=2)
	{
		for(j=2;j<=sqrt(i);j++)
		{
			if(i%j==0)
			break;
		}
	    if(j>sqrt(i))
		{
			printf("%d ",i);
			count++;
		}
	}
			printf("\n %d\n",count);

	return 0;
}
#include<stdio.h>//从1+1/2+1/3+...+1/100
int main()
{
	int i;
	double sum=0.0;
	for(i=1;i<=100;i++)
	{
		sum+=1.0/i;
	}	
	printf("%lf\n",sum);
	return 0;
}
#include<stdio.h>//从1-1/2+1/3+...-1/100;
int main()
{
	int i;
	int flag=1;
	double sum=0.0;
	for(i=1;i<=100;i++)
	{
		sum+=flag*1.0/i;
		flag=-flag;
	}	
	printf("%lf\n",sum);
	return 0;
}
#include<stdio.h>//求十个整数中的最大值;
int main()
{
	int arr[]={1,2,3,4,5,6,7,8,9,10,};
	int i,max=arr[0];//max应该为数组中的数，而不应该是直接赋值，可能数组中还有负数
	int sz=sizeof(arr)/sizeof(arr[0]);
	for(i=0;i<sz;i++)
	{
		if(arr[i]>max)
			max=arr[i];
	}
	printf("%d\n",max);
	return 0;
}
#include<stdio.h>//打印九九乘法表
int main()
{
	int i=0,j=0,sum=0;
	for(i=1;i<10;i++)
	{
		for(j=1;j<=i;j++)
		{
			sum=i*j;
			printf("%d*%d=%-2d ",i,j,sum);
		}
		printf("\n");
	}
	return 0;
}
#include<stdio.h>//猜数字游戏
#include<stdlib.h>
#include<time.h>
void game()
{
	int guess;
	int ret=0;
	//srand((unsigned int)time(NULL));//使()中的数一直发生变化,使用时间戳，因为时间一直在变化。
	//NULL为空指针
	ret=rand()%100+1;//产生随机数0到RAND_MAX=0x7fff=32767.%100以后生成0-99的随机数
	//RAND_MAX=0x7fff
	//printf("%d\n",ret);这里是产生的随机数的值
	while(1)//2.猜数字，没猜对就一直猜，猜对了break，跳出循环。
	{
		printf("输入猜的数字\n");
		scanf("%d",&guess);
		if(guess>ret)
		{
			printf("猜大了\n");
		}
		else if(guess<ret)
		{
			printf("猜小了\n");
		}
		else
		{
			printf("恭喜你，猜对了\n");
			break;
		}
	}
}
void menu()
{
	printf("******************\n");
    printf("**1.play 0.exit **\n");
	printf("******************\n");

}
int main()
{
	int input=0;
	srand((unsigned int)time(NULL));//使()中的数一直发生变化,使用时间戳，因为时间一直在变化。
	//NULL为空指针

	do
	{
		menu();//菜单函数
		printf("请选择>:");
		scanf("%d",&input);
		switch(input)
		{
case 1: 
			game();//猜数字游戏的一个函数
			break;
case 0:
			printf("退出游戏\n");
			break;
default:
			printf("选择错误\n");
			break;
		}

	}while(input);//若为1进入循环，为0结束循环，其他的数字进入default输出选择错误。非常巧妙。

	return 0;
}
#include<stdio.h>//goto的简单用法。
int main()
{
	goto again;
	printf("aaa\n");
	again:
	printf("hhh\n");
	return 0;
}
#include<stdio.h>//60s内关机的程序
#include<string.h>
#include<windows.h>
#include<stdlib.h>
int main()
{
	char input[]={0};
	again:
	printf("请输入666，不然你的电脑将在60s后关机\n");
	scanf("%s",input);
	system("shutdown -s -t 60");
	if(strcmp(input,"666"))//比较字符串
	{
		system("shutdown -a");
	}
	else
	{
		printf("输入错误\n");
		goto again;
	}
	return 0;
}
#include<stdio.h>//求十个整数中的最大值;
int main()
{
	int arr[]={1,2,3,4,5,6,7,8,9,10,};
	int i,max=arr[0];//max应该为数组中的数，而不应该是直接赋值，可能数组中还有负数
	int sz=sizeof(arr)/sizeof(arr[0]);
	for(i=0;i<sz;i++)
	{
		if(arr[i]>max)
			max=arr[i];
	}
	printf("%d\n",max);
	return 0;
}
#include<stdio.h>//打印九九乘法表
int main()
{
	int i=0,j=0,sum=0;
	for(i=1;i<10;i++)
	{
		for(j=1;j<=i;j++)
		{
			sum=i*j;
			printf("%d*%d=%-2d ",i,j,sum);
		}
		printf("\n");
	}
	return 0;
}
#include<stdio.h>//猜数字游戏
#include<stdlib.h>
#include<time.h>
void game()
{
	int guess;
	int ret=0;
	//srand((unsigned int)time(NULL));//使()中的数一直发生变化,使用时间戳，因为时间一直在变化。
	//NULL为空指针
	ret=rand()%100+1;//产生随机数0到RAND_MAX=0x7fff=32767.%100以后生成0-99的随机数
	//RAND_MAX=0x7fff
	//printf("%d\n",ret);这里是产生的随机数的值
	while(1)//2.猜数字，没猜对就一直猜，猜对了break，跳出循环。
	{
		printf("输入猜的数字\n");
		scanf("%d",&guess);
		if(guess>ret)
		{
			printf("猜大了\n");
		}
		else if(guess<ret)
		{
			printf("猜小了\n");
		}
		else
		{
			printf("恭喜你，猜对了\n");
			break;
		}
	}
}
void menu()
{
	printf("******************\n");
    printf("**1.play 0.exit **\n");
	printf("******************\n");

}
int main()
{
	int input=0;
	srand((unsigned int)time(NULL));//使()中的数一直发生变化,使用时间戳，因为时间一直在变化。
	//NULL为空指针

	do
	{
		menu();//菜单函数
		printf("请选择>:");
		scanf("%d",&input);
		switch(input)
		{
case 1: 
			game();//猜数字游戏的一个函数
			break;
case 0:
			printf("退出游戏\n");
			break;
default:
			printf("选择错误\n");
			break;
		}

	}while(input);//若为1进入循环，为0结束循环，其他的数字进入default输出选择错误。非常巧妙。

	return 0;
}
#include<stdio.h>//goto的简单用法。
int main()
{
	goto again;
	printf("aaa\n");
	again:
	printf("hhh\n");
	return 0;
}
#include<stdio.h>
#include<string.h>
#include<windows.h>
#include<stdlib.h>
int main()
{
	char input[]={0};
	again:
	printf("请输入我是猪，不然你的电脑将关机\n请输入:>\n");
	scanf("%s",input);
	system("shutdown -s -t 60");
	if(strcmp(input,"我是猪"))
	{
		system("shutdown -a");
	}
	else
	{
		printf("输入错误\n");
		goto again;
	}
	return 0;
}
#include<stdio.h>
#include<string.h>
int main()
{
    char arr1[]="abc";
	char arr2[20]="#####";
	strcpy(arr2,arr1);
	printf("%s\n",arr2);
	return 0;
}
#include<stdio.h>
#include<string.h>
int main()
{
	char arr[]="abc";
	memset(arr,'*',2);
	printf("%s\n",arr);
	return 0;
}

#include<stdio.h>
void Swap1(int* pa,int* pb)
{
	int tmp=0;
	tmp=*pa;
	*pa=*pb;
	*pb=tmp;
}
int main()
{
	int num1=10;
	int num2=20;
	Swap1( &num1,&num2 );
	printf("%d,%d",num1,num2);
	return 0;
}
#include<stdio.h>//用函数输出100-200之间的素数
int is_prime(int n)
{
	int j=0;
	for(j=2;j<n;j++)
	{
		if(n%j!=0)
			return 1;
		else
			return 0;
	}
}
int main()
{
	int i=0;
	for(i=100;i<=200;i++)
	{
		if(is_prime(i)==1)
			printf("%d ",i);
	}
	if(is_prime(i)==1)
	return 0;
}
#include<stdio.h>//用函数输出100-200之间的素数
int is_prime(int n)
{
	int j=0;
	for(j=2;j<n;j++)
	{
		if(n%j==0)
			return 0;
	}
	return 1;
}
int main()
{
	int i=0;
	for(i=100;i<=200;i++)
	{
		if(is_prime(i)==1)
			printf("%d ",i);
	}
	if(is_prime(i)==1)
	return 0;
}
#include<stdio.h>//用函数求闰年
int is_leap_year(int x)
{
	if((x%4==0&&x%100!=0)||(x%400==0))
		return 1;
}
int main()
{
	int year=0;
	int count=0;
	for(year=1000;year<=2000;year++)
	{
		if(is_leap_year(year)==1) 
			printf("%d ",year);
	}
	return 0;
}
