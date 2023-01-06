### 回溯算法
给你一个 无重复元素 的整数数组 candidates 和一个目标整数 target ，找出 candidates 中可以使数字和为目标数 target 的 所有 不同组合 ，并以列表形式返回。你可以按 任意顺序 返回这些组合。  
candidates 中的 同一个 数字可以 无限制重复被选取 。如果至少一个数字的被选数量不同，则两种组合是不同的。  
输入：candidates = [2,3,6,7], target = 7  
输出：[[2,2,3],[7]]  
解释：  
2 和 3 可以形成一组候选，2 + 2 + 3 = 7 。注意 2 可以使用多次。  
7 也是一个候选， 7 = 7 。  
仅有这两种组合。  
```c++
void dfs(vector<int>& candidates, int target, vector<vector<int>>& ans, vector<int>& combine, int idx) {
    if (idx == candidates.size()) {
        return;
    }
    if (target == 0) {
        ans.push_back(combine);
        return;
    }
    // 直接跳过
    dfs(candidates, target, ans, combine, idx + 1);
    // 选择当前数
    if (target - candidates[idx] >= 0) {
        combine.push_back(candidates[idx]);
        dfs(candidates, target - candidates[idx], ans, combine, idx);
        combine.pop_back();
    }
}

vector<vector<int>> combinationSum(vector<int>& candidates, int target) {
    vector<vector<int>> ans;
    vector<int> combine;
    dfs(candidates, target, ans, combine, 0);
    return ans;
}
```
