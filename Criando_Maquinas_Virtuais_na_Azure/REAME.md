# 💻 Guia para Criar uma Máquina Virtual no Azure

Este guia orientar no processo de criação e configuração de uma Máquina Virtual (VM) no Azure usando o Portal do Azure.

---
## 🌍 Passo 1: Acessar o Portal do Azure

1. Vá até o [Portal do Azure](https://portal.azure.com/) e entre com suas credenciais.
2. No painel principal, pesquise por **"Máquinas Virtuais"** e clique no resultado correspondente.

---

## 🏗️ Passo 2: Criando a Máquina Virtual

1. No topo da página, clique em **"Criar"** e depois selecione **"Máquina Virtual"**.
2. Isso abrirá o assistente de criação da VM, onde você precisará preencher diversas informações.

---

## 🔧 Passo 3: Configurações Básicas da VM

### Informações Básicas:
- **Assinatura**: Selecione a assinatura vinculada à sua conta.
- **Grupo de Recursos**: Crie um grupo de recursos ou escolha um já existente.
- **Nome da VM**: Escolha um nome descritivo para a sua máquina virtual.
- **Região**: Escolha a localização geográfica da VM (ex.: **East US**, **West Europe**).

### Disponibilidade e Tamanho:
- **Opções de Disponibilidade**: Escolha entre **Alta Disponibilidade** ou **Nenhuma** dependendo das suas necessidades.
- **Imagem**: Selecione o sistema operacional (ex.: **Windows Server 2019**, **Ubuntu Server**).
- **Tamanho**: Defina o tamanho da VM com base nos requisitos de CPU e memória. Use a opção **Ver todos os tamanhos** para explorar mais opções.

---

## 🔑 Passo 4: Configurando Autenticação e Acesso

1. **Nome do Administrador**: Escolha o nome do administrador da VM.
2. **Método de Autenticação**: Selecione entre **Senha** ou **Chave SSH**:
   - Para **Senha**, crie uma senha forte.
   - Para **Chave SSH**, insira a chave pública.
3. **Portas de Entrada**: Defina as portas necessárias:
   - **RDP (3389)** para VMs Windows.
   - **SSH (22)** para VMs Linux.

---

## 💾 Passo 5: Configurando Armazenamento

1. **Tipo de Disco do Sistema Operacional**: Escolha entre **SSD Premium**, **SSD Padrão** ou **HDD Padrão**, conforme a necessidade de desempenho.
2. **Discos de Dados**: Caso precise de armazenamento adicional, adicione discos clicando em **Criar e Anexar Novo Disco**.

---

## 🌐 Passo 6: Configurações de Rede

1. **Rede Virtual**: Selecione uma rede virtual existente ou crie uma nova.
2. **Sub-rede**: Escolha uma sub-rede para a VM.
3. **Endereço IP Público**: Ative o IP público para acessar a VM externamente.
4. **Grupo de Segurança de Rede (NSG)**: Crie ou selecione um NSG para configurar as regras de firewall para o tráfego de entrada e saída.

---

## ✅ Passo 7: Revisão e Criação

1. Clique em **Revisar + Criar** para verificar suas configurações.
2. Revise todas as informações e, se estiver tudo certo, clique em **Criar**. A implantação da VM pode demorar alguns minutos.

---

## 🔌 Passo 8: Acessar sua Máquina Virtual

### Conectando à VM:
1. Após a criação, vá até **Máquinas Virtuais** no portal.
2. Selecione a VM recém-criada.
3. Clique em **Conectar** e escolha o método de conexão:
   - **RDP** para VMs Windows.
   - **SSH** para VMs Linux.

### Para Windows:
- Baixe o arquivo **RDP** gerado e use-o para se conectar à VM via **Remote Desktop**.

### Para Linux:
- Utilize o comando **SSH** fornecido para se conectar via terminal.

---

## 🔐 Dicas de Segurança

- Use **senhas fortes** ou **chaves SSH** para aumentar a segurança de acesso à VM.
- Defina regras de firewall adequadas no **NSG** para limitar o tráfego de entrada.
- Considere configurar backups regulares e ative monitoramento para garantir o bom funcionamento da VM.

---
