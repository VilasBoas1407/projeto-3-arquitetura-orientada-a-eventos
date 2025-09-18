# 🚛 Projeto 3 – Rastreamento da Frota de Caminhões em Tempo Real  

> 📖 Este projeto é baseado no conteúdo do livro  
> **Arquitetura Orientada a Eventos: Soluções Escaláveis e em Tempo Real com EDA**  
> Autor: *Roberto Picanço*  

---

## 📌 Sobre o Projeto  
O objetivo deste projeto é propor a implementação de uma solução de **rastreamento de frota de caminhões em tempo real**.  

Essa solução pode ser utilizada por transportadoras que desejam acompanhar sua carga através das **coordenadas geográficas dos caminhões**, possibilitando:  
- Monitoramento em tempo real.  
- Estimativa precisa de chegada (ETA).  
- Mais segurança e otimização da logística.  

---

## 📂 Estrutura do Conteúdo  

- [📖 Descrição do Problema e Escopo](#-descrição-do-problema-e-escopo)  
- [⚙️ Como Executar o Projeto](#️-como-executar-o-projeto)  
- [✅ Requisitos](#-requisitos)  
- [📚 Referências](#-referências)  

---

## 📖 Descrição do Problema e Escopo  

A empresa fictícia **TrackerJá** oferece serviço de rastreamento da frota em tempo real para diversas transportadoras.  
- Atualmente atende **500 transportadoras** ao redor do mundo.  
- Previsão de crescimento de **40%** no próximo ano.  
- Exemplo: cliente principal possui **5 mil caminhões** na frota.  

### Funcionalidade principal:
- Consultar localização da frota em tempo real.  
- Possibilidade de visualizar em mapas, calcular distância, configurar alertas de rota e gerar relatórios.  

### Futuro (fase 2 – clientes premium):  
- Visualização da frota em **mapa integrado** fornecido pela própria TrackerJá.  

---

## ⚙️ Como Executar o Projeto  

### Pré-requisitos
- [Node.js](https://nodejs.org/) (>= 18.x)  
- [NestJS CLI](https://docs.nestjs.com/cli/overview)  

### Passos

```bash
# Clone este repositório
git clone https://github.com/seu-usuario/seu-repositorio.git

# Acesse a pasta do projeto
cd seu-repositorio

# Instale as dependências
npm install

# Execute a aplicação em modo desenvolvimento
npm run start:dev

# Ou em modo produção
npm run build
npm run start:prod

A aplicação por padrão sobe em:
👉 http://localhost:3000

```


## ✅ Requisitos  

### 📌 Requisitos Funcionais – Fase 1  
- 🚚 O sistema de GPS em cada caminhão deve enviar:  
  - Identificador do caminhão  
  - Coordenadas geográficas (latitude e longitude)  
  - Data e hora (a cada 5 segundos)  
- 🧑‍✈️ A base de dados de motoristas deve conter:  
  - Nome do motorista  
  - Identificador do caminhão em que está alocado  
- 🔎 Transportadoras podem consultar via **API** a localização da frota em tempo real.  
- ⏪ Transportadoras podem **reproduzir uma viagem específica** via API.  

---

### 📌 Requisitos Funcionais – Fase 2 (Clientes Premium)  
- 🗺️ Clientes podem visualizar em **mapa** a localização da frota em tempo real.  
- 📅 Clientes podem reproduzir e visualizar no mapa **uma viagem em uma data escolhida**.  

---

### 📌 Requisitos Não Funcionais  
- ⚡ **Alta disponibilidade**:  
  - Garantir recebimento de informações de localização a cada 5 segundos.  
  - Atender todas as consultas de localização.  
- 📈 **Escalabilidade**:  
  - Atender consultas em tempo real, independentemente da quantidade de caminhões.  
- 🚀 **Baixa latência**:  
  - Consultas devem ser rápidas.  
  - Estimativa de **56 mil QPS (queries per second)** nas consultas por caminhão.  

---

## 📚 Referências  

- Picanço, Roberto. *Arquitetura Orientada a Eventos: Soluções Escaláveis e em Tempo Real com EDA*.  
- [NestJS Documentation](https://docs.nestjs.com/)  
- [Node.js](https://nodejs.org/)  
- [Event-Driven Architecture (EDA) – AWS Reference](https://aws.amazon.com/architecture/event-driven-architecture/)  

