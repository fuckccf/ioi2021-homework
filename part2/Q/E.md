我们考虑数只有两种情况，要么被乘了某个数，要么没有。我们可以认为是被乘了的数先全被拿走，然后考虑放在哪里。

如果有一个数放在了原先没有数的地方，那么我们可以把所有拿走的数改成都放在这些数的 LCM 位置。

否则每个数都放在了某个倍数的位置，这种方案成立当且仅当我们拿掉的数都有比它大的倍数存在。

我们发现两种情况都可以贪心拿走占据同一个位置最少的数。倍数判据可以做到 $O(A\log \log A)$ 但是 $O(A\log n)$ 足够通过。贪心可以做到 $O(n)$ 但是 $O(n\log n)$ 足够通过。