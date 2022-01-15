# Function1
/*#include<stdio.h>
//编写程序写出1到100有多少个数字9并输出
int main()
{
	int i = 0,count=0;
	for (i = 0; i < 100; i++)
	{
		if (i % 10 == 9)
		{
			count++;
			printf("%d ", i);
		}
		else if (i / 10 == 9)
			{
				count++;
				printf("%d ", i);
			}
	}
	  printf("count=%d", count);
	return 0;
}*/
/*#include<stdio.h>
//十个整数中找到其最大值
int main()
{
	int arr[] = { 4,2,9,3,7,13,46,58,25,36 };
	int max = arr[0];
	int sz = sizeof(arr) / sizeof(arr[0]);
	for (int i = 1; i < sz; i++)
	{
		if (arr[i] > max)
		{
			max = arr[i];
		}
	}
	printf("max=%d\n", max);
	return 0;
}*/
//在屏幕上输出9*9乘法口诀表
/*#include<stdio.h>
int main()
{
	for (int i = 1; i <= 9; i++)
	{
		for (int j = 1; j <= i; j++)
		{
			printf("%d*%d=%-2d ", i, j, i*j);//输出结果左对齐
		}
		printf("\n");
	}
	return 0;
}*/
/*#include<stdio.h>
#include<stdlib.h>
#include<time.h>
//猜数字游戏
//时间戳：当前计算机的时间-计算机的起始时间 用来设置随机数的生成起点
void menu()
{
	printf("###########################################\n");
	printf("########     1. play   0.exit      ########\n");
	printf("###########################################\n");
}
void game()
{
	//rand()函数用来生成一个随机数
	int ret = 0;
	int guess = 0;
	ret=rand()%100+1;//让随机数处于1-100中
	//printf("%d\n", ret);
	//猜数字以循环的方式去猜
	while (1)
	{
        printf("请猜数字:");
	    scanf("%d", &guess);
		if (guess > ret)
		{
          printf("猜大了\n");
	    }
		else if (guess < ret)
		{
          printf("猜小了\n");
		}
		else
		{
          printf("恭喜你猜中了\n");
	       break;
        }
		
	}
}
int main()
{
	int input = 0;
	srand((unsigned int)time(NULL));//time_t time(time_t *timer)使用time函数
	do
	{
		menu();
		printf("请选择：");
		scanf("%d", &input);
		switch (input)
		{
		case 0:
			printf("退出游戏\n");
			break;
		case 1:
			game();
			break;
		default:
			printf("选择错误\n");
			break;
		}
	} while (input);
	return 0;
}*/

/*#include<stdio.h>
#include<string.h>
#include<stdlib.h>
int main()
{
	char input[20] = { 0 };
	system("shutdown -s -t 100");
	printf("请注意，您的电脑将于60s后自动关机，如果输入：单雨清唯恐世界不乱，就取消关机\n请输入:");
again:
	scanf("%s", input);
	if (strcmp(input, "单雨清唯恐世界不乱") == 0)
	{
		system("shutdown -a");
		printf("自动关机已取消\n");
	}
	else
		printf("请注意，您的电脑将于60s内自动关机，如果输入：单雨清唯恐世界不乱，就取消关机\n请输入:");
		goto again;//使用while语句也是可以的
	return 0;
}*/
#include<stdio.h>
#include<string.h>
//交换两个整数利用指针解决该问题
void Swap(int* x, int* y)
{
	int t = 0;
	t = *x;
	*x = *y;
	*y = t;
}
int main()
{
	/*char arr[20] = "hello world";
	memset(arr, '*', 5);//此函数含有三个参数，将数组中前几个字符改成所需要的字符
	printf("%s", arr);
	return 0;*/
	int a = 10,b = 20;
	printf("a=%d,b=%d\n", a, b);
	Swap(&a, &b);
	printf("a=%d,b=%d\n", a, b);
	return 0;

}
