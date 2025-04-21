public class Solution {
    public int NumberOfArrays(int[] differences, int lower, int upper) {
        int x = 0, y = 0, cur = 0;
        foreach (var d in differences) {
            cur += d;
            x = Math.Min(x, cur);
            y = Math.Max(y, cur);
            if (y - x > upper - lower) {
                return 0;
            }
        }
        return (upper - lower) - (y - x) + 1;
    }
}
