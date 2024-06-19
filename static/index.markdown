---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---

Itcoin (as in: **Bitcoin** without the **B**) is a permissioned Distributed Ledger (DLT) powered by the Bitcoin technology. As opposed to Bitcoin, the issuance of the token and the operation of the infrastructure is carried out by a distributed federation of trusted nodes.
Apart from these two substantial modifications, everything else is left unchanged in order to maintain compatibility with the Bitcoin protocol and to inherit and reuse all the existing ecosystem of applications that are built on top of its core infrastructure. 

* More information on the **itcoin** project is available at [our website](https://bankit.art/projects/itcoin-a-digital-currency-prototype).

## Consensus Protocol 

The itcoin blockchain uses a Proof-of-Authority (PoA) consensus algorithm called **FBFT (Frosted Byzantine Fault Tolerance)**, which we designed using a combination of [PBFT](https://pmg.csail.mit.edu/papers/osdi99.pdf) (Practical Byzantine Fault Tolerance) and [FROST](https://eprint.iacr.org/2020/852.pdf) (Flexible Round-Optimized Schnorr Threshold signatures). Being based on PBFT, our consensus algorithm is resilient to a number of Byzantine failures of nodes in the federation. Thanks to FROST, our consensus algorithm protects the federation and the quorum confidentiality. Combining Bitcoin, FROST, and PBFT turned out to be a nontrivial exercise, one that led to the following publications:

*  M. Benedetti, F. De Sclavis, M. Favorito, G. Galano, S. Giammusso, A. Muci, M. Nardelli, *Certified Byzantine Consensus with Confidential Quorum for a Bitcoin-derived Permissioned DLT*, in: Proceedings of the 5th Distributed Ledger Technology Workshop, May 25–26, 2023. ([CEUR](https://ceur-ws.org/Vol-3460/papers/DLT_2023_paper_1.pdf))
* M. Benedetti, F. De Sclavis, M. Favorito, G. Galano, S. Giammusso, A. Muci, M. Nardelli, *PoW-less Bitcoin with Confidential Byzantine PoA*, in: Proceedings of the 2023 IEEE International Conference on Blockchain and Cryptocurrency (ICBC), 2023. ([IEEE](https://doi.org/10.1109/ICBC56567.2023.10174972), [infographic](assets/IEEE_ICBC_2023_Poster.pdf)).
* M. Benedetti, F. De Sclavis, M. Favorito, G. Galano, S. Giammusso, A. Muci, M. Nardelli, *A PoW-less Bitcoin with Certified Byzantine Consensus*, arXiv:2207.0687, 2022. ([ArXiv](https://arxiv.org/abs/2207.06870))


### Repositories

True to the nature of Bitcoin, we want our software be **as open as possible**; so, the following prototype implementations are made available as open source repositories:

1. [itcoin-core](https://github.com/bancaditalia/itcoin-core): contains the itcoin node implementation;
2. [secp256k1-frost](https://github.com/bancaditalia/secp256k1-frost): contains an implementation of the FROST signature scheme over *secp256k1*;
3. [itcoin-fbft](https://github.com/bancaditalia/itcoin-fbft): contains our FBFT consensus algorithm implementation.

## Payment Channel Networks

Payment Channel Networks (PCNs) promise to solve the scalability
(and privacy) issue of blockchains. Understanding them is a key
pillar to define a blockchain-based payment system that can correctly sustain a real load of payments. 

To this end, building on state of the art frameworks, we develop **itcoin-pcn-simulator**, an ecosystem for evaluating large-scale PCNs using Parallel Discrete Event Simulations (PDES).
Our solution extends the PCN simulation model proposed by [CLoTH](https://doi.org/10.1016/j.softx.2021.100717), an [open-source](https://github.com/marcono/cloth/) sequential simulator of a LN implementation widely used in recent works, and runs on [ROSS](https://ross-org.github.io/), a distributed-memory architecture PDES that can run on multiprocessor systems.

Further details can be found in the following publications:

* M. Benedetti, F. De Sclavis, M. Favorito, G. Galano, S. Giammusso, A. Muci, M. Nardelli, *Self-Balancing Semi-Hierarchical Payment Channel Networks for Central Bank Digital Currencies*, in: Proceedings of 2024 IEEE International Conference on Pervasive Computing and Communications Workshops and other Affiliated Events (PerCom Workshops 2024), pp. 530-536, Biarritz, France, March 11-15, 2024. ([IEEE](https://doi.org/10.1109/PerComWorkshops59983.2024.10503409))
* G. Galano, S. Giammusso, M. Nardelli, *Modeling Central Bank Digital Currency over Payment Channels: A Parallel ROSS-based Approach*, in: Proceedings of the 38th ACM SIGSIM Conference on Principles of Advanced Discrete Simulation (SIGSIM PADS '24), Atlanta, Georgia, USA, June 24-26, 2024. ([ACM](https://doi.org/10.1145/3615979.3656052))
* M. Benedetti, F. De Sclavis, G. Galano, S. Giammusso, A. Muci, M. Nardelli, *Impact of Layer-1 Characteristics on Scalability of Layer-2 Semi-Hierarchical Payment Channel Networks*, in: Proceedings of the 6th Distributed Ledger Technology Workshop (DLT 2024), Turin, Italy, May 14-15, 2024. To appear.
* M. Benedetti, F. De Sclavis, M. Favorito, G. Galano, S. Giammusso, A. Muci, M. Nardelli, "Self-Balancing Semi-Hierarchical PCNs for CBDCs", CoRR abs/2401.11868, ArXiv. 2024. ([arXiv](https://doi.org/10.48550/arXiv.2401.11868)) 

### Repositories

Our **itcoin-pcn-simulator** is available as an open source project:

* [itcoin-pcn-simulator](https://github.com/bancaditalia/itcoin-pcn-simulator/): contains our simulator of PCNs and the topology generator of Semi-Hierarchical PCNs, a special family of topologies that exploit the three-tier structure of the traditional financial system.

## Disclaimer
Itcoin is a research project by the [Applied Research Team of Bank of Italy](https://bankit.art/). It aims at academic results (publications, open source software, prototypes); it has no bearing on the official Digital Euro initiative by the Eurosystem. All the software is currently intended for testing and experimentation purposes, and not for use in a production environment.
