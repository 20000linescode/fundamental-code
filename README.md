# fundamental-code
C语言日常基础
#include<stdio.h>
int main()
{
	/*int age=55;
	if(age<18) printf("未成年\n");
	else if(age>=18&&age<50) printf("成年\n");
	else if(age>=50&&age<60) printf("壮年\n");
	else  printf("老年\n");
	return 0;*/
}
#include<stdio.h>
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
#include<stdio.h>
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
#include<stdio.h>
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
#include<stdio.h>
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
#include<stdio.h>
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
#include<stdio.h>
int main()
{
	int i=0,k=0;
	for(i=0,k=0;k=1;i++,k++)
	{k++;}
	printf("%d\n",k);
	
	return 0;
}
#include<stdio.h>
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
#include<stdio.h>
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
