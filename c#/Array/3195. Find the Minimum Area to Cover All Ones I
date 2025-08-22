public class Solution {
    public int MinimumArea(int[][] grid) {
        int n = grid.Length, m = grid[0].Length;
        int min_i = n, max_i = 0;
        int min_j = m, max_j = 0;
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                if (grid[i][j] == 1) {
                    min_i = Math.Min(min_i, i);
                    max_i = Math.Max(max_i, i);
                    min_j = Math.Min(min_j, j);
                    max_j = Math.Max(max_j, j);
                }
            }
        }
        return (max_i - min_i + 1) * (max_j - min_j + 1);
    }
}
