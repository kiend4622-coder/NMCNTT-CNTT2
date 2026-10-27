\# SmartFarm Monitor



\## Huong dan chay script



```powershell

cd scripts

powershell -ExecutionPolicy Bypass -File .\\\\auto\\\_report.ps1

```



\## Checklist kiem tra thiet bi



\- \[x] Kiem tra ket noi mang

\- \[x] Kiem tra RAM

\- \[ ] Kiem tra nguon dien

\- \[ ] Kiem tra o cung



\## Bang thong so phan cung



| Ten thiet bi | Don gia | Loai storage |

|--------------|----------|--------------|

| Raspberry Pi 4 Model B | 1450000 | SSD |

| Intel NUC i3 | 6200000 | SSD |

| Synology DS220j NAS | 3900000 | HDD |



\## Phan tich he thong



\### IPO



\*\*Input\*\*

\- log-he-thong.log



\*\*Process\*\*

\- Doc file log

\- Loc ERROR va CRITICAL

\- Dem tong so su co

\- Tao bao cao



\*\*Output\*\*

\- bao-cao-su-co.txt



\### DIKW



\- \*\*Data:\*\* 2026-10-12 08:15:01 \[ERROR] sensor-03 Connection TIMEOUT after 30s



\- \*\*Information:\*\* Hom nay he thong ghi nhan 8 su co, trong do 4 su co den tu sensor-03



\- \*\*Knowledge:\*\* Tram sensor-03 hay mat ket noi vao buoi chieu do song yeu, can lap them anten



\- \*\*Wisdom:\*\* Quyet dinh thay modem tram sensor-03 truoc thu Sau

