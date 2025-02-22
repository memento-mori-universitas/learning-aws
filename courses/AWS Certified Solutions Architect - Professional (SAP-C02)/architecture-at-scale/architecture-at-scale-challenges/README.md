# Architecture At Scale Challenges

## Challenge #1

![Architecture Scale Challenge](../../assets/aws-architecture-at-scale-challenge-1.png)

My answer: C

A. Messages dont get pushed from SQS, you have to pull the queue

D. SWF is a statusing framework, no weighted routing feature

Clue: Pictures a high resolution multi-megabytes pictures

B. SNS has a limit, 256K

C. Kinesis has a maximum inbound message of 1 MB

**Best option: E**

## Challenge #2

![Architecture Scale Challenge](../../assets/aws-architecture-at-scale-challenge-2.png)

My answer: F

A. Cooldown might be too long. Maybe

B. Internet Gateway aren’t susceptible to saturation, they have no bandwidth limit

C. Scheduled scheduling, our demand in unpredictable so it will not help

D. Reasonable suggestion

E. Once you create a launch configuration, you can edit after it’s been created

F. Step scaling policies don’t have a cooldown period, they have a warmup period, where you can specify how long to allow your new instances to come up before another step scale can be triggered.

**Best option: A, D**

### Up next [Business Continuity](../../business-continuity/README.md)...
