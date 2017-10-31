# Popular-A-B

Popular A+B

Problem Description

这个题目的A和B不是简单的整数，而是两个时间，A和B 都是由3个整数组成，分别表示时分秒，比如，假设A为34 45 56，就表示A所表示的时间是34小时 45分钟 56秒。

 
Input

输入数据有多行组成，首先是一个整数N，表示测试实例的个数，然后是N行数据，每行有6个整数AH,AM,AS,BH,BM,BS，分别表示时间A和B所对应的时分秒。题目保证所有的数据合法。 


Output

对于每个测试实例，输出A+B，每个输出结果也是由时分秒3部分组成，同时也要满足时间的规则（即：分和秒的取值范围在0~59），每个输出占一行，并且所有的部分都可以用32位整数表示。

 
Sample Input

2

1 2 3 4 5 6

34 45 56 12 23 34

 
Sample Output

5 7 9

47 9 30 



解答：

#include<stdio.h>

main()

{int i,j,a,b,c,d,e,f,n,s;

while(scanf("%d",&n)!=EOF)

{    c=0;d=0;e=0;

    for(i=0;i<n;i++)
    
    {   a=0;b=0;c=0;d=0;e=0;f=0;
    
        scanf("%d%d%d%d%d%d",&a,&b,&c,&d,&e,&f);
        
        a=a+d;
        
        b=b+e;c=c+f;
        
        j=0;
        
        while(c>60)
        
        {
        
            c=c-60;
            
            j=j+1;
            
        }
        
        b=b+j;
        
        s=0;
        
        while(b>60)
        
        {
        
            b=b-60;
            
            s=s+1;
            
        }
        
        a=a+s;
        
        printf("%d %d %d\n",a,b,c);
        

    }
    
}

}

