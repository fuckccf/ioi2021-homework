注意到当两个方向截到的最大值是相等的时候，图像就一定是合法的。考虑 $(x,y,z)$ 在图形内部当且仅当 $(x,y), (x,z)$ 都各自满足投影的条件。

通过离散化，我们可以处理出 $f(x)$ 表示 $y$ 轴有多长部分是 $\ge x$ 的，以及 $g(x)$ 表示 $z$ 轴。那么我们可知 $f(x)g(x)$ 就是 $\ge x$ 部分的面积。因此答案就是
$$
\int_0^\infty f(x)g(x)\,\mathrm{d}x
$$
不难注意到由于给出的图像是折线图，所以 $f,g$ 都是分段一次函数。那么 $f\cdot g$ 是分段二次函数，其积分是容易计算的。瓶颈在于离散化，也就是 sort。
