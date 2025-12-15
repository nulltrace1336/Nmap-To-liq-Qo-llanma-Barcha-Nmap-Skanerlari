# 🎬 Ushbu YouTube video rolik

[![YouTube Video](https://img.youtube.com/vi/yhOXm_Kgc10/maxresdefault.jpg)](https://www.youtube.com/watch?v=yhOXm_Kgc10)

## 1️⃣ Host mavjudligini tekshirish
```bash
nmap 192.168.56.102
```

📌 Izoh:

Default scan

Open portlar

TCP SYN (root bo‘lsa)

## 2️⃣ Ping Scan (Host discovery)
```bash
nmap -sn 192.168.56.102
```

📌 Izoh:

Port skan qilmaydi

Faqat tirikligini tekshiradi

## 3️⃣ To‘liq TCP port skan
```bash
nmap -p- 192.168.56.102
```

📌 Izoh:

1–65535 port

Sekin, lekin to‘liq

## 4️⃣ Tezkor TCP scan
```bash
nmap -F 192.168.56.102
```

📌 Izoh:

Eng ko‘p ishlatiladigan portlar

Tez reconnaissance

## 5️⃣ SYN scan (eng mashhur)
```bash
sudo nmap -sS 192.168.56.102
```

📌 Izoh:

Half-open scan

IDS’ni kamroq qo‘zg‘atadi

## 6️⃣ Service va version aniqlash
```bash
nmap -sV 192.168.56.102
```

📌 Izoh:

Apache, vsftpd, MySQL va boshqalar

Exploit izlash uchun muhim

## 7️⃣ OS aniqlash
```bash
sudo nmap -O 192.168.56.102
```

📌 Izoh:

Kernel fingerprint

Taxminiy OS

## 8️⃣ Aggressive scan (HAMMASI BIRGA)
```bash
sudo nmap -A 192.168.56.102
```

📌 Izoh:

OS + Version + Scripts + Traceroute

Shovqinli, lekin kuchli

## 9️⃣ UDP scan (Metasploitable’da foydali)
```bash
sudo nmap -sU 192.168.56.102
```

📌 Izoh:

SNMP, DNS, NFS topilishi mumkin

Sekin ishlaydi

## 🔟 NSE script scan (ENG QIZIQ QISM 🔥)
Default scriptlar
```bash
nmap -sC 192.168.56.102
```
Vulnerability scan
```bash
nmap --script vuln 192.168.56.102
```


📌 Izoh:

Anonymous FTP

Weak services

Known CVE’lar

## 1️⃣1️⃣ FTP misoli (Metasploitable classic)
```bash
nmap -p 21 --script ftp-anon 192.168.56.102
```

📌 Izoh:

Anonymous login ochiqmi?

Real pentest holati

## 1️⃣2️⃣ Natijani faylga saqlash
```bash
nmap -A 192.168.56.102 -oN scan.txt
```

📌 Izoh:

Report yozish

Professional workflow