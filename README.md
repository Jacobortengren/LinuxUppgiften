# Linuxbaserad plattform för centrala nätverkstjänster

Detta projekt är en del av min LIA-praktik på TUC Yrkeshögskola, där jag har designat, installerat och driftsatt en virtuell Linux-server som levererar fyra centrala nätverkstjänster: **DHCP, DNS, Syslog** och **Zabbix-övervakning**.

Syftet med projektet är att få praktisk erfarenhet av konfiguration, felsökning, säkerhetshärdning samt dokumentation av verkliga nätverkstjänster på Ubuntu Server samt lärdom av hur Github fungerar.

## Tjänster och konfigurationer

### 1. DHCP – Automatisk IP : och DNS-distribution
- [dhcpd.conf](https://github.com/Jacobortengren/LinuxUppgiften/blob/DHCP/dhcpd.conf)

### 2. DNS (BIND9) : Intern zonhantering och forwarder
- [named.conf.local](https://github.com/Jacobortengren/LinuxUppgiften/blob/DNS-(Bind9)/named.conf.local)
- [zonfil: db.jacob.local](https://github.com/Jacobortengren/LinuxUppgiften/blob/DNS-(Bind9)/zones/db.jacob.local)

### 3. Syslog : Central logghantering med logrotate
- [rsyslog.conf](https://github.com/Jacobortengren/LinuxUppgiften/blob/Syslog/rsyslog.conf)
- [logrotate.conf](https://github.com/Jacobortengren/LinuxUppgiften/blob/Syslog/logrotate.conf)
- [rsyslog_custom.sh](https://github.com/Jacobortengren/LinuxUppgiften/blob/Logrotate/rsyslog_custom)

### 4. Zabbix : Övervakning med tröskelvärden och notifieringar
- [zabbix_server.conf](https://github.com/Jacobortengren/LinuxUppgiften/blob/Zabbix-Server/zabbix_server.conf)
- [zabbix_agentd.conf](https://github.com/Jacobortengren/LinuxUppgiften/blob/Zabbix-Server/zabbix_agentd.conf)

## Automatisering

Två egna Bash-skript har använts för:
1. Daglig backup av konfigurationsfiler till detta Git-repo
2. Kontroll av tjänsternas status med loggning till syslog

## Tack för du tittade! Ha det gott!
