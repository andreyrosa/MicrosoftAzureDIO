# MicrosoftAzureDIO

# 💻 Laboratório Azure: Criação e Configuração de Máquina Virtual 🚀

Este repositório documenta o passo a passo para criação e configuração de uma máquina virtual (VM) no Microsoft Azure, com resumos, anotações e dicas práticas. O objetivo é servir como material de apoio para estudos e futuras implementações. 📚✨

---

## 📋 Sumário

- [Introdução](#introdução)
- [Passo a Passo: Criando uma VM no Azure](#passo-a-passo-criando-uma-vm-no-azure)
- [Opções de Redundância de Armazenamento](#opções-de-redundância-de-armazenamento)
- [SLA (Service Level Agreement) e Disponibilidade](#sla-service-level-agreement-e-disponibilidade)
- [Dicas e Boas Práticas](#dicas-e-boas-práticas)
- [Referências](#referências)

---

## 📖 Introdução

A criação de máquinas virtuais no Azure permite provisionar rapidamente ambientes de testes, desenvolvimento ou produção, com alta disponibilidade e flexibilidade de configuração. ☁️⚙️

---

## 🛠️ Passo a Passo: Criando uma VM no Azure

1. **Acesse o Portal do Azure**  
   Vá para [portal.azure.com](https://portal.azure.com) e faça login. 🔐

2. **Inicie a criação da VM**  
   No menu lateral, selecione **Máquinas virtuais** e clique em **Criar**. ➕

3. **Preencha os detalhes da instância**  
   - **Nome da máquina virtual:** Defina um nome identificador. 🏷️  
   - **Região:** Escolha a localização do datacenter (ex: East US). 🌍  
   - **Opções de disponibilidade:** Escolha entre zona de disponibilidade ou nenhuma. 🏢  
   - **Zona de disponibilidade:** Selecione a zona desejada (ex: Zona 1). 📍

4. **Configurações de segurança e imagem**  
   - **Tipo de segurança:** Recomenda-se “Computadores virtuais de inicialização confiável”. 🔒  
   - **Imagem:** Escolha o sistema operacional (ex: Windows Server 2019 Datacenter). 🖥️

5. **Avance e revise as configurações**  
   Clique em **Avançar: Discos**, configure conforme necessidade e finalize em **Revisar + criar**. ✅

---

## 💾 Opções de Redundância de Armazenamento

O Azure oferece diferentes tipos de redundância para armazenamento, cada um indicado para cenários específicos:

| Tipo                      | Descrição                                         | Indicação              |
|---------------------------|-------------------------------------------------|-----------------------|
| **LRS** (Local Redundant Storage)    | Proteção básica contra falhas de hardware locais | Cenários não críticos  |
| **GRS** (Geo Redundant Storage)      | Failover entre regiões, proteção contra falhas regionais | Backup                 |
| **ZRS** (Zone Redundant Storage)     | Proteção contra falhas no nível de datacenter    | Alta disponibilidade   |
| **GZRS** (Geo-Zone Redundant Storage)| Combina redundância de zona e geográfica         | Dados críticos         |

---

## 📊 SLA (Service Level Agreement) e Disponibilidade

O SLA define o tempo máximo de inatividade permitido para cada nível de serviço. Exemplos:

| SLA      | Inatividade semanal | Inatividade mensal | Inatividade anual    |
|----------|---------------------|--------------------|---------------------|
| 99%      | 1,68 hora ⏳        | 7,2 horas ⏳       | 3,65 dias ⏳         |
| 99,9%    | 10,1 minutos ⏳     | 43,2 minutos ⏳    | 8,76 horas ⏳        |
| 99,95%   | 5 minutos ⏳        | 21,6 minutos ⏳    | 4,38 horas ⏳        |
| 99,99%   | 1,01 minuto ⏳      | 4,32 minutos ⏳    | 52,56 minutos ⏳     |
| 99,999%  | 6 segundos ⏳       | 25,9 segundos ⏳   | 5,26 minutos ⏳      |

---

## 💡 Dicas e Boas Práticas

- 🌐 Escolha a região mais próxima dos usuários finais para menor latência.  
- 🛡️ Utilize zonas de disponibilidade e armazenamento redundante para aplicações críticas.  
- 📝 Documente cada etapa do processo para facilitar futuras manutenções.  
- 🏷️ Use tags e nomes padronizados para facilitar a gestão dos recursos.  
- 🔄 Revise periodicamente as configurações de segurança e backup.

---

## 📚 Referências

- [Documentação Oficial Microsoft Azure: Criar uma máquina virtual](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)  
- [GitHub Docs: Sintaxe de Markdown](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

---

> 🙌 **Contribuições são bem-vindas!** Sinta-se à vontade para adicionar novas dicas, resumos ou experiências para enriquecer este material. 🚀
