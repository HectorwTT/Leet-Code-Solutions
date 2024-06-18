class Solution {

    public int maxProfitAssignment(
        int[] difficulty,
        int[] profit,
        int[] worker
    ) {
        List<int[]> jobProfile = new ArrayList<>();
        for (int i = 0; i < difficulty.length; i++) {
            jobProfile.add(new int[] { difficulty[i], profit[i] });
        }

        // Sort both worker and jobProfile arrays
        Arrays.sort(worker);
        jobProfile.sort((a, b) -> Integer.compare(a[0], b[0]));

        int netProfit = 0, maxProfit = 0, index = 0;
        for (int i = 0; i < worker.length; i++) {
            // While the index has not reached the end and worker can pick a job
            // with greater difficulty move ahead.
            while (
                index < difficulty.length &&
                worker[i] >= jobProfile.get(index)[0]
            ) {
                maxProfit = Math.max(maxProfit, jobProfile.get(index)[1]);
                index++;
            }
            netProfit += maxProfit;
        }
        return netProfit;
    }
}
