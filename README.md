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
