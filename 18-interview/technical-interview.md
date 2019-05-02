# Technical Interview 

> Make the interviewer engaged!  面试就是一场能力表现赛，让面试官共鸣很重要！


## Why?

> 思考要全面，沟通要流畅，代码要硬核。

* **精心准备**: 胜兵先胜而后求战，败兵先战而后求胜。
* **保持精力**: 面试当天，不要复习。请给当天面试的大脑留满电量的计算资源。
* **平常心态**: 就像和小伙伴一起在解题一样，有问题请当场问。Be a **co-worker** instead of a candidate.
* **当场思考**: 不要依赖记忆，依赖记忆会卡顿，无法呈现出你的逻辑链，而沟通的流畅性却无比重要，请一定一定要现场思考，你可以做得更好哒！
* **自留余地**: Think loud固然好，但有时说话不利于思考。首先是做题(完成)，其次是传达(完善)。 不妨先说：“Could you give me one or two minute to think? I'll tell you my idea later?”
* **系统表达**: 在面试官那里，如果你没说，他便觉得你没有想到。所以，在表达时，一定一定一定要**分类讨论**，全面叙述，细节展开。系统化思考是软件工程师的基本素养。如果觉得时间有限，请总分叙述，一个节点之后适时地问一下：“Would you like me to go into more depth?”

## How?

- **Ask** 
	- Please ask **questions** if you need **clarification**.
	- Why? 
		- We want the interview process to be collaborative.
		- We also want to learn what it would be like to work with you on a day-to-day basis in our open environment.
	- How?
		-  If you are asked a question, but not given enough information to solve the problem, drill down to get the information that you need.
		-  If that information isn’t available, focus on how you would attempt to solve the problem given the limited information you have. Often times at the Company, we have to make quick decisions in the absence of all of the relevant data.
- **Answer**
	- When answering questions, be as **concise** and **detailed** in your response as possible.
	- Why? We realize it’s hard to gauge how much information is too much versus not sufficient enough. 
	- How? An effective litmus test is pausing after your succinct response to ask 
		- if you’ve provided enough detail, 
		- or if the interviewer would like you to go into more depth.
- **Code** 
	- writing scalable, robust, and well-tested code
	- A few missed commas or typos here and there aren’t that big of a deal, but the goal is to write code that’s as close to **production-ready** as possible. This is your chance to show off your coding ability.


## What: Benchmark

- **Problem Solving**: answering correctly, without much help or hints
	- `Struggling`: Had trouble grasping the problem
	- `Decent`: Worked out a rough solution
	- `Good `: Solved the problem with hints
	- `Amazing`: Got an optimal solution with **minimal guidance** 
- **Coding**: bug-less, clean, readable, reusable and maintainable code
	- `Beginner`: Unfamiliar with some of the basics
	- `Decent`: Struggled to get from idea to running code
	- `Strong`: Works but not quite readable, reusable or maintainable
	- `Ninja`: Flawless code: readable, reusable & **maintainable**
- **Communication**: clarity of your answers and line of reasoning
	- `Awkward`: Hardly spoke, or was very unclear
	- `Decent`: I wasn't able to understand some parts
	- `Good`: Communicated well
	- `Amazing`: Every single bit was **crystal** clear

