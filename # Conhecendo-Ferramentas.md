# Conhecendo Ferramentas

Aqui vamos reunir uma curadoria prática e objetiva sobre ferramentas essenciais no dia a dia de profissionais de tecnologia — de infraestrutura a desenvolvimento.

---

## Sumário

1. [Linux](#linux)
2. [VSCode](#vscode)
3. [Providers (AWS, Azure, etc.)](#providers)
4. [GitLab](#gitlab)
5. [Docker](#docker)
6. [Portainer](#portainer)
7. [Mikrotik](#mikrotik)
8. [OpenStack](#openstack)
9. [Proxmox](#proxmox)
10. [Grafana](#grafana)
11. [Loki](#loki)
12. [Ansible](#ansible)
13. [Terraform](#terraform)
14. [Nginx](#nginx)

---

## Linux

### O que é?
Linux é um sistema operacional open source baseado em Unix. Ele oferece flexibilidade, segurança e é amplamente usado em servidores, dispositivos IoT e sistemas embarcados.

### Por que usar?
- Gratuito e de código aberto
- Seguro e estável
- Ampla documentação e comunidade

### Como começar?
- Instale uma distribuição como Ubuntu, Fedora ou Debian.
- Aprenda comandos básicos do terminal.
- Configure o sistema conforme sua necessidade.

### Instalação e configuração:
```bash
sudo apt update && sudo apt upgrade
sudo apt install build-essential curl git
```

### Configurações de Rede:
```bash
sudo nano /etc/netplan/01-netcfg.yaml
sudo netplan apply
```

### Instalação de Programas:
```bash
sudo apt install nome-do-programa
```

### Recursos adicionais:
- [Comandos Linux - Repositório de Referência](https://github.com/user/comandos-linux)
- [Tutoriais para iniciantes (Linux.org)](https://linux.org/forums/linux-beginner-tutorials.123/)
- [Documentação Oficial do Ubuntu](https://ubuntu.com/tutorials)

---

## VSCode

Editor de código leve e extensível da Microsoft, amplamente usado por desenvolvedores front-end e back-end.

- [Documentação oficial](https://code.visualstudio.com/docs)

*(Conteúdo em desenvolvimento)*

---

## Providers (AWS, Azure, etc.)

Serviços de nuvem que fornecem infraestrutura sob demanda.

- [AWS Documentation](https://docs.aws.amazon.com/)
- [Azure Documentation](https://learn.microsoft.com/azure/)
- [Google Cloud Docs](https://cloud.google.com/docs)

*(Conteúdo em desenvolvimento)*

---

## GitLab

Plataforma de DevOps que integra controle de versão, CI/CD e gerenciamento de projetos.

- [Documentação oficial](https://docs.gitlab.com/)

*(Conteúdo em desenvolvimento)*

---

## Docker

Ferramenta para empacotar aplicações em containers, garantindo consistência entre ambientes.

- [Documentação oficial](https://docs.docker.com/)

*(Conteúdo em desenvolvimento)*

---

## Portainer

Interface de gerenciamento para Docker e Kubernetes.

- [Documentação oficial](https://docs.portainer.io/)

*(Conteúdo em desenvolvimento)*

---

## Mikrotik

Fabricante de equipamentos de rede e software RouterOS.

- [Documentação oficial](https://help.mikrotik.com/)

*(Conteúdo em desenvolvimento)*

---

## OpenStack

Plataforma open source para criação de nuvens privadas.

- [Documentação oficial](https://docs.openstack.org/)

*(Conteúdo em desenvolvimento)*

---

## Proxmox

Solução para virtualização baseada em KVM e LXC, com gerenciamento via interface web.

- [Documentação oficial](https://pve.proxmox.com/pve-docs/)

*(Conteúdo em desenvolvimento)*

---

## Grafana

Ferramenta de visualização de métricas e dashboards dinâmicos.

- [Documentação oficial](https://grafana.com/docs/)

*(Conteúdo em desenvolvimento)*

---

## Loki

Solução de logging integrada ao Grafana.

- [Documentação oficial](https://grafana.com/docs/loki/)

*(Conteúdo em desenvolvimento)*

---

## Ansible

Automatizador de configurações e tarefas em infraestrutura.

- [Documentação oficial](https://docs.ansible.com/)

*(Conteúdo em desenvolvimento)*

---

## Terraform

Ferramenta de infraestrutura como código, gerenciando recursos em vários provedores.

- [Documentação oficial](https://developer.hashicorp.com/terraform/docs)

*(Conteúdo em desenvolvimento)*

---

## Nginx

Servidor web e proxy reverso de alta performance.

- [Documentação oficial](https://nginx.org/en/docs/)

*(Conteúdo em desenvolvimento)*

