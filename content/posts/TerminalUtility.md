+++
title = 'Interview Experience: MS(R) CSE IIT Delhi (Winter)'
date = 2025-12-04T00:41:17+05:30
draft = false
+++

## Winter Admission Process

This time, when I received the mail for the written test, I was much more confident. The pattern was again Programming + Core CSE, but unlike the summer exam, there was no break—we had 2 hours total for both sections.

The paper was definitely harder than the summer written test, without any doubt. I immediately realized that it was hard for me → hard for everyone. So I focused on accuracy, as negative marking was there (+4, -1).

Before the exam started, the HoD of CSE came in, cracked a few jokes to ease the tension, and said:

> “The written test is easy. Maybe half of you will get interview calls. Even I can solve it!”

*Everyone laughed.*

Then he added that there would be two interview rounds this time, and they wanted the process to be as complex as possible to select the best candidates.

At that moment, I genuinely felt… *Damn IITD.*

- **Written:** Dec 3  
- **Result:** Same night  
- **Interview:** Next day   


## Round 1 Interview (4th Dec)
---
I was the last candidate in my panel.

There were three professors. To my surprise, I was able to recoginize some of the previous faces from summer, which felt strangely nostalgic after the summer interview.

One professor read my application from his laptop and asked me to introduce myself. I gave a brief introduction, mentioned my interest in systems, and said that I had prepared OS, COA, and Data Structures.

They looked at each other, and someone from them — “OS anyone?”

---

### Questions

Dr. Subhod Kumar Asked:

**Difference between a process and a thread?**  
I answered that a process is a program in execution, while a thread is a lightweight part of a process that can run concurrently.

Follow-up:  
**What do you mean by lightweight?**

I explained that threads share the address space, which reduces overhead. After that, the discussion went deep with multiple follow-up questions. At one point, he said:

> “You are giving vague answers.”

I tried to be careful and precise, but when I felt I might go wrong, I stopped myself. I didn’t want to say something incorrect just to continue.

---

**What happens when a computer is powered on?**  
I explained the entire boot sequence. As soon as I mentioned the bootloader, he interrupted:

> “What runs before the bootloader? Who runs the bootloader?”

I paused due to nervousness. He clarified the CPU. That moment stayed with me.

---

Dr. X (Let's say):

**Can we run multiple operating systems on a single machine?**  
I explained dual booting and virtual machines. He asked about memory allocation in VMs. I admitted honestly that I had only practical exposure and wasn’t fully clear internally. I guessed one part incorrectly.

---

Dr. Y (Let's say):

**Difference between Heap and BST?**  
I answered, but mistakenly started explaining an array-based BST implementation. That led to a long discussion on insertion, shifting, and time complexity. Initially, I was getting grilled, but then I realized my mistake and explained how insertion complexity changes in an inorder-based array representation of BST. He seemed satisfied.

Finally, they asked about my programming experience and the length/scale of code I’ve worked on. I spoke about my recent open-source contributions, including implementing packages, benchmarks, and tests.

---

**Round 1 ended.**

I was honestly disappointed. I called a friend immediately after the interview. Later, I had lunch with another friend. I was not expecting anything further.

## Round 2
---
Then I entered the room in which everyone was waiting. I saw my name for Round 2 at 14:20. Both rounds were on the same day.

While waiting, they offered samosas and chai, which helped calm the nerves 🙂. I was waiting separately in the corridor while others were waiting in the room.

---

### Entry

I was already nervous due to Round 1. My turn came and I entered the room and froze for a while.

There was a large round table with around 25 professors sitting around it. For a second, I genuinely didn’t know whom to greet first.

Then I recognized Dr. Rohit, Dr. Tarun and few other profs (from Summer + Round 1).

Dr. Rohit read my application and said that I had applied under systems, and since the relevant professors were present, they would continue from there.

---

## Core Question (Hardware)

Dr. Preeti Ranjan Panda started:

> I will ask something related to hardware as you have applied in systems…  
> You are given 10 numbers, and a new number comes. How will you search for it?  
> Assume 32-bit numbers. Think about hardware.

---

### Initial Attempt

Initially, I answered from a software perspective (searching algorithm). He immediately stopped me and reminded me: hardware.

I asked for clarification, and another professor helped explain the intent.

---

### Thinking Process

I started thinking aloud. I talked about comparing two numbers only. He said that was fine and asked me to proceed.

Slowly, I realized this was about bitwise comparison. I said comparator, tried to make logic, but seemed like not going anywhere. Stuck! Professors told me to at least try.

One professor pointed out that we don’t need greater-than or less-than comparisons. 

Dr. Vaishnavi said:

> “Think simple!....Think of something that gives 1 when inputs are the same.”

---

### Breakthrough

That’s when it clicked — Logic Gates → Opposite XOR gate (XNOR).

I explained:

A = 10110110 
B = 10110110

C = XNOR(A, B) = 11111111

AND(all bits in C) = 1 → numbers are equal

---

### Follow-up

**How will you know that all outputs are 1?**

I struggled again. A professor said, “You are almost there.”

I had paper and pen. I asked for permission to use them. Later, Dr. Vaishnavi asked me to go to the board.

---

### Board Work

I was blank initially.

After some time, something clicked.

- Started with 8 bits
- Wrote all 1s
- Drew an AND-gate chain

They asked how many AND gates were required:

- 7 AND gates for 8-bit
- 31 AND gates for 32-bit
![Image 1](/images/1.png)
They seemed satisfied.

---

### Delay Question

Each AND gate = 1 ns

- 7 ns for 8-bit
- 31 ns for 32-bit

---

They asked:
### Optimization

**Can you optimize this delay?**

I went blank again.

Dr. Vaishnavi said:

> “How do we usually optimize a process?”

Then she added:

> “Draw a binary tree.”

That immediately clicked.

I redesigned using a balanced AND tree.

- Delay = number of levels
- Answer: 3 ns for 8-bit

![Image 2](/images/2.png)

They were satisfied.

Someone asked:

**Delay reduced?**

I replied:

> Yes, drastically.

---

## Final Questions

Dr. Tarun asked about Computer Networks. I said yes, but honestly mentioned I wasn’t confident as I hadn’t revised.

Then questions about programming and GitHub. I said I could show my work.

Dr. Vaishnavi asked if I was open to other domains.

I said yes and mentioned my ML project, then joked:

> “But I know we shouldn’t say ML in front of IIT professors.”

Everyone laughed. The atmosphere relaxed.

They wished me luck.

---

## Final Verdict

**Selected**

---

## Stats

- 350+ candidates (Written)
- 35 shortlisted (Interviews)
- Final selection:
    - 6 PhD
    - 3 MSR
---

## My Experience

The IIT Delhi admission process was smooth. Both teaching and non-teaching staff were respectful and polite.

---

## Advice

- Read past interview experiences
- Answer in your own way
- Play to your strengths
- Be honest if you don’t know something
- Don’t give vague answers
- Think aloud

You can be nervous, tense, and sometimes clueless—but face the challenge.

---

## Random Fact (MSR)

3 MSR's were selected

1. Quantum guy (B.Tech from IIT Hyderabad in Physics)
2. Systems guy (Me B.Tech from NIT Hamirpur in CSE)
3. Systems guy (B.Tech from non-CFTI, was pursuing M.Tech from NIT Trichy)

Interestingly, no AI person (but it does not signify anything).
        
---

## Closing

All the best to those appearing for interviews!
You can reach out to me on LinkedIn.

<!-- Burnvill Crenberry  -->
