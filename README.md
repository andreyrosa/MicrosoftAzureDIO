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


## 📚 O que aprendi no Azure

- 🌐 **Grupo de Recursos**  
- 📜 **Log de Atividades**  
- 🔐 **IAM (Controle de Acesso)**  
- ⛔ **Bloqueios**  
- ⚡ **Eventos e Automatizações**  
- 🌍 **VNET e Endereçamento de Rede**


![GitHub repo size](https://img.shields.io/github/repo-size/seuusuario/seurepositorio?style=flat-square)
![GitHub language count](https://img.shields.io/github/languages/count/seuusuario/seurepositorio?style=flat-square)
![GitHub top language](https://img.shields.io/github/languages/top/seuusuario/seurepositorio?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/seuusuario/seurepositorio?style=flat-square)

### 🛠 Tecnologias Utilizadas

### 🛠 Tecnologias Utilizadas

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/azure/azure-original.svg" width="40" alt="Azure" /> 
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/terraform/terraform-original.svg" width="40" alt="Terraform" /> 
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="40" alt="Docker" />
</div>



