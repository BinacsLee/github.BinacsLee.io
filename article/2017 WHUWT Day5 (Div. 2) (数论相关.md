### 2017-02-17
### 题目链接 https://vjudge.net/contest/149932


## A Codeforces 762 A
寒假做过..素数测试 略
WA 1 边界条件 1 2 3



## B Codeforces 735 D
收税问题 
哥德巴赫猜想：
    
    任意大于2的偶数都可以分解为两个质数之和
    推出——> 任一大于7的奇数可写成三个质数之和 以及三素数定理(充分大的奇质数可以写成三个质数的和
    
对于此题
1 n为偶数 则可分为两个质数 tax为2
2 n为奇数 则
   1) n为质数 tax为1
   2) n不是质数 但n-2是 tax为2
   3) 以上都不是 则可以分为一个偶数(tax=2 和一个质数(tax=1  共计3
WA 1 处理边界条件n==2



## C Aizu 0005
求gcd和lcm 略


## D poj 1930
小数(循环 化分数

RE (
        
        
        int zi=0,mu=1;
        for(int i=2;i<s.size();i++){
            if(s[i]=='.') break;
            zi=zi*10+s[i]-'0';
            mu*=10;
        }
        int div=10;
        int minmu=INF;
        int anszi,ansmu;
        while(mu>=div){
            int fenzi=zi-zi/div;
            int fenmu=mu-mu/div;
            int g=gcd(fenzi,fenmu);
            if(fenmu/g<minmu){
                minmu=fenmu/g;
                anszi=fenzi/g;
                ansmu=fenmu/g;
            }
            div*=10;
        }
        printf("%d/%d\n",anszi,ansmu);
        
        
EXP 1 此类型记住


## E Aizu 0009
数素数个数 略



## F poj 3641
快速幂取模
EXP 1 边界条件
    
    if(x==1||x==2||x==3) return true;
    

