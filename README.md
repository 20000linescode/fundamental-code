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
