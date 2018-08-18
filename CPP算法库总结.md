# 算法库总结

## algorithm中的

```
count(iter1, iter2, val) 返回 [*iter1, *iter2) 中值等于 val 的个数

count_if(iter1, iter2, p) 返回令一元谓词（单参数的可调用对象） p 为真的元素个数，例如 p 可以用lambda表达式这么写 [](const int& val){return val == 1;}，其中val就是每次迭代时传入谓词的元素

find(iter1, iter2, val) 返回 [*iter1, *iter2) 中第一个指向值为val的迭代器

find_if(iter1, iter2, p) 返回第一个令一元谓词 p 为真的迭代器

find_if_not(iter1, iter2, q) 返回第一个令一元谓词 q 为假的迭代器

find_end(iter1, iter2, iter3, iter4) 返回在 [*iter1, *iter2) 末尾中能匹配 [*iter3, *iter4) 的起始迭代器，可用于匹配最末尾字符串

find_end(iter1, iter2, iter3, iter4, p) 返回在 [*iter1, *iter2) 末尾中 [*iter3, *iter4) 中的元素能使得二元谓词 p 为真的起始迭代器

reverse(iter1, iter2) 将[*iter1, *iter2) 中的元素颠倒顺序

unique(iter1, iter2) 删除重复的元素

lower_bound(iter1, iter2, val) 返回第一个大于或等于给定值的迭代器，要求区间已排序
upper_bound(iter1, iter2, val) 返回第一个大于给定值的迭代器，要求区间已排序
binary_search(iter1, iter2, val) 判断给定值是不是在元素内，在则返回指向该元素的迭代器，否则返回尾后迭代器
equal_range(iter1, iter2, val) 返回等于val的左闭右开区间组成的pair，要求区间已排序
merge(iter1, iter2, iter3, iter4, iter_d) 合并[*iter1, *iter2) 和 [*iter3, *iter4) 到以 iter_d 为起始迭代器的容器，要求 iter_d 到该容器的尾后迭代器能容下这两个区间内所有元素，另外要合并的两个区间必须已排序

max(val1, val2) 返回两者之间最大值
max_element(iter1, iter2) 返回区间内最大元素的迭代器
类似的还有min和min_element

sort(iter1, iter2) 按升序排列区间内元素
sort(iter1, iter2, comp) 以二元谓词为true的比较运算来排序区间内的元素，如sort(iter1, iter2, [](const T& lft, const T& rht){return rht < lft;}) 能按降序排列区间内的元素
```

## numeric 中的

```
accumulate(iter1, iter2, init) 求区间[*iter1, *iter2)元素之和，再加上init的值，如果是数组求和，则令init为零

adajacent_difference(iter1, iter2, iter_d) 将[*iter1, *iter2)中的后一个元素与前一个元素之差写入以 iter_d 为首的后面的区间，*iter_d等于*iter1

partial_sum(iter1, iter2, iter_d) 将区间内的前n项和写入以 iter_d 为首的后面的区间
```

## string中的成员函数

```
str.find(str1) 返回str中第一个匹配子串str1的起始索引，没有返回string::npos，pos的类型为size_type
str.find(str1, pos) 返回str中从索引pos第一个匹配子串str1的起始索引，没有返回string::npos

str.rfind(str2) 返回str中最后一个匹配子串str1的起始索引，没有返回string::npos
str.rfind(str2, pos) 返回str从索引pos开始最后一个匹配子串str1的起始索引，没有返回string::npos
```
