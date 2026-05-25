# Tool qo'llanma

## Razvedka (Reconnaissance)

### Nmap — Port skaner

```bash
# Tez skan
nmap -T4 -F 192.168.1.0/24

# To'liq skan
nmap -sC -sV -p- target.com

# UDP skan
sudo nmap -sU -T4 target.com

# OS aniqlash
sudo nmap -O target.com
```

### Subfinder — Subdomain topish

```bash
subfinder -d target.com -o subdomains.txt
```

### Nuclei — Zaiflik skaneri

```bash
# Barcha template bilan
nuclei -u https://target.com

# Ma'lum severity bilan
nuclei -u https://target.com -severity critical,high
```

## Web xavfsizlik

### SQLMap — SQL Injection

```bash
# GET parametr bilan
sqlmap -u "https://target.com/page?id=1" --dbs

# POST so'rov bilan
sqlmap -u "https://target.com/login" --data="user=admin&pass=test" --dbs

# Cookie bilan
sqlmap -u "https://target.com/page?id=1" --cookie="session=abc123"
```

### FFuf — Web fuzzer

```bash
# Directory fuzzing
ffuf -w /usr/share/seclists/Discovery/Web-Content/common.txt -u https://target.com/FUZZ

# Subdomain fuzzing
ffuf -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt \
     -u https://FUZZ.target.com -fs 0
```

### Burp Suite

```bash
burpsuite
```

Proxy: `127.0.0.1:8080` ga sozlang.

## Tarmoq

### Wireshark

```bash
# GUI
wireshark

# CLI — tshark
tshark -i eth0 -f "port 80"
```

## Parol hujumlari

### John the Ripper

```bash
# Hash faylni sindirish
john --wordlist=/usr/share/seclists/Passwords/rockyou.txt hashes.txt

# Ko'rsatish
john --show hashes.txt
```

### Hydra — Brute force

```bash
# SSH brute force
hydra -l admin -P /usr/share/seclists/Passwords/rockyou.txt ssh://target.com

# Web form
hydra -l admin -P passwords.txt target.com http-post-form "/login:user=^USER^&pass=^PASS^:Incorrect"
```

## Exploit

### Metasploit

```bash
# Ishga tushirish
msfconsole

# Exploit qidirish
msf> search eternalblue

# Ishlatish
msf> use exploit/windows/smb/ms17_010_eternalblue
msf> set RHOSTS target.com
msf> exploit
```

## Reverse Engineering

### Ghidra

```bash
ghidra
```

### GDB + pwndbg

```bash
gdb ./binary
pwndbg> checksec
pwndbg> disassemble main
```

## WordList yo'llari

```
/usr/share/seclists/                       — SecLists to'liq
/usr/share/seclists/Passwords/rockyou.txt  — Eng mashhur parollar
/usr/share/seclists/Discovery/Web-Content/ — Web directory/file
/usr/share/seclists/Discovery/DNS/         — Subdomain
/usr/share/seclists/Fuzzing/               — Fuzzing payload
/usr/share/wordlists/                      → SecLists symlink
```

→ [HackNow platforma](05-platforma.md)
