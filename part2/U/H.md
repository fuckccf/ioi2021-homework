我们相对于可以把所有相同 $k$ 长度前缀的字符串放到一个集合，或在后缀。考虑给每种不同前缀建一个点，后缀建一个点。每个字符串都是前缀点到后缀点连的一条边。这就是一个二分图最小覆盖问题了，我们用 Dinic 跑最小割就可以了，只需给两边的点流量赋为 $1$，中间的边流量赋为正无穷。时间复杂度 $O(nk+n^{1.5})$。
