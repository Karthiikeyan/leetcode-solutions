# LeetCode Solutions

My accepted LeetCode solutions, synced from LeetCode by the LeetSync browser extension. Each folder
holds the problem statement and my submitted code.

![Solved](https://img.shields.io/badge/solved%20on%20LeetCode-1000%2B-f89f1b)
![Contest rating](https://img.shields.io/badge/contest%20rating-1785%20(top%208.7%25)-f89f1b)
![In this repo](https://img.shields.io/badge/in%20this%20repo-132-555)
![C++](https://img.shields.io/badge/C%2B%2B-119-00599c)

**132 solutions here: 43 Hard · 59 Medium · 30 Easy.** Mostly C++ (119), plus Python (10) and Java (4).
They were written between March 2024 and September 2025, most of them in mid-2024. This is a subset of
the 1,000+ problems I've solved overall; I also hold a 3-star rating on CodeChef (max 1685).

## Featured Hard problems

A few solutions I'd point an interviewer to, with the idea behind each.

| Problem | Idea | Complexity |
| --- | --- | --- |
| [Sum of Distances in Tree](863-sum-of-distances-in-tree/) | **Rerooting.** One DFS from node 0 computes subtree sizes and the answer for the root. A second DFS moves the root to each child: `ans[child] = ans[parent] - size[child] + (n - size[child])`, since `size[child]` nodes get one step closer and the rest one step further. | O(n) |
| [Number of Good Paths](2505-number-of-good-paths/) | **Union-Find in value order.** Sort edges by the larger endpoint value and merge components. When two components have the same maximum value, every pair of max-valued nodes across them forms a new good path, so add `countA × countB`. | O(n log n) |
| [Word Ladder II](126-word-ladder-ii/) | **BFS for distances, then backtracking.** BFS records each word's level, then a DFS walks back from the end word only through words exactly one level closer, which builds every shortest path without exploring longer ones. | O(N · L · 26) for BFS, plus output |
| [Minimum Window Substring](76-minimum-window-substring/) | **Sliding window with a need-count map.** Expand right until all characters of `t` are covered, then shrink from the left while the window stays valid, recording the smallest. | O(\|s\| + \|t\|) |
| [Find Median from Data Stream](295-find-median-from-data-stream/) | **Two heaps.** A max-heap holds the lower half and a min-heap the upper half, rebalanced on every insert, so the median is always at the tops. | O(log n) insert, O(1) query |
| [Minimum Number of K Consecutive Bit Flips](1037-minimum-number-of-k-consecutive-bit-flips/) | **Greedy with a flip parity.** Scan left to right and track whether the current bit has been flipped an odd number of times, dropping flips that fall out of the last `k` positions. Flip whenever the effective bit is 0. | O(n) |
| [Wildcard Matching](44-wildcard-matching/) | **2D DP** over string and pattern prefixes, after collapsing runs of `*` into one. A `*` either matches nothing (`dp[i][j-1]`) or one more character (`dp[i-1][j]`). | O(n · m) |
| [Sliding Window Median](480-sliding-window-median/) | Keep the window sorted, insert and erase with binary search, read the middle. Simple and passes; a two-multiset version would bring each step down to O(log k). | O(n · k) |

## All solutions by pattern

Folders are named `<leetcode-internal-id>-<problem-slug>`. The prefix is LeetCode's internal question
id, which isn't always the public problem number, so use the links below.

<details>
<summary><b>Dynamic Programming</b> (24 · 15 Hard)</summary>

| Problem | Difficulty | Solution |
| --- | --- | --- |
| [Best Time to Buy and Sell Stock III](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-iii/) | Hard | [C++](123-best-time-to-buy-and-sell-stock-iii/) |
| [Best Time to Buy and Sell Stock IV](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-iv/) | Hard | [C++](188-best-time-to-buy-and-sell-stock-iv/) |
| [Check if There Is a Valid Parentheses String Path](https://leetcode.com/problems/check-if-there-is-a-valid-parentheses-string-path/) | Hard | [C++](2349-check-if-there-is-a-valid-parentheses-string-path/) |
| [Count Stepping Numbers in Range](https://leetcode.com/problems/count-stepping-numbers-in-range/) | Hard | [C++](2921-count-stepping-numbers-in-range/) |
| [Count Vowels Permutation](https://leetcode.com/problems/count-vowels-permutation/) | Hard | [C++](1332-count-vowels-permutation/) |
| [Distinct Subsequences](https://leetcode.com/problems/distinct-subsequences/) | Hard | [Python](115-distinct-subsequences/) |
| [Distinct Subsequences II](https://leetcode.com/problems/distinct-subsequences-ii/) | Hard | [C++](977-distinct-subsequences-ii/) |
| [Find the Maximum Sum of Node Values](https://leetcode.com/problems/find-the-maximum-sum-of-node-values/) | Hard | [C++](3307-find-the-maximum-sum-of-node-values/) |
| [Frog Jump](https://leetcode.com/problems/frog-jump/) | Hard | [C++](403-frog-jump/) |
| [Longest Increasing Path in a Matrix](https://leetcode.com/problems/longest-increasing-path-in-a-matrix/) | Hard | [C++](329-longest-increasing-path-in-a-matrix/) |
| [Maximum Deletions on a String](https://leetcode.com/problems/maximum-deletions-on-a-string/) | Hard | [C++](2510-maximum-deletions-on-a-string/) |
| [Minimum Cost to Cut a Stick](https://leetcode.com/problems/minimum-cost-to-cut-a-stick/) | Hard | [Python](1669-minimum-cost-to-cut-a-stick/) |
| [Number of Increasing Paths in a Grid](https://leetcode.com/problems/number-of-increasing-paths-in-a-grid/) | Hard | [C++](2409-number-of-increasing-paths-in-a-grid/) |
| [Wildcard Matching](https://leetcode.com/problems/wildcard-matching/) | Hard | [C++](44-wildcard-matching/) |
| [Word Break II](https://leetcode.com/problems/word-break-ii/) | Hard | [C++](140-word-break-ii/) |
| [Best Team With No Conflicts](https://leetcode.com/problems/best-team-with-no-conflicts/) | Medium | [C++](1748-best-team-with-no-conflicts/) |
| [Different Ways to Add Parentheses](https://leetcode.com/problems/different-ways-to-add-parentheses/) | Medium | [C++](241-different-ways-to-add-parentheses/) |
| [Maximum Alternating Subsequence Sum](https://leetcode.com/problems/maximum-alternating-subsequence-sum/) | Medium | [C++](2022-maximum-alternating-subsequence-sum/) |
| [Maximum Length of Pair Chain](https://leetcode.com/problems/maximum-length-of-pair-chain/) | Medium | [C++](646-maximum-length-of-pair-chain/) |
| [Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/) | Medium | [C++](152-maximum-product-subarray/) |
| [Minimum Falling Path Sum](https://leetcode.com/problems/minimum-falling-path-sum/) | Medium | [C++](967-minimum-falling-path-sum/) |
| [Ones and Zeroes](https://leetcode.com/problems/ones-and-zeroes/) | Medium | [C++](474-ones-and-zeroes/) |
| [Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings/) | Medium | [C++](647-palindromic-substrings/) |
| [Triangle](https://leetcode.com/problems/triangle/) | Medium | [C++](120-triangle/) |

</details>

<details>
<summary><b>Graphs (BFS / DFS / Union-Find / Topological sort)</b> (12 · 5 Hard)</summary>

| Problem | Difficulty | Solution |
| --- | --- | --- |
| [Build a Matrix With Conditions](https://leetcode.com/problems/build-a-matrix-with-conditions/) | Hard | [C++](2472-build-a-matrix-with-conditions/) |
| [Longest Cycle in a Graph](https://leetcode.com/problems/longest-cycle-in-a-graph/) | Hard | [C++](2439-longest-cycle-in-a-graph/) |
| [Number of Good Paths](https://leetcode.com/problems/number-of-good-paths/) | Hard | [C++](2505-number-of-good-paths/) |
| [Shortest Path Visiting All Nodes](https://leetcode.com/problems/shortest-path-visiting-all-nodes/) | Hard | [C++](877-shortest-path-visiting-all-nodes/) |
| [Word Ladder II](https://leetcode.com/problems/word-ladder-ii/) | Hard | [C++](126-word-ladder-ii/) |
| [Clone Graph](https://leetcode.com/problems/clone-graph/) | Medium | [C++](133-clone-graph/) |
| [Find Closest Node to Given Two Nodes](https://leetcode.com/problems/find-closest-node-to-given-two-nodes/) | Medium | [C++](2438-find-closest-node-to-given-two-nodes/) |
| [Keys and Rooms](https://leetcode.com/problems/keys-and-rooms/) | Medium | [C++](871-keys-and-rooms/) |
| [Maximum Total Importance of Roads](https://leetcode.com/problems/maximum-total-importance-of-roads/) | Medium | [C++](2379-maximum-total-importance-of-roads/) |
| [Most Stones Removed with Same Row or Column](https://leetcode.com/problems/most-stones-removed-with-same-row-or-column/) | Medium | [C++](984-most-stones-removed-with-same-row-or-column/) |
| [Number of Closed Islands](https://leetcode.com/problems/number-of-closed-islands/) | Medium | [C++](1380-number-of-closed-islands/) |
| [Rotting Oranges](https://leetcode.com/problems/rotting-oranges/) | Medium | [C++](1036-rotting-oranges/) |

</details>

<details>
<summary><b>Trees</b> (9 · 3 Hard)</summary>

| Problem | Difficulty | Solution |
| --- | --- | --- |
| [Cycle Length Queries in a Tree](https://leetcode.com/problems/cycle-length-queries-in-a-tree/) | Hard | [C++](2597-cycle-length-queries-in-a-tree/) |
| [Longest Path With Different Adjacent Characters](https://leetcode.com/problems/longest-path-with-different-adjacent-characters/) | Hard | [C++](2364-longest-path-with-different-adjacent-characters/) |
| [Sum of Distances in Tree](https://leetcode.com/problems/sum-of-distances-in-tree/) | Hard | [C++](863-sum-of-distances-in-tree/) |
| [Balance a Binary Search Tree](https://leetcode.com/problems/balance-a-binary-search-tree/) | Medium | [C++](1285-balance-a-binary-search-tree/) |
| [Count Good Nodes in Binary Tree](https://leetcode.com/problems/count-good-nodes-in-binary-tree/) | Medium | [C++](1544-count-good-nodes-in-binary-tree/) |
| [Delete Leaves With a Given Value](https://leetcode.com/problems/delete-leaves-with-a-given-value/) | Medium | [C++](1450-delete-leaves-with-a-given-value/) |
| [Distribute Coins in Binary Tree](https://leetcode.com/problems/distribute-coins-in-binary-tree/) | Medium | [C++](1021-distribute-coins-in-binary-tree/) |
| [Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/) | Medium | [C++](236-lowest-common-ancestor-of-a-binary-tree/) |
| [Path Sum II](https://leetcode.com/problems/path-sum-ii/) | Medium | [C++](113-path-sum-ii/) |

</details>

<details>
<summary><b>Sliding Window / Two Pointers</b> (8 · 4 Hard)</summary>

| Problem | Difficulty | Solution |
| --- | --- | --- |
| [Minimum Number of K Consecutive Bit Flips](https://leetcode.com/problems/minimum-number-of-k-consecutive-bit-flips/) | Hard | [C++](1037-minimum-number-of-k-consecutive-bit-flips/) |
| [Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/) | Hard | [C++](76-minimum-window-substring/) |
| [Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/) | Hard | [C++](239-sliding-window-maximum/) |
| [Sliding Window Median](https://leetcode.com/problems/sliding-window-median/) | Hard | [C++](480-sliding-window-median/) |
| [Append Characters to String to Make Subsequence](https://leetcode.com/problems/append-characters-to-string-to-make-subsequence/) | Medium | [C++](2572-append-characters-to-string-to-make-subsequence/) |
| [Boats to Save People](https://leetcode.com/problems/boats-to-save-people/) | Medium | [C++](917-boats-to-save-people/) |
| [Sort Colors](https://leetcode.com/problems/sort-colors/) | Medium | [C++](75-sort-colors/) |
| [Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/) | Medium | [C++](167-two-sum-ii-input-array-is-sorted/) |

</details>

<details>
<summary><b>Heaps, Greedy & Sorting</b> (12 · 5 Hard)</summary>

| Problem | Difficulty | Solution |
| --- | --- | --- |
| [Find Median from Data Stream](https://leetcode.com/problems/find-median-from-data-stream/) | Hard | [C++](295-find-median-from-data-stream/) |
| [IPO](https://leetcode.com/problems/ipo/) | Hard | [C++](502-ipo/) |
| [Minimum Cost to Equalize Array](https://leetcode.com/problems/minimum-cost-to-equalize-array/) | Hard | [C++](3402-minimum-cost-to-equalize-array/) |
| [Minimum Cost to Hire K Workers](https://leetcode.com/problems/minimum-cost-to-hire-k-workers/) | Hard | [C++](887-minimum-cost-to-hire-k-workers/) |
| [Patching Array](https://leetcode.com/problems/patching-array/) | Hard | [C++](330-patching-array/) |
| [Design a Food Rating System](https://leetcode.com/problems/design-a-food-rating-system/) | Medium | [C++](2429-design-a-food-rating-system/) |
| [Hand of Straights](https://leetcode.com/problems/hand-of-straights/) | Medium | [C++](876-hand-of-straights/) |
| [K-th Smallest Prime Fraction](https://leetcode.com/problems/k-th-smallest-prime-fraction/) | Medium | [C++](802-k-th-smallest-prime-fraction/) |
| [Longest Square Streak in an Array](https://leetcode.com/problems/longest-square-streak-in-an-array/) | Medium | [C++](2586-longest-square-streak-in-an-array/) |
| [Maximize Happiness of Selected Children](https://leetcode.com/problems/maximize-happiness-of-selected-children/) | Medium | [C++](3351-maximize-happiness-of-selected-children/) |
| [Minimum Difference Between Largest and Smallest Value in Three Moves](https://leetcode.com/problems/minimum-difference-between-largest-and-smallest-value-in-three-moves/) | Medium | [C++](1616-minimum-difference-between-largest-and-smallest-value-in-three-moves/) |
| [Score After Flipping Matrix](https://leetcode.com/problems/score-after-flipping-matrix/) | Medium | [C++](891-score-after-flipping-matrix/) |

</details>

<details>
<summary><b>Binary Search</b> (5 · 3 Hard)</summary>

| Problem | Difficulty | Solution |
| --- | --- | --- |
| [Max Sum of Rectangle No Larger Than K](https://leetcode.com/problems/max-sum-of-rectangle-no-larger-than-k/) | Hard | [C++](363-max-sum-of-rectangle-no-larger-than-k/) |
| [Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/) | Hard | [Python](4-median-of-two-sorted-arrays/) |
| [Number of Flowers in Full Bloom](https://leetcode.com/problems/number-of-flowers-in-full-bloom/) | Hard | [C++](2334-number-of-flowers-in-full-bloom/) |
| [Find Right Interval](https://leetcode.com/problems/find-right-interval/) | Medium | [C++](436-find-right-interval/) |
| [Magnetic Force Between Two Balls](https://leetcode.com/problems/magnetic-force-between-two-balls/) | Medium | [C++](1675-magnetic-force-between-two-balls/) |

</details>

<details>
<summary><b>Backtracking & Recursion</b> (7 · 3 Hard)</summary>

| Problem | Difficulty | Solution |
| --- | --- | --- |
| [Find Minimum Time to Finish All Jobs](https://leetcode.com/problems/find-minimum-time-to-finish-all-jobs/) | Hard | [C++](1825-find-minimum-time-to-finish-all-jobs/) |
| [N-Queens](https://leetcode.com/problems/n-queens/) | Hard | [C++](51-n-queens/) |
| [Sudoku Solver](https://leetcode.com/problems/sudoku-solver/) | Hard | [C++](37-sudoku-solver/) |
| [Palindrome Partitioning](https://leetcode.com/problems/palindrome-partitioning/) | Medium | [C++](131-palindrome-partitioning/) |
| [Permutations II](https://leetcode.com/problems/permutations-ii/) | Medium | [C++](47-permutations-ii/) |
| [Subsets](https://leetcode.com/problems/subsets/) | Medium | [C++](78-subsets/) |
| [The k-th Lexicographical String of All Happy Strings of Length n](https://leetcode.com/problems/the-k-th-lexicographical-string-of-all-happy-strings-of-length-n/) | Medium | [C++](1516-the-k-th-lexicographical-string-of-all-happy-strings-of-length-n/) |

</details>

<details>
<summary><b>Strings, Tries & Hashing</b> (12 · 4 Hard)</summary>

| Problem | Difficulty | Solution |
| --- | --- | --- |
| [First Missing Positive](https://leetcode.com/problems/first-missing-positive/) | Hard | [C++](41-first-missing-positive/) |
| [Longest Happy Prefix](https://leetcode.com/problems/longest-happy-prefix/) | Hard | [C++](1508-longest-happy-prefix/) |
| [Sum of Prefix Scores of Strings](https://leetcode.com/problems/sum-of-prefix-scores-of-strings/) | Hard | [C++](2494-sum-of-prefix-scores-of-strings/) |
| [Total Appeal of A String](https://leetcode.com/problems/total-appeal-of-a-string/) | Hard | [C++](2340-total-appeal-of-a-string/) |
| [Compare Version Numbers](https://leetcode.com/problems/compare-version-numbers/) | Medium | [C++](165-compare-version-numbers/) |
| [Continuous Subarray Sum](https://leetcode.com/problems/continuous-subarray-sum/) | Medium | [C++](523-continuous-subarray-sum/) |
| [Find the Length of the Longest Common Prefix](https://leetcode.com/problems/find-the-length-of-the-longest-common-prefix/) | Medium | [C++](3329-find-the-length-of-the-longest-common-prefix/) |
| [Print Words Vertically](https://leetcode.com/problems/print-words-vertically/) | Medium | [C++](1449-print-words-vertically/) |
| [Remove Sub-Folders from the Filesystem](https://leetcode.com/problems/remove-sub-folders-from-the-filesystem/) | Medium | [C++](1350-remove-sub-folders-from-the-filesystem/) |
| [Replace Words](https://leetcode.com/problems/replace-words/) | Medium | [Python](648-replace-words/) |
| [Vowel Spellchecker](https://leetcode.com/problems/vowel-spellchecker/) | Medium | [C++](1006-vowel-spellchecker/) |
| [Zigzag Conversion](https://leetcode.com/problems/zigzag-conversion/) | Medium | [C++](6-zigzag-conversion/) |

</details>

<details>
<summary><b>Linked Lists, Stacks & Design</b> (10 · 1 Hard)</summary>

| Problem | Difficulty | Solution |
| --- | --- | --- |
| [Reverse Nodes in k-Group](https://leetcode.com/problems/reverse-nodes-in-k-group/) | Hard | [C++](25-reverse-nodes-in-k-group/) |
| [Asteroid Collision](https://leetcode.com/problems/asteroid-collision/) | Medium | [C++](735-asteroid-collision/) |
| [Double a Number Represented as a Linked List](https://leetcode.com/problems/double-a-number-represented-as-a-linked-list/) | Medium | [C++](2871-double-a-number-represented-as-a-linked-list/) |
| [Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation/) | Medium | [C++](150-evaluate-reverse-polish-notation/) |
| [Insertion Sort List](https://leetcode.com/problems/insertion-sort-list/) | Medium | [C++](147-insertion-sort-list/) |
| [LRU Cache](https://leetcode.com/problems/lru-cache/) | Medium | [C++](146-lru-cache/) |
| [Remove Nodes From Linked List](https://leetcode.com/problems/remove-nodes-from-linked-list/) | Medium | [C++](2573-remove-nodes-from-linked-list/) |
| [Reorder List](https://leetcode.com/problems/reorder-list/) | Medium | [C++](143-reorder-list/) |
| [Reverse Linked List II](https://leetcode.com/problems/reverse-linked-list-ii/) | Medium | [C++](92-reverse-linked-list-ii/) |
| [Simplify Path](https://leetcode.com/problems/simplify-path/) | Medium | [C++](71-simplify-path/) |

</details>

<details>
<summary><b>Bit Manipulation & Math</b> (3 · 0 Hard)</summary>

| Problem | Difficulty | Solution |
| --- | --- | --- |
| [Count Triplets That Can Form Two Arrays of Equal XOR](https://leetcode.com/problems/count-triplets-that-can-form-two-arrays-of-equal-xor/) | Medium | [Python](1553-count-triplets-that-can-form-two-arrays-of-equal-xor/) |
| [Minimum Operations to Make the Integer Zero](https://leetcode.com/problems/minimum-operations-to-make-the-integer-zero/) | Medium | [C++](2837-minimum-operations-to-make-the-integer-zero/) |
| [Single Number III](https://leetcode.com/problems/single-number-iii/) | Medium | [C++](260-single-number-iii/) |

</details>

<details>
<summary><b>Easy warm-ups</b> (30)</summary>

| Problem | Difficulty | Solution |
| --- | --- | --- |
| [Alternating Groups I](https://leetcode.com/problems/alternating-groups-i/) | Easy | [C++](3463-alternating-groups-i/) |
| [Apple Redistribution into Boxes](https://leetcode.com/problems/apple-redistribution-into-boxes/) | Easy | [C++](3334-apple-redistribution-into-boxes/) |
| [Circular Sentence](https://leetcode.com/problems/circular-sentence/) | Easy | [Python](2580-circular-sentence/) |
| [Count the Number of Special Characters I](https://leetcode.com/problems/count-the-number-of-special-characters-i/) | Easy | [C++](3408-count-the-number-of-special-characters-i/) |
| [Delete Characters to Make Fancy String](https://leetcode.com/problems/delete-characters-to-make-fancy-string/) | Easy | [C++](1302-delete-characters-to-make-fancy-string/) |
| [Evaluate Boolean Binary Tree](https://leetcode.com/problems/evaluate-boolean-binary-tree/) | Easy | [C++](2416-evaluate-boolean-binary-tree/) |
| [Find Center of Star Graph](https://leetcode.com/problems/find-center-of-star-graph/) | Easy | [C++](1916-find-center-of-star-graph/) |
| [Find Pivot Index](https://leetcode.com/problems/find-pivot-index/) | Easy | [C++](724-find-pivot-index/) |
| [Find The Sum Of Encrypted Integers](https://leetcode.com/problems/find-the-sum-of-encrypted-integers/) | Easy | [C++](3367-find-the-sum-of-encrypted-integers/) |
| [Find the Distance Value Between Two Arrays](https://leetcode.com/problems/find-the-distance-value-between-two-arrays/) | Easy | [C++](1486-find-the-distance-value-between-two-arrays/) |
| [Find the Encrypted String](https://leetcode.com/problems/find-the-encrypted-string/) | Easy | [Java](3468-find-the-encrypted-string/) |
| [Find the Number of Good Pairs I](https://leetcode.com/problems/find-the-number-of-good-pairs-i/) | Easy | [C++](3446-find-the-number-of-good-pairs-i/) |
| [Find the Winning Player in Coin Game](https://leetcode.com/problems/find-the-winning-player-in-coin-game/) | Easy | [C++](3511-find-the-winning-player-in-coin-game/) |
| [Height Checker](https://leetcode.com/problems/height-checker/) | Easy | [C++](1137-height-checker/) |
| [Intersection of Two Arrays II](https://leetcode.com/problems/intersection-of-two-arrays-ii/) | Easy | [C++](350-intersection-of-two-arrays-ii/) |
| [Largest Local Values in a Matrix](https://leetcode.com/problems/largest-local-values-in-a-matrix/) | Easy | [C++](2454-largest-local-values-in-a-matrix/) |
| [Largest Positive Integer That Exists With Its Negative](https://leetcode.com/problems/largest-positive-integer-that-exists-with-its-negative/) | Easy | [Python](2524-largest-positive-integer-that-exists-with-its-negative/) |
| [Length of Last Word](https://leetcode.com/problems/length-of-last-word/) | Easy | [Java](58-length-of-last-word/), [Python](58-length-of-last-word/) |
| [Longest Palindrome](https://leetcode.com/problems/longest-palindrome/) | Easy | [C++](409-longest-palindrome/) |
| [Longest Strictly Increasing or Strictly Decreasing Subarray](https://leetcode.com/problems/longest-strictly-increasing-or-strictly-decreasing-subarray/) | Easy | [C++](3372-longest-strictly-increasing-or-strictly-decreasing-subarray/) |
| [Maximum Number of Words You Can Type](https://leetcode.com/problems/maximum-number-of-words-you-can-type/) | Easy | [Python](1264-maximum-number-of-words-you-can-type/) |
| [Minimum Average of Smallest and Largest Elements](https://leetcode.com/problems/minimum-average-of-smallest-and-largest-elements/) | Easy | [C++](3471-minimum-average-of-smallest-and-largest-elements/) |
| [Minimum Number of Moves to Seat Everyone](https://leetcode.com/problems/minimum-number-of-moves-to-seat-everyone/) | Easy | [Java](2148-minimum-number-of-moves-to-seat-everyone/) |
| [Minimum Operations to Exceed Threshold Value I](https://leetcode.com/problems/minimum-operations-to-exceed-threshold-value-i/) | Easy | [Python](3331-minimum-operations-to-exceed-threshold-value-i/) |
| [Relative Sort Array](https://leetcode.com/problems/relative-sort-array/) | Easy | [Java](1217-relative-sort-array/) |
| [Score of a String](https://leetcode.com/problems/score-of-a-string/) | Easy | [C++](3379-score-of-a-string/) |
| [Snake in Matrix](https://leetcode.com/problems/snake-in-matrix/) | Easy | [C++](3533-snake-in-matrix/) |
| [Special Array With X Elements Greater Than or Equal X](https://leetcode.com/problems/special-array-with-x-elements-greater-than-or-equal-x/) | Easy | [C++](1730-special-array-with-x-elements-greater-than-or-equal-x/) |
| [Sum of All Subset XOR Totals](https://leetcode.com/problems/sum-of-all-subset-xor-totals/) | Easy | [C++](1993-sum-of-all-subset-xor-totals/) |
| [Valid Perfect Square](https://leetcode.com/problems/valid-perfect-square/) | Easy | [C++](367-valid-perfect-square/) |

</details>

---

Ten folders contain only a problem statement without a solution file; they are not counted above.
More about me: [github.com/Karthiikeyan](https://github.com/Karthiikeyan) · [sparktime.in](https://sparktime.in)
