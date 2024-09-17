
---

# Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure

Este documento oferece um guia passo a passo sobre como configurar e dimensionar recursos em máquinas virtuais (VMs) no Microsoft Azure.

## Pré-requisitos

Antes de iniciar, certifique-se de ter o seguinte:

- Conta no Microsoft Azure com permissão para criar recursos.
- Familiaridade com o Azure Portal ou Azure CLI.
- Conhecimento básico sobre máquinas virtuais.

## Criando uma Máquina Virtual no Azure

1. Acesse o [Azure Portal](https://portal.azure.com).
2. No painel esquerdo, selecione "Máquinas Virtuais".
3. Clique em "Criar" e selecione "Máquina Virtual".
4. Preencha os detalhes básicos, como nome, região, tipo de imagem (Windows, Linux), e tamanho da máquina virtual.
5. Configure a rede, segurança, armazenamento e outros recursos de acordo com suas necessidades.
6. Finalize a criação da VM e aguarde a inicialização.

## Dimensionando Recursos

O dimensionamento de VMs no Azure pode ser feito de duas formas principais: **dimensionamento vertical** e **dimensionamento horizontal**.

### Dimensionamento Vertical

O dimensionamento vertical envolve a alteração dos recursos de uma VM, como CPU e memória, para um nível maior ou menor. Isso pode ser feito quando há necessidade de mais poder computacional ou para economizar custos quando a demanda é menor.

#### Como alterar o tamanho da VM:

1. Acesse a VM no Azure Portal.
2. Vá para a seção "Tamanho".
3. Selecione um novo tamanho de VM com base em suas necessidades.
4. Confirme a alteração e aguarde a VM ser reiniciada.

### Dimensionamento Horizontal

O dimensionamento horizontal refere-se à adição de mais instâncias da mesma VM para balancear a carga de trabalho. Isso é útil em arquiteturas de microsserviços ou aplicações que demandam alta disponibilidade.

#### Como habilitar o dimensionamento horizontal:

1. Configure um Conjunto de Escala de Máquinas Virtuais (VM Scale Set).
2. Defina as regras de autoescala, como o aumento de instâncias baseado no uso de CPU ou de memória.
3. O Azure gerenciará automaticamente o aumento ou redução das instâncias conforme a demanda.

## Configurações de CPU e Memória

Para ajustar o desempenho da sua VM, você pode escolher diferentes séries de máquinas virtuais com variações de CPU e memória:

- **Série B**: Melhor para cargas de trabalho leves ou de baixo uso.
- **Série Dsv3**: Ideal para aplicações que exigem alta performance de CPU.
- **Série Esv3**: Focada em cargas de trabalho que demandam grandes quantidades de memória.

Esses tipos de VM podem ser selecionados durante a criação ou reconfigurados conforme necessário.

## Discos Gerenciados e Armazenamento

Ao configurar a VM, é possível selecionar diferentes tipos de discos gerenciados para armazenar dados:

- **Discos Standard HDD**: Melhor para armazenamento econômico e de baixa prioridade.
- **Discos Standard SSD**: Uma opção intermediária com desempenho consistente.
- **Discos Premium SSD**: Recomendado para aplicações que exigem alta performance de I/O, como bancos de dados.

Para aumentar a capacidade de armazenamento, você pode adicionar novos discos à VM através do Azure Portal.

## Rede e Segurança

Ao configurar redes e segurança, é importante:

- Criar um grupo de segurança de rede (NSG) para controlar o tráfego de entrada e saída da VM.
- Definir regras de firewall para garantir que a VM seja acessível apenas pelos canais necessários.
- Configurar IPs públicos ou balanceadores de carga para gerenciamento eficiente de rede.

## Monitoramento e Ajustes

Monitore o desempenho da sua VM usando o **Azure Monitor** para rastrear métricas, como uso de CPU, memória e disco. Com essas informações, você pode ajustar o dimensionamento e as configurações de recursos para otimizar sua aplicação e minimizar custos.

## Boas Práticas

- **Escolha o tamanho certo de VM**: Evite o uso de VMs superdimensionadas ou subdimensionadas.
- **Use autoescala**: Configure o autoescalamento para ajustar automaticamente o número de instâncias de acordo com a demanda.
- **Monitore continuamente**: Use alertas e o Azure Monitor para garantir que os recursos estão sendo utilizados de maneira eficiente.
- **Segurança**: Utilize regras de segurança rigorosas e atualize suas VMs regularmente.

## Conclusão

Configurar e dimensionar corretamente suas máquinas virtuais no Azure é essencial para garantir o desempenho ideal e evitar custos desnecessários.

---
