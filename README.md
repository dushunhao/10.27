#define _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>

int main()

{

	int n = 0;
  
	int i = 0;
  
	int ret = 1;
  
	int sum = 0;
  
	for (n = 1; n <= 3; n++)
  
	{
  
		ret = 1;
    
		for (i = 1; i <= n; i++)
    
		{
    
			ret *= i;
      
		}
    
		sum += ret;
    
	}
  
	printf("%d\n", sum);
  
	return 0;
  
}



#include<string.h>

int main()

{

	int arr[] = { 1,2,3,4,5,6,7,8,9,10 };
  
	int k = 7;
  
	int sz = sizeof(arr) / sizeof(arr[0]);//数组元素个数
  
	int left = 0;
  
	int right = sz - 1;
  

	while (left <= right)
  
	{
  
		int mid = (left + right) / 2;
    
		if (arr[mid] < k)
    
		{
    
			left = mid + 1;
      
		} 
    
		else if (arr[mid] > k)
    
		{
    
			right =mid - 1;
      
		}
    
		else
    
		{
    
			printf("找到了，下标为:%d\n", mid);
      
			break;
      
		}
    
	}
  
	if (left > right)
  
	{
  
		printf("找不到了\n");
    
	}
  

	return 0;
  
}


int main()

{

	char arr1[] = { "welcome to beijing!!!!!!" };
  
	char arr2[] = { "************************" };
  
	int left = 0;
  
	int right = strlen(arr1) - 1;
  

	while (left <= right)
  
	{
  
		arr2[left] = arr1[left];
    
		arr2[right] = arr1[right];
    
		printf("%s\n", arr2);
    

		left++;
    
		right--;
    
	}
  
	return 0;
  
}



#include<windows.h>

int main()

{

	char arr1[] = { "welcome to beijing!!!!!!" };
  
	char arr2[] = { "************************" };
  
	int left = 0;
  
	int right = strlen(arr1) - 1;
  

	while (left <= right)
  
	{
  
		arr2[left] = arr1[left];
    
		arr2[right] = arr1[right];
    
		printf("%s\n", arr2);
    
		Sleep(1000);//睡眠1秒
    

		left++;
    
		right--;
    
	}
  
	return 0;
  
}



#include<stdlib.h>

int main()

{

  char arr1[] = { "welcome to beijing!!!!!!" };
  
	char arr2[] = { "************************" };
  
	int left = 0;
  
	int right = strlen(arr1) - 1;
  

	while (left <= right)
  
	{
  
		arr2[left] = arr1[left];
    
		arr2[right] = arr1[right];
    
		printf("%s\n", arr2);
    

		Sleep(1000);
    
		system("cls");
    
		left++;
    
		right--;
    
	}
  
	return 0;
  
}


#include<stdlib.h>

void menu()

{

	printf("*********************************\n");
  
	printf("**********  1.play  *************\n");
  
	printf("**********  0.exit  *************\n");
  
	printf("*********************************\n");
  
}




#include<time.h>

void game()

{

	//猜数字游戏的实现
  
	//1.生成随机数
  
	int ret = rand()%100+1;
  
	//printf("%d\n", ret);
  
	//2.猜数字
  
	int guess = 0;
  
	while (1)
  
	{
  
		printf("请输数字:>");
    
		scanf("%d", &guess);
    
		if (guess < ret)
    
		{
    
			printf("猜小了\n");
      
		}
    
		else if(guess > ret)
    
		{
    
			printf("猜大了\n");
      
		}
    
		else
    
		{
    
			printf("恭喜你,猜对了\n");
      
			break;
      
		}
    
	}
  
}


int main()

{

	int input = 0;
  
	srand((unsigned int)time(NULL));
  
	do
  
	{
  
		menu();//打印菜单
    
		printf("请选择:>\n");
    
		scanf("%d", &input);
    
		switch (input)
    
		{
    
		case 1:
    
			game();
      
			break;
      
		case 0:
    
			printf("退出游戏\n");
      
			break;
      
		default:
    
			printf("选择错误，请重新选择\n");
      
			break;
      
		}
    

	} while(input);
  


	return 0;
  
}


int main()

{

	int a = 0;
  
	int b = 0;
  
	int c = 0;
  
	//输入
  
	scanf("%d%d%d", &a, &b, &c);
  
	//调整顺序
  
	if (a < b)
  
	{
  
		int tmp = a;
    
		a = b;
    
		b = tmp;
    
	}
  
	if (a < c)
  
	{
  
		int tmp = a;
    
		a = c;
    
		c = tmp;
    
	}
  
	if (b < c)
  
	{
  
		int tmp = b;
    
		b = c;
    
		c = tmp;
    
	}
  
	//输出
  
	printf("%d %d %d\n", a, b, c);
  
	return 0;
  
}



int main()

{

	int i = 0;
  
	int m = 0;
  
	for (i = 1; i < 34; i++)
  
	{
  
		m = i * 3;
    
		printf("%d ", m);
    
	}
  
	return 0;
  
}



int main()

{

	int i = 0;
  
	for (i = 1; i <= 100; i++)
  
	{
  
		if (0 == i % 3)
    
		{
    
			printf("%d ", i);
      
		}
    
	}
  
	return 0;
  
}


int main()

{

	int m = 0;
  
	int n = 0;
  
	scanf("%d%d", &m, &n);//24,18
  
	//int max = m > n ? m : n;
  
	int max = 0;
  
	//假设最大公约数就是m和n的较小值
  
	if (m > n)
  
	{
  
		max = m;
    
	}
  
	else
  
	{
  
		max = n;
    
	}
  
	while (1)
  
	{
  
		if (m % max == 0 && n % max == 0)
    
		{
    
			printf("最大公约数是%d\n", max);
      
			break;
      
		}
    
		max--;
    
	}
  
	return 0;
  
}


//辗转相除法


int main()

{

	int m = 0;
  
	int n = 0;
  
	scanf("%d%d", &m, &n);
  
	int t = 0;
  
	while (t=m%n)
  
	{
  
		m = n;
    
		n = t;
    
	}
  
	printf("最大公约数：%d\n", n);
  
	return 0;
  
}


//打印1000到2000之间的闰年


int main()

{

	int y = 0;
  
	int count = 0;
  
	for (y = 1000; y <= 2000; y++)
  
	{
  
		if (0 == y % 4 )
    
		{
    
			if (0 != y % 100)
      
			{
      
				printf("%d ", y);
        
				count++;
        
			}
      
		}
    
		if (0 == y % 400)
    
		{
    
			printf("%d ", y);
      
			count++;
      
		}
    
	}
  
	printf("\ncount = %d ", count);
  
	return 0;
  
}


int main()

{

	int y = 0;
  
	int count = 0;
  
	for (y = 1000; y <= 2000; y++)
  
	{
  
		if ((y % 4 == 0 && y % 100 != 0) || (y % 400 == 0))
    
		{
    
			printf("%d ", y);
      
			count++;
      
		}
    
	}
  
	printf("\ncount = %d ", count);
  
	return 0;
  
}


打印100-200之间的素数

质数，1和本身整除


int main()

{

	int i = 0;
  
	for (i = 100; i <= 200; i++)
  
	{
  
		//判断i是否为素数
    
		//2-(i-1)之间，试除i，看能不能整除
    
		int j = 0;
    
		for (j=2;j<i;j++)
    
		{
    
			if (i%j == 0)
      
			{
      
				break;//不是素数
        
			}
      
		}
    
		if (i == j)
    
		{
    
			printf("%d ", i);//i为素数
      
		}
    
	}
  
	return 0;
  
 }
 


int main()

{

	int i = 0;
  
	int count = 0;
  
	for (i = 100; i <= 200; i++)
  
	{
  
		//判断i是否为素数
    
		//2-(i-1)之间，试除i，看能不能整除
    
		int j = 0;
    
		int flag = 1;//假设i就是素数
    
		for (j = 2;j < i; j++)
    
		{
    
			if (i % j == 0)
      
			{
      
				flag = 0;//不是
        
				break;//不是素数
        
			}
      
		}
    
		if (flag == 1)
    
		{
    
			count++;
      
			printf("%d ", i);//i为素数
      
		}
    
		printf("\ncount=%d\n", count);
    

	}
  
	return 0;
  
}
