# SRE-Interviews

I am preparing the list of interview questions for SRE/PE role in this repository to help others to prepare for their interviews.

Please feel free to provide any suggestions either through the pull-request or an issue.

## Practical Coding Questions:
- [Design In-Memory File System](https://leetcode.com/articles/design-in-memory-file-system/)
- [LFU cache](https://leetcode.com/problems/lfu-cache/)
- [LRU cache](https://leetcode.com/problems/lru-cache/)
- [Insert Delete GetRandom O(1) - Duplicates allowed](https://leetcode.com/problems/insert-delete-getrandom-o1-duplicates-allowed/)
- [Find Duplicate File in System](https://leetcode.com/problems/find-duplicate-file-in-system/)
- [Find k most frequent words from a file](https://www.geeksforgeeks.org/find-the-k-most-frequent-words-from-a-file)
- [How to Sort a Large File](https://www.algosome.com/articles/how-to-sort-large-file.html)
- [Subdomain Visit Count](https://leetcode.com/problems/subdomain-visit-count/)
- [Add and Search Word - Data structure design](https://www.lintcode.com/problem/add-and-search-word-data-structure-design/description)
- [Design Twitter](https://www.lintcode.com/problem/design-twitter/description)
- **Question:** Use minimum bombs to find out the `N` sized ship in `p x r` matrix. Here `p >> N & r >> N`.  <img src="https://edent.github.io/SuperTinyIcons/images/svg/facebook.svg" width="20" title="Facebook" />
  ```
  You can divide p x r matrix in many N x N matrix. Then put the bomb diagonally in each N x N matrix. 
  ```

## Competitive Coding Questions:
- [Word Break](https://leetcode.com/problems/word-break-ii/) <img src="https://edent.github.io/SuperTinyIcons/images/svg/google.svg" width="20" title="Google" />

## Linux troubleshooting
- CPU is under high I/O. How to find the issue?
- What can go wrong in the filesystem?
- What if the system has no more inodes available?
- How to increase your I/O?
- How to tune I/O?
- You can’t see your mounted filesystem. What can be the issue? etc.
- You are trying to create a new process but it says no more process ids what can be the issue? (fork bomb, reached to ulimit etc)
- How would you troubleshoot network communication between two servers?
- **Question:** You are seeing the high workload on your CPU. How would you identify the problem? <img src="https://edent.github.io/SuperTinyIcons/images/svg/facebook.svg" width="20" title="Facebook" />
  ```
  Now there can be two cases:
  1) It is happening because of CPU intensive processes
  2) Or it may be due to high I/O.
  Next you need to narrow down these cases by using various tools. Use top command to check I/O WA time. Checkout utime command. Find out which process is causing this trouble. Then use strace or perf command to find out which function is causing the problem. Then check out which system calls this function is generating. This problem was because of the RAID in the file system. RAID performs sync operation after a specific duration and during that it freezes all read/write operations, From the system call list, you can find out the file system path. Use mount command to find out filesystem type. Now check the configurations and solve it.
  ```


## System Internals
- How do fork and exec work?
- Linux booting process
- What is swap memory?
- Process memory layout
- What is virtual memory?
- Types of processes
- What (really) happens when you type ls -l in the shell


## System Design
- Design basic api rate limiter
- How many machines do you need when you design an online photo uploading service?(Include SPOF)
- Design message passing system like kafka
- Design distributed key-value pair system.
- How would you shard SQL databases
- Design storage system for tiny url website
