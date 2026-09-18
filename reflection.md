# Reflection

## Questions

1. At what array size did your baseline algorithm become noticeably sluggish to execute?

Ans: The baseline algorithm became noticeably sluggish to execute when the array size was 10,000. So, It seems like the algorithm becomes more and more sluggish when the array size becomes larger.

Below is the output for baseline algorithm and the time it took to run different array size:
```bash
Generated 6 lists with sizes: [100, 500, 1000, 2500, 5000, 10000]
Example list (n=100): [81, 7, 90, -56, 16, -87, 52, -60, 62, -25]...
Baseline (n=100): avg time over 5 runs = 0.000785s
Baseline (n=500): avg time over 5 runs = 0.013037s
Baseline (n=1000): avg time over 5 runs = 0.027279s
Baseline (n=2500): avg time over 5 runs = 0.171515s
Baseline (n=5000): avg time over 5 runs = 0.709616s
Baseline (n=10000): avg time over 5 runs = 2.768232
```

2. Based on your empirical data and the shape of your graph, estimate how long (in seconds, minutes, or hours) your baseline algorithm would take to process an array of $1,000,000$ elements. Show your reasoning.

Ans: For `O(n^2)` algorithm, runtime is proportional to `n^2`. And, I measured baseline algorithm at `n = 10000` to get `2.77s` for execution. Since we want to estimate for `1,000,000` elements, the array will be 100 times larger than `10000` elements. But, the runtime grows by `100^2` ,i.e. `10,000`. So, total estimated time will be `2.77 x 10,000 = 27,700 seconds `approx.

3. Based on your empirical data and the shape of your graph, estimate how long (in seconds, minutes, or hours) your Kadane's algorithm would take to process an array of $1,000,000$ elements. Show your reasoning.

Ans: For `O(n)` algorithm, runtime is proportional to `n`. And, I measured Kadane algorithm at `n = 10000` to get `0.002278s` for execution. Since we want to estimate for `1,000,000` elements, the array will be 100 times larger than `10000` elements. But, the runtime grows by `100`. So, total estimated time will be `0.002278 x 100 = 0.23 seconds `approx.