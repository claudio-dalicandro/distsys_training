# PingPong

## Goal

The goal of this exercise is to connect Nodes together, send some messages
across them, and see what happens when those messages fail.

## Part 1

A producer has already been built. When this producer starts it registers its
name and then waits for a consumer. Your job is to implement the consumer.

When the consumer connects it needs to keep track of the number of messages that the producer has sent. If the consumer gets out of sync with the producer then it should
default to the producers count. But if the producer crashes then the consumer
should reset its count to 0.

For local testing it may be convenient to use the functions in the `Node` module
to connect and disconnect local nodes.

## Additional exercises

* Try spawning a few thousand consumers all monitoring a single producer. What
happens when you disconnect the node now?
* What would happen if the producer crashes while the network was partitioned?
Are there ways to make our algorithm more robust?
