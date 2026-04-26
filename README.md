# Inbox Invaders

> Built for **LA Hacks 2026** — Track 3: Safety

**Play it:** https://www.roblox.com/games/86299320607236/Inbox-Invaders
**Devpost:** https://devpost.com/software/1256252

## What it is

A Roblox game that teaches online safety by making it the gameplay loop. Aliens attack Earth through phishing emails, suspicious downloads, privacy breaches, and notification spam. You spot scams in your inbox and complete cybersecurity mini-games to earn credits — then spend those credits on tower defense turrets (Antivirus, Firewall, VPN) to fight off the alien fleet attacking your house.

Every scam in the game is a 1:1 reskin of a real-world phishing pattern (fake Roblox security, Apple ID lockouts, "Mom" with a typo'd domain). Spotting one in-game is the same skill as spotting the next one in real life.

## How it works

Two loops, one shared credit economy:

- **Computer (learning).** Sort emails as Safe or Dangerous; for dangerous mail, identify the red flag — typo, personal info request, urgency, suspicious link, or impersonation. Four mini-games cover passwords, downloads, privacy, and notifications. Correct calls earn credits; mistakes cost them.
- **Tower defense (combat).** Spend credits on cybersecurity-themed turrets. 50 hand-tuned waves of aliens, balanced against your inbox performance.
- **Story + tutorial.** Orbit, an alien cat guide, onboards the player and weaves both loops into a single narrative.

## Tech

- **Roblox Studio + Luau** for everything in-game
- **Custom diegetic OS UI** rendered procedurally on the in-world monitor (inbox, password manager, downloads, privacy, notifications)
- **Server-authoritative DataStore + Replica** for cross-session save state — player progress, credits, placed turrets, current round
- **Anthropic Claude API** powers the password-strength mini-game; the LLM evaluates user-created passwords against defined security criteria and returns a score plus targeted feedback
- **Network optimization** — tower shot effects batched at 20 Hz, dropping bandwidth from ~500 KB/s to ~14 KB/s

## Team

Mark · Marlon · Kian · Aaron

## Submission contents

`InboxInvaders.rbxl` — place file. The live game runs at the Roblox link above.