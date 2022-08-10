---
layout: archive
title: "Personal"
permalink: /thoughts/
author_profile: true
---

{% include base_path %}

# Spot it
Recently I came across the cards game "Spot it", which I found quite
interesting! Its rules are quite simple: each of the 55 cards contains 8 symbols
from a set of 57 symbols in total. The deck is shuffled and split equally
between the players. A stack of open cards will be populated in the middle.
Initially, it contains a single cards. Then all players race in getting rid of
their cards by first naming *the* common symbol between one of their cards and
the card in the top of the stack, and subsequently throwing their card on top of
the stack. The first person to get rid of all their cards wins the game.

The game was designed so that each pair of cards shares a single symbol. How is
this possible? Although there is a
[geometric](https://www.smithsonianmag.com/science-nature/math-card-game-spot-it-180970873/)
explanation on this, here I aim to present an elegant non-constructive proof.

## The Probablistic Method
The probabilistic method is a very elegant way to proof the existence of
something without actually contructing it. Introduced by Paul Erdős, the
technique works as follows. Define a probability space and a probabilistic event
corresponding to this "something" that we look for. Compute the probability of
this event, and as long as this probability is positive, we are sure there is
an assignment to the random variables that make the event possible.

## Application on Spot it
Consider the 8 slots in each of the 55 cards and follow the following randomized
process. For each of the 8 slots pick a random size-8 subset of the 57 symbols
and fill in the slots. What is the probability that each pair of cards shares a
single symbol? In particular, is this probability non-zero? If so, then we are 
sure there is such an assignment.

So, let Good be the event that each pair of cards shares a unique symbol and
consider Pr[Good]. The complement of this event is that there is at least one
pair that does not share exactly one symbol. For a pair p, let Bad[p] be the
event that p does not share exactly one symbol:

Pr[Good] = 1 - Pr[∃ p: Bad[p]].

Applying union bound, we can find an upper bound on Pr[∃ p: Bad[p]] as

Pr[∃ p: Bad[p]] ≤ ∑ Pr[Bad[p]], where the sum is over all pairs of cards p. The
number of pairs is given by the binomial coefficient 55-choose-2. So it is
enough to compute Pr[Bad[p]] for an arbitrary p. The number of possible
assignments of symbols to two cards is 57-choose-2 squared. The "bad"
assignments are all these assignments that share 0,2,3,4,5,6,7 or 8 symbols;
i.e., any number but 1. For a number c of common symbols, the number of
assignments that share c symbols are 57-choose-c times (57-c)-choose-(16-2c).

Putting everything together we get

$\Pr[\text{Good}]\ge 1-\binom{55}{2}\frac{\binom{57}{16}+\sum_{c=2}^8 \binom{57}{c}\binom{57-c}{16-2c}}{\binom{57}{8}^2} = -0.0351$.

But wait! This is not positive. Well, the above is only a lower
bound so we lost a little bit there. By picking 58 symbols instead, we get $\Pr[\text{Good}]\ge 0.004$.