# 쇠막대기 자르기 문제 연습 


오늘은 쇠막대기 자르기 문제 연습을 했다 


T = int(input())


for T in range(1, T+ 1):


    n=list(input())
    tmp=0
    check=0
    ans=0
    for i in n:
        if i =='(':
            tmp+=1
            check=1
        else:
            if check==1:
                check=0
                tmp-=1
                ans+=tmp
            else:
                tmp-=1
                ans+=1
    print('#%d %d'%(T,ans))


제출 했던 코드인데 어렵다 ! 

쉽게 푸는 날이 왔으면 좋겠다 

오늘은 꽤나 오랜시간이 걸렸고 사람들과 얘기도 하면서 가까스로 ~~적어봤다