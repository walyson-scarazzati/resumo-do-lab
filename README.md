# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

# Criando virtual machine
Há duas maneiras via linha de comandos e Portal Azure 
# Criando uma VM pelo Portal do Azure (Interface Gráfica)
1 Acesse o Portal do Azure.
2 No menu esquerdo, clique em Máquinas Virtuais.
3 Clique em Criar e selecione Máquina Virtual.
4 Escolha a assinatura e grupo de recursos (ou crie um novo).
5 Defina o Nome da VM, Região, Imagem (SO) e Tamanho da VM.
6 Configure a Autenticação (Senha/Chave SSH).
7 Defina as configurações de Rede, Disco e Monitoramento conforme necessário.
8 Clique em Revisar + Criar, verifique os detalhes e clique em Criar.

# 2 Criando uma VM via Linha de Comando (Azure CLI)
Se você prefere usar a linha de comando, siga estes passos:

2.1 Criando a VM no Azure CLI
Abra um terminal e execute os comandos:

# Faça login no Azure
az login  

# Criar um grupo de recursos (substitua "<meu-grupo>" e "eastus" conforme necessário)
az group create --name meu-grupo --location eastus  

# Criar a VM
az vm create \
  --resource-group meu-grupo \
  --name MinhaVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --authentication-type password \
  --admin-password MinhaSenhaForte123!  

  # Criar Banco de dados 
2. Criar um novo Banco de Dados SQL
No menu esquerdo, clique em "Criar um recurso".
Selecione "Bancos de Dados" > "Banco de Dados SQL".
Clique em "Criar".

3. Configurar o banco de dados
Assinatura: Escolha sua assinatura do Azure.
Grupo de recursos: Crie um novo grupo de recursos ou escolha um existente.
Nome do Banco de Dados: Defina um nome para o banco de dados.
Servidor:
Selecione um servidor existente ou crie um novo.
Para um novo servidor, defina um nome, região, usuário e senha.
Camada de Preço: Escolha entre DTU-based ou vCore-based, dependendo da necessidade.

4. Configurar rede e segurança
Vá para a guia "Rede" e defina o acesso:
Permitir acesso da internet pública ou configurar regras específicas de firewall.
Configure "Autenticação" (SQL ou Azure AD).

5. Revisar e Criar
Clique em "Revisar e Criar".
Aguarde a validação e clique em "Criar".

Contêineres e Kubernetes
(Instâncias de Contêiner do Azure,
Serviços de Kubernetes do Azure)

Área de Trabalho Virtual do Azure

Serviços de Rede (Rede Virtual do Azure e Peering, Gateway de VPN, Express Route, Azure Load Balancer, CDN, Azure Application Gateway)

Tipos de armazenamento
(Dados estruturados, semi-estruturados, não-estruturados)

Serviços de armazenamento
(contêiner, disco, arquivos)

Serviços de banco de dados
(Cosmos Database, SQL do Azure, Azure para MySQL, Azure para PostgreSQL, Database Migration Service)

Load Balancer -> escalonamento automático para acesso de alta disponibilidade (rodízio de placa)

Content Delivery Network -> Microsoft entrega o conteúdo com menor latência

Application Gateway -> balanceador de carga (faixa reversível)

Palavras-Chave: IoT

•	Azure IoT Central: como um console de monitoramento de todos os dispositivos IoT, a saúde, um "dashboard" de gestão

•	

•	IoT Hub: gerencia e comunica com os dispositivos bidirecionalmente


•	Azure Sphere: plataforma de aplicativo segura - camada de segurança de alto nível.

Azure Synapse Analytics -> análise ilimitada, data warehouse
 
Azure HDInsight -> serviço de análise open-source (palavra-chave: cluster, e diversos apaches)

 
Azure Databricks -> serviço de análise para descoberta de insights e criação de soluções de IAs (palavra-chave: insights, IAs)
 
Azure Data Lake Analytics: simplifica transformações paralelas de forma massiva

Azure PowerShell e Azure CLI -> linhas de comando -> posso conectar no portal e executar a partir do powershell no portal online

Powershell: CMDLets
CLI: Bash
Cloudshell: pode ter tanto powershell quanto o CLI
Assistente do Azure = Advisor
Peering = emparelhamento
JSON = ARM
Palavras-chave: Tipos de nuvem
Nuvem pública: cloud, azure, opex, pagar conforme o uso (pay-as-you-go)  
Nuvem privada: on-premises, datacenter local, capex, upfront costs (custos antecipados)  
Nuvem híbrida: parte pública, parte privada
Benefícios:
Alta disp.: disponível na maior parte do tempo (+SLA)
Tolerância a falha: redundância e replicação em outra região
Recuperação de desastre: "perdi tudo" -> replicar serviços em locais distintos e independentes
Elasticidade: subir e descer o número e poder das VMs por demanda
Escalabilidade: "o quanto posso crescer"?
Agilidade: rapidez em criar e remover provisionamentos
Segurança: compliance, conformidade
Alcance global: não tem datacenter em todos os locais, mas as regiões são acessíveis em todo o globo
Custo preditivo: estimativa de custo usando a calculadora do azure
Capacidades de latência: tempo de rede -> migrar entre regiões até menor latência possível

Serviços de Nuvem
IaaS, PaaS e SaaS -> é bastante cobrado os "limites" entre cada um destes serviços (ex.: um SO, um software X e uma máquina virtual, qual deles faz parte do IaaS/SaaS/PaaS?) 


Serverless - Palavras-Chave   Azure Functions: infraestrutura criada com base em evento, com código executando seu serviço. 
Azure Logic Apps: automatização e orquestração de tarefas (fluxos de trabalho) 
Grade de Eventos (Event Grid) -> baseado em eventos

Regiões do Azure
Um ou mais datacenters próximos. Nem todos os recursos estão disponíveis em todas as regiões
Regiões Pares
As regiões tem seus pares para replicação automática 300 milhas de separação (ao mínimo) -> a fim de minimizar impacto devido desastres. Prioriza a recuperação da região em caso de paralização
Zonas de Disponibilidade
Uma zona de disponibilidade é um conjunto de datacenters para separar fisicamente dentro da mesma região.
Azure PowerShell e Azure CLI -> linhas de comando -> posso conectar no portal e executar a partir do powershell no portal online
Powershell: CMDLets 
CLI: Bash 
Cloudshell: pode ter tanto powershell quanto o CLI

ACI -> Azure Container Instances -> executa um contêiner sem precisar gerenciar uma VM
AKS -> Azure Kubernetes Service -> orquestração de contêineres (grandes volumes de contêineres)
Serviços de Rede
VNet do Azure: recursos se comuniquem entre si -> emparelhamento (peering)
Gateway de VPN: tráfego criptografado entre uma VNet do Azure e um local na internet pública
Express Route: conexão facilitada por um provedor

Azure Network Services
Load Balancer: escalonamento automático para alta disponibilidade
CDN: entrega conteúdo com menor latência; cache
Application Gateway: balanceador de carga


Tipos de Armazenamento
Estruturado: banco de dados relacionais (tabelas, colunas)
Semi-Estruturado: noSQL (xml, json, html)
Não-Estruturado: BLOBs (pdf, jpg)

Serviços de armazenamento
Disco: disco de VMs, apps, etc
Contêiner: grande quantidade de dados não estruturados
File Service: protocolo SMB

Camada de acesso -> tier
Hot: vídeos em alta, por exemplo, carregam rapidamente pois estão na tier hot. Menor latência, maior custo.
Cool: intermediário, dados em média de 30 dias
Archive: dados menos acessados, maior latência, menor custo.
Palavras-Chave: IoT
Azure IoT Central: como um console de monitoramento de todos os dispositivos IoT, a saúde, um "dashboard" de gestão (web-based user interface)
IoT Hub: gerencia e comunica com os dispositivos bidirecionalmente

Azure Sphere: plataforma de aplicativo segura - camada de segurança de alto nível. 

Palavras-Chave: Big data

Azure Synapse Analytics -> análise ilimitada, data warehouse 

Azure HDInsight -> serviço de análise open-source (palavra-chave: cluster, e diversos apaches)
Azure Databricks -> serviço de análise para descoberta de insights e criação de soluções de IAs (palavra-chave: insights, IAs, apache spark)

Azure Data Lake Analytics: simplifica transformações paralelas de forma massiva

Palavras-Chave: Inteligência Artificial e Machine Learning
Machine Learning: desenvolver, treinar e implantar aprendizado de máquina 
Cognitive Services: ver, ouvir, falar, entender e interpretar as necessidades do usuário 
Bot Service: bots inteligentes de nível corporativo para comunicação em linguagem 'humana'.

DevOps e GitHub
Azure Devops: criar tarefas, pipelines, testes automatizados, deploy
GitHub: versionamento, bugs, tarefas, gerenciamento de código
GitHub Actions: automatiza fluxos de construir, testar e implantar
DevTest Labs: monta ambiente dev de forma rápida

Azure Advisor (PT: Assistente do Azure): recomendações (analisa os recursos e faz recomendações referentes a práticas e otimização)

Azure Monitor: coleta, analisa, atua na telemeria
Azure Service Health (PT: Integridade de Serviço do Azure): monitora os incidentes e faz a análise RCA (análise de causa raiz) para saber o que ocorreu -> é o 'downdetector' do Azure
Uma palavra chave para a Central de Segurança / Microsoft Defender é "pontuação" - ele faz como se fosse uma análise para detectar ameaças e fornecer recomendações, dando uma pontuação pra sua segurança e fazendo a comparação do que já está em prática e do que pode ser aplicado
Azure Sentinel: SIEM (gerenciamento de informações de segurança) e SOAR (resposta automatizada de segurança) Responder automaticamente -> coleta os logs, detecta ameaças, investiga incidentes e responde rapidamente
Azure Key Vault
Auxilia no armazenamento de credenciais (senhas, chaves, certificados, etc).

Calculadora de preços
Carga de trabalho -> estimativa de custos; você estima custos de produtos do Azure inserindo região, nível, opções de cobrança/suporte, etc.
Calculadora do custo total de propriedade (TCO)
Compara e estima a economia de custos possível ao migrar do on-premises para a nuvem
Fatores que afetam os custos:

Tráfego de saída -> download 
Tráfego de entrada -> upload

Tráfego de entrada não é cobrado (dados que entram no datacenter do azure), mas tráfego de saída sim. Os preços são baseados em Zonas.


