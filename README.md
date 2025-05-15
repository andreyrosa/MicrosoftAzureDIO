# 💻 Laboratório Azure: Documentação do que Aprendi sobre Máquinas Virtuais 🚀

Este repositório reúne resumos, anotações e conceitos aprendidos sobre máquinas virtuais (VMs) no Microsoft Azure, com foco em documentação técnica clara e estruturada para apoiar estudos e futuras implementações. 📚✨

---
## 📑 Sumário

- [Introdução](#introdução)
- [Sobre mim](#sobre-mim)  
- [O que aprendi no Azure](#o-que-aprendi-no-azure)  
- [Contato](#contato)

- [Conceitos Fundamentais sobre Máquinas Virtuais no Azure](#conceitos-fundamentais-sobre-máquinas-virtuais-no-azure)
- [Redundância e Alta Disponibilidade](#redundância-e-alta-disponibilidade)
- [SLA (Service Level Agreement) e Disponibilidade](#sla-service-level-agreement-e-disponibilidade)
- [Tamanhos, Preços e Escalabilidade](#tamanhos-preços-e-escalabilidade)
- [Dicas e Boas Práticas](#dicas-e-boas-práticas)
- [Referências](#referências)

---

## 📖 Introdução

As máquinas virtuais do Azure são recursos de computação sob demanda que oferecem flexibilidade para criar ambientes virtuais com controle total sobre o sistema operacional e software instalado, sem a necessidade de adquirir hardware físico. Elas são amplamente usadas para desenvolvimento, teste, hospedagem de aplicativos na nuvem e extensão de datacenters. ☁️⚙️

---

## 🧠 Conceitos Fundamentais sobre Máquinas Virtuais no Azure

- **Ambientes sob demanda e escaláveis:** As VMs permitem criar rapidamente computadores virtuais com configurações específicas para atender às necessidades de processamento, memória e armazenamento.  
- **Gerenciamento:** Embora o Azure cuide da virtualização e do hardware subjacente, o usuário é responsável por configurar, corrigir e instalar o software dentro da VM.  
- **Regiões e localizações:** A localização da VM determina onde os discos virtuais são armazenados e pode impactar latência e conformidade. O Azure oferece múltiplas regiões globais para escolha.  
- **Autenticação:** É possível usar nome de usuário e senha ou chaves SSH para acesso seguro às VMs.  
- **Discos gerenciados:** O Azure gerencia automaticamente o armazenamento dos discos, facilitando escalabilidade e manutenção.  

---

## 🔄 Redundância e Alta Disponibilidade

- **Zonas de disponibilidade:** São áreas fisicamente separadas dentro de uma mesma região que garantem alta disponibilidade, com conectividade garantida de 99,99% ao implantar múltiplas instâncias em zonas diferentes.  
- **Conjuntos de dimensionamento:** Permitem criar grupos de VMs com balanceamento de carga e escalabilidade automática, garantindo alta disponibilidade e gerenciamento centralizado.  
- **Tipos de redundância de armazenamento:**  
  | Tipo                      | Descrição                                         | Indicação              |
  |---------------------------|-------------------------------------------------|-----------------------|
  | **LRS** (Local Redundant Storage)    | Proteção contra falhas locais de hardware          | Cenários não críticos  |
  | **GRS** (Geo Redundant Storage)      | Replicação geográfica para proteção contra falhas regionais | Backup                 |
  | **ZRS** (Zone Redundant Storage)     | Proteção contra falhas em datacenters               | Alta disponibilidade   |
  | **GZRS** (Geo-Zone Redundant Storage)| Combinação de redundância geográfica e por zona     | Dados críticos         |

---

## 📊 SLA (Service Level Agreement) e Disponibilidade

O SLA do Azure define os níveis de disponibilidade e o tempo máximo de inatividade permitido para as VMs, com diferentes níveis que impactam diretamente na confiabilidade do serviço:

| SLA      | Inatividade semanal | Inatividade mensal | Inatividade anual    |
|----------|---------------------|--------------------|---------------------|
| 99%      | 1,68 hora ⏳        | 7,2 horas ⏳       | 3,65 dias ⏳         |
| 99,9%    | 10,1 minutos ⏳     | 43,2 minutos ⏳    | 8,76 horas ⏳        |
| 99,95%   | 5 minutos ⏳        | 21,6 minutos ⏳    | 4,38 horas ⏳        |
| 99,99%   | 1,01 minuto ⏳      | 4,32 minutos ⏳    | 52,56 minutos ⏳     |
| 99,999%  | 6 segundos ⏳       | 25,9 segundos ⏳   | 5,26 minutos ⏳      |

---

## ⚖️ Tamanhos, Preços e Escalabilidade

- **Tamanhos:** O tamanho da VM define recursos como núcleos de CPU, memória, armazenamento e largura de banda. Deve ser escolhido conforme a carga de trabalho desejada.  
- **Preços:** Cobrança por hora baseada no tamanho da VM e sistema operacional; minutos parciais são cobrados proporcionalmente. O custo pode ser otimizado com benefícios como o Azure Hybrid Benefit.  
- **Escalabilidade:** É possível escalar verticalmente (tamanho da VM) ou horizontalmente (número de VMs) para atender demandas variáveis, usando conjuntos de dimensionamento e políticas de autoescalonamento.  
- **Limites:** Por padrão, há limites de núcleos por assinatura e região, que podem ser aumentados mediante solicitação.  

---

## 💡 Dicas e Boas Práticas

- Escolha a região mais próxima dos usuários para minimizar latência. 🌐  
- Utilize zonas de disponibilidade


# ☁️ Aprendizados no Microsoft Azure – Módulo Prático

![Azure](https://img.shields.io/badge/Microsoft%20Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Status](https://img.shields.io/badge/Status-Concluído-2ea44f?style=for-the-badge)
![Lab](https://img.shields.io/badge/Lab-AZ--900-blue?style=for-the-badge)

## 📘 Sobre

Neste módulo prático do curso **AZ-900 (Microsoft Azure Fundamentals)**, adquiri conhecimentos essenciais sobre o uso do Azure para gerenciamento de recursos em nuvem. Abaixo estão os principais tópicos que estudei e pratiquei na plataforma.

---

## 🧠 Habilidades e Conceitos Aprendidos

### 📦 Grupo de Recursos
- Criação de **Resource Groups** para organizar e gerenciar recursos relacionados a uma mesma solução.
- Escolha de região e associação com assinatura adequada.
  
### 📜 Log de Atividades
- Monitoramento de **ações e eventos** dentro do Azure.
- Verificação de **quando e por quem** um recurso foi criado, alterado ou excluído.

### 👥 IAM - Controle de Acesso
- Uso do **IAM (Identity and Access Management)** para:
  - Adicionar e remover usuários.
  - Gerenciar **permissões** e funções (RBAC – Role-Based Access Control).

### 🔒 Bloqueios
- Aplicação de **Locks** (`Read-only` e `Delete`) para evitar exclusões ou modificações acidentais de recursos.

### ⚙️ Eventos
- Utilização de **Eventos** para criar **automatizações** com base em ações dentro do ambiente (ex: criação de recurso).

### 🌐 Rede Virtual (VNET)
- Criação de **VNETs (Virtual Networks)** para organização de redes privadas no Azure.
- Definição de **endereçamento IP** para os ambientes virtuais.
---

## 🧰 Tecnologias Utilizadas

- 🌐 **Microsoft Azure**
- 🛠️ **Painel do Azure Portal**
- 🔐 **IAM (Controle de Acesso)**
- 🖥️ **Resource Manager**

---

## 🏁 Conclusão

Esse aprendizado foi fundamental para entender como gerenciar a **infraestrutura em nuvem de forma segura, organizada e automatizada**. Agora estou preparado para criar ambientes cloud com boas práticas e maior controle.

---

## 📎 Links úteis

- [Portal do Azure](https://portal.azure.com/)
- [Documentação Oficial do Azure](https://learn.microsoft.com/pt-br/azure/)
- [Curso AZ-900 na DIO](https://www.dio.me/)

### 🛠 Tecnologias Utilizadas
<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/azure/azure-original.svg" width="40" alt="Azure" /> 
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/terraform/terraform-original.svg" width="40" alt="Terraform" /> 
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="40" alt="Docker" />
</div>



