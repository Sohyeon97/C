# C언어 14주차
-정올 2514번
<br>
<br><b>문제</b>
```
주어진 문자열에서 연속 3개의 문자가 IOI 이거나 KOI인 문자열이 각각 몇 개 있는지 찾는 프로그램을 작성하라.
문자열은 알파벳의 대문자로만 이루어진다. 
예를 들어 "KOIOIOI"라는 문자열은 KOI 1개 , IOI 2개가 포함되어있다.
```

```
#include <stdio.h>
#include <string.h>

int main()
{
    char arr[10001];
    int i,KOI = 0, IOI=0;

    scanf("%s",arr);

    for(i=0; i< strlen(arr) - 2; i++)
    {
        if(arr[i] =='K' && arr[i+1] == 'O' && arr[i+2] == 'I')
        KOI++;
        else if(arr[i] =='I' && arr[i+1]=='O' && arr[i+2] == 'I')
        IOI++;
    }
    printf("%d\n%d",KOI,IOI);

    return 0;   
}
```
<br> <b>ㄴ정답</b>
<br> 각각의 값 접근 '&arr[]', 배열 사용할 땐 & 사용 X

<hr>
