# Naměřená data k projektu PDS

## Generování provozu - algoritmy řízení zahlcení
Adresáře `<scénář>_(cubic|bbr)` obsahují následující pro daný <scénář> a pro algoritmus (cubic|bbr):
* `.json` výstup nástroje `iperf3`
* `.csv` data zaznamenaná utilitou `ss` (time,cwnd,rtt,rto,ssthresh)

## Stahování 30 souborů velikosti 2MB - transportní protokoly
Adresáře `<scénář>_protocols` obsahují následující pro daný <scénář>:
* `http2_results.csv` výstup nástroje `curl` při použití HTTP2 (`time_total` - celkový čas \[s\], `speed_download` - průměrná rychlost stahování pro soubor \[B/s\], `time_starttransfer` - čas do stažení prvního bajtu \[s\], `time_appconnect` - čas dokončení handshake \[s\], `time_connect` - čas, než se provede TCP connect)
* `http3_results.csv` to samé pro HTTP3, s rozdílem, že hodnota `time_connect` značí čas nastavení QUIC spojení.
