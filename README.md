# Java Virtual Machine

## Table of Contents
* [Introduction to the JVM](#introduction-to-the-jvm)

### Introduction to the JVM

Think about the CPU in your computer. No matter what make or model of CPU you own, it serves the same basic functions as any other CPU: it performs arithmetic calculations, controls access to memory, manages the flow of
control of programs, and provides a way for programs to use hardware attached to the system.

Even though all CPUs perform essentially the same job, programs designed for one CPU do not work on another.The developers of Java had a simple idea: design an abstraction of a CPU, and implement it for a variety of computers. Once this virtual computer is implemented on a particular system, all programs written for the virtual computer will run on that system. This allows programmers to write a program once, then run it anywhere. This
virtual computer is called the Java virtual machine (JVM). Because the JVM isn't biased toward any particular CPU, it can provide a more abstract view of memory.

Instead of providing direct access to the bits-and-bytes level of memory, the JVM treats memory as a collection of objects. This is a paradigm called object-oriented programming, and it offers a number of advantages. One advantage is that it allows better control over which programs are allowed to access which parts of memory.

This affords the JVM control over access to the hardware of the system. The JVM developers created a set of rules
all programs must play by. As long as all programs play by the rules, it is possible to provide assurances to
program users that the programs are not trying to damage the system.

These rules are made concrete in an algorithm called verification, which detects which programs follow the rules
and which don't. A key goal of verification is to detect invalid programs even before they run. Only programs that
are approved by the verification algorithm run. This prevents malicious or mistaken software from doing
unpleasant things: it never gets a chance to run.
