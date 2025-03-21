Planilha de Recursos e Custos - E-commerce OCI (Alto Desempenho)
================================================================

1. Infraestrutura Front-End
---------------------------

| Componente | Serviço OCI | Dimensionamento | Custo Mensal Estimado (USD) |
| --- | --- | --- | --- |
| CDN | Oracle CDN | 15 TB de transferência mensal | $1,200 |
| Static Frontend | Object Storage + CDN | 50GB de armazenamento | $2 (Storage) + já incluído acima |
| **Subtotal Front-End** |  |  | **$1,202** |

2. Camada de Aplicação
----------------------

| Componente | Serviço OCI | Dimensionamento | Custo Mensal Estimado (USD) |
| --- | --- | --- | --- |
| E-Commerce App | OKE (Kubernetes) | 20 nós VM.Standard.E4.2 (2 OCPUs, 16GB) | $2,640 |
| API Gateway | API Gateway | 100 milhões de solicitações mensais | $400 |
| Functions | OCI Functions | 20 milhões de invocações | $100 |
| Messaging | Oracle Streaming | 50 TB processados | $250 |
| Notificações | OCI Notifications | 10 milhões de notificações | $90 |
| **Subtotal Camada de Aplicação** |  |  | **$3,480** |

3. Camada de Dados
------------------

| Componente | Serviço OCI | Dimensionamento | Custo Mensal Estimado (USD) |
| --- | --- | --- | --- |
| Customers DB | ATP (Autonomous Transaction Processing) | 8 OCPUs, 64 GB de RAM | $2,304 |
| Orders DB | ATP | 8 OCPUs, 64 GB de RAM | $2,304 |
| Catalog DB | ATP | 4 OCPUs, 32 GB de RAM | $1,152 |
| Pricing DB | ATP | 2 OCPUs, 16 GB de RAM | $576 |
| Cache | Redis Enterprise | 4 nós de cache distribuído | $800 |
| NoSQL DB | NoSQL Database | 15 TB de armazenamento, 20M de operações/dia | $900 |
| **Subtotal Camada de Dados** |  |  | **$8,036** |

4. Monitoramento e Operações
----------------------------

| Componente | Serviço OCI | Dimensionamento | Custo Mensal Estimado (USD) |
| --- | --- | --- | --- |
| Monitoring | OCI Monitoring | Monitoramento básico + 100GB de métricas | $150 |
| Logging | OCI Logging | 100GB de logs | $100 |
| Application Performance Monitoring | APM | Monitoramento premium | $300 |
| Health Checks | Health Checks | 50 endpoints | $45 |
| **Subtotal Monitoramento** |  |  | **$595** |

5. Segurança e Rede
-------------------

| Componente | Serviço OCI | Dimensionamento | Custo Mensal Estimado (USD) |
| --- | --- | --- | --- |
| WAF | OCI WAF | 100 milhões de solicitações | $350 |
| DDoS Protection | OCI DDoS Protection | Proteção avançada | $1,000 |
| Identity | OCI IAM | Gestão de identidade | Incluído |
| Load Balancers | Load Balancer | 2 balanceadores (100 Mbps) | $292 |
| Bastion | Bastion Service | Acesso seguro | Incluído |
| **Subtotal Segurança e Rede** |  |  | **$1,642** |

6. Custos de Transferência de Dados
-----------------------------------

| Tipo | Volume Estimado | Custo Mensal Estimado (USD) |
| --- | --- | --- |
| Saída de dados (além do CDN) | 5 TB | $225 |
| Transferência entre regiões | 10 TB | $225 |
| **Subtotal Transferência** |  | **$450** |

7. Custos de Suporte
--------------------

| Plano | Cobertura | Custo Mensal Estimado (USD) |
| --- | --- | --- |
| OCI Premium Support | 24/7 suporte técnico + acesso a especialistas | $950 |
| **Subtotal Suporte** |  | **$950** |

Resumo de Custos
----------------

| Categoria | Custo Mensal Estimado (USD) |
| --- | --- |
| Front-End | $1,202 |
| Camada de Aplicação | $3,480 |
| Camada de Dados | $8,036 |
| Monitoramento e Operações | $595 |
| Segurança e Rede | $1,642 |
| Transferência de Dados | $450 |
| Suporte | $950 |
| **Total Mensal Estimado** | **$16,355** |
| **Total Anual Estimado** | **$196,260** |

Potenciais Otimizações de Custo na OCI
--------------------------------------

1.  **Oracle Universal Credits**: Compromissos anuais para descontos de 25-35%
2.  **Bring Your Own License (BYOL)**: Reutilizar licenças Oracle existentes para redução significativa
3.  **OCI Reservations**: Reserva de capacidade com desconto de até 50% para compromissos de 1-3 anos
4.  **Autoscaling**: Configuração para escalar recursos automaticamente baseado em demanda
5.  **Always Free Services**: Utilização de serviços gratuitos da OCI onde viável
6.  **Storage Tiering**: Implementação de políticas para dados acessados com menos frequência
