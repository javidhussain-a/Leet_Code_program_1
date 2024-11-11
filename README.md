# Leet_Code_program_1
This program i got from leetcode. This programs mainly belongs to finding the k th max value from the given list.
def find_Kth_max(l,k):  
    if k==len(l)+1:
        return -1
    for i in range(k-1):
        if k>len(l) and len(l)==0:
            return -1
        else:
            l.remove(max(l))
    return l
l=[2,1,3,5,4,6]
k=int(input("Enter K value: -"))
acc=find_Kth_max(l,k)
if(acc==-1):
    print("You are entered k value is out of range")
else:
    print("Max Kth value is :- ",max(acc))
