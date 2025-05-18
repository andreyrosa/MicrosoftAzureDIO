# 💻 Laboratório Azure: Documentação do que Aprendi sobre Máquinas Virtuais 🚀

Este repositório reúne resumos, anotações e conceitos aprendidos sobre máquinas virtuais (VMs) no Microsoft Azure, com foco em documentação técnica clara e estruturada para apoiar estudos e futuras implementações. 📚✨

---

## 📑 Sumário

- [Introdução](#introdução)
- [Sobre Mim](#sobre-mim)
- [O que Aprendi no Azure](#o-que-aprendi-no-azure)
- [Contato](#contato)
- [Conceitos Fundamentais sobre Máquinas Virtuais no Azure](#conceitos-fundamentais-sobre-máquinas-virtuais-no-azure)
- [Redundância e Alta Disponibilidade](#redundância-e-alta-disponibilidade)
- [SLA (Service Level Agreement) e Disponibilidade](#sla-service-level-agreement-e-disponibilidade)
- [Tamanhos, Preços e Escalabilidade](#tamanhos-preços-e-escalabilidade)
- [Backups e Snapshots](#backups-e-snapshots)
- [Acesso Seguro com Azure Bastion](#acesso-seguro-com-azure-bastion)
- [Monitoramento com Azure Monitor](#monitoramento-com-azure-monitor)
- [Dicas e Boas Práticas](#dicas-e-boas-práticas)
- [Passos Práticos na Criação de Recursos no Azure](#passos-práticos-na-criação-de-recursos-no-azure)
- [Referências](#referências)

---

## 📖 Introdução

As máquinas virtuais do Azure são recursos de computação sob demanda que oferecem flexibilidade para criar ambientes virtuais com controle total sobre o sistema operacional e software instalado, sem a necessidade de adquirir hardware físico. Elas são amplamente usadas para:

- Desenvolvimento
- Teste
- Hospedagem de aplicativos na nuvem
- Extensão de datacenters

☁️⚙️

---
## 🎓 O que Aprendi no Azure

Este repositório documenta meu aprendizado sobre máquinas virtuais no Azure, incluindo conceitos fundamentais, configurações, boas práticas e implementações práticas. Os conhecimentos adquiridos fazem parte do curso AZ-900 (Microsoft Azure Fundamentals).

---

## 🧠 Conceitos Fundamentais sobre Máquinas Virtuais no Azure

- **Ambientes sob demanda e escaláveis**: As VMs permitem criar rapidamente computadores virtuais com configurações específicas para atender às necessidades de processamento, memória e armazenamento.
- **Gerenciamento**: Embora o Azure cuide da virtualização e do hardware subjacente, o usuário é responsável por configurar, corrigir e instalar o software dentro da VM.
- **Regiões e localizações**: A localização da VM determina onde os discos virtuais são armazenados e pode impactar latência e conformidade. O Azure oferece múltiplas regiões globais para escolha.
- **Autenticação**: É possível usar nome de usuário e senha ou chaves SSH para acesso seguro às VMs.
- **Discos gerenciados**: O Azure gerencia automaticamente o armazenamento dos discos, facilitando escalabilidade e manutenção.

---

## 🔄 Redundância e Alta Disponibilidade

- **Zonas de disponibilidade**: Áreas fisicamente separadas dentro de uma mesma região que garantem alta disponibilidade, com conectividade garantida de 99,99% ao implantar múltiplas instâncias em zonas diferentes.
- **Conjuntos de dimensionamento**: Permitem criar grupos de VMs com balanceamento de carga e escalabilidade automática, garantindo alta disponibilidade e gerenciamento centralizado.
- **Tipos de redundância de armazenamento**:

| Tipo | Descrição | Indicação |
|------|-----------|-----------|
| LRS (Local Redundant Storage) | Proteção contra falhas locais de hardware | Cenários não críticos |
| GRS (Geo Redundant Storage) | Replicação geográfica para proteção contra falhas regionais | Backup |
| ZRS (Zone Redundant Storage) | Proteção contra falhas em datacenters | Alta disponibilidade |
| GZRS (Geo-Zone Redundant Storage) | Combinação de redundância geográfica e por zona | Dados críticos |

---

## 📊 SLA (Service Level Agreement) e Disponibilidade

O SLA do Azure define os níveis de disponibilidade e o tempo máximo de inatividade permitido para as VMs, com diferentes níveis que impactam diretamente na confiabilidade do serviço:

| SLA | Inatividade Semanal | Inatividade Mensal | Inatividade Anual |
|-----|---------------------|--------------------|--------------------|
| 99% | 1,68 hora ⏳ | 7,2 horas ⏳ | 3,65 dias ⏳ |
| 99,9% | 10,1 minutos ⏳ | 43,2 minutos ⏳ | 8,76 horas ⏳ |
| 99,95% | 5 minutos ⏳ | 21,6 minutos ⏳ | 4,38 horas ⏳ |
| 99,99% | 1,01 minuto ⏳ | 4,32 minutos ⏳ | 52,56 minutos ⏳ |
| 99,999% | 6 segundos ⏳ | 25,9 segundos ⏳ | 5,26 minutos ⏳ |

---

## ⚖️ Tamanhos, Preços e Escalabilidade

- **Tamanhos**: O tamanho da VM define recursos como núcleos de CPU, memória, armazenamento e largura de banda. Deve ser escolhido conforme a carga de trabalho desejada.
- **Preços**: Cobrança por hora baseada no tamanho da VM e sistema operacional; minutos parciais são cobrados proporcionalmente. O custo pode ser otimizado com benefícios como o Azure Hybrid Benefit.
- **Escalabilidade**: É possível escalar verticalmente (tamanho da VM) ou horizontalmente (número de VMs) para atender demandas variáveis, usando conjuntos de dimensionamento e políticas de autoescalonamento.
- **Limites**: Por padrão, há limites de núcleos por assinatura e região, que podem ser aumentados mediante solicitação.

---

## 💾 Backups e Snapshots

- **Backups**: O Azure Backup permite criar cópias de segurança automatizadas das VMs, armazenadas em um Recovery Services Vault. Os backups podem ser agendados e restaurados em caso de falhas ou exclusões acidentais.
- **Snapshots**: Imagens instantâneas dos discos de uma VM, úteis para criar pontos de restauração rápidos ou clonar VMs. Snapshots são armazenados como blobs no Azure e podem ser usados para recuperação ou replicação.
- **Boas práticas**:
  - Configure políticas de backup com retenção adequada para equilibrar custo e proteção.
  - Use snapshots para testes ou mudanças temporárias, mas prefira backups para recuperação de longo prazo.

---

## 🔐 Acesso Seguro com Azure Bastion

- **Azure Bastion**: Serviço que fornece acesso remoto seguro (RDP ou SSH) às VMs sem expor portas públicas. Ele atua como um host gerenciado, reduzindo riscos de ataques.
- **Vantagens**:
  - Conexão via navegador ou Azure Portal, sem necessidade de clientes adicionais.
  - Integração com redes virtuais para maior controle.
- **Configuração**: Associar o Bastion a uma VNET e configurar regras de acesso via NSG (Network Security Group).

---

## 📈 Monitoramento com Azure Monitor

- **Azure Monitor**: Ferramenta para coleta, análise e visualização de métricas e logs das VMs, permitindo monitoramento de desempenho e detecção de problemas.
- **Funcionalidades**:
  - Coleta de métricas como uso de CPU, memória e disco.
  - Configuração de alertas para eventos críticos, como alta utilização de recursos.
  - Integração com Log Analytics para consultas detalhadas.
- **Boas práticas**:
  - Habilite o agente do Azure Monitor nas VMs para coleta de dados detalhada.
  - Crie dashboards personalizados para acompanhar KPIs específicos.

---

## 💡 Dicas e Boas Práticas

- Escolha a região mais próxima dos usuários para minimizar latência. 🌐
- Utilize zonas de disponibilidade para cargas de trabalho críticas.
- Implemente backups regulares e teste restaurações para garantir recuperação.
- Use Azure Bastion para acesso seguro, evitando portas públicas.
- Monitore o desempenho com Azure Monitor e configure alertas proativos.
- Aplique o princípio do menor privilégio no IAM para maior segurança.

---

## ☁️ Aprendizados no Microsoft Azure – Módulo Prático

### 📘 Sobre

Neste módulo prático do curso AZ-900 (Microsoft Azure Fundamentals), adquiri conhecimentos essenciais sobre o uso do Azure para gerenciamento de recursos em nuvem. Abaixo estão os principais tópicos que estudei e pratiquei na plataforma.

### 🧠 Habilidades e Conceitos Aprendidos

#### 📦 Grupo de Recursos

- Criação de Resource Groups para organizar e gerenciar recursos relacionados a uma mesma solução.
- Escolha de região e associação com assinatura adequada.

#### 📜 Log de Atividades

- Monitoramento de ações e eventos dentro do Azure.
- Verificação de quando e por quem um recurso foi criado, alterado ou excluído.

#### 👥 IAM - Controle de Acesso

- Uso do IAM (Identity and Access Management) para:
  - Adicionar e remover usuários.
  - Gerenciar permissões e funções (RBAC – Role-Based Access Control).

#### 🔒 Bloqueios

- Aplicação de Locks (Read-only e Delete) para evitar exclusões ou modificações acidentais de recursos.

#### ⚙️ Eventos

- Utilização de Eventos para criar automatizações com base em ações dentro do ambiente (ex.: criação de recurso).

#### 🌐 Rede Virtual (VNET)

- Criação de VNETs (Virtual Networks) para organização de redes privadas no Azure.
- Definição de endereçamento IP para os ambientes virtuais.

### 🧰 Tecnologias Utilizadas

- 🌐 Microsoft Azure
- 🛠️ Painel do Azure Portal
- 🔐 IAM (Controle de Acesso)
- 🖥️ Resource Manager

### 🏁 Conclusão

Esse aprendizado foi fundamental para entender como gerenciar a infraestrutura em nuvem de forma segura, organizada e automatizada. Agora estou preparado para criar ambientes cloud com boas práticas e maior controle.

### 📎 Links Úteis

- [Portal do Azure](https://portal.azure.com)
- [Documentação Oficial do Azure](https://docs.microsoft.com/azure)
- [Curso AZ-900 na DIO](https://dio.me)

---
## 🛠 Passos Práticos na Criação de Recursos no Azure

A seguir, documentei os passos práticos realizados no Azure Portal para criar uma máquina virtual, um pool de hosts e um aplicativo de funções, com foco nas configurações de redundância, armazenamento e diagnóstico.

### Criação de uma Máquina Virtual

1. **Seleção da assinatura e grupo de recursos**: Escolhi a assinatura "Azure subscription 1" e criei um grupo de recursos chamado "AZ-900_LAB_DIO" para organizar os recursos.
2. **Configuração básica da VM**: Nomeei a VM como "machine01", selecionei a região "(US) East US 2", e optei por nenhuma redundância de infraestrutura (indicado como "Nenhuma redundância infraestrutura necessária").
3. **Zona de disponibilidade**: Mantive a configuração padrão "Nenhuma" para zona de disponibilidade, já que o cenário não exigia alta disponibilidade.
4. **Imagem e tamanho da VM**: Escolhi a imagem "Ubuntu Server 24.04 LTS - x64 Gen2" e o tamanho "Standard B1s" (1 vCPU, 1 GiB de memória).
5. **Arquitetura**: Selecionei a arquitetura "x64" para compatibilidade com a imagem escolhida.
6. **Outras configurações**: Habilitei o uso de discos SSD Premium para armazenamento e deixei as opções de segurança e rede com os valores padrão (ex.: portas públicas RDP abertas, mas com alerta para usar o Azure Bastion para maior segurança).

### Criação de um Pool de Hosts

1. **Assinatura e localização**: Utilizei a mesma assinatura "Azure subscription 1" e escolhi a localização "East US".
2. **Grupo de recursos**: Mantive o grupo de recursos "AZ-900_LAB_DIO" para centralizar os recursos do laboratório.
3. **Ambiente de validação**: Habilitei o ambiente de validação para testes, selecionando "Sim".
4. **Tipo de grupo de aplicativos**: Escolhi "Área de Trabalho" como tipo de grupo de aplicativos preferencial.
5. **Tipo de pool de hosts**: Selecionei o tipo padrão (não especificado como "agrupado" ou "pessoal").

### Criação de um Aplicativo de Funções

1. **Configuração inicial**: Criei um aplicativo de funções com suporte a "Armazenamento de Blobs, Filas e Tabelas", associando-o a uma nova conta de armazenamento chamada "testeavalgroup59a".
2. **Configurações de diagnóstico**: Optei por não definir configurações de diagnóstico inicialmente, mantendo a opção "Não definir as configurações de diagnóstico agora".

### Conceitos Revisados Durante o Processo

- **Tipos de recursos**: Aprendi sobre tipos de computação, instâncias de contêiner, máquinas virtuais e funções no Azure.
- **Hospedagem de aplicativos**: Entendi as opções de hospedagem, como Aplicativos Web do Azure, contêineres e máquinas virtuais.
- **Redes e conectividade**: Revisei conceitos de redes virtuais, sub-redes, emparelhamento, DNS, Gateway de VPN e ExpressRoute.

---

🧠 Análise de Texto e Resposta a Perguntas
Aprendi como utilizar os serviços cognitivos do Azure para analisar textos, identificar sentimentos, extrair entidades e responder a perguntas automaticamente, facilitando a criação de soluções inteligentes baseadas em linguagem natural.

🤖 Serviço de Bot do Azure
Explorei como criar, configurar e integrar bots inteligentes utilizando o Azure Bot Service, permitindo interações automatizadas com usuários por meio de canais como chat, Teams e outros.

🗣️ Compreensão da Linguagem Coloquial
Estudei como treinar modelos capazes de entender linguagem informal e expressões cotidianas, algo essencial para tornar aplicações mais próximas da forma como as pessoas realmente se comunicam.

🔗 Links Úteis
Foram disponibilizados recursos e materiais de apoio com links para a documentação oficial da Microsoft, exemplos práticos e laboratórios online, que complementaram muito bem o conteúdo apresentado.

🧪 Conhecendo o Estúdio de Fala
Aprendi a utilizar o Speech Studio para criar, testar e melhorar modelos de conversão de fala em texto e vice-versa, além de reconhecer comandos de voz e ajustar sotaques ou pronúncias específicas.

🧰 Conhecendo o Language Studio
Tive contato com o Language Studio, uma ferramenta poderosa do Azure que permite a criação de projetos de linguagem natural com foco em classificação de texto, extração de informações e análise semântica.


## 🛠️ Gerenciamento de Recursos no Azure

- **Listagem e Filtros**: Aprendi a listar e filtrar recursos no Azure Portal, como serviços de pesquisa (`azuresearchmod5`), contas de armazenamento (`storageacc11`) e contas multi-serviços (`instancename01`).
- **Detalhes dos Recursos**:
  - **Grupo de Recursos**: `AZ-900_LAB_DIO`
  - **Localização**: `East US`
  - **Assinatura**: `Azure subscription 1`
- **Organização**: Utilizei filtros para agrupar recursos por tipo, localização e assinatura, facilitando a gestão.

## 📦 Azure Blob Storage

- **Contêineres**: Trabalhei com a conta de armazenamento `storageacc11`, explorando a criação e gerenciamento de contêineres.
- **Gerenciamento de Contêineres**:
  - Criei contêineres como `slogs` e `coffeereviews`.
  - Configurei níveis de acesso (público, privado, contêiner) e verifiquei estados de conexão.
  - Acompanhei a última modificação dos contêineres (ex.: `18/05/2025`).
- **Uso Prático**: Entendi como o Blob Storage pode ser usado para armazenar dados não estruturados, como logs e arquivos de texto.

## 🔍 Azure AI Search

- **Serviço de Pesquisa**: Configurei e explorei o `azuresearchmod4`, um serviço de pesquisa baseado em IA.
- **Índices e Pesquisa**:
  - Criei um índice chamado `coffee-index`.
  - Realizei consultas específicas, como `search=locations:'Chicago'`, para buscar dados com base em critérios.
- **Funcionalidades**:
  - Naveguei pelo **Search Explorer** para testar consultas.
  - Aprendi sobre a integração do Azure AI Search com outros serviços para criar experiências de busca com texto completo e ranqueamento semântico.



## 📚 Referências

- [Documentação Oficial do Azure](https://docs.microsoft.com/azure)
- [Guia de Máquinas Virtuais no Azure](https://docs.microsoft.com/azure/virtual-machines)
- [Curso AZ-900 na DIO](https://dio.me)
