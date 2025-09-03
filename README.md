# 歯科データの統計解析

## 使用データ
ToothGrowth（R内蔵データ）

## 分析コード
```r
library(ggplot2)
data(ToothGrowth)
t.test(len ~ supp, data = ToothGrowth)
ggplot(ToothGrowth, aes(x=dose, y=len, color=supp)) + geom_point()
