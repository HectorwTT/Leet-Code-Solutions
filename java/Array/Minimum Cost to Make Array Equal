class Solution {
    public long minCost(int[] nums, int[] cost) {
        TreeMap<Integer, Long> numCosts = new TreeMap<>();
        for (int i = 0; i < nums.length; i++) {
            numCosts.put(nums[i], numCosts.getOrDefault(nums[i], (long) 0) + cost[i]);
        }
        long preSum = 0;  // exclusive
        long postSum = 0;  // inclusive
        for (int n : numCosts.keySet()) {
            postSum += numCosts.get(n);
        }
        int target = numCosts.firstKey();
        long currCost = 0;
        for (int n : numCosts.keySet()) {
            currCost += Math.abs(n - target) * numCosts.get(n);
        }
        long minCost = currCost;
        while (numCosts.higherKey(target) != null) {
            int nextTarget = numCosts.higherKey(target);
            preSum += numCosts.get(target);
            postSum -= numCosts.get(target);
            currCost += Math.abs(nextTarget - target) * (preSum - postSum);
            minCost = Math.min(minCost, currCost);
            target = nextTarget;
        }
        return minCost;
    }
}
