This is a document outlining the key functions I expect to include in this new iteration of Mukkava:
- Written in C++ (way better native lib support for the majority of the elements I used originally)
- Using UDP rather then TCP
- Capable of supporting numerous individual clients on a single public IP
- Capable of connecting via both ipv6 and ipv4
- Supports Lyra and or Opus
- Has a GUI
- Cross Platform

- Persistancy for the following static elements:
  - individual UUID
  - individual Public / Private asymetric key
  - hashed peer UUIDs
  - peer Public keys
  - peer previous addresses (use TOFU to make roaming acceptable
---
TOFU VS PAKE:

I think tofu is honestly better for the user as while PAKE defeats MITM, the weakness of the key and chance of impersonation is a bigger problem in my mind
UNLESS I use the above model where PAKE is only used for the inital handshake between two clients, in this case, you could treat passwords as disposable
or even supply a "list" of passwords to try (making coordination easier between multiple users)
---

Suggested libraries:
- portaudio
- libsndfile
- qt, deariamgui
- libsodium
- sockpp
 
