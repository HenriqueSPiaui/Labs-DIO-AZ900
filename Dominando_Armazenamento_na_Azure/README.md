# Guia de Criação de Contas de Armazenamento, Migração e Gerenciamento de Dados no Azure

---
## Introdução
O **Microsoft Azure** é uma das principais plataformas de nuvem pública, oferecendo uma variedade de serviços de computação, rede e armazenamento. Este guia detalha o processo de criação de contas de armazenamento no Azure, além das práticas de migração e gerenciamento de dados.

---

## Criando uma Conta de Armazenamento no Azure

### Passo 1: Acessar o Portal do Azure

1. Acesse o [Portal do Azure](https://portal.azure.com) e faça login com sua conta.
2. No painel de navegação esquerdo, clique em **"Criar um recurso"** e depois em **"Armazenamento"**.

### Passo 2: Selecionar "Conta de Armazenamento"
1. Escolha a opção **"Conta de Armazenamento"** para criar um novo recurso de armazenamento.
2. Na tela seguinte, você precisará fornecer algumas informações:
   - **Assinatura**: Selecione a assinatura do Azure que será usada.
   - **Grupo de Recursos**: Crie ou selecione um grupo de recursos existente.
   - **Nome da Conta de Armazenamento**: Escolha um nome único para sua conta.
   - **Localização**: Selecione a região em que os dados serão armazenados.

### Passo 3: Configurações Adicionais
1. **Tipo de Desempenho**: Escolha entre **Standard** ou **Premium**, dependendo da necessidade de latência e IOPS.
2. **Redundância**: Defina o nível de redundância de seus dados:
   - **LRS** (Locally-redundant storage): Redundância local.
   - **GRS** (Geo-redundant storage): Redundância entre diferentes regiões geográficas.

### Passo 4: Revisar e Criar
1. Após configurar todos os parâmetros, clique em **"Revisar + Criar"**.
2. Após a validação, clique em **"Criar"** para provisionar a conta de armazenamento.

---

## Tipos de Contas de Armazenamento no Azure

### 1. **Blob Storage**
   - Usado principalmente para armazenar grandes quantidades de dados não estruturados, como imagens, vídeos ou logs.
   
### 2. **File Storage**
   - Sistema de arquivos em nuvem que permite montar compartilhamentos de arquivos SMB (Server Message Block) para armazenar e acessar dados.

### 3. **Queue Storage**
   - Utilizado para armazenar grandes volumes de mensagens que podem ser processadas de forma assíncrona por aplicativos distribuídos.

### 4. **Table Storage**
   - Oferece armazenamento de dados NoSQL, permitindo consultas rápidas e escaláveis.

---

## Migrando Dados para o Azure

### Método 1: Azure Storage Explorer
1. Faça o download do [Azure Storage Explorer](https://azure.microsoft.com/features/storage-explorer/).
2. Conecte-se à sua conta de armazenamento no Azure.
3. Navegue até o contêiner ou compartilhamento de arquivos de destino.
4. Arraste e solte arquivos ou pastas para iniciar a migração.

### Método 2: AzCopy (CLI)
1. Instale a ferramenta [AzCopy](https://docs.microsoft.com/pt-br/azure/storage/common/storage-use-azcopy-v10).
2. Use o seguinte comando para copiar dados de uma fonte local para o Blob Storage:
   ```bash
   azcopy copy "C:\path\to\source" "https://<account-name>.blob.core.windows.net/<container-name>?<SAS-token>"
