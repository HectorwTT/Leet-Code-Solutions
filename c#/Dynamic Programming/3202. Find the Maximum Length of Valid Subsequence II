public class Solution {
    public int MaximumLength(int[] nums, int k) {
        int[,] dp = new int[k, k];
        int res = 0;
        foreach (int num in nums) {
            int mod = num % k;
            for (int prev = 0; prev < k; prev++) {
                dp[prev, mod] = dp[mod, prev] + 1;
                res = Math.Max(res, dp[prev, mod]);
            }
        }
        return res;
    }
}
