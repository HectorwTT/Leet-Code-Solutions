class Solution {
    public String getPermutation(int n, int k) {
        int fact[]=new int[n+1];
        fact[0]=1;
        for(int i=1; i<n;i++) fact[i]=fact[i-1]*i;
        String nums="123456789".substring(0,n);
        char[] perm=new char[n];

        for(int i=n, j=0; i>0;i--, j++) {
            int p=(k-1)/fact[i-1];
            perm[j]=nums.charAt(p);
            nums=nums.substring(0, p)+nums.substring(p+1);
            k=k-p*fact[i-1];
        }
        return new String(perm);
    }
}
