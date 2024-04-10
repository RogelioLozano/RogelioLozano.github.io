---
sidebar_position: 1
---

# Relevant Peer to peer network concepts

A p2p network is a distributed system. We use it to share data between nodes of the system without having a central server that manages the policies of moving, storing, etc. data between nodes.

Four important concepts arise:
1. **Confidentiality**. How do we assure that the data we are sending is confidential? If I send my bank account details, I don't want anyone to see them. For that we use cryptography to encrypt the message and only allow the intended receipt to read it.

2. **Integrity**. Even if we send data that we are fine letting other people see it. We want to be sure that the data has not been tampered.

3. **Non-repudiation**. We want to use a mechanism to assure that if someone sent a message, then they can't lie and say that the did not sent it, we want to make sure that once you send it, you are recorded and we all know what and who sent it.

4. **Authentication**. We want to get sure that whenever we receive a message, the sender is the one who says it is. Say A sent a message. We authenticate the message to see if it was really A who sent it in the first place.

