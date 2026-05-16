# ECOTRACK — Plateforme IoT Gestion des Déchets Urbains

## L'équipe
- **Imelda** : VM6 Splunk SIEM + VM7 Snort IDS + VM8 MQTT
- **Marie Claude** : VM1 ECO-PROXY HAProxy+WAF + VM5 ECO-DB PostgreSQL
- **Ephra** : VM0 pfSense + VM3 ECO-APP Node.js + VM4 ECO-WEB Nginx

## Ordre de démarrage (OBLIGATOIRE)
1. pfSense → attendre 2 minutes
2. ECO-DB → attendre 1 minute
3. ECO-MQTT
4. ECO-PROXY
5. ECO-APP + ECO-WEB
6. ECO-MON Splunk → attendre 2 minutes
7. ECO-SEC Snort

## Accès aux interfaces
| Service | URL | Identifiants |
|---------|-----|--------------|
| pfSense | https://10.10.2.1 | admin / EcoPfsense2026! |
| Splunk SIEM | http://10.10.3.10:8000 | admin / Ecotrack2026! |
| Grafana | http://10.10.3.10:3000 | admin / admin |
| ECO-APP API | http://10.10.2.10:3000 | — |
| ECO-WEB | http://10.10.2.20 | — |
| HAProxy stats | http://10.10.1.10:8080/haproxy-stats | — |

## Adressage IP
| VM | IP | Zone | Responsable |
|----|----|------|-------------|
| pfSense DMZ | 10.10.1.1 | DMZ | Ephra |
| ECO-PROXY | 10.10.1.10 | DMZ | Marie Claude |
| ECO-APP | 10.10.2.10 | LAN | Ephra |
| ECO-WEB | 10.10.2.20 | LAN | Ephra |
| ECO-DB | 10.10.2.30 | LAN | Marie Claude |
| ECO-MON | 10.10.3.10 | MGT | Imelda |
| ECO-SEC | 10.10.3.20 | MGT | Imelda |
| ECO-MQTT | 10.10.4.10 | IoT | Imelda |
