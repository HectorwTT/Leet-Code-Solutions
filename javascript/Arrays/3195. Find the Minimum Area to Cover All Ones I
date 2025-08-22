var minimumArea = function (grid) {
    const n = grid.length,
        m = grid[0].length;
    let min_i = n,
        max_i = 0;
    let min_j = m,
        max_j = 0;
    for (let i = 0; i < n; i++) {
        for (let j = 0; j < m; j++) {
            if (grid[i][j] === 1) {
                min_i = Math.min(min_i, i);
                max_i = Math.max(max_i, i);
                min_j = Math.min(min_j, j);
                max_j = Math.max(max_j, j);
            }
        }
    }
    return (max_i - min_i + 1) * (max_j - min_j + 1);
};
