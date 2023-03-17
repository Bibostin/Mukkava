This is a document outlining the key functions I expect to include in this new iteration of Mukkava:
- Written in C++ (way better native lib support for the majority of the elements I used originally)
- Using UDP rather then TCP
- Capable of supporting numerous individual clients on a single public IP
- Capable of connecting via both ipv6 and ipv4
- Supports Lyra and or Opus
- Has a GUI
- Cross Platform

---

Persistancy for the following static elements should be achieved in line with the flaws found in the
original version of Mukkava's PAKE method:
  - individual UUID
  - individual Public / Private asymetric key
  - hashed peer UUIDs
  - peer Public keys
  - peer previous addresses (use TOFU to make roaming acceptable

A combination of PAKE and TOFU are probably the best solution, as while PAKE defeats MITM, key weakness
and a chance of impersonation is a significant problem. making PAKE keys "disposable" in that you only
need to use a key once per authentication between yourself and another user is ideal as the key weakness
is only present given a user reuses the key (which we can account for in the program) and for a small 
period where the inital key exchange occurs.)

I should look at what TOX does in regards for this (I'm pretty sure its STUN) 

---

Suggested libraries:
- portaudio
- libsndfile
- qt, deariamgui
- libsodium
- sockpp
 
