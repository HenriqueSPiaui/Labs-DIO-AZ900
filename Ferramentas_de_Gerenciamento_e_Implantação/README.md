# Guia de Ferramentas de Gerenciamento e Implantação no Azure

---

## 1. **Azure Portal**

### O que é:
O **Azure Portal** é a interface gráfica baseada na web que permite gerenciar, implantar e monitorar os serviços da Azure. Ele oferece uma experiência visual e amigável para configurar e controlar recursos.

### Como usar:
1. Acesse o [Azure Portal](https://portal.azure.com).
2. Navegue até o recurso ou serviço que deseja criar (VMs, Redes Virtuais, Bancos de Dados, etc.).
3. Preencha as informações necessárias, como nome do recurso, localização, etc.
4. Clique em **Criar** para implantar o recurso.
5. Use os painéis de monitoramento e gerenciamento para acompanhar os recursos em execução.

---

## 2. **Azure CLI**

### O que é:
O **Azure CLI** é uma ferramenta de linha de comando multiplataforma que permite gerenciar e automatizar os recursos da Azure por meio de comandos no terminal.

### Como usar:
1. Instale o Azure CLI seguindo as instruções [aqui](https://docs.microsoft.com/pt-br/cli/azure/install-azure-cli).
2. Faça login na Azure:
   ```bash
   az login
   ```
3. Execute comandos para criar e gerenciar recursos. Exemplo para criar uma VM:
   ```bash
   az vm create --resource-group MyResourceGroup --name MyVM --image UbuntuLTS --admin-username azureuser --generate-ssh-keys
   ```

---

## 3. **Azure PowerShell**

### O que é:
O **Azure PowerShell** é uma interface de linha de comando para gerenciamento de recursos da Azure, focada em administradores e engenheiros que preferem usar o PowerShell.

### Como usar:
1. Instale o módulo **Az** do PowerShell:
   ```bash
   Install-Module -Name Az -AllowClobber -Scope CurrentUser
   ```
2. Faça login na Azure:
   ```bash
   Connect-AzAccount
   ```
3. Crie e gerencie recursos usando cmdlets do PowerShell. Exemplo para criar uma VM:
   ```bash
   New-AzVM -ResourceGroupName "MyResourceGroup" -Name "MyVM" -Location "EastUS" -Image "UbuntuLTS"
   ```

---

## 4. **Azure Resource Manager (ARM) Templates**

### O que é:
Os **ARM Templates** são arquivos JSON que definem a infraestrutura da Azure como código. Eles são usados para implantações repetíveis e consistentes de recursos.

### Como usar:
1. Crie um arquivo JSON com a configuração dos recursos.
   ```json
   {
     "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#",
     "contentVersion": "1.0.0.0",
     "resources": [
       {
         "type": "Microsoft.Compute/virtualMachines",
         "apiVersion": "2019-07-01",
         "name": "myVM",
         "location": "East US",
         "properties": {
           "hardwareProfile": {
             "vmSize": "Standard_DS1_v2"
           }
         }
       }
     ]
   }
   ```
2. Implemente o template via Azure CLI:
   ```bash
   az deployment group create --resource-group MyResourceGroup --template-file template.json
   ```

---

## 5. **Bicep**

### O que é:
**Bicep** é uma linguagem declarativa de Infraestrutura como Código (IaC) mais simplificada que os ARM Templates. Ela permite implantações mais fáceis e menos verbosas.

### Como usar:
1. Crie um arquivo `.bicep` com a configuração de recursos:
   ```bicep
   resource myVM 'Microsoft.Compute/virtualMachines@2021-07-01' = {
     name: 'myVM'
     location: 'EastUS'
     properties: {
       hardwareProfile: {
         vmSize: 'Standard_DS1_v2'
       }
       osProfile: {
         computerName: 'myVM'
         adminUsername: 'azureuser'
         adminPassword: 'password123!'
       }
     }
   }
   ```
2. Implemente o Bicep template:
   ```bash
   az deployment group create --resource-group MyResourceGroup --template-file main.bicep
   ```

---

## 6. **Terraform**

### O que é:
**Terraform** é uma ferramenta de código aberto que permite a implantação de recursos em múltiplos provedores de nuvem, incluindo a Azure, usando uma linguagem de configuração simples (HCL).

### Como usar:
1. Instale o Terraform [aqui](https://www.terraform.io/downloads.html).
2. Crie um arquivo de configuração `.tf`:
   ```hcl
   provider "azurerm" {
     features {}
   }

   resource "azurerm_resource_group" "example" {
     name     = "example-resources"
     location = "East US"
   }

   resource "azurerm_virtual_network" "example" {
     name                = "example-network"
     address_space       = ["10.0.0.0/16"]
     location            = azurerm_resource_group.example.location
     resource_group_name = azurerm_resource_group.example.name
   }
   ```
3. Execute os comandos:
   ```bash
   terraform init
   terraform apply
   ```

---

## 7. **Azure Arc**

### O que é:
O **Azure Arc** permite que você gerencie e implemente recursos locais e em outras nuvens (como AWS ou Google Cloud) usando o controle centralizado da Azure.

### Como usar:
1. Registre servidores, VMs ou clusters Kubernetes externos via **Azure Arc** no [Azure Portal](https://portal.azure.com).
2. Para conectar um servidor físico, use o comando:
   ```bash
   az connectedmachine connect --resource-group MyResourceGroup --location EastUS --name MyServer
   ```
3. Uma vez conectados, os recursos podem ser gerenciados como se fossem nativos da Azure.

---

## 8. **Azure Kubernetes Service (AKS)**

### O que é:
O **Azure Kubernetes Service (AKS)** facilita a implantação, o gerenciamento e a escalabilidade de aplicativos em contêiner usando Kubernetes.

### Como usar:
1. No **Azure Portal**, navegue até **Kubernetes Services** e clique em **Criar**.
2. Configure os parâmetros do cluster Kubernetes (número de nós, tamanho, etc.).
3. Após a criação, use o **kubectl** para gerenciar o cluster:
   ```bash
   az aks get-credentials --resource-group MyResourceGroup --name MyAKSCluster
   kubectl get nodes
   ```

---

## 9. **Azure DevOps**

### O que é:
**Azure DevOps** oferece um conjunto de ferramentas para planejamento, desenvolvimento e entrega contínua de software. Ele permite a integração de pipelines CI/CD para a implantação de recursos na Azure.

### Como usar:
1. Crie um repositório no [Azure DevOps](https://dev.azure.com/).
2. Configure um pipeline de CI/CD no Azure DevOps para automatizar a construção e implantação de recursos e aplicativos.
3. Use tarefas pré-configuradas para implantar diretamente na Azure, integrando-se com **ARM Templates**, **Bicep** ou **Terraform**.

---

## 10. **Azure Blueprints**

### O que é:
O **Azure Blueprints** permite a criação de templates pré-configurados que incluem políticas, permissões e recursos, facilitando implantações seguras e padronizadas em grandes organizações.

### Como usar:
1. No **Azure Portal**, acesse **Blueprints** e crie um novo blueprint.
2. Defina os artefatos do blueprint, como políticas e ARM templates.
3. Atribua o blueprint a um escopo (grupo de recursos ou assinatura) para implantar os recursos automaticamente.

---
