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
#include<stdio.h>
int binary_search(int arr[],int k,int sz)//数组的传递；
{
	int left=0;
	int right=sz-1;
	int i=0;
	//int mid=(left+right)/2;
	while(left<=right)
	{
		int mid=(left+right)/2;
		if(arr[mid]<k)
			{
				left=mid+1;
		    }
	else if(arr[mid]>k)
	 {
		right=mid-1;
	 }
		else 
		{
			return mid;
	    }
	}
	return -1;
}
int main()
{
	int k=7;//7为要找的元素，我们返回7的下标；
	int arr[]={1,2,3,4,5,6,7,8,9,10};
	int sz=sizeof(arr)/sizeof(arr[0]);
	int ret=binary_search(arr,k,sz);
	printf("%d\n",ret);
	return 0;
}
#include<stdio.h>//调用一次num加1
void Add(int* p)
{
	(*p)++;
}
int main()
{
	int num=0;
	Add(&num);
	printf("%d\n",num);
	Add(&num);
	printf("%d\n",num);
	Add(&num);
	printf("%d\n",num);
	return 0;
}
#include<stdio.h>
int main()
{
	printf("%d",printf("%d",printf("%d",43)));
	return 0;
}
#include<stdio.h>
int Add(int a,int b);
int main()
{
	int a=10,b=20;
	int sum=Add(a,b);
	printf("%d\n",sum);
	return 0;
}
int Add(int a,int b )
{
	int z=a+b;
	return z;
}
#include<stdio.h>
int main()
{
	printf("hhh\n");
	main();
	return 0;
}
#include<stdio.h>
void print(int n)
{
    if(n>9)
	{
		print(n/10);
	}
	printf("%d ",n%10);
}
int main()
{
	int n=1234;
	unsigned int ret=0;
	//scanf("%d\n",&n);
	print(n);
	return 0;
}
#include<stdio.h>//函数代替strlen.
int my_strlen(char* arr)
{
	int count=0;
	while(arr!=0)
	{
		arr++;
		count++;
	}
	return count;
}
int main()
{
	char arr[]="abc";
	int len=my_strlen(arr);
	printf("%d\n",len);
	return 0;
}
#include<stdio.h>//不创建变量，用递归求字符串长度；
int my_strlen(char* arr)
{
	if (*arr!='\0')//使用解引用操作符，得到arr中的内容；
        return 1+my_strlen(arr+1);//递归运行得到的应该是1+1+1+0=3；
	else                          //一直到\0停止调用
        return 0;
}
int main()
{
	char arr[]="abc";
	int len=my_strlen(arr);
	printf("len=%d\n",len);//主函数调用一次
	return 0;
}
#include<stdio.h>//递归求阶乘，但是要注意是否会溢出；
int Fac1(int n)
{
	if(n<=1)
		return 1;
	else
		return n*Fac1(n-1);
}
int main()
{
	int n=0;
	int ret;
	scanf("%d",&n);
	 ret=Fac1(n);
	printf("%d\n",ret);
	return 0;
}
#include<stdio.h>//求第n个斐波那契数的值,使用函数
int Fib(int n)
{
	int a=1;
	int b=1;
	int c=1;
	while(n>2)
	{
		c=a+b;
		a=b;
		b=c;
		n--;
	}
    return c;
}
int main()
{
	int ret=0;
	int n=0;
	scanf("%d",&n);
	ret=Fib(n);
	printf("%d\n",ret);
	return 0;
}
#include<stdio.h>//求第n个斐波那契数的值,使用递归；
int Fib(int n)
{
	if(n<=2) return 1;
	else return Fib(n-1)+Fib(n-2);
}
int main()
{
	int ret=0;
	int n=0;
	scanf("%d",&n);
	ret=Fib(n);
	printf("%d\n",ret);
	return 0;
}
#include<stdio.h>
int main()
{
   int x=0,y=0,sum=0;
   scanf("%d %d",&x,&y);
   sum=x+y;
   printf("%d\n",sum);
   return 0;
}
#include<stdio.h>
int main()
{
	double Sn=0;
	int k=1;
	int n=1;
	scanf("%d",&k);
	while(Sn<=k)
	{
		Sn=Sn+1.0/n;
		n++;
	}
	printf("%d\n",n-1);
	return 0;
}
#include<stdio.h>
#include<string.h>
int main()
{
	char arr[10]="abcdef";
	char arr1[]="abc";
	char arr2[]={'a','b','c'};
	printf("%d\n",sizeof(arr));
	printf("%d\n",strlen(arr));
	printf("%d\n",sizeof(char));
	printf("%d\n",sizeof(arr1));
	printf("%d\n",sizeof(arr2));
	printf("%d\n",strlen(arr1));
	printf("%d\n",strlen(arr2));
	return 0;
}
#include<stdio.h>
int main()
{
	int i=0;
	int arr[]={1,2,3,4,5,6,7,8,9,10};
	for(i=0;i<10;i++)
	{
		printf("&arr[%d]=%p\n",i,&arr[i]);
	}
	return 0;
}
#include<stdio.h>
int main()
{
	int i=0,j=0;
	int arr[3][4];
	for(i=0;i<3;i++)
	{
		for(j=0;j<4;j++)
		{
			printf("arr[%d][%d],%p\n",i,j,&arr[i][j]);
		}
	}
	return 0;
}
#include<stdio.h>//冒泡排序,升序；可以使用任意数组的数进行排序；
void bubble_sort (int arr[],int sz)
{
	int i=0,j=0;
	//for(i=0;i<sz-1;i++)//控制交换的次数
	//{
		for(j=0;j<sz-i-1;j++)
		{

			if(arr[j]>arr[j+1])//比较arr[j]与arr[j+1],较大就交换。
			{                  //交换二者的值千万别错了
							int tmp=arr[j+1];
							arr[j+1]=arr[j];
							arr[j]=tmp;
							i++;
			}

		}
	//}
}
	int main()
{
	int sz=0,i=0;
	int arr[]={10,9,8,7,6,5,4,3,2,1};
	sz=sizeof(arr)/sizeof(arr[0]);
	bubble_sort(arr,sz);
	for(i=0;i<sz;i++)
	{
		printf("%d ",arr[i]);
	}
	return 0;
}
#include<stdio.h>//输入十个整数，再输入一个数加30
int main()       //输出比那个数小的十个整数中的数
{
	int i=0,count=0;
	int n=0;
	int arr[10]={0};
	for(i=0;i<10;i++)
	{
			scanf("%d",&arr[i]);
	}
	scanf("%d",&n);
	for(i=0;i<10;i++)
	{
		if(arr[i]<=(n+30))//注意小于等于
			count++;
	}
	printf("%d\n",count);
	return 0;

#include<stdio.h>//0表示该树未砍，1表示砍了（校门外的树）
int main()
{
	
	int l=0,m=0;//l为树的总数，m为区域数。
	int i=0,j=0;
	int count=0;
	int arr1[10001]={0};//存放马路长度
	int arr2[2]={0};//存放区域的起始点和终止点的坐标
	scanf("%d %d",&l,&m);//输入马路长度和区域数
	for(i=0;i<m;i++)//以区域数控制输入起始点和终止点的坐标的个数
	{
	   for(j=0;j<2;j++)//循环一次放入区域的起始点和终止点的坐标
       scanf("%d",&arr2[j]);
	   for(j=0;j<=l;j++)//直接使用区域的起始点和终止点的坐标进行比较赋值1
	   {
		   if(j<=arr2[1]&&j>=arr2[0])//这样赋值可以覆盖
			   arr1[j]=1;
	   }
	}
	for(i=0;i<=l;i++)//注意i<=1因为l为树的总数，若无等于号则会少一颗树
	{
		if(arr1[i]==0)//求未砍的树
			count++;
	}
	printf("%d\n",count);
	return 0;
}
#include<stdio.h>//冒泡排序,升序；可以使用任意数组的数进行排序；
void bubble_sort (int arr[],int sz)
{
	int i=0,j=0;
    int flag=1;
	for(i=0;i<sz-1;i++)//控制交换的次数
	{
		flag=1;//每进入循环一次就给flag重新初始化
		for(j=0;j<sz-i-1;j++)//冒泡一次
		{

			if(arr[j]>arr[j+1])//比较arr[j]与arr[j+1],较大就交换。
			{                  //交换二者的值千万别错了
							int tmp=arr[j+1];
							arr[j+1]=arr[j];
							arr[j]=tmp;
							flag=0;
			}

		}//一次冒泡完成跳出循环，进行比较，若if未执行则再进行第二次冒泡，
		          if(flag==1)//若执行了if跳出最外层for循环，说明已经有序不需要再进行比较，减少了计算时间
	          {
		          break;
	          }
	}
}
	int main()
{
	int sz=0,i=0;
	int arr[]={1,2,3,4,5,6,7,8,10,9};
	sz=sizeof(arr)/sizeof(arr[0]);
	bubble_sort(arr,sz);
	for(i=0;i<sz;i++)
	{
		printf("%d ",arr[i]);
	}
	return 0;
}
#include<stdio.h>
int main()
{
	int arr[]={1,2,3,4,5,6,7};
	printf("%p\n",arr);
	printf("%p\n",arr+1);
	printf("%p\n",&arr[0]);
	printf("%p\n",&arr[0]+1);
	printf("%p\n",&arr);
	printf("%p\n",&arr+1);
	return 0;
}


//test.c
#include"game.h"
void menu()
{
	printf("******************\n");
	printf("**1.play  0.exit**\n");
	printf("******************\n");
}
void game()
{
	char mine[ROWS][COLS]={0};//存放雷的信息
	char show[ROWS][COLS]={0};//显示雷的信息
	//初始化棋盘
	InitBoard(mine,ROWS,COLS,'0');//这个是非常细节的传过去的是0，
	InitBoard(show,ROWS,COLS,'*');//这个初始化为*
	//打印棋盘
	//DisplayBoard(mine,ROW,COL);
	DisplayBoard(show,ROW,COL);
	//放入雷
	SetMine(mine,ROW,COL);
	DisplayBoard(mine,ROW,COL);
	//排查雷
	FindMine(mine,show,ROW,COL);
}
void test()
{
	int input=0;
	srand((unsigned int)(time(NULL)));
	do
	{
		menu();
		printf("请选择:>");
        scanf("%d",&input);
        switch(input)
		{
		case 0:
			{
				printf("退出游戏\n");
				break;
			}
		case 1:
			{
				game();
				break;
			}
		default:
			{
				printf("输入错误，请重新选择\n");
				break;
			}
		}
	}
	while(input);
}
int main()
{
	test();
	return 0;
}

//game.c
//实现9*9的棋盘要使用11*11的棋盘存放，每个棋盘就是一个char型数组
//一个棋盘存放雷的信息，一个存放显示雷的信息，0表示没有雷，1表示有雷
//显示雷信息的数字表示该数字周围有多少个雷
#include "game.h"
static int get_mine_count(char mine[ROWS][COLS],int x,int y)//得到（x,y）坐标周围雷个数
{
	return mine[x-1][y]+//将坐标（x,y）周围的八个字符类型元素加起来减去8个字符0得到就是返回的雷个数
		mine[x-1][y-1]+
		mine[x][y-1]+
		mine[x+1][y-1]+
		mine[x+1][y]+
		mine[x+1][y+1]+
		mine[x][y+1]+
		mine[x-1][y+1]-8 * '0';
}
void InitBoard(char board[ROWS][COLS],int rows,int cols,char set)//将game.h中的两个函数结合为一个函数，传入参数的不同那么
{                                                                //初始化的值不同，两个函数分别调用同一个初始化函数
	int i=0,j=0;
	for(i=0;i<rows;i++)
	{
		for(j=0;j<cols;j++)
		{
			board[i][j]=set;//不用加'set',不然直接报错
		}
	}
}
void DisplayBoard(char board[ROWS][COLS],int row,int col)//棋盘不够好，不能准确找到行和列
{
	int i=0,j=0;
	printf("-----扫雷游戏-----\n");
    for(i=0;i<=col;i++)
	{
		printf("%d ",i);
	}
	printf("\n");
	for(i=1;i<=row;i++)
	{
		printf("%d ",i);
		for(j=1;j<=col;j++)
		{
			printf("%c ",board[i][j]);
 		}
		printf("\n");
	}
	printf("-----扫雷游戏-----\n");

}
void SetMine(char mine[ROWS][COLS],int row,int col)
{
	//布置十个雷，布置一个count-1当count=0使停止循环
	int count=10;
	while(count)
		{
			int x=rand()%row+1;//产生的x,y坐标应该在1-9之间%9余数在0-8之间加1就在1-9之间
			int y=rand()%col+1;//若%10则产生0-9之间，不满足效果
			//判断是否放雷，无雷才能放入
			if(mine[x][y]=='0')
			{
				mine[x][y]='1';
				count--;
			}
		}
}
//排查雷，1输入雷的坐标 2.检查雷数量
void FindMine(char mine[ROWS][COLS],char show[ROWS][COLS],int row,int col)
{
	int count=0;
	int x=0,y=0;
	printf("请输入所要排查的坐标:>");
    scanf("%d%d",&x,&y);//x>=1&&x<=row
	while(1)
  {
		if(x>=1 && x<=row && y>=1 && y<=col)
	{
		if(mine[x][y]=='1')
		{
			printf("很遗憾，你被炸死了\n");
			DisplayBoard(mine,row, col);//打印棋盘，让玩家看到怎么被炸死的，调用函数
			break;
		}
		else
		{
			//写一个函数统计雷的个数
			count=get_mine_count(mine,x,y); 
			show[x][y]=count+'0';      //拿到了数组周围有几个雷返回的count放入show数组表示周围的雷数量
		    DisplayBoard(show,row,col);//为什么要加‘0’，因为返回的count是数字，而加上‘0’才是字符，而show数组是char类型
		}                        
	}
	else
	{
		printf("坐标不合法，请重新输入");
	}
  }
	
}


//game.h
#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
#define ROW 9
#define COL 9
#define ROWS ROW+2
#define COLS COL+2
//初始化棋盘的函数
void InitBoard(char board[ROWS][COLS],int rows,int cols,char set);//非雷为0，否则为1
//void InitBoard(char show[ROWS][COLS],int rows,int cols,char set);//非雷为*，否则为#
//打印函数
void DisplayBoard(char board[ROWS][COLS],int row,int col);//传递的是11*11的棋盘，所以行与列传递的是9*9
//void DisplayBoard(char show[ROWS][COLS],int row,int col);//两个函数同时调用一个
//设置雷
void SetMine(char mine[ROWS][COLS],int row,int col);
//排雷
void FindMine(char mine[ROWS][COLS],char show[ROWS][COLS],int row,int col);
//统计坐标周围有几个雷的函数
//int get_mine_count(char mine[ROWS][COLS],int x,int y);//该函数无需声明
#include<stdio.h>
int main()
{
	int b=-1;
	int a=b<<1;
	printf("%d\n",a);
	return 0;
}
#include<stdio.h>
int main()
{
	int a=5,b=3;
	//101
	//011
	int c=a&b;
	int d=a|b;
	int e=a^b;
	printf("%d\n%d\n%d\n",c,d,e);
	return 0;
}
//方法1，加减法
#include<stdio.h>//不创建变量换a,b的值,a,b可以是任意数
int main()  
{                     
	int a=5;
	int b=3;
	a=a+b;//该代码有缺陷，如果a,b两个数相加超过了int型能够储存的范围，则会溢出。
	b=a-b;
	a=a-b;
}
//方法2，异或
#include<stdio.h>
int main()
{
	int a=5,b=3;
	//a=101
	//b=011
	a=a^b;//a=110
	b=a^b;//b=101,变成了a的值
	a=a^b;//a=011,变成了b的值
	printf("%d\n%d\n",a,b);
	return 0;
}
#include<stdio.h>//求一个数在内存中的1的个数
int main()       //即求其补码中1的个数,就是求一个二进制数的一的个数
{
	int num=-1;
	int count=0;
    while(num)
	{
		if(num%2==1)
		num=num/2;
		count++;
		
	}
	printf("%d\n",count);
	return 0;
}
上面那个代码有问题取5为死循环下面代码更为巧妙
#include<stdio.h>
int main()
{
	int num=-1;
	int count=0,i=0;
	for(i=0;i<32;i++)//由于数字由32位二进制组成求的是补码的1的个数
	{
		if(num>>i&1==1)//双目运算符优先级比单目运算符更高，所以不需要加（）先算右移
			count++;   
	}
	printf("%d\n",count);
	return 0;
}
#include<stdio.h>
int main()
{
	int arr[10]={0};
	printf("%d\n",sizeof(arr));
	printf("%d\n",sizeof(int [10]));
	printf("%d\n",sizeof(int [5]));
	return 0;
}
#include<stdio.h>
int main()
{
	short s=0;
	int a=10;
	printf("%d\n",sizeof(short));
	printf("%d\n",sizeof(s=5+a));
	printf("%d\n",s);
	return 0;
}


#include<stdio.h>
int main()
{
	int i=0,a=1,b=2,c=3,d=4;
	i=a++&&b++&&d++;//全为真才为真，都要进行运算，建立在a!=0的基础上 
	i=a++||b++||d++;//有一个为真其他的都为真，有真就不用算后面的，b++,d++都不算
	printf("%d\n%d\n%d\n%d\n",a,b,c,d);
	return 0;
}
#include<stdio.h>
int main()
{
	int a=1,b=2;
	int c=1;
	c=(a=a+b,b=2*a,c*b);
	printf("%d\n",c);
	return 0;
}

#include<stdio.h>
int main()
{
    char a=3;
	char b=127;
	char c=a+b;
	printf("%d\n",c);
	return 0;
}
#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
int main()
{
    char a=3;
	char b=127;
	char c=a+b;
	printf("%d\n",c);
	return 0;
}
#include<stdio.h>
int main()
{
	int i=0;
	int arr[10]={0};
	int* p=arr;
	//char* p=arr;
	for(i=0;i<10;i++)
	{
		*(p+i)=1;
		printf("%d\n",arr[i]);
	}
	return 0;
}
#include<stdio.h>
#include<math.h>
int main()
{
	int n=0,arr[10000]={0};
	int i=0,j=0,pp=0;
	scanf("%d",&n);
	for(i=2;i<sqrt(n);i++)
	{
		if(n%i==0)
		{
			pp=i;
			arr[j]=pp;
			j++;
		}
	}
if(j==2)
{
    if(arr[0]>arr[1])
		printf("%d\n",arr[0]);
	else
		printf("%d\n",arr[1]);
}
	return 0;
}

#include<stdio.h>
int main()
{
	int arr[10]={0},i=0;
	int* p=arr;
	for(i=0;i<10;i++)
	{
		*(p+i)=i;
	}
	for(i=0;i<10;i++)
	{
		//printf("%d\n",arr[i]);
		printf("%d\n",*(p+i));
	}
	return 0;
}
#include<stdio.h>//用指针求字符串数组字符的个数
int my_strlen(char *str)
{
	char* start=str;
	char* end=str;
	while(*end!='\0')
	{
		end++;
	}
	return end-start;
}
int main()
{
	char arr[]="bit";
	int len =my_strlen(arr);
	printf("%d\n",len);
	return 0;
}
#include<stdio.h>
int main()
{
	int a=10;
	int* pa=&a;
	int** ppa=&pa;//二级指针
	printf("%d\n",**ppa);
	return 0;
}
#include<stdio.h>
int main()
{
	int a=10,b=20,c=30,i=0;
	int* pa=&a;
	int* pb=&b;
	int* pc=&c;
	int* arr[3]={&a,&b,&c};//指针数组：存放指针的数组
	for(i=0;i<3;i++)
	{
		printf("%d ",*(arr[i]));
	}
	return 0;
}
#include<stdio.h>
int main()
{
	int arr[]={1,2,(3,4),5};
	printf("%d\n",sizeof(arr));
	return 0;
}
#include<stdio.h>
//void Init(int arr[],int sz)//初始化为0
//{
//	int i=0;
//	for(i=0;i<sz;i++)
//	{
//		arr[i]=0;
//	}
//}
void Printf(int arr[],int sz)//打印
{
	int i=0;
	for(i=0;i<10;i++)
	{
		printf("%d ",arr[i]);
	}
printf("\n");
}
void reserve(int arr[],int sz)//置换
{
	int left=0,right=sz-1;
	int i=0,tmp=0;
	while(left<right)
	{
		tmp=arr[left];
	    arr[left]=arr[right];
		arr[right]=tmp;
	    left++;
	    right--;
	}
}
int main()
{
	int arr[10]={1,2,3,4,5,6,7,8,9,10};
	int sz=sizeof(arr)/sizeof(arr[0]);
	//Init(arr,sz);
	Printf(arr,sz);
	reserve(arr,sz);
	Printf(arr,sz);
	return 0;
}
#include<stdio.h>//数组交换
void Printf(int arr[],int sz)//打印
{
	int i=0;
	for(i=0;i<sz;i++)
	{
		printf("%d ",arr[i]);
	}
printf("\n");
}
int main()
{
	int arr1[]={1,3,5,7,9};
	int arr2[]={2,4,6,8,10};
	int tmp=0,i=0;
	int sz=sizeof(arr1)/sizeof(arr1[0]);
	for(i=0;i<sz;i++)
	{
		tmp=arr2[i];
		arr2[i]=arr1[i];
		arr1[i]=tmp;
	}
	Printf(arr1,sz);
	Printf(arr2,sz);
	return 0;
}



#include<stdio.h>
int main()
{
	int a,b,c;
	a=5;
	c=++a;//c=6,a=6
	b=++c,c++,++a,a++;//=的优先级大于，所以++a赋值给b，b=7，c=8,a=8
	b+=a++ +c;//+的优先级大于+=，先算+：a=9,b=8+7+8=23
	printf("a=%d b=%d c=%d\n",a,b,c);//9,23,8
	return 0;
}
方法一:使用库函数进行逆序
#include<string.h>
void reverse_string(char arr[])//逆序打印字符串例如abcd,则打印dcba
{
	int a=strlen(arr);//strlen可以直接求出arr的字符个数不需要传参
	char tmp;
	int i=0;
	int left=0,right=sz-1;
	while(left<right)//若left=right则无需交换，因为指向了同一个元素
	{
		tmp=arr[left];
		arr[left]=arr[right];
		arr[right]=tmp;
		left++;
		right--;
	}
	for(i=0;i<sz;i++)//打印6个，sz=6
	{
		printf("%c ",arr[i]);
	}
	printf("%d\n",a);
}
方法2:使用递归的方法进行逆序
void reverse_string(char arr[])
{
	char tmp=arr[0];
	int len=strlen(arr);
	arr[0]=arr[len-1];
	arr[len-1]='\0';
	if(strlen(arr)>=2)
	reverse_string(arr+1);//当arr+1时数组下标应该为arr[1]然后进行交换
	arr[len-1]=tmp;//交换完成后第一组
}
int main()
{
	char arr[]="abcdefg";
	reverse_string(arr);
	printf("%s\n",arr);
	return 0;
}
#include<stdio.h>//任意数的各个位数之和
//方法1:
int DigitSum(int num)
{
	int i=0;
	while(num)
	{
		i+=num%10;
		num=num/10;
	}
	return i;
}
方法2:递归很神奇的东西
int DigitSum(int num)
{                    
	if(num>9)//递归终止条件
	{        //例如输入1729:第一次算1729的9，第二次172传入得到2，再传入17得到7最后剩下1
		return DigitSum(num/10)+num%10;
	}
	else
	{
		return num;//当只剩下1的时候，1进入函数进行判断小于9返回1,所以递归得到值19
	}
}
int main()//1729=1+7+2+9=19
{
	int num=0,sum=0;
	scanf("%d",&num);
	sum=DigitSum(num);
	printf("sum=%d\n",sum);
	return 0;
}
#include<stdio.h>//n的k次方递归
double Pow(int n,int k)
{
	if(k<0)
	{
		return(1.0/Pow(n,-k));
	}
	else if(k==0)
	{
		return 1;
	}
	else
	{
		return n*Pow(n,k-1);//n的k次方递归
	}
}

int main()
{
   double ret=0;
   int n=0,k=0;
   scanf("%d%d",&n,&k);
   ret=Pow(n,k);
   printf("%lf\n",ret);
   return 0;
}
#include<stdio.h>
typedef struct stu//定义一个结构体变量不占储存空间的大小
{
	char name[10];//在struct前加上一个typedef可以直接使用stu定义类型
	int age[10];
	char sex[10];
	int tele[20];
}stu;//需要加分号,直接使用stu定义类型要在{}加名字相当于将struct stu定义成stu
int main()
{
	struct stu s1;//定义了一个结构体变量的类型，类似于int，此时开辟了空间
	stu s2;
	return 0;
}
#include<stdio.h>
struct S
{
	int a;
	char c;
	char arr[20];
    double d;
};
struct T
{
	char ch[10];
	struct S s;
	char *pc;
};
int main()
{
	char arr[]="hello world";
	struct T t={"hehe",{100,'w',"hello bit",3.14}, arr};//嵌套结构体定义同样需要{}
	printf("%s\n",t.ch);
	printf("%s\n",t.s.arr);
	printf("%s\n",t.pc);
	printf("%d\n",t.s.a);
	printf("%lf\n",t.s.d);
	return 0;
}
#include<stdio.h>
typedef struct stu
{
	char name[10];
	int  age;//年龄是比较小用int即可
	char sex[10];//性别是字符串也用字符数组存放
	char tele[12];//电话号码比较长用字符类型数组存放使用""
}stu;
void print1(stu tmp)//结构体传参仍然需要定义一个结构体接收
{
	printf("%d\n",tmp.age);
	printf("%s\n",tmp.name);
	printf("%s\n",tmp.sex);
	printf("%s\n",tmp.tele);
}
void print2(stu* s)//使用结构体指针接收，若未定义stu那么就要使用struct stu*接
{
	printf("%d\n",s->age);
	printf("%s\n",s->name);
	printf("%s\n",s->sex);
	printf("%s\n",s->tele);
}

int main()
{
	stu s={"李四",10,"man","13133677362"};
	print1(s);//传过去的是定义的s
	print2(&s);//传递的是s的地址
	return 0;
}
#include<stdio.h>
int main()
{
	int i=0;
	int arr[10]={1,2,3,4,5,6,7,8,9,10};
	for(i=0;i<=12;i++)
	{
		printf("hehe\n");
		arr[i]=0;
	}
	return 0;

} 
#include<stdio.h>
int main()
{
	int i=0;
	for(i=0;i<100;i++)
	{
		printf("%d ",i);
	}
	for(i=0;i<100;i++)
	{
		printf("%d ",10-i);//按下F9在此处打上断点按下F5直接跳到此处逻辑运算处
	}
	return 0;
}
#define  _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
int main()
{
	int i=0,sum=0,n=0,ret=1;
	scanf("%d",&n);//3
	for(i=1;i<=n;i++)//1，2，3
	{
		int j=0;ret=1;
		for(j=1;j<=i;j++)
		{
			ret*=j;//ret未初始化为一
		}
		sum+=ret;
	}
	printf("%d\n",sum);
	return 0;
}
#include<stdio.h>
int main()
{
	int i=0;
	int arr[10]={1,2,3,4,5,6,7,8,9,10};
	for(i=0;i<=12;i++)
	{
		printf("hehe\n");
		arr[i]=0;
	}
	return 0;
}
#include<stdio.h>//不高兴的津津
int main()
{
	int a=0,b=0,i=0;
    int max_time=0;
	int arr[7]={0},count=0;
	for(i=0;i<7;i++)
	{
		scanf("%d%d",&a,&b);
		arr[i]=a+b;
        if(arr[i]>8)
			count++;
		if(arr[i]>max_time)
			max_time=arr[i];
	}//将大于8的日期全部存储到了arr数组中
	if(count==0)
		printf("%d",count);
	else
	{
		for(i=0;i<7;i++)
		{
			if(arr[i]==max_time)
			{
				printf("%d",i+1);
				break;
			}
		}
	}
	return 0;
}
#include<stdio.h>
#include<string.h>
void my_strcpy(char* arr1,char* arr2)//写一个与strcpy一样功能的函数
{
    while(*arr2!='\0')//为'\0'才循环
	{
		*arr1=*arr2;//交换元素解引用
		arr1++;//都自增找到下个元素地址
		arr2++;
	}
	*arr1=*arr2;//当arr2为'\0'时，那么在交换一次，即完成了
}
void my_strcpy(char* arr1,char* arr2)//优化代码
{
	    while(*arr1++=*arr2++)//当传输为'b'时,()里面就是'b'，为真，直到为'\0'时，其ASCII码值为0，即程序停止
	{
		;
	}
}
#include<assert.h>
void my_strcpy(char* arr1,const char* arr2)//优化代码
{
	assert(arr1!=NULL);//断言，若为空指针会提醒错误在哪便于Debug
	assert(arr2!=NULL);
	    while(*arr1++=*arr2++)//当传输为'b'时,()里面就是'b'，为真，直到为'\0'时，其ASCII码值为0，即程序停止
	{                         //当arr2放入arr1中时，即源作为接收时，则const会进行报错
		;
	}
}
int main()
{
	char arr1[]="#########";
	char arr2[]="bit";
	strcpy(arr1,arr2);//全部拷贝过去了包括\0，打印\0之前的元素虽然后面还有#但是不打印
	my_strcpy(arr1,NULL);//用地址接受
	printf("%s\n",arr1);
	return 0;
}
#include<stdio.h>
int main()
{
	const int num=10;
	int n=100;
	 //int*const p=&num;//限制了p但是没有限制*p,*p想改可以改变
	const int* p=&num;
	p=&n;
	printf("%d\n",num);
	return 0;
}
#include<stdio.h>
#include<assert.h>
int my_strlen(const char* arr)//注意加上const修饰
{
	int ret=0;
	assert(arr!=NULL);//加上断言
	while(*arr!='\0')
	{
		arr++;
		ret++;
	}
	return ret;
}
int main()
{
	char arr[]="abcdef";
	int len=my_strlen(arr);
	printf("%d\n",len);
	return 0;
}
#define  _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
void print(void)
{
	printf("hehe\n");
}
int main()
{
	print(100);//虽然无需接受参数，但是传参仍不报错
	return 0;
}
#include<stdio.h>
int main()
{
	int a=1;
	//printf("%p\n",a);
	char* p=(char*)&a;
	if(*p==1)
	{
		printf("小端\n");
	}
	else
	{
		printf("大端\n");
	}
	return 0;
}
#include<stdio.h>
int check_sys()
{
	int i=1;
	return (*(char*)&i);
}   //char*只能访问1个字节，即01处，解引用
int main()
{
	int ret=check_sys();
	if(ret==1)
	{
		printf("小端\n");
	}
	else
	{
		printf("大端\n");
	}
	return 0;
}
#include<stdio.h>
int main()
{
    char a=-1;
    //10000000000000000000000000000001
	//11111111111111111111111111111110
	//11111111111111111111111111111111
	//由于-1放入char中，所以只能放
	//11111111
	//打印int型进行整形提升，补符号位得
	//11111111111111111111111111111111
	signed char b=-1;
	//11111111
	//与上述相同所以：
	//11111111111111111111111111111111
	unsigned char c=-1;
	//11111111
	//无符号数高位补0
	//00000000000000000000000011111111
	//其为正数得到结果255
	printf("a=%d,b=%d,c=%d",a,b,c);
	return 0;
}
#include<stdio.h>
int main()
{
	char a=-128;
	//100000000000000000000000 10000000
	//111111111111111111111111 01111111
	//111111111111111111111111 10000000
	//10000000
	//111111111111111111111111 10000000
	printf("%u\n",a);
	//由于打印的是%u所以系统认为他是一个无符号整数，直接原反补相同得到
	//111111111111111111111111 10000000
	//%d-打印有符号数字
	//%u-打印无符号数字
	return 0;
}
#include<stdio.h>
int main()
{
    int i=-20;
	//100000000000000000000000 00010100
	//111111111111111111111111 11101011
	//111111111111111111111111 11101100
	unsigned int j=10;
	//000000000000000000000000 00001010
	//111111111111111111111111 11110110
	//111111111111111111111111111110101
	//100000000000000000000000 00001010
	//1作为符号位得到2+8=-10
	printf("%d\n",i+j);
	return 0;
}
#include<stdio.h>
#include<windows.h>
int main()
{
	unsigned int i;//由于unsigned为无符号数所以-1就是1，进入死循环
	for(i=9;i>=0;i--)
	{
		printf("%u\n",i);
		Sleep(100);//Sleep是以ms做单位，暂停0.1s输出数字，使用window.h的头文件
	}
	return 0;
}
#include<stdio.h>
#include<string.h>
int main()
{
	char a[1000];//char类型数组只能储存-128-127之间的数
	int i;
	for(i=0;i<1000;i++)
	{
		a[i]=-1-i;
	}//-1~-1000
	printf("%d",strlen(a));//strlen遇到'\0'停止，即是遇到字符0停止，根据循环圈得到结果
	return 0;
}
#include<stdio.h>//死循环，因为达到256时，进入循环变成0，再一直进行循环
unsigned char i=0;
int main()
{
	unsigned char i=0;
	for(i=0;i<=255;i++)
	{
		printf("hello world\n");
	}
	return 0;
}
#include<stdio.h>
int main()
{
	double d=1E10;
	1E10就是，1.0*10的10次方
	printf("%lf\n",d);
	printf("%d\n",sizeof(float));
	int n=9;
	float *pFloat=(float*)&n;
	printf("%d\n",n);
	printf("%f\n",*pFloat);
	*pFloat=9.0;
	printf("%d\n",n);
	printf("%f\n",*pFloat);
	return 0;
}
#include<stdio.h>
int main()
{
	int n=9;
	//0 00000000 00000000000000000000101-9补码
	//
	float *pFloat=(float*)&n;
	printf("%d\n",n);//9
	printf("%f\n",*pFloat);//0.000000
	//(-1)^0*00000000000000000000101*2^-126无限接近0，所以得到结果打印为0
	*pFloat=9.0;
	//1001.0
	//（-1）^0*1.001*2^3
	//S=0 M=001 E=3->129
	//0 10000001 00100000000000000000000
	//上面的二进制数字转化为10进制则为1091567616
	printf("%d\n",n);
	printf("%f\n",*pFloat);//9.000000
    return 0;
}
#include<stdio.h>
int main()
{
	float a=5.5;
	//5.5
	//101.1
	//(-1)^0*1.011*2^2
	//S=0
	//M=1.011
	//E=2
	//0 E+129 M
	//0100 0000 1011 0000 0000 0000 0000 0000
	//0x40b00000,此为a的地址
	return 0;
}
#include<stdio.h>
void test(int arr[])
{
	int ret=sizeof(arr)/sizeof(arr[0]);
	printf("%d\n",ret);
}
int main()
{
	int arr[10]={0};
	test(arr);
	return 0;
}
#include<stdio.h>
int main()
{
	const char* p="abcdef";//把"abcdef"看成一个常量字符串
	printf("%c\n",*p);//存入的其实是首元素a
	//*p='W';//这样的写法是错误的，存入了指针常量其值不能改变，要在char前加一个const
	printf("%s\n",p);
	return 0;
}
#include<stdio.h>
int main()
{
	char arr1[]="abcdef";
	char arr2[]="abcdef";
	const char* p1="abcdef";
	const char* p2="abcdef";
	//if(arr1==arr2)//代表元素首地址，两个数组不同开辟的空间也不一样所以不相等
	//{             //打印haha
	//	printf("hehe\n");
	//}
	//else
	//{
	//	printf("haha\n");
	//}
    if(p1==p2)//同一个字符串所以首地址相同，打印hehe
	{             
		printf("hehe\n");
	}
	else
	{
		printf("haha\n");
	}
	return 0;
}
#include<stdio.h>
int main()
{
	int arr1[]={1,2,3,4,5};
	int arr2[]={2,3,4,5,6};
	int arr3[]={3,4,5,6,7};
	int* parr[]={arr1,arr2,arr3};//指针数组
	int i=0,j=0;
	for(i=0;i<3;i++)
	{
		for(j=0;j<5;j++)
		{
			printf("%d ",*(parr[i]+j));//parr[]为首元素地址+j向后遍历
		}
		printf("\n");
	}
   	return 0;
}
#include<stdio.h>
int main()
{
	//int arr[10]={1,2,3,4,5,6,7,8,9,10};
	//int (*p)[10]=&arr;//数组指针，还是指针
	//int *p[10]={arr};//指针数组，这个是数组
    char* arr[5];//指针数组
	char*(*pa)[5]=&arr;//存放指针数组
	//[5]代表指向的数组是五个元素的
	int arr2[10]={0};//数组
	int(*pa2)[10]=&arr2;//存放数组的指针
	return 0;
}
#include<stdio.h>
extern "C" void fd();
extern "C" void fc();
int x=0;
int main()
{
	printf("%d\n",x);
	 fd();
	 fc();
	x++;
	printf("%d\n",x);
	return 0;
}
#include<stdio.h>
void print1(int arr[][5],int x,int y)//二维数组列不能少
{
	int i=0,j=0;
	for(i=0;i<x;i++)
	{
		for(j=0;j<y;j++)
		{
			printf("%d ",arr[i][j]);
		}
		printf("\n");
	}
}
void print2(int (*p)[5],int x,int y)//传的是第一行的地址，即第一行所有元素的地址
{                                   
	int i=0,j=0;
	for(i=0;i<x;i++)//代表行，三行，
	{
		for(j=0;j<y;j++)///代表列，5列
		{
			printf("%d ",*(p[i]+j));
		}
		printf("\n");
	}
}
int main()
{
	int arr[3][5]={{1,2,3,4,5},{2,3,4,5,6},{3,4,5,6,7}};
	print1(arr,3,5);
	print2(arr,3,5);
	return 0;
}
#include<stdio.h>
int main()
{
	int arr[10]={1,2,3,4,5,6,7,8,9,10};
	int i=0;
	int (*p)[10]=&arr;
	for(i=0;i<10;i++)
	{
		printf("%d ",*(arr+i));//此四者等价
		printf("%d ",arr[i]);
		printf("%d ",*(p+i));
		printf("%d ",p[i]);
	}
	return 0;
}
#include<stdio.h>
int main()
{
	int arr[5];//存放了5个int类型的数组
	int *parr1[10];//parr1是一个数组，存放10个int*指针类型的数组
	int (*parr2)[10];//是一个指针，指向了一个数组，该数组为10个元素，每个元素为int型
	int (*parr3[10])[5];//是一个数组，该数组有十个元素，每个元素都是一个数组指针，该数组指针指向的数组有5个元素，每个元素都是int型
	return 0;
}
#include<stdio.h>
void test1(int (*arr)[5])//三行五列传递的是第一行的地址
{}                       //*arr代表是一个指针，【5】则表示是一个5个元素的数组
void test2(int arr[][5])//传参时只可以省略行。不可以省略列。
{}
int main()
{
	int arr[3][5]={0};
	test1(arr);//二维数组传参，传递地址，也可直接传递各个元素用二维数组接收
	test2(arr);
	return 0;
}
#include<stdio.h>
void test(int **ptr)
{}
int main()
{
	int *p;
	int **pp=&p;
	test(&p);//二级指针传参无非就是两种情况：1.传递一级指针的地址
	test(pp);//2.传递二级指针
	int* arr[10]={0};
	test(arr);//还有一种特殊即传递指针数组的首地址，用二级指针接收
	return 0;
}
#include<stdio.h>
int Add(int a,int b)
{
	int z=0;
	z=a+b;
	return z;
}
int main()
{
	//int a=2,b=3;
	//Add(a,b);
	//printf("%p\n",Add);
	//printf("%p\n",Add);
	int (*pa)(int,int)=Add;
	printf("%d\n",(*pa)(2,5));
	return 0;
}
(*(void(*)())0)();//将0强制类型转换为void(*)()此为函数指针，即此时的0是一个函数指针，再进行解引用
                  就是调用以0为地址的该函数，句末的（）即为函数调用
void(*signal(int,void(*)(int)))(int);//signal是函数名，signal(int,void(*)(int))代表接受的类型为int和函数指针void(*)(int)
                                     //剩下的就是void(*)(int),代表返回类型为void(*)(int)的函数指针，
                                     //即返回类型为void,参数为int
//可以对上述函数进行简化即
typedef void(* pfun_t)(int)//用typedef将
pfun_t signal( int, pfun_t)
#include<stdio.h>
int Add(int x,int y)
{
	int z=0;
	z=x+y;
	return z;
}
int main()
{
	int (*p)(int,int)=Add;
	printf("%d\n",(p)(2,3));//对于函数指针来说*有或者没有都不影响结果，但是有意义
	printf("%d\n",(*p)(2,3));//加不加，加几个都不影响结果都是5
	printf("%d\n",(**p)(2,3));
	printf("%d\n",(***p)(2,3));
	return 0;
}
#include<stdio.h>
int Add(int x,int y)
{
	return x+y;
}
int Sub(int x,int y)
{
	return x-y;
}
int Mul(int x,int y)
{
	return x*y;
}
int Div(int x,int y)
{
	return x/y;
}

int main()
{
	int i=0;
	//int* arr[5];//此为指针数组，存放指针的数组，
	int(*parr[4])(int,int)={Add,Sub,Mul,Div};//函数指针的数组，即为存放函数指针的数组
	for(i=0;i<4;i++)
	{
		printf("%d\n",parr[i](2,3));
	}
	return 0;
}
#define  _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
void test1(int (*arr)[5])//三行五列传递的是第一行的地址
{}                       //*arr代表是一个指针，【5】则表示是一个5个元素的数组
void test2(int arr[][5])//传参时只可以省略行。不可以省略列。
{}
int main()
{
	int arr[3][5]={0};
	test1(arr);//二维数组传参，传递地址，也可直接传递各个元素用二维数组接收
	test2(arr);
	return 0;
}
#include<stdio.h>
void test(int **ptr)
{}
int main()
{
	int *p;
	int **pp=&p;
	test(&p);//二级指针传参无非就是两种情况：1.传递一级指针的地址
	test(pp);//2.传递二级指针
	int* arr[10]={0};
	test(arr);//还有一种特殊即传递指针数组的首地址，用二级指针接收
	return 0;
}
#include<stdio.h>
int Add(int a,int b)
{
	int z=0;
	z=a+b;
	return z;
}
int main()
{
	//int a=2,b=3;
	//Add(a,b);
	//printf("%p\n",Add);
	//printf("%p\n",Add);
	int (*pa)(int,int)=Add;
	printf("%d\n",(*pa)(2,5));
	return 0;
}
(*(void(*)())0)();//将0强制类型转换为void(*)()此为函数指针，即此时的0是一个函数指针，再进行解引用
                  就是调用以0为地址的该函数，句末的（）即为函数调用
void(*signal(int,void(*)(int)))(int);//signal是函数名，signal(int,void(*)(int))代表接受的类型为int和函数指针void(*)(int)
                                     //剩下的就是void(*)(int),代表返回类型为void(*)(int)的函数指针，
                                     //即返回类型为void,参数为int
//可以对上述函数进行简化即
typedef void(* pfun_t)(int)//用typedef将
pfun_t signal( int, pfun_t)
#include<stdio.h>
int Add(int x,int y)
{
	int z=0;
	z=x+y;
	return z;
}
int main()
{
	int (*p)(int,int)=Add;
	printf("%d\n",(p)(2,3));//对于函数指针来说*有或者没有都不影响结果，但是有意义
	printf("%d\n",(*p)(2,3));//加不加，加几个都不影响结果都是5
	printf("%d\n",(**p)(2,3));
	printf("%d\n",(***p)(2,3));
	return 0;
}
#include<stdio.h>
int Add(int x,int y)
{
	return x+y;
}
int Sub(int x,int y)
{
	return x-y;
}
int Mul(int x,int y)
{
	return x*y;
}
int Div(int x,int y)
{
	return x/y;
}

int main()
{
	int i=0;
	//int* arr[5];//此为指针数组，存放指针的数组，
	int(*parr[4])(int,int)={Add,Sub,Mul,Div};//函数指针的数组，即为存放函数指针的数组
	for(i=0;i<4;i++)
	{
		printf("%d\n",parr[i](2,3));
	}
	return 0;
}
#include<stdio.h>
int main()
{
	char* my_strcpy(char* dest,const char* src);//const不能丢
	char* (*pf)(char*,const char*);//函数指针
	char* (*pfArr[10])(char*,const char*)={my_strcpy};//函数指针数组
	return 0;
}
#include<stdio.h>
void menu()
{
	printf("******************\n");
	printf("** 1.Add  2.Sub **\n");
	printf("** 3.Mul  3.Div **\n");
	printf("** 5.Xor  0.exit**\n");
	printf("******************\n");
}
int Add(int x,int y)
{
	return x+y;
}
int Sub(int x,int y)
{
	return x-y;
}
int Mul(int x,int y)
{
	return x*y;
}
int Div(int x,int y)
{
	return x/y;
}
int Xor(int x,int y)
{
	return x^y;
}
int main()
{  //parr是一个函数指针数组--也叫转移表，引用以后直接转移到某个函数中了
	int(*parr[])(int,int)={0,Add,Sub,Mul,Div,Xor};//此处[]里可以直接不给元素,方便加元素上去
	int input=0,x=0,y=0;
	do
	{
		menu();
		printf("请选择一个数\n");
	    scanf("%d",&input);
		if(input==0)
		{
			printf("退出\n");
		}
		else if(input>=1&&input<=4)
		{
	       printf("请输入两个操作数\n");
	       scanf("%d%d",&x,&y);
	       printf("%d\n",parr[input](x,y));
		}
		else
		{
			printf("选择错误，请重新选择\n");
		}
	}while(input);
	return 0;
}
int main()//第一种虽然能够达到效果，但是加入另一种算法不够方便
{
	int input=0;
	int x=0,y=0,ret=0;
	do
	{
		menu();
		printf("请选择:>");
		scanf("%d",&input);
		if(input!=0)
	{
		printf("输入两个操作数:\n");
		scanf("%d%d",&x,&y);
		switch(input)
		{
		   case 1:printf("%d\n",Add(x,y));
			   break;
		   case 2:printf("%d\n",Sub(x,y));
			   break;
		   case 3:printf("%d\n",Mul(x,y));
               break;
		   case 4:printf("%d\n",Div(x,y));
			   break;
		   default:
			   printf("选择错误，请重新选择\n");
			   break;
		}
	}
		else printf("退出\n");
	}
	while(input);
	return 0;
}
#include<stdio.h>
int main()
{
	int arr[10]={0};//整形数组
	int (*p)[10]=&arr;//数组指针
	int (*pfArr[4])(int,int);//函数指针数组--它是一个数组那么肯定有一个指针能够存放他的地址
	//指向函数指针数组的指针--存放pfArr的地址
	int (*(*ppfArr)[4])(int,int)=&pfArr;
	//ppfArr是一个指针数组，指向的数组有四个元素
	//指向函数指针数组的类型是int(*)(int , int)
	return 0;
}
#include<stdio.h>
//void print(char arr[])
void print(char* str)//char*类型可用于接收字符串--char arr[]
{
	printf("hehe:%s\n",str);
}
void test(void(*p)(char*))//test接收的是print函数，使用test调用p时，就是调用print函数
{
	printf("test\n");
	p("bit");//输入所要接收的字符串
}
int main()
{
	test(print);
	return 0;
}
#include<stdio.h>
void print(char* str)
{
	printf("%s\n",str);
}
int main()
{
	//int a;
	//int* pa;
	void (*p)(char*)=print;
	(*p)("hello bit");
	 p("hello bit");//加不加*不影响结果
	return 0;
}
#include<stdio.h>
int main()
{
	int a=10;
	char b='a';
	void* p=&a;
	void* c=&b;//1.void* 类型的指针为无类型指针，char ,int都能存放，即可以接受任意类型的指针
	           //2.void* 类型的指针不能进行解引用操作
	           //3.void* 类型的指针不能进行加减整数的操作
	//*p=1;
	p=&b;
	printf("%c\n",p);
	return 0;
}
#include<stdio.h>
#include<stdlib.h>
//void qsort(void* base,size_t num,size_t width,int ( *cmp)(const void*,const void*));
//int (*cmp)(const void* e1,const void* e2),为函数指针，接受的是函数
int cmp_int(const void* e1,const void* e2)//接受两个整形指针进行比较
{
//由于接受的是两个无类型的指针可以用强制类型转换成int*的指针再进行解引用操作，即可找到两个整数
//规定返回的是e1>e2返回>0数
//e1=e2返回=0
//e1<e2返回<0
		return *(int*)e1-*(int*)e2;
}
void test1()
{
	int i=0;
	int arr[10]={9,8,7,6,5,4,3,2,1,0};
	int sz=sizeof(arr)/sizeof(arr[0]);
	qsort(arr,sz,sizeof(arr[0]),cmp_int);//只需要引头文件stdlib.h即可
	for(i=0;i<sz;i++)
	{
		printf("%d ",arr[i]);
	}
}
int main()
{
	test1();
	return 0;
}
#include<stdio.h>
#include<stdlib.h>
int cmp_float(const void* e1,const void* e2)//使用qsort函数的时候的返回值一定要使用int类型，不能使用float,否则报错
{                                           //float类型相加减同样满足qsort的要求，即<0 =0 >0.
	//return *(float*)e1-*(float*)e2;       //此为比较浮点型
	return (int)(*(float*)e1-*(float*)e2);  //把结果（即用()将相减的结果括起来）进行强制类型转换为int也一样能够满足<0 =0 >0.
}                                           

void test2()
{
	int i=0;
	float farr[10]={9.0,8.0,7.0,6.0,5.0,4.0,3.0,2.0,1.0,0.0};
	int sz=sizeof(farr)/sizeof(farr[0]);
	qsort(farr,sz,sizeof(farr[0]),cmp_float);
		for(i=0;i<sz;i++)
	{
		printf("%0.2lf ",farr[i]);
	}
}
int main()
{
	test2();
	return 0;
}
