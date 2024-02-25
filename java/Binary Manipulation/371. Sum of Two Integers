class Solution {
    public int getSum(int a, int b) {
        while ((a&b) != 0) {
            int olda = a;
            a = olda^b;
            b = (olda&b) << 1;
        }
        return a|b;
    }
}
