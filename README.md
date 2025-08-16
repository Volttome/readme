# readme


📌 Purpose of the Code

This module implements Binary Search (both iterative and recursive).
Additionally, it provides helper functions like lower_bound, upper_bound, first_occurrence, and last_occurrence, similar to the functions available in C++ STL.


🧩 Sections
1. binary_search_iterative(a, x)
    ● Iterative implementation of binary search.
    ●Variables:
        ● lo = 0  →  start index
        ● hi = len(a) - 1  →  end index
    ● In a loop while lo <= hi:
       ● Compute mid:
            mid = lo + (hi - lo) // 2
        ● If a[mid] == x → found ✅
        ● If a[mid] < x → search the right half (lo = mid + 1)
        ● Else → search the left half (hi = mid - 1)
    ● If nothing found, returns -1.
binary_search_recursive(a, x)


2. Recursive implementation of binary search.

● Uses an inner function _bs(lo, hi):

● Base case: if lo > hi: return -1

    ● Compute mid: mid = (lo + hi) // 2

    ● If found → return index

    ● If smaller → search right side (_bs(mid + 1, hi))

    ● Else → search left side (_bs(lo, mid - 1))

3. lower_bound(a, x)

    ● Finds the first index of an element that is not less than x (i.e., >= x).

    ● Equivalent to C++ std::lower_bound.

    ● Example:

        ● a = [1,3,3,3,5]

        ● lower_bound(a, 3) → 1


4. upper_bound(a, x)

    ● Finds the first index of an element that is greater than x.

    ● Equivalent to C++ std::upper_bound.
        
    ● Example:

        ● a = [1,3,3,3,5]

        ● upper_bound(a, 3) → 4
