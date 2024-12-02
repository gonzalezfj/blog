+++
title = "Learn you a concurrency for great interleaving! ⚡"
date = "2024-12-02T07:31:00-03:00"
author = "Facundo J Gonzalez"
authorTwitter = "facujgg"
draft = false
tags = ["programming", "concurrency", "software-engineering", "computing", "distributed-systems", "parallel-computing"]
keywords = ["concurrency", "parallel computing", "asynchronous programming", "modern software", "distributed systems", "concurrent programming", "multithreading"]
description = "A beginner-friendly guide to understanding concurrency in computing, from basic concepts to real-world applications, with practical examples and clear explanations."
showFullContent = false
readingTime = true
hideComments = false
+++

# Learn you a concurrency for great interleaving! ⚡

This is a series of posts about **concurrency**, **distributed systems**, and **parallelism**. I'll try to explain it in a way that is easy to understand and that makes you want to learn more about it. While I'm learning, I'll share my thoughts and what I'm discovering.

I want to explore **concurrency** as a separate concept from _parallel computing_ and _distributed systems_. Because textbooks and courses on computer science usually explain concurrency as a concept from the point of view of parallel computing or distributed systems. We'll focus on **concurrent programming models**, their _practical applications_ in modern systems, _implementation approaches_ across different programming languages, and the _theoretical foundations_ that underpin them. By examining concurrency in isolation, we can better understand its unique challenges and solutions.

## Understanding Concurrency: How computers juggle tasks 🤹‍♀️

In the modern world of computing, **concurrency is everywhere**. Whether you're loading a web page, running applications on your phone, or working with distributed systems in the cloud, you're benefiting from the ability of systems to do multiple things at once. Yet, despite its ubiquity, concurrency remains one of the most complex topics in computer science.

### The concurrency in the real world 🌍

Imagine your are making your breakfast 🍳. You need to boil some water, make some coffee ☕, fry some eggs, and toast some bread 🍞. You could do these tasks one after the other, in order. This is similar to how **sequential programs** work - one task at a time, in order. But you can do other things while you are waiting for the water to boil, right? This is where **concurrency** comes into play. _Concurrency is about dealing with multiple tasks at the same time_.

In computing, concurrency allows systems to maximize their resources and handle multiple users, processes, or requests efficiently. Without it, much of the technology we take for granted today simply wouldn't work.

The world is full of events that we need to handle concurrently, the programs we write need to handle them too, we need to react to them in an efficient way, some of them might take a long time to complete, we need to be able to handle them without stopping to wait for them to finish.

## The Challenge of Understanding Concurrency 🤔

However, understanding concurrency is no easy feat. It's a field rich in terminology, overlapping concepts, and intricate details. From _threads_ and _coroutines_ to _promises_, _schedulers_, and _lock-free structures_, it's easy to feel lost in a sea of jargon. Even seasoned developers often struggle to navigate the complexities of concurrent and parallel programming.

Even something as fundamental as the distinction between **concurrency** and **parallelism** can be confusing. While related, these concepts are quite different:

- **Concurrency** is about structuring your program to handle multiple tasks, even if they're not executing simultaneously. It's about _dealing with lots of things at once_.

- **Parallelism** is about actually executing multiple tasks simultaneously, using multiple processors or cores.

To use our breakfast analogy: _Concurrency_ is like one person efficiently managing multiple cooking tasks by switching between them. _Parallelism_ is like having multiple cooks working on different dishes simultaneously.

Rob Pike explains this distinction brilliantly in his famous talk [**Concurrency is not Parallelism**](https://www.youtube.com/watch?v=cN_DpYBzKso), which I highly recommend watching for a deeper understanding.

Also there is not single definition for concurrency programming, it can be defined in different ways depending on the context and authors.

For instance, the _merriam-webster dictionary_ writes about what concurrency means:

> Things that are concurrent usually not only happen at the same time but also are similar to each other. So, for example, multitasking computers are capable of performing concurrent tasks. When we take more than one medication at a time, we run the risks involved with concurrent drug use. And at any multiplex theater several movies are running concurrently.

Then several authors describe concurrency in different ways. For example:

**A Science of Concurrent Programs** by _Edsger Dijkstra_ 📚

Dijkstra describes concurrency by comparing sequential and multiprocess programs. He explains that in traditional programs, when the program hasn't terminated, there is just one program statement that can be executed. In multiprocess programs, however, it is possible for multiple statements to be executed, each in a different process.

**Teaching Concurrency** by _Leslie Lamport_ 📖

Leslie Lamport describes concurrency through two key concepts: _computation_ and _invariance_.
A computation can be understood as a sequence of states, where each state is connected to the previous one through a transition relation. The critical insight for understanding concurrent systems lies in the concept of invariance - a property that remains unchanged across a set of states despite the transitions between them.

**Concepts, Techniques, and Models of Computer Programming** by _Peter Van Roy_ 📘

Van Roy describes concurrency as a way to model independent activities executing simultaneously. He explains that concurrent programs consist of multiple activities running at their own pace, similar to real-world processes. The key insight is that these activities should remain independent unless explicit communication is required by design. This approach mirrors how the real world works outside of the system, providing a natural way to model real-world behavior within the system.

The idea is clear, **concurrency is about dealing with multiple tasks at the same time, but not necessarily executing them at the same time**. And this is the key concept that we need to understand, concurrency is not about parallelism, it enables parallelism, but it is not parallelism. Also distributed systems are a form of concurrency, but they are a different concept, and we'll talk about it later.

## What This Series Will Cover 📋

This blog series aims to demystify concurrency, breaking it down into manageable pieces while exploring its history, challenges, and modern solutions. Over the next several posts, we'll dive into topics such as:

1. **The origins of concurrency**: How it all started with early operating systems in the 1960s. 🕰️
2. **The confusing terminology**: Exploring process, threads, fibers, coroutines, and other concurrency constructs. 🔤
3. **The evolution to asynchronous programming**: And the question on how we land from "subroutines and coroutines" to "await and async functions". 🔄
4. **Hybrid models**: Finding the balance between event-driven and thread-oriented programming with examples from Go and Python. 🔀
5. **Advanced architectures**: Examining thread per core architecture and the work stealing algorithm. 🏗️

## What to Expect 🎯

Each post in the series will focus on a specific topic, starting with the basics and gradually moving into advanced concepts. By the end of the series, you'll have a **solid understanding** of concurrency's foundations, its role in modern systems, and why mastering it is essential for any developer.

## Join the Journey 🚶‍♂️

Whether you're just starting out or looking to deepen your knowledge, this series is for you. In the next post, we'll explore how concurrency began and the early solutions that paved the way for today's systems. _Stay tuned!_ ✨
