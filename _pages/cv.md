---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

In [printable version](https://docs.google.com/document/d/1cQ0d0CVGzYeGkpc_2Wu0gw3RMXgCAl4kxxrNCcdT4xU/export?format=pdf).

Industry experience
======
* Winter 2019: Cryptography Consultant
  * ThunderCore, California
    * Reviewed cryptographic code and confirm an attack on a previous version of a cryptographic protocol for signature aggregation.
    * Compared existing libraries implementing the [Boneh, Lynn, Shacham] signature aggregation scheme.
    * Provided additional resources and answer cryptographic questions to the Core team.

* Summer 2018: Intern
  * ThunderCore, California
    * Designed and developed in Solidity several versions of smart contracts for 1 vs 1 fair randomness generation using modifications of coin-flipping protocols.
    * Unit, functional and manual testing of smart contracts for randomness generation, Ethereum Name Service and Timestamping contracts, ERC-20 and ERC-721 tokens.

* Summer 2017: Intern
  * University of Edinburgh and IOHK, United Kingdom
    * Compared different post-quantum signature schemes according to key/signature size and signing/verification times and their applicability to quantum-secure blockchains.
    * Designed a quantum money protocol without need for a public common ledger and with classical communication. The protocol makes use of a modification of quantum lightning.

Education
======
* Ph.D in Computer Science, City University of New York, 2020 (expected)
* M.S. in Computer Science, University Paris 7, Diderot, 2014
* B.S. in Electrical and Computer Engineering, National Technical University of Athens, 2013
  
Skills
======
* Blockchain
  * Hands-on experience with Solidity, blockchain technology internals, expertise on smart contracts.
* Generic
  * Python, C, Java, Haskell, ML, Prolog, Mathematica, Git, LaTex.

Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Teaching Assistant
======
* Introduction to Cryptography, Fall 2015, by Prof. Oded Regev, NYU
* Modern Cryptography, Spring 2016, by Prof. Nelly Fazio, CUNY
