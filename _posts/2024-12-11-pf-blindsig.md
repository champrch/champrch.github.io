---
layout: post
title: Pairing-Free Blind Signatures and Our Constructions from CDH
date: 2024-12-11
description: Summary of state-of-the-art on pairing-free blind signatures
tags: blind-signatures pairing-free
categories: paper-summary
featured: true

toc:
  beginning: true

---

## Background 

Blind signatures are protocols between a signer, who holds a secret signing key, and a user who wants its message signed. The protocol has to satisfy two properties, blindness and one-more unforgeability. Blindness says that the signer should not be able to learn anything about the message or the signature that the user receives. One-more unforgeability (OMUF) says that no malicious user can output more message-signature pairs than the number of signing sessions. Note that we consider the notion of concurrent one-more unforgeability where the malicious user can  interleave the signing protocols arbitrarily.
The primitive has seen applications in anonymous credentials, electronic cash, anonymous tokens, etc. It has also been used to provide privacy in some real-world systems. 

***

## Motivation for Pairing-Free Blind Signatures

Our work mainly considers blind signatures constructed relying on pairing-free elliptic curves. You might wonder "why pairing-free curves?" 

1. They are easy to implement with already existing libraries, and are usually more efficient compared to pairing-based constructions. 
2. They can be a first-step towards an efficient lattice-based blind signature scheme. 
3. But mainly, the reason we are interested in building pairing-free blind signatures is because it is a hard problem. A short reason is due to less cryptographic primitives being available. 

To see further why this problem is hard, let's look at existing schemes (before our work). 


| Scheme       | OMUF (# of sessions & assumption) | Idealized Model | Blindness (assumption)       |
| :----------- | :---------------------: | :--------------: | :--------------: |
| Blind Schnorr | Limited & OMDL     | AGM + ROM | Statistical |
| Okamoto-Schnorr | Limited & DL       | ROM       | Statistical |
| Abe-Okamoto | Limited & DL        | ROM       | Statistical |
| Abe | Unbounded & DL        | AGM + ROM | DDH |
| Clause Blind Schnorr  | Unbounded & DL | AGM + ROM | Statistical |
| Snowblind  | Unbounded & DL | AGM + ROM  | Statistical |

Note that everything here requires the ROM due to an impossibility result. 


***

## Our Results






***

## Remarks and Open Problems


***

## References
