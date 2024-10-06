---
layout: post
title: "Nearby Duplicates"
date: 2024-10-07
categories: array
---

### Problem Description:
Given an integer array nums and an integer k, return true if there are two distinct indices i and j in the array such that nums[i] == nums[j] and abs(i - j) <= k

### Approach:
- Since we only want nearby duplicates there's no need to store the elements at the starting of the array which are greater than k distance
- We use map to store the indices of each element
- iterate over each index of the array and check 
- if it exists in the map and the distance between the indices is < k
- else update the index of the element in the map to current i value

### Pseudo Code
for(int i = 0; i< n ; i++)
{
    if(mp[i].count())
    if(abs(i-mp[arr[i]]<=k)) return true;
    else
    mp[arr[i]]=i;
}
return false;

### Real Life Application
check for duplicate elements in a range of numbers. For example, you could use this problem to check if a number is a duplicate within a certain range of numbers in a database