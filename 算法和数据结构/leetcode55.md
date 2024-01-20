# LeetCode 55：跳跃游戏

![leetcode55](../Assets/Algo/leetcode55.JPG)

```C++
bool canJump(vector<int>& nums) {
    int n = nums.size(); // 数组长度
    int rightmost = 0; // 最右边的
    for (int i = 0; i < n; i++) { // 遍历
        if (i <= rightmost) {
            // 记录目前能达到的最远距离
            rightmost = max(rightmost, i + nums[i]);
        }
        // 已经到最后一个位置
        if (rightmost >= n - 1) {
            return true;
        }
    }
    // 达不到
    return false;
}
