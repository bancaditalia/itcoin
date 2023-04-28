---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---

Itcoin is literally **Bitcoin without the B**: a permissioned Distributed Ledger powered by the Bitcoin technology, in which the issuance of the token and the operation of the infrastructure is carried out by a distributed federation of nodes.
Apart from these two substantial modifications, everything else is left unchanged in order to maintain compatibility with the Bitcoin protocol and to inherit and reuse all the existing ecosystem of applications that are built on top of its core infrastructure. 

* More information on the itcoin project is available on [our website](https://bankit.art/projects/itcoin-a-digital-currency-prototype)

Our itcoin blockchain uses a Proof-of-Authority consensus algorithm called **FBFT (Frosted Byzantine Fault Tolerance)**, which we designed using a combination of [PBFT](https://pmg.csail.mit.edu/papers/osdi99.pdf) (Practical Byzantine Fault Tolerance) and [FROST](https://eprint.iacr.org/2020/852.pdf) (Flexible Round-Optimized Schnorr Threshold signatures). Being based on PBFT, our consensus algorithm is resilient to a number of Byzantine failures of nodes in the federation. Thanks to FROST, our consensus algorithm protects the federation and the quorum confidentiality. 

* M. Benedetti, F. De Sclavis, M. Favorito, G. Galano, S. Giammusso, A. Muci, M. Nardelli, *A PoW-less Bitcoin with Certified Byzantine Consensus*, arXiv:2207.0687, 2022. ([ArXiv](https://arxiv.org/abs/2207.06870))
* M. Benedetti, F. De Sclavis, M. Favorito, G. Galano, S. Giammusso, A. Muci, M. Nardelli, *PoW-less Bitcoin with Confidential Byzantine PoA*, in: Proceedings of the 2023 IEEE International Conference on Blockchain and Cryptocurrency (ICBC), 2023. (to appear, [infographic](assets/IEEE_ICBC_2023_Poster.pdf)).
*  M. Benedetti, F. De Sclavis, M. Favorito, G. Galano, S. Giammusso, A. Muci, M. Nardelli, *Certified Byzantine Consensus with Confidential Quorum for a Bitcoin-derived Permissioned DLT*, in: Proceedings of the 5th Distributed Ledger Technology Workshop, May 25–26, 2023. (to appear)

True to the nature of Bitcoin, we want our software be **as open as possible**: The following prototype implementation are made available in open source:

* [itcoin-core](https://github.com/bancaditalia/itcoin-core) contains the itcoin node implementation
* [libsecp256k1-frost](https://github.com/bancaditalia/libsecp256k1-frost) contains an implementation of the FROST signature scheme for secp256k1
* itcoin-fbft contains our FBFT consensus algorithm implementation (coming soon!)
<!-- [itcoin-fbft](https://github.com/bancaditalia/itcoin-fbft)  -->

Itcoin is a pure research project of the [Applied Research Team of Bank of Italy](https://bankit.art/). It aims at academic results (publications, open source software, prototypes); it has no bearing on the official Digital Euro initiative by the Eurosystem. All the software is currently intended for testing and experimentation purposes, and not for use in a production environment.
