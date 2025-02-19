stu* arr[n];

    for(int i=0;i<n;i++){
        arr[i]=(stu*)malloc(sizeof(stu));
        scanf("%s", (arr[i]->id));
        getchar();
        scanf("%d", &(arr[i]->a));
        getchar();
        scanf("%d", &(arr[i]->b));
        getchar();
        scanf("%d", &(arr[i]->c));
        arr[i]->aver=(float)(((arr[i]->a)+(arr[i]->b)+(arr[i]->c)))/3.0;
    }
和
 stu* arr = (stu*)malloc(n * sizeof(stu));

    for(int i=0;i<n;i++){
        scanf("%ld", &(arr[i].id));
        getchar();
        scanf("%d", &(arr[i].a));
        getchar();
        scanf("%d", &(arr[i].b));
        getchar();
        scanf("%d", &(arr[i].c));
        arr[i].aver=(float)(((arr[i].a)+(arr[i].b)+(arr[i].c)))/3.0;
    }

为什么这两段代码在表示结构体内部的数据时的表示方法不同？一个是->另一个是.？
这两段代码的主要区别在于使用的指针方式不同。
在 stu* arr[n]; 这种方式中，arr 是一个指针数组，每个元素 arr[i] 本身就是一个指针，所以要访问结构体成员需要使用 -> 操作符。
而在 stu* arr = (stu*)malloc(n * sizeof(stu)); 这种方式中，arr 是一个单独的指针，指向一块连续的内存区域，其中存储了多个结构体。通过 arr[i] 可以获取到具体的结构体对象，所以访问结构体成员使用 . 操作符。


两段不同风格的代码

#include <stdio.h>
#include<stdlib.h>

typedef struct 
{
    char id[11];
    int a;
    int b;
    int c;
    float aver;
}stu;

int main(){
    int n;
    scanf("%d",&n);
    stu* arr[n];

    for(int i=0;i<n;i++){
        arr[i]=(stu*)malloc(sizeof(stu));
        scanf("%s", (arr[i]->id));
        getchar();
        scanf("%d", &(arr[i]->a));
        getchar();
        scanf("%d", &(arr[i]->b));
        getchar();
        scanf("%d", &(arr[i]->c));
        arr[i]->aver=(float)(((arr[i]->a)+(arr[i]->b)+(arr[i]->c)))/3.0;
    }

for(int i=0;i<n-1;i++){
    for(int k=0;k<n-1-i;k++){
    if((arr[k]->aver)>(arr[k+1]->aver)){
        stu *temp=arr[k];
        arr[k]=arr[k+1];
        arr[k+1]=temp;
    }
    }}
for(int i=0;i<n;i++){
    printf("%s %d %d %d %.2f\n",arr[i]->id,arr[i]->a,arr[i]->b,arr[i]->c,arr[i]->aver);
free(arr[i]);}


    

    return 0;
}



#include <stdio.h>
#include <stdlib.h>

typedef struct 
{
    char id[11];
    int a;
    int b;
    int c;
    float aver;
} stu;

int main() {
    int n;
    scanf("%d", &n);
stu* arr = (stu*)malloc(n * sizeof(stu));
也可以修改为结构体数组
Stu arr[n];

    for (int i = 0; i < n; i++) {
        scanf("%s", (arr[i].id));
        getchar();
        scanf("%d", &(arr[i].a));
        getchar();
        scanf("%d", &(arr[i].b));
        getchar();
        scanf("%d", &(arr[i].c));
        arr[i].aver = (float)(((arr[i].a) + (arr[i].b) + (arr[i].c)) / 3.0);
    }

    for (int i = 0; i < n - 1; i++) {
        for (int k = 0; k < n - 1 - i; k++) {
            if ((arr[k].aver) > (arr[k + 1].aver)) {
                stu temp = arr[k];
                arr[k] = arr[k + 1];
                arr[k + 1] = temp;
            }
        }
    }

    for (int i = 0; i < n; i++) {
        printf("%s %d %d %d %.2f\n", arr[i].id, arr[i].a, arr[i].b, arr[i].c, arr[i].aver);
    }

    free(arr);

    return 0;
}
