# 💾 Como Configurar uma Instância de Banco de Dados no Azure

Guia para criar e configurar uma instância de banco de dados no Azure usando o serviço **Azure SQL Database**.

---

## 🔧 Passo 1: Acessar o Portal do Azure

1. Vá até o [Portal do Azure](https://portal.azure.com/).
2. Faça login com suas credenciais.

---

## 🛠️ Passo 2: Criar um Servidor SQL

1. No painel do Azure, pesquise por **"SQL Database"** na barra de pesquisa.
2. Clique em **SQL Database** nos resultados.
3. Na nova tela, clique em **Criar** para iniciar a configuração de um novo banco de dados.

---

## ⚙️ Passo 3: Configurar o Banco de Dados

### Informações Básicas
1. **Assinatura**: Escolha a assinatura vinculada à sua conta.
2. **Grupo de Recursos**: Crie um novo grupo de recursos ou selecione um já existente.
3. **Nome do Banco de Dados**: Insira o nome do banco de dados.
4. **Servidor**: Crie um novo servidor SQL ou selecione um servidor já existente:
   - Para criar um novo servidor, insira:
     - **Nome do Servidor**.
     - **Login de Administrador do Servidor** e **Senha**.
     - **Localização** (escolha a região do servidor).

---

## 💾 Passo 4: Escolher Plano de Desempenho

1. Na seção **Plano de Desempenho**, você poderá escolher o nível de serviço:
   - **Uso Geral**: Para cargas de trabalho de uso geral.
   - **Crítico para a Empresa**: Para cargas de trabalho críticas.
   - **Hiperscale**: Para escalabilidade massiva.
2. Selecione o número de **vCores** e o tamanho de armazenamento conforme necessário.

---

## 🌐 Passo 5: Configurar Rede

1. Na aba **Rede**, configure o **Acesso à Rede**:
   - Defina se o banco de dados será acessível via **IP público** ou **Rede Virtual**.
   - Configure regras de firewall, se necessário, para permitir o acesso de endereços IP específicos.

---

## 🔒 Passo 6: Configurações de Segurança

1. **Autenticação**: Configure o método de autenticação:
   - **Autenticação SQL**: Utiliza login e senha definidos na criação do servidor.
   - **Autenticação do Azure Active Directory**: Usar contas do AD para autenticar no banco.
2. **Proteção contra ameaças avançadas** (opcional): Ative para proteger contra ataques e vulnerabilidades.

---

## 🔍 Passo 7: Revisão e Criação

1. Clique em **Revisar + Criar** para revisar todas as suas configurações.
2. Revise os detalhes e, se estiver tudo certo, clique em **Criar**. O processo de criação da instância do banco de dados pode levar alguns minutos.

---
