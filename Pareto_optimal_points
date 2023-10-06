import random
import time


def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr) // 2
        left_half = arr[:mid]
        right_half = arr[mid:]

        merge_sort(left_half)
        merge_sort(right_half)

        i = j = k = 0

        while i < len(left_half) and j < len(right_half):
            if left_half[i][1] >= right_half[j][1]:
                arr[k] = left_half[i]
                i += 1
            else:
                arr[k] = right_half[j]
                j += 1
            k += 1

        while i < len(left_half):
            arr[k] = left_half[i]
            i += 1
            k += 1

        while j < len(right_half):
            arr[k] = right_half[j]
            j += 1
            k += 1

def compute_staircase(P):
    merge_sort(P)  # Sort points in descending order of Y values using Merge Sort
    staircase = []  # Initialize an empty list to store Pareto-optimal points
    max_x = float('-inf')  # Initialize the maximum x-coordinate to negative infinity
    
    for point in P:
        x, y = point
        
        # If the current point has an x-coordinate higher than the current highest x-coordinate,
        # it is Pareto-optimal. Add it to the staircase.
        if x >= max_x:
            staircase.append(point)
            max_x = x
    
    return staircase

import random

#number of points(n)
n = 10  

# Generate random points
P = [(random.uniform(0, 100), random.uniform(0, 100)) for _ in range(n)]

# Compute the Pareto-optimal staircase of P
start_time= time.time_ns()
staircase = compute_staircase(P)
end_time= time.time_ns()
time_complexity = end_time- start_time
##len_point = len(P)
##print(len_point)
##len_staircase = len(staircase)
##print(len_staircase)
print(f"Execution Time: {time_complexity:.6f} seconds")


# Print the sorted random points and the Pareto-optimal staircase
"""print("Sorted Random Points:")
for point in P:
    print(point)

print("\nPareto-Optimal Staircase:")
for point in staircase:
    print(point)"""
