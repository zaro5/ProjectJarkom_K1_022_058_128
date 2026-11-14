# Checklist Screenshot — Kelompok 1 (STATUS: SEMUA SUDAH DIAMBIL)

Semua screenshot yang dirujuk `README.md` **sudah di-capture** (total 65 file di `Screenshot/`, 58 tautan README semuanya resolve). Daftar asal masing-masing file (device, tab, konten):

## Panduan Dasar (umum/)
| File | Sumber |
| --- | --- |
| `langkah-klik-perangkat.png` | Jendela R-PUSAT via klik ikon |
| `langkah-tab-cli.png` | R-PUSAT tab CLI |
| `cli-simpan-konfigurasi.png` | R-PUSAT `copy run start` → `[OK]` |
| `langkah-simpan-file.png` | PT main window (toolbar Save terlihat) |
| `topologi-ospf-canvas.png` | Kanvas K1_VLSM_OSPF (dengan L7) |
| `topologi-ospf-gambar1.png` | Kanvas OSPF versi Gambar 1 |
| `email-send-status.png` | Status `sent to budi@...` di pengirim |

## Soal 1
| File | Sumber |
| --- | --- |
| `topologi.png` | Kanvas K1_VLSM static + label (capture fresh) |
| `langkah-place-note-label.png` | Kanvas dgn label (satu topologi) |
| `langkah-modul-hwic2t.png` | R-PUSAT Physical (HWIC-2T terpasang) |
| `langkah-pilih-kabel.png` | PT main window (palette koneksi) |
| `langkah-rename-hostname.png` | R-PUSAT Config → Settings |
| `langkah-ssid-ap.png` | AP-WIFI-BARAT Config → Port 1 → SSID WIFI-BARAT |
| `langkah-ssid-hp.png` | HP-WIFI-BARAT Config → Wireless0 → SSID |
| `cli-pusat-gigabit.png` | R-PUSAT show run (G0/0–G0/2) |
| `cli-pusat-serial-clockrate.png` | R-PUSAT clock rate 64000 |
| `cli-utara-interface.png` · `cli-dc-interface.png` | show run R-UTARA / R-DC |
| `bukti-ip-int-brief-pusat.png` | show ip int brief (semua up/up) |
| `bukti-cdp-neighbors-pusat.png` | show cdp neighbors |
| `bukti-controllers-dce.png` | show controllers s0/0/0 (DCE, clock 64000) |
| `bukti-hp-lease-dhcp.png` | HP-WIFI-BARAT DHCP lease `10.8.192.11` |

## Soal 3
| File | Sumber |
| --- | --- |
| `langkah-buka-command-prompt.png` | PC-PEGAWAI-BK Desktop (ikon IP Config/CP terlihat) |
| `cli-pusat-static-route.png` `cli-utara-static-route.png` `cli-dc-default-route.png` | show run \| include ip route |
| `bukti-route-static-pusat.png` `bukti-route-static-utara.png` `bukti-route-dc.png` | show ip route (static) |
| `ping-antar-lan-3.png` | PC-KANTOR-PB `ping 10.8.224.11` via tunnel |

## Soal 4
| File | Sumber |
| --- | --- |
| `cli-pusat-dhcp-pool.png` `cli-utara-dhcp-pool.png` | show run \| section dhcp |
| `cli-dc-helper-address.png` | R-DC `ip helper-address 10.8.239.2` |
| `bukti-lease-pc-pegawai.png` | PC-PEGAWAI-BK DHCP `10.8.224.11` |
| `bukti-lease-pc-lalin.png` | PC-LALIN-UTARA DHCP `10.8.236.11` |
| `bukti-dhcp-cctv-pool.png` | SRV-DC pool `DHCP-CCTV` |

## Soal 5
| File | Sumber |
| --- | --- |
| `cli-pusat-nat.png` + `bukti-config-nat-pusat.png` | NAT config R-PUSAT |
| `bukti-nat-translations.png` | show ip nat translations |
| `bukti-ping-internet-pegawai.png` | PC-PEGAWAI-BK `ping 8.8.8.8` OK |
| `bukti-route-isp.png` | R-ISP tanpa rute privat |
| `ping-internet-ke-privat-gagal.png` | SRV-INTERNET ping 10.8.224.11 gagal (memang demikian) |

## Soal 6
| File | Sumber |
| --- | --- |
| `cli-pusat-tunnel.png` | show run \| section Tunnel |
| `bukti-tunnel-up.png` `bukti-tunnel-up-pelabuhan.png` | Tunnel0 up/up kedua ujung |
| `cli-crypto-pusat.png` | show run (ISAKMP + crypto map) |
| `bukti-license-feature.png` | show license feature → securityk9 yes |
| `bukti-ipsec-sa-pkts.png` | show crypto ipsec sa (counter pkts) |
| `bukti-tracert-tunnel.png` · `bukti-crypto-map.png` · `bukti-isakmp-sa.png` | bukti awal (tracert hop 192.168.1.2) |

## Soal 7 (file K1_VLSM_OSPF)
| File | Sumber |
| --- | --- |
| `cli-l7-dc-utara.png` | R-DC S0/0/1 L7 config |
| `bukti-failover-l7.png` | Saat L1 down: R-DC route `via 10.8.241.58` (L7) — capture saat OSPF sudah konvergen ke jalur cadangan |
| `bukti-failover-ping.png` | Ping lintas-rota tetap OK saat L1 down |
| `bukti-neighbor-route-utara.png` `bukti-route-ospf-pusat.png` `bukti-route-ospf-pelabuhan.png` | bukti OSPF |

## Soal 8
Semua perangkat: SRV-DC DNS/FTP, SRV-BALAIKOTA HTTP/EMAIL, PC client (browser/nslookup/ftp/email). File: `bukti-dns-records`, `bukti-portal-http`, `bukti-browser-portal`, `bukti-nslookup`, `bukti-ftp-upload`, `bukti-ftp-server-filelist`, `bukti-akun-email-srv`, `bukti-email-konfigurasi-client`, `bukti-email-inbox-budi`.

---
**Tugas manual truly-remaining = nihil.** Bila ingin anotasi ①②③ ala repo ETS, cukup sorot pada screenshot yang ada; baris `*![Screenshot ditambahkan: ...]*` di README bisa diganti embed `![judul](Screenshot/...)`.