source: [pramp](https://www.pramp.com/dashboard#/) 
 

## What: Flow? 

### Before

- Go through [Do and Don't](https://github.com/yangshun/tech-interview-handbook/blob/master/preparing/cheatsheet.md)

### In

- **Confirm**:
	- Read the questions and Repeat the question back at the interviewer. (input(format & range) -> output)
	- Clarify any assumptions you made subconsciously. Many questions are under-specified on purpose. 	
		- e.g. *Can I assume the input well-formed and non-null? (If not, raise exception)*
	- Work through a small example to ensure you understood the question.
- **Think**:
	- If you don't have any idea, Try it first on **concrete** examples. 🕵️‍♂️ What would do if you just do it by hand?
	- Be quiet for a while is OK but please tell your interviewer you need think quietly for 2 minutes.
	- DFS, BFS, DP, Greedy, Sliding window...
- **Explain**:
	- Explain a high level approach even if it is a brute force one. 
	- Define and confirm **signature** with the interviewer. This helps you clarify with the **interviewer** about required details
		- e.g. Let dp(i) == ? 
	- Clarify the **meaning** of your variable, especially when you define:
		- **Entries** of DP array
		- Hashmap 
	- **Why** do you use this DS and Algorithm? **Pros and Cons?** Trade-off? (show you are reliable with **systematical** thinking approach 💯)
	- Think carefully, then state and explain **the time and space complexity of your approaches**. Ask interviewer if it's okay to go on and code the solution if complexity analysis takes too long to figure out. Interviewer can tell you if it's worth coding it or not.
	- Explain your idea before coding, make sure it makes sense to the interview
	- Use **hints** that the interviewer gives you.
	- Improve upon the approach and optimize. Reduce duplicated work and cache repeated computations.
	- ❌ 💥But don't take too much to explain, otherwise, you don't have enough time to code. (Practice to explain your solution quickly)
- **Code:** 
	- e.g. *Is it good to code?*
	- Coding while you are **talking**
		- **Think loud** but not **murmur**! 💥
	- Check **Edge case** in advance, raise **an exception** if there is edge cases. 💯
	- Base case, General case.
	- Demonstrate mastery of your chosen programming language.
	- Demonstrate technical knowledge in data structures and algorithms.
	- Write **in a modular fashion**. Extract out chunks of repeated code into functions.
	- Ask for permission to use **trivial functions** without having to implement them; saves you some time.
	- If you are cutting corners in your code, state that out loud to your interviewer and **say what you would do in a non-interview setting** (no time constraints). E.g., I would write a regex to parse this string rather than using split() which may not cover all cases.
- **Test**: 
	- Be proactive to find your **bug** after finish your code
	- Be proactive to **propose test cases**: thoroughly tested the code before submitting it (💯 shows you are thoughtful and reliable)
	- Try to be **comprehensive** to cover **corner cases**, when proposing test cases
	- Use table to **go through** test cases when possible. Explain how does states of each variable change, when going through the code.
- **Optimize**:
	- Be proactive to think and propose **optimization** of your current code
		- Look out for places where you can **refactor**.
	- **Reiterate** the time and space complexity of your code.
	- Explain **trade-offs** and how the code/approach can be improved if given more time.




### After

**Questions** to ask:

* tech stack 
* product 
* typical week 
* engineering culture 

👉 More [Quesions](https://github.com/yangshun/tech-interview-handbook/blob/master/non-technical/questions-to-ask.md)


## What: Example?
	
- [a good exmaple: what you are going to do when coding](https://youtu.be/0PcB1aOQHB4)
- [How to: Work at Google — Example Coding/Engineering Interview](https://www.youtube.com/watch?v=XKu_SEDAykw) 

## What: Say?

> Be a co-worker instead of a candidate.

- Should I take care of input input validation?
- Let's write down some **test case** that helps us to understand the problem.
- Can you give me one-two minute to think? I tell you my idea later.
- Can I assume that ... ? **x 10**
- There are **several ideas** that I come up with. We can use A, B or C. Let's try the most intuitive solution first and improve it step by step. If we have time, we can talk about trade-off of each solution.
- Now, let's focus on solution A and let me write a test-case and run it by hand to help you understand my idea.
- Let us analysis the solution's time-complexity and space-complexity to see if it is good enough. 
- I'll code this solution first. I'll explain my other solutions if we have time.
- We need two variables to represent A and B. 
- Let make the code more readable and let us call it X.
- We need a hashmap to store A **so that** we can access X in O(1) time complexity.
- Ok, we implement the solution basically and let me see if there is any bug or any that I can improve.
- Let me write some different test cases to cover typical use cases. 

## What: Terms?

> 流畅沟通，系统表达。

- ideas
- trade-off
- time complexity
- space complexity
- string
- array
- heap
- BFS
- DP
- binary search
- two pointers
- sorting
- test  

### Ideas

* A simple solution would be to use an efficient sorting algorithm to sort the whole array again. This method **also do not use the fact that** array is k-sorted.

### trade-off

* Insertion Sort performs really well for small values of k but it is not recommended for large value of k (use it for k < 12).
* depends on the input parameters
	* There are two strategies to enumerating these neighbors:
		* One strategy is, for every word2 in the given words, check that word and word2 differ by 1.
		* Another strategy is, for every index i from 0 .. word.length - 1 and for every lowercase letter c, clone word into word2, replace word2[i] with c, and check whether the resulting word2 is in words.
	* The decision to use one strategy or another depends on the input parameters.  
	* -- [127. Word Ladder](https://www.pramp.com/challenge/MW75pP53wAtzNPVLPG0d)

### time complexity 

* However, we can do better than that. If we use min heap, we can get an asymptotically better time complexity. 
* Building a heap takes O(K) time for K+1 elements. Insertion into and extraction from the min-heap take O(log(K)), **each**. **Across all three loops**, we do at least one of these actions N times, so the total time complexity is O(N⋅log(K)). if K is **substantially** smaller than N, then we can consider log(K) constant and **argue** that the complexity is **practically linear**.
* Our `fitsOneByte` operation takes **a linear amount of time** and space for each chunk, and **the sum of** the chunks is the whole string.
* O(N*K^2) , where N is the length of words and K is the maximum length of any given word. For each word in words, in order to find neighbors we may **construct O(K) new words**, each in O(K) time. [BFS for LC127]
* we have **three nested loops** whose combined time complexity is O(N^3), where N is the size of arr. We also using sorting in the beginning and that’s additional O(N⋅log(N)). The total time complexity is still O(N^3) because O(N⋅log(N)) **gets thrown away since in the asymptotic calculation it’s not material.** [[LC18 4sum](https://www.pramp.com/challenge/gKQ5zA52mySBOA5GALj9)]

### space complexity

* We need to a maintain min-heap of size K+1 **throughout the algorithm**, so the **auxiliary** space complexity is O(K).
* O(N), the space used when **considering each part** of the original string `ip`.
* O(N), the space typically used by compilers in their implementation of sorting operations.  -- [Absolute Value Sort](https://www.pramp.com/challenge/4E4NW7NjbnHQEx1AxoXE)




### string 

**Key words**: chunks, parsing, delimited, leading zeroes, bffer

- We record seen characters into a buffer, and flush the buffer into our answer every time we see a delimiting character. -- [LC 468. Validate IP Address](https://www.pramp.com/challenge/Q5G1jZ1OWdtZ3GbAGpNE)


### array

**Key words**: shift

### heap 

* We can solve this problem **in O(N⋅log(K))**. The idea is to **construct a min-heap of size k+1** and insert first k+1 elements into the heap. Then we remove min from the heap and insert next element from the array into the heap and **continue the process until both array and heap are exhausted.** Each **pop operation** from the heap should insert **the corresponding top element** in its correct position in the array.


### BFS 

**Key words**: neighbors, 

* Finding a shortest path **is typically done** with a breadth first search. Here, we have **some underlying graph of words**, and two words are connected (neighbors) if they differ by exactly one letter (and have the same length). 
* The breadth first search **explores** all nodes distance 0 from the source, then all nodes distance 1, then all nodes distance 2, **and so on**. **This ensure that** if we find the target word, we found it at the least possible distance and thus the answer is correct. -- [127. Word Ladder](https://www.pramp.com/challenge/MW75pP53wAtzNPVLPG0d)

### DP 

> Define your **recurrence relation** and **base cases**.
> Besides, try to improve your space complexity if possible.

* **Let** dp(i) **be the answer for the string** S[i:]. We can calculate dp(i) in terms of dp(i+1) and dp(i+2).  
* If S[i] == 0 ... 2 ... > 2...  Putting this all together ...
* Of course, **since at each step** we only **reference** dp[i+1] and dp[i+2], we could **store these as variables** `first` and `second`. This means we do not need to store the entire array. -- [LC91 Decode Variations](https://www.pramp.com/challenge/r1Kw0vwG6OhK9AEGAy6L)
 
### binary search 

key words: lower and upper bound, cut by half 
 
- As we can see, the function finds an initial lower and upper bound for the answer, and sets the initial guess for the answer to be the average. **Then the iteration begins**, and the we notice that **the following facts** are true in every step of the iteration: ... 
	- At the end of every iteration, the real root **always satisfies the inequality** `lowerBound < root < upperBound`: this is true since in the beginning of the iteration, we check if approxRoot to the power of n is greater than or lesser than x. The power function is **monotonically** increasing (i.e. a < b dictates that a^n < b^n) meaning this indicates whether the approximation is too high or too low. 
	- The value of `(upperBound - lowerBound)` is **cut by half** in every iteration - since in every step we replace one of the values of `upperBound` or `lowerBound` by their current average. Obviously it means that **eventually** the distance between the bounds is lower than `0.001`. Since the real root is between the bounds, this **promises** the algorithm stops.
	- [root of number](https://www.pramp.com/challenge/jKoA5GAVy9Sr9jGBjzN4)
 
### two pointers

> Define your 2 pointers 

* Instead, we need to **maintain** two pointers: a write-head, and a read-head. The read-head will read each nonzero element from left to right, and we will write those values to the write-head, then increment the write-head.  -- [LC 283 Move Zeros](https://www.pramp.com/challenge/9PNnW3nbyZHlovqAvxXW)

### sorting 

* **Leverage** the sort function of your languages library. Usually, it will have support for either a custom comparison function. For a custom comparison function compare(a, b), **typically we want to** return -1 if a < b, 1 if a > b, and 0 if a == b. -- [Absolute Value Sort](https://www.pramp.com/challenge/4E4NW7NjbnHQEx1AxoXE)

### test 

- Write some tests and let's give it a shot.

## What: Lesson for Mock Interview

### Things you should work on:

* Find the solution that could use the minimal amount of work first. -- 2018.06.08 [Largest Smaller BST Key](https://www.pramp.com/challenge/pK6A4GA5YES09qKmqG33) 
* Look at familiar **code patterns** used for bfs as well as others. 
* Don't spend too much much time on **complexity analysis** of there are errors in it, ask interviewer if it's okay to go on and code the solution if complexity analysis takes too long to figure out. Interviewer can tell you if it's worth coding it or not.
* It would be helpful to be more communicative when **debugging**.
* I would prefer more discussion about **what you're thinking**, the possible **trade-offs**, etc. It would be good to **mention** you could write **a custom merge/quick sort**, etc. -- 2019.04.05 [Absolute Value Sort](https://www.pramp.com/challenge/4E4NW7NjbnHQEx1AxoXE) 
## What: Suggestions on Google Docs coding?

1. Close page break: View -> Print layout
2. Prevent from auto capitalization: Tools -> Preferences -> Automatically capitalize words 


## More

*  Interviews Tips from [Vince Grimes](https://www.linkedin.com/in/vincegrimes/detail/recent-activity/shares/)
*  [Google Interview Questions Deconstructed: Synonymous Queries](https://medium.com/@alexgolec/google-interview-problems-synonymous-queries-36425145387c)