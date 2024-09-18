# Governança e Conformidade na Azure

A governança e conformidade na Azure são práticas essenciais para gerenciar recursos em nuvem de maneira segura, eficiente e em conformidade com regulamentações. A Microsoft Azure fornece várias ferramentas para auxiliar nesse processo, como Azure Policy, Azure Blueprints e Microsoft Purview.

## 1. **Azure Policy**

O **Azure Policy** é uma ferramenta que permite criar, atribuir e gerenciar políticas que aplicam regras e efeitos sobre os recursos na Azure. Ele garante que os recursos sejam usados em conformidade com padrões corporativos e requisitos regulatórios.

### Recursos do Azure Policy:
- Criação de políticas personalizadas.
- Auditoria de conformidade e aplicação automática de políticas.
  
## 2. **Azure Blueprints**

O **Azure Blueprints** facilita a criação e implantação de ambientes de nuvem consistentes e em conformidade, incluindo políticas, grupos de recursos e funções.

### Recursos do Azure Blueprints:
- Modelos reutilizáveis para ambientes de nuvem.
- Controle de versão e implantação automatizada.

## 3. **Gerenciamento de Identidades e Acessos (IAM)**

O **Gerenciamento de Identidades e Acessos (IAM)** controla quem pode acessar os recursos da Azure e o que pode ser feito com esses recursos. Usando o **Azure Active Directory (Azure AD)**, você pode gerenciar identidades de usuários e aplicativos.

### Funcionalidades:
- Controle de Acesso Baseado em Função (RBAC).
- Autenticação Multifator (MFA).
- Integração com Azure AD.

## 4. **Azure Security Center**

O **Azure Security Center** oferece gerenciamento de segurança e conformidade, fornecendo recomendações para melhorar a segurança dos recursos do Azure.

### Funcionalidades:
- Avaliações de segurança e monitoramento contínuo.
- Recomendações automatizadas para melhorar a segurança.

## 5. **Microsoft Purview**

O **Microsoft Purview** é uma plataforma de governança de dados unificada, projetada para ajudar as organizações a gerenciar, proteger e governar seus dados em ambientes híbridos e multinuvem. O Microsoft Purview oferece visibilidade e controle total dos dados, garantindo conformidade com regulamentos e otimizando a gestão de dados.

### Funcionalidades do Microsoft Purview:
- **Mapeamento de dados**: Descubra, classifique e rastreie dados sensíveis em toda a organização, sejam eles locais ou na nuvem.
- **Catálogo de Dados**: Crie um catálogo centralizado para garantir que os dados sejam gerenciados de acordo com as políticas da empresa.
- **Compliance e Governança de Dados**: Automatize a conformidade com regulamentações como GDPR e LGPD, aplicando políticas e auditorias.
  
### Exemplos de uso do Microsoft Purview:
- Classificação automática de dados sensíveis, como números de cartão de crédito.
- Criação de relatórios de conformidade para auditorias internas ou externas.

## 6. **Criando Bloqueios em Recursos (Resource Locks)**

O bloqueio de recursos é uma funcionalidade que impede a modificação ou exclusão acidental de recursos críticos na Azure. Com os **Resource Locks**, você pode adicionar uma camada extra de proteção aos seus recursos mais importantes.

### Tipos de Bloqueios:
- **CanNotDelete (Não pode excluir):** Os usuários podem ler e modificar o recurso, mas não podem excluí-lo.
- **ReadOnly (Somente leitura):** Os usuários podem ler os recursos, mas não podem excluí-los ou modificá-los.

### Como criar um bloqueio em um recurso:
1. Navegue até o **Portal do Azure**.
2. Selecione o recurso, grupo de recursos ou assinatura que você deseja bloquear.
3. Na página do recurso, vá até a opção "Bloqueios" no painel esquerdo.
4. Selecione "Adicionar" e defina o tipo de bloqueio (**CanNotDelete** ou **ReadOnly**).
5. Salve as alterações.

### Exemplos de uso:
- Adicionar um bloqueio **CanNotDelete** em um banco de dados crítico para impedir exclusões acidentais.
- Adicionar um bloqueio **ReadOnly** em uma assinatura para que usuários possam visualizar, mas não alterar ou excluir recursos.

## 7. **Azure Compliance Offerings**

A Azure possui certificações e conformidade com vários padrões internacionais e setoriais, garantindo que os serviços possam ser usados para gerenciar dados e workloads regulamentadas de forma segura.

### Principais certificações:
- **ISO 27001, ISO 27018**: Certificações de segurança e privacidade.
- **SOC 1, SOC 2, SOC 3**: Relatórios de controles internos para segurança e privacidade.
- **GDPR**: Conformidade com o Regulamento Geral de Proteção de Dados da UE.
- **LGPD**: Conformidade com a Lei Geral de Proteção de Dados brasileira.
