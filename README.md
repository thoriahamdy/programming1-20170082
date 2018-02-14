# programming1-20170082
Tec tac teo by numbers1
arr1=[a,b,c,d,e,f,g,h,i]
arr2=[a,b,c,d,e,f,g,h,i]
arr3=[0,0,0,0,0,0,0,0,0]
n1=[1,3,5,7,9]
n2=[0,2,4,6,8]
draw=1
count=0
while draw==1:
  while count<=9:
     p=1
     print("|",arr1[0],"|",arr1[1],"|",arr1[2],"|")
     print("|",arr1[3],"|",arr1[4],"|",arr1[5],"|")
     print("|",arr1[6],"|",arr1[7],"|",arr1[8],"|")
     print("n1","=",n1)
     x1=int(input("player1 choose num from n1"))
     for i in range(len(n1)):
        if n1[i]==x1:
          n1.remove(n1[i])
          p=0
          break
     while p==1:    
        print("n1","=",n1)
        x1=int(input("player1 please choose num from n1:"))
     d1=input("player1 choose position from board:")
     p=1
     while p==1:    
        for i in range(len(arr1)):
          if arr1[i]==d1:
             arr2.remove(arr1[i])
             arr1[i]=x1
             arr3[i]=x1
             p=0
             break
        d1=input("player1 please choose position from board:")
     count=count+1     
     if ((arr2[0]+arr2[1]+arr2[2]==15) or (arr2[3]+arr2[4]+arr2[5]==15) or (arr2[6]+arr2[7]+arr2[8]==15) or (arr2[2]+arr2[4]+arr2[6]==15) or (arr2[0]+arr2[4]+arr2[8]==15) or (arr2[0]+arr2[3]+arr2[6]==15) or (arr2[1]+arr2[4]+arr2[7]==15) or (arr2[2]+arr2[5]+arr2[8]==15)):
         print("player1 is winner")
         draw=0
         break
     p=1
     print("|",arr1[0],"|",arr1[1],"|",arr1[2],"|")
     print("|",arr1[3],"|",arr1[4],"|",arr1[5],"|")
     print("|",arr1[6],"|",arr1[7],"|",arr1[8],"|")
     print("n2","=",n2)
     x2=int(input("player2 choose num from n2:"))
     for i in range(len(n2)):
        if n2[i]==x2:
          n2.remove(n2[i])
          p=0
          break
     while p==1:    
        print("n2","=",n2)
        x2=int(input("player2 please choose num from n2:"))
     d2=input("player2 choose position from board:")
     p=1
     while p==1:    
        for i in range(len(arr1)):
          if arr1[i]==d1:
             arr2.remove(i)
             arr1[i]=x2
             arr3[i]=x2
             p=0
             break
        d2=input("player2 please choose position from board:") 
     count=count+1    
     if ((arr2[0]+arr2[1]+arr2[2]==15) or (arr2[3]+arr2[4]+arr2[5]==15) or (arr2[6]+arr2[7]+arr2[8]==15) or (arr2[2]+arr2[4]+arr2[6]==15) or (arr2[0]+arr2[4]+arr2[8]==15) or (arr2[0]+arr2[3]+arr2[6]==15) or (arr2[1]+arr2[4]+arr2[7]==15) or (arr2[2]+arr2[5]+arr2[8]==15)):
         print("player2 is winner")
         draw=0
         break
  if draw==1:
     print("no winner,try again")
