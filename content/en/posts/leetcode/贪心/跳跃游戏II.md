---
title: "跳跃游戏II"
date: 2023-10-23T10:37:15+08:00
categories: ["题解"]
tags: ["贪心法"]
draft: false
---

## 题目描述[^1]

## 代码

{{< codes c java python >}}
  {{< code >}}
  ```c
#include <iostream>
#include <vector>

using namespace std;

class Solution {
public:
    int jump(vector<int>& nums) {
        // 数组大小为 1 时, 当前位置即终点.
        if (nums.size() == 1) return 0;
        /**
         * curDistance: 当前覆盖最远距离下标
         * nextDistance: 下一步覆盖最远距离下标
         * ans: 记录走的最大步数.
         */
        int nextDistance = 0, current = 0, ans = 0;
        for (int i = 0; i < nums.size(); i++) {
            // 每个索引能够到达的最大索引(取最大值).
            nextDistance = max (nums[i] + i, nextDistance);
            // 当前索引到达当前能够覆盖到的索引位置
            if (i == current) {
                // 起跳的次数
                ans++;
                // 当前能够覆盖到的索引位置
                current = nextDistance;
                // 覆盖的最大索引 >= 数组最大索引, 停止起跳.
                if (nextDistance >= nums.size() - 1) break;
            }
        }
        return ans;
    }
};

int main() {
    vector<int> nums = {2, 3, 1, 1, 4, 2, 1, 1, 1};
    Solution solution;
    int ans = solution.jump(nums);
    cout << ans << endl;
    return 0;
}

  ```{{< /code >}}
  {{< code >}}
  ```java
  func main(){
    fmt.Printf("Hello World~")
    return
  }
  ```{{< /code >}}
  {{< code >}}
  ```python
  def main():
      print("Hello World~")
      return
  ```{{< /code >}}
  {{< /codes >}}



## 链接
[^1]:跳跃游戏II[https://leetcode.cn/problems/jump-game-ii/description/](https://leetcode.cn/problems/jump-game-ii/description/)