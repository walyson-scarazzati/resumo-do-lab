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
