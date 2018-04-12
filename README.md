# API
OpenFAM API

Recent technology advances in high-density, byte-addressable non-volatile memory (NVM) and low-latency interconnects have enabled building large-scale systems with a large disaggregated fabric-attached memory (FAM) pool shared across heterogeneous and decentralized compute nodes. In this model, compute nodes are decoupled from FAM, which allows separate evolution and scaling of processing and fabric-attached memory. The large capacity of the FAM pool means that large working sets can be maintained as in-memory data structures. The fact that all compute nodes share a common view of memory means that data sharing and communication may be done efficiently through shared memory, without requiring explicit messages to be sent over heavyweight network protocol stacks. Additionally, data sets no longer need to be partitioned between compute nodes, as is typically done in clustered environments. Any compute node can operate on any data item, which enables more dynamic and flexible load balancing. 

The OpenFAM API is an API for programming with persistent FAM that is inspired by partitioned global address space (PGAS) models. Unlike traditional PGAS models, where each node contributes local memory toward a logically shared global address space, FAM isn't associated with a particular node and can be addressed directly from any node without the cooperation or involvement of another node. The OpenFAM API enables programmers to manage memory allocations, access FAM-resident data structures, and order FAM operations. Because state in FAM can survive program termination, the API also provides interfaces for naming and managing data beyond the lifetime of a single program invocation.



