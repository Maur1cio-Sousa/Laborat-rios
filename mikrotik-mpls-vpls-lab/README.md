# MikroTik MPLS/VPLS Backbone Lab

Laboratório de redes desenvolvido como desafio técnico, com o objetivo
de projetar, implementar e validar uma infraestrutura utilizando
MikroTik RouterOS, OSPF, MPLS/LDP e VPLS.

O ambiente possui 13 roteadores e foi construído com foco em
roteamento dinâmico, redundância, transporte MPLS e extensão
Layer 2 através de VPLS.

## 🗺️ Topologia

![Topologia do laboratório](Captura%20de%20tela%202026-09-06%20022050.png)

## 🎯 Objetivos

- Implementar roteamento dinâmico utilizando OSPF
- Configurar métricas para seleção de caminhos
- Implementar MPLS/LDP no backbone
- Estabelecer VPLS entre R1 e R8
- Permitir comunicação Layer 2 entre endpoints remotos
- Implementar redundância e failover
- Integrar servidor Linux com Nginx
- Validar conectividade através de ping e traceroute
- Realizar troubleshooting de falhas reais encontradas durante a implementação

## 🛠️ Tecnologias

- MikroTik RouterOS v7
- OSPF
- MPLS
- LDP
- VPLS
- Linux
- Nginx
- PNETLab

## 🔄 Arquitetura

O OSPF atua como IGP do backbone, sendo responsável pela
distribuição das rotas e seleção dos melhores caminhos.

Sobre essa infraestrutura foi implementado MPLS/LDP.

O VPLS utiliza as loopbacks dos roteadores R1 e R8 como endpoints,
permitindo a extensão de um domínio Layer 2 através do backbone MPLS.

Fluxo simplificado:

VPC-R1
   ↓
Bridge R1
   ↓
VPLS
   ↓
MPLS/LDP
   ↓
Backbone OSPF
   ↓
VPLS
   ↓
Bridge R8
   ↓
VPC-R8
