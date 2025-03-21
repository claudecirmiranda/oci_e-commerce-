Planilha de Recursos e Custos Otimizados - E-commerce OCI
=======================================================================

1. Infraestrutura Front-End
---------------------------

| Componente | Serviço OCI | Dimensionamento Reduzido | Custo Mensal Estimado (USD) |
| --- | --- | --- | --- |
| CDN | Oracle CDN | 8 TB de transferência mensal | $650 |
| Static Frontend | Object Storage + CDN | 30GB de armazenamento | $1 (Storage) + já incluído acima |
| **Subtotal Front-End** |  |  | **$651** |

2. Camada de Aplicação
----------------------

| Componente | Serviço OCI | Dimensionamento Reduzido | Custo Mensal Estimado (USD) |
| --- | --- | --- | --- |
| E-Commerce App | OKE (Kubernetes) | 10 nós VM.Standard.E3.Flex (2 OCPUs, 8GB) | $1,200 |
| API Gateway | API Gateway | 50 milhões de solicitações mensais | $200 |
| Functions | OCI Functions | 10 milhões de invocações | $50 |
| Messaging | Oracle Streaming | 20 TB processados | $100 |
| Notificações | OCI Notifications | 5 milhões de notificações | $45 |
| **Subtotal Camada de Aplicação** |  |  | **$1,595** |

3. Camada de Dados
------------------

| Componente | Serviço OCI | Dimensionamento Reduzido | Custo Mensal Estimado (USD) |
| --- | --- | --- | --- |
| Customers DB | ATP (Autonomous Transaction Processing) | 2 OCPUs, 16 GB RAM | $576 |
| Orders DB | ATP | 2 OCPUs, 16 GB RAM | $576 |
| Catalog DB | ATP (Autoscaling) | 2 OCPUs base, escala até 4 OCPUs | $576 |
| Pricing DB | ADW (Autonomous Data Warehouse) | 1 OCPU, 8 GB RAM | $288 |
| Cache | Redis in OKE | Gerenciado em containers no cluster | Incluído em OKE |
| NoSQL DB | NoSQL Database | 5 TB de armazenamento, 5M de operações/dia | $300 |
| **Subtotal Camada de Dados** |  |  | **$2,316** |

4. Monitoramento e Operações
----------------------------

| Componente | Serviço OCI | Dimensionamento Reduzido | Custo Mensal Estimado (USD) |
| --- | --- | --- | --- |
| Monitoring | OCI Monitoring | Monitoramento básico + 50GB de métricas | $75 |
| Logging | OCI Logging | 50GB de logs | $50 |
| Health Checks | Health Checks | 20 endpoints | $18 |
| **Subtotal Monitoramento** |  |  | **$143** |

5. Segurança e Rede
-------------------

| Componente | Serviço OCI | Dimensionamento Reduzido | Custo Mensal Estimado (USD) |
| --- | --- | --- | --- |
| WAF | OCI WAF | 50 milhões de solicitações | $175 |
| DDoS Protection | OCI DDoS Protection | Proteção básica | Incluído |
| Identity | OCI IAM | Gestão de identidade | Incluído |
| Load Balancers | Load Balancer | 2 balanceadores (10 Mbps) | $146 |
| Bastion | Bastion Service | Acesso seguro | Incluído |
| **Subtotal Segurança e Rede** |  |  | **$321** |

6. Custos de Transferência de Dados
-----------------------------------

| Tipo | Volume Estimado Reduzido | Custo Mensal Estimado (USD) |
| --- | --- | --- |
| Saída de dados (além do CDN) | 3 TB | $135 |
| Transferência entre regiões | 5 TB | $112 |
| **Subtotal Transferência** |  | **$247** |

7. Custos de Suporte
--------------------

| Plano | Cobertura | Custo Mensal Estimado (USD) |
| --- | --- | --- |
| OCI Basic Support | Suporte básico em horário comercial | $100 |
| **Subtotal Suporte** |  | **$100** |

8. Descontos com Compromissos
-----------------------------

| Estratégia | Aplicação | Economia Mensal Estimada (USD) |
| --- | --- | --- |
| Oracle Universal Credits | Compromisso anual (25% desconto) | -$1,200 |
| OCI Reservations | Reserva ATP/OKE por 1 ano | -$800 |
| **Subtotal Economia** |  | **-$2,000** |

Resumo de Custos
----------------

| Categoria | Custo Mensal Estimado (USD) |
| --- | --- |
| Front-End | $651 |
| Camada de Aplicação | $1,595 |
| Camada de Dados | $2,316 |
| Monitoramento e Operações | $143 |
| Segurança e Rede | $321 |
| Transferência de Dados | $247 |
| Suporte | $100 |
| Subtotal | $5,373 |
| Descontos com Compromissos | -$2,000 |
| **Total Mensal Base Estimado** | **$3,373** |
| **Reserva para Contingências (25%)** | **$844** |
| **Reserva para Escala em Picos (40%)** | **$1,350** |
| **Total Mensal com Reservas** | **$5,567** |
| **Total Anual Estimado** | **$66,804** |

Limitações e Considerações deste Orçamento
------------------------------------------

1.  **Vantagens OCI**:
    *   Modelo de preços mais previsível que outros provedores
    *   ATP com autoscaling permite economizar recursos em períodos de baixa demanda
    *   Custos de transferência de dados significativamente mais baixos que em outros provedores
2.  **Capacidade**:
    *   Suporta 3-5 milhões de visitantes mensais
    *   Capacidade para 200-300 mil transações mensais
    *   Margens para escala em momentos de pico (incluídas nas reservas)
3.  **Otimizações adicionais disponíveis**:
    *   Pré-pago anual em vez de mensal (economia adicional de 10-15%)
    *   Use de licenças Oracle existentes (BYOL) se disponíveis
    *   Versões "standard" do ATP em vez de "enterprise" para bancos de dados menos críticos

![image](https://github.com/user-attachments/assets/7fe6bba7-fd61-46cb-9374-323c2a44c89b)
