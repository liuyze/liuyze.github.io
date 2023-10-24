---
title: C
date: 2020-01-05 20:31:36
categories: 
- C/C++
tags:
- C/C++
---
## 1.无重复字符的最长子串（leecode）【有待改进】

*给定一个字符串，请你找出其中不含有重复字符的 **最长子串** 的长度。*

示例 1:

输入: "abcabcbb"
输出: 3 
解释: 因为无重复字符的最长子串是 "abc"，所以其长度为 3。
示例 2:

输入: "bbbbb"
输出: 1
解释: 因为无重复字符的最长子串是 "b"，所以其长度为 1。
示例 3:

输入: "pwwkew"
输出: 3
解释: 因为无重复字符的最长子串是 "wke"，所以其长度为 3。
    请注意，你的答案必须是 子串 的长度，"pwke" 是一个子序列，不是子串。

  >int lengthOfLongestSubstring(string s) {
  >
  >​    int size=s.size();
  >
  >​    int k,i,j,m=0;
  >
  >​    int max=0;
  >
  >​    for(i=0;i<size;i++){
  >
  >​      for(j=m;j<i;j++){
  >
  >​        if(s[i]==s[j]){
  >
  >​          m=j+1;
  >
  >​          break;
  >
  >​        }
  >
  >​      }
  >
  >​      if(i-m+1>max){
  >
  >​        max=i-m+1;
  >
  >​      }
  >
  >​    }
  >
  >​    return max;
  >
  >  }
## 2.
