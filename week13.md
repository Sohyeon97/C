# C언어 13주차
- 정올 1430번 : 숫자의 갯수

```
#include <stdio.h>
int main(void){
    
    int a=150, b=266, c=427, sum=0, count=0; //scanf("%d %d %d", &a, &b, &c);
    char t[10]={0};
    
    scanf("%d", &a);
    scanf("%d", &b);
    scanf("%d", &c);
    
    sum = a*b*c
    printf("sum:%d\n",sum);
    
    while(1)
    {
        count = sum % 10;
        sum /= 10;
        t[count]++;
        
        if(sum==0)
        {
            break;
        }
    }
    for (int i=0; i <= 9; i++)
    {
        printf("%d\n", t[i]);
    }
    return 0;
}
```

ㄴ 오류 

```
# include <stdio.h>

int main()
{
	int a,b,c,i;
	int arr[10]={0,};
	long sum=0;
	
	scanf("%d %d %d",&a,&b,&c);
	
	sum = a*b*c;
    
	while(1)
	{
		
		arr[sum%10]+=1;
		sum= sum/10;
		if(sum == 0)
			break;
	}
	
	for(i = 0; i<10; i++)
	{
		printf("%d\n",arr[i]);
	}
	
	return 0;
}
```
<br> ㄴ 정답
