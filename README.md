# September07_2025
The problem that i solved today in leetcode

Given an integer n, return any array containing n unique integers such that they add up to 0.

Code:
class Solution {
    public int[] sumZero(int n) {
        int[] res=new int[n];
        int ind=0;
        if(n%2==1)
            res[ind++]=0;
        int x=1;
        for(int i=ind;i<n;i+=2)
        {
            res[i]=x;
            res[i+1]=-x;
            x++;
        }
        return res;
    }
}
