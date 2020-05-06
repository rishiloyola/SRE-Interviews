# SRE-Interviews

I am preparing the list of interview questions for SRE/PE role in this repository to help others to prepare for their interviews. Most of these questions are seen before during my interviews.

Please feel free to provide any suggestions either through the pull-request or an issue. Please feel free to add your interview questions in this repo.


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
- **Question:** Given a list of servers and ports write a script to check if you are able to connect on that port.
- **Question:** Identify if there is a SQL injection in the given query. Cover all the corner cases. Basically it was string manipulation question. You just need to check the structure of string inside any double quotation. [Databricks](https://databricks.com/)

## Competitive Coding Questions:
- [Word Break](https://leetcode.com/problems/word-break-ii/) <img src="https://edent.github.io/SuperTinyIcons/images/svg/google.svg" width="20" title="Google" />
- **Question:** Given a string with special character `*`. Replace all the stars in the given string by all the characters and generate all possible strings. Example: `ab*d`. Now generate strings like ab1d, ab2d, etc. <img src="https://edent.github.io/SuperTinyIcons/images/svg/google.svg" width="20" title="Google" />
- An array should be split into two halves such that sum of two arrays is same (order of elements should not be changed)

## Linux troubleshooting
- CPU is under high I/O. How to find the issue?
- What can go wrong in the filesystem?
- What if the system has no more inodes available?
- How to increase your I/O?
- How to tune I/O?
- You can’t see your mounted filesystem. What can be the issue? etc.
- Someone started forkbomb on your system how would you stop it?  <img src="https://edent.github.io/SuperTinyIcons/images/svg/google.svg" width="20" title="Google" />
- How would you troubleshoot network communication between two servers?
- **Question:** You are trying to run the command but it says no more PIDs available. What can be the reason? How will you solve the issue? <img src="https://edent.github.io/SuperTinyIcons/images/svg/google.svg" width="20" title="Google" />
  ```
  Try to think about it from every aspects. There can be following cases
  1) ulimit for your user/group is set to very low. You can't create processes more than ulimit range.
  2) Someone started fork bomb. There are no PIDs available actually.
  3) All PIDs have specific fd in the file system. You are running out of inodes.
  ```
  
- Unable to boot OS. What can be the issue?
 

## System Internals
- How do fork and exec work?
- Linux booting process
- What is swap memory?
- Process memory layout
- What is virtual memory?
- Types of processes
- What (really) happens when you type ls -l in the shell
- What are the difference between external and internal kill command <img src="https://edent.github.io/SuperTinyIcons/images/svg/google.svg" width="20" title="Google" />
- What are the inbuilt Linux commands? <img src="https://edent.github.io/SuperTinyIcons/images/svg/google.svg" width="20" title="Google" />
- Difference between RSS and VSZ?


## System Design
- Design basic api rate limiter
- How many machines do you need when you design an online photo uploading service?(Include SPOF, load balancer) <img src="https://edent.github.io/SuperTinyIcons/images/svg/google.svg" width="20" title="Google" />
- Design message passing system like kafka
- Design distributed key-value pair system.
- How would you shard SQL databases
- Design storage system for tiny url website


## Home Assignment
- [Scheduler Design Mesosphere](https://github.com/chuchao333/mesosphere-challenge)
- [Resource Manager Databricks](https://github.com/awelm/resource-manager)


## Networking
- Explain routing protocol. You can pick any routing protocol.  <img src="https://edent.github.io/SuperTinyIcons/images/svg/google.svg" width="20" title="Google" />
