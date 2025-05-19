# Boas Práticas em Redes

Este documento tem como objetivo reunir boas práticas aplicadas no contexto de redes, com foco em segurança, desempenho e manutenção de ambientes de produção. As recomendações estão organizadas por categorias por aqui vamos aprender que todo acesso deverá ser solicitad, agendado e documentado para não se perder em meio a ambiente de produção. 

## 1. VPN (Virtual Private Network)

### Tipos recomendados
- OpenVPN (com certificados e TLS)
- IPsec (com autenticação mútua e hashing forte)
- WireGuard (moderno, leve e com criptografia padrão forte)

### Hash e Criptografia recomendados
- SHA-256 ou superior (evite MD5 e SHA1)
- AES-256-CBC ou ChaCha20 para criptografia
- TLS 1.2 ou 1.3 para tunelamento seguro

### Outras recomendações
- Desabilitar protocolos inseguros como PPTP
- Validar certificados com durabilidade limitada e renovação automatizada
- Utilizar autenticação multifator (MFA) quando possível
- Separar o tráfego VPN em VLAN ou regra específica de firewall

## 2. Firewall e Segmentação de Rede

### Boas práticas gerais
- Regra default: negar tudo e liberar por necessidade
- Criar zonas ou segmentos de rede por finalidade (produção, DMZ, convidados, monitoramento)
- Utilizar firewalld, iptables ou pf com controle por interface e serviço
- Registrar regras e motivações "Adicionar comentarios em regras de segurança para melhor visualização"

### Exemplo de regra iptables
```bash
iptables -A INPUT -p tcp --dport 22 -s 192.168.1.0/24 -j ACCEPT
iptables -A INPUT -j DROP
```

## 3. NAT e Roteamento

### Considerações
- Utilizar masquerade apenas onde necessário (ex: saída para internet)
- Evitar NAT dentro da mesma organização (prefira roteamento direto com rotas estáticas ou OSPF)
- Documentar todas as traduções de porta (DNAT)

## 4. DNS Interno e Externo

- Utilizar servidores autoritativos e recursivos separados
- Bloquear consultas DNS externas vindas da LAN (usar DNS forwarder interno)
- Monitorar consultas suspeitas e domínios maliciosos
- Utilizar DNSSEC se aplicável

## 5. Monitoramento de Rede

- Utilizar ferramentas como Zabbix, Prometheus+Blackbox ou LibreNMS
- Monitorar:
  - Latência entre gateways
  - Disponibilidade de links
  - Uso de banda por interface
  - Erros e colisões em interfaces

## 6. Logs e Auditoria

- Centralizar logs de firewall e proxy (ex: rsyslog, Loki, Graylog)
- Armazenar logs com retenção mínima de 6 meses
- Criar alertas para acessos não autorizados ou tráfego fora do padrão

## 7. Considerações adicionais

- Utilizar VLANs para isolar serviços críticos
- Evitar uso de protocolos legados como Telnet, FTP e SNMPv1
- Atualizar firmwares de roteadores, switches e firewalls periodicamente
- Documentar topologia e regras de acesso em ferramentas como NetBox ou diagramas Visio/Draw.io

---

Este documento está em evolução conforme novos aprendizados e aplicações reais são incorporados ao ambiente de rede.