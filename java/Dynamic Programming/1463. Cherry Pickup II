class Solution {
    Integer[][][] memo;
    public int cherryPickup(int[][] grid) {
        int m=grid.length,n=grid[0].length;
        memo=new Integer[m][n][n];
        return sol(grid,0,0,grid[0].length-1);
    }
    public int sol(int[][] grid,int r,int c1,int c2){
        int m=grid.length,n=grid[0].length;
        if(r==m) return 0;
        if(c1<0 || c2<0 || c1>=n || c2>=n) return Integer.MIN_VALUE;
        if(memo[r][c1][c2]!=null) return memo[r][c1][c2];
        int ans=grid[r][c1]+grid[r][c2];
        if(c1==c2) ans-=grid[r][c1];
        return memo[r][c1][c2]=Math.max(sol(grid,r+1,c1-1,c2+1),Math.max(sol(grid,r+1,c1-1,c2),Math.max(sol(grid,r+1,c1-1,c2-1),Math.max(sol(grid,r+1,c1,c2+1),Math.max(sol(grid,r+1,c1,c2),Math.max(sol(grid,r+1,c1,c2-1),Math.max(sol(grid,r+1,c1+1,c2+1),Math.max(sol(grid,r+1,c1+1,c2),sol(grid,r+1,c1+1,c2-1)))))))))+ans;
    }
}
