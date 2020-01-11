## 买股票的最佳时机II
每天都可以买入卖出，单卖出要在买入之后，要收益最大，就只要遍历数组比较后一天的价格比前一天的价格高，就可以执行一次买入卖出操作。这样只要有一点正向的收入都会加到利润中，实现润最大化。

```java
public int maxProfit(int[] prices) {
        if(prices.length < 1) return 0;
        int sum = 0;
        for(int i = 0;i < prices.length-1;i++){
            if(prices[i] < prices[i+1]){
                sum += prices[i+1] - prices[i];
            }
        }
        return sum;
    }
```
