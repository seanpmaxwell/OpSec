# Terminology

## Basics

#### OpSec (Operational Security)
User-defined behaviors and habits for keeping digital information and activity secure.

#### Cybersecurity
The practice of protecting devices, networks, and data from unauthorized access or attack, using software, hardware, and procedures.

---

**OpSec** vs **CyberSecurity**: _Cybersecurity stops someone getting into your device or accounts (e.g. keeping your computer up-to-date). OpSec stops you from giving information away yourself (using different email aliases for different websites to keep your identity hidden)._

---

#### IP (Internet Protocol) Address
A numerical identifier assigned to a device on a network (e.g., a computer, router, or server).

#### ISP (Internet Service Provider)
A company that provides a user with internet access (e.g., Xfinity).

#### DNS (Domain Name System)
Maps a user-friendly name (e.g., google.com) to a server's IP address.

#### PGP (Pretty Good Privacy)
A standardization for encryption so a user can receive private messages. It consists of two keys: one public one private. The user shares the public one with the outside world and keeps the private one to themself. The public key encrypts the message by the party wanting to send, and only the private key can be used to decrypt the message. Side note: a few privacy-focused services (e.g., Proton Mail) use PGP and manage the user’s keys automatically, so that only the sender and recipient can read a message.

#### Malware
Malware (short for “malicious software”) is any software designed to harm, spy on, or take control of a device without the owner’s consent (e.g. trojans, spyware, ransomware). Side note: viruses are malware which spread by copying themselves into other files are less common today. 

#### Firmware
Software which exists below the operating system (e.g. BIOS/UEFI). Firmware is attacked less often than ordinary software because attacks must be tailored to specific hardware, but malware that does infect it is especially dangerous: it is hard to detect and can survive reinstalling the operating system.

## Services

#### VPN (Virtual Private Network)
A service that protects a user from entities that could normally observe their identity or activity. In the context of a personal VPN subscription (e.g., NordVPN, Proton VPN, or Brave VPN), this typically involves a desktop or mobile application that encrypts the user's traffic and routes all of it through the VPN provider's server. This hides which websites the user visits from the ISP, and hides the user's IP address from the website.

Three things worth knowing:

- The ISP can still see how much data is being transferred, and when.
- Because all traffic goes to the VPN's server, the ISP can usually tell that a VPN is in use, and often which one.
- The VPN provider can see what the ISP no longer can, so trust is shifted rather than removed.

> see [How does a VPN work](./How-does-a-VPN-work.md)

#### Firewall
A firewall is a filter between a user's device (or network) and the internet that blocks unwanted connections based on a set of rules (e.g., the Great Firewall of China blocks connections to the TOR network).

#### Sandbox
A isolated environment (often built into an operating system, browser, or app) where a program can run without being able to affect the rest of your device. For example, `flatpak --unshare=network vlc` runs VLC media player without allowing it to have any internet acces.
