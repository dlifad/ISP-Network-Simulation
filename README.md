# Enterprise Network Design — VLAN + OSPF + BGP + DNS Server

## 🔎 Ringkasan
Project ini mensimulasikan jaringan perusahaan dengan beberapa gedung, beberapa VLAN,
routing protocol OSPF dan BGP, serta layanan server (Web + DNS). Simulasi dibuat menggunakan Cisco Packet Tracer.

## 🎯 Tujuan
- Memisahkan jaringan menggunakan VLAN (Pegawai, Administrator, Public)
- Mengimplementasikan OSPF multi-area
- Menghubungkan dua ISP menggunakan BGP
- Membangun DNS dan Web Server internal & eksternal
- Menguji konektivitas end-to-end antar perangkat

## 🧰 Tools & Devices
- Cisco Packet Tracer 8.x
- Router: 2811
- Switch: 2960
- Wireless Router/AP
- DNS Server + Web Server

## 🧱 Topologi
![Topology](topology.png)

## ⚙️ Konfigurasi Utama
### VLAN
- VLAN 10 → Pegawai  
- VLAN 20 → Administrator  
- VLAN 30 → Public  

### Routing Protokol
- OSPF Area 0 & Area 1
- BGP peering antar ISP simulasi

### Server
- DNS → domain: `www.gugle.com`  
- Hosting Web App sederhana

## 📌 Fitur Koneksi
- Semua VLAN dapat mengakses internet
- Internal routing via OSPF
- External routing via BGP
- DNS resolving berjalan normal

## ✔️ Hasil Pengujian
- Ping antar VLAN: OK
- ping website internal (www.gugle.com): OK
- traceroute menunjukkan jalur ISP sesuai routing protocol

## 📂 File
| File | Fungsi |
|------|--------|
| `topology.pkt` | File simulasi |
| `configs/` | Konfigurasi CLI per perangkat |
| `docs/testing-results.md` | Dokumentasi hasil test |
