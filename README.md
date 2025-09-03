# 歯科データの統計解析

## 使用データ
ToothGrowth（R内蔵データ）モルモットの歯の成長に対するビタミンCの効果

## 分析コード
```r
library(ggplot2)
data(ToothGrowth)
t.test(len ~ supp, data = ToothGrowth)
ggplot(ToothGrowth, aes(x=dose, y=len, color=supp)) + geom_point()

### 結果
**t検定（サプリメント種類による比較）:**
- オレンジジュース群の平均: 20.66
- ビタミンC群の平均: 16.96
- p-value = 0.06（有意差なし）

**分散分析（投与量による比較）:**
- 投与量による効果は統計的に有意（p = 1.23e-14）
- F値 = 105.1（非常に大きな効果）

### 結論
投与量の増加は明確に歯の成長を促進する。サプリメントの種類による差は統計的に有意ではない。
