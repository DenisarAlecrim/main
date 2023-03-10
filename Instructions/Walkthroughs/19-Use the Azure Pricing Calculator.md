---
wts:
  title: 19 – Usar a Calculadora de Preços do Azure (10 min)
  module: 'Module 06: Describe Azure cost management and service level agreements'
---
# <a name="19---use-the-pricing-calculator-10-min"></a>19 – Usar a Calculadora de Preços do Azure (10 min)

Neste passo a passo, usaremos a Calculadora de Preços do Azure para gerar uma estimativa de custo para uma máquina virtual do Azure e recursos de rede relacionados.

# <a name="task-1-configure-the-pricing-calculator"></a>Tarefa 1: Configurar a calculadora de preços

Nesta tarefa, vamos estimar o custo de uma infraestrutura de amostra usando a Calculadora de Preços do Azure. 

**Observação**: Este passo a passo oferece configurações de exemplo para criar uma estimativa pela Calculadora de Preços do Azure para a VM e recursos relacionados. Use essas configurações de exemplo ou forneça detalhes dos seus requisitos *reais* de recursos à Calculadora de Preços do Azure.

1. No navegador, navegue até a página da web da [Calculadora de Preços do Azure](https://azure.microsoft.com/en-us/pricing/calculator/).

2. Para adicionar detalhes de sua configuração de VM, clique em **Máquinas virtuais** na guia **Produtos**. Role para baixo para ver os detalhes da máquina virtual. 

3. Substitua o texto **Sua estimativa** e **Máquinas virtuais** por nomes mais descritivos para a sua estimativa da Calculadora de Preços do Azure e para a sua configuração de VM. Este exemplo de explicação passo a passo usa **Minha estimativa da calculadora de preços** para a estimativa e a **VM do Windows** para a configuração da VM.

   ![Captura de tela da área de configuração de VM na página da web de estimativa da Calculadora de Preços do Azure. O nome da estimativa e o nome da configuração de VM realçados indicam como adicionar um nome de estimativa e um nome de configuração de VM a uma estimativa da Calculadora de Preços do Azure.](../images/1901.png)

4. Modifique a configuração padrão da VM.

    | Configurações | Valor |
    | -- | -- |
    | Região | **Norte da Europa** |
    | Sistema operacional | **Windows** |
    | Type | **(Somente SO)** |
    | Camada | **Standard** |  
    | Instância | **A2: 2 núcleos(s), 3,5 GB de RAM, 135 GB de armazenamento temporário** |

   ![Captura de tela da área de configuração de VM na página da web de estimativa da Calculadora de Preços do Azure. Os exemplos destacados de valores de propriedade de configuração de VM inseridos pelo usuário indicam como especificar uma configuração de VM em uma estimativa da Calculadora de Preços do Azure.](../images/1902.png)

    **Observação**: As especificações e os preços da instância de VM podem ser diferentes dos mostrados neste exemplo. Siga este passo a passo, escolhendo uma instância que corresponda ao exemplo o mais próximo possível. Para visualizar os detalhes sobre as diferentes opções do produto VM, escolha **Detalhes do produto** no menu **Mais informações** à direita.

5. Defina a **Opção de cobrança** para **Pré-pago**.

   ![Captura de tela da área de opções de cobrança de VM na página da web de estimativa da Calculadora de Preços do Azure. A opção de cobrança pré-paga realçada indica como especificar uma opção de cobrança para uma VM dentro de uma estimativa da Calculadora de Preços do Azure.](../images/1903.png)

6. No Azure, um mês é definido como 730 horas. Se a sua VM precisa estar disponível 100 por cento do tempo a cada mês, você define o valor de horas por mês para `730`. Este exemplo passo a passo requer que uma VM esteja disponível 50 por cento do tempo a cada mês.

    Deixe o número de VMs definido em `1` e altere o valor de horas por mês para `365`.

   ![Captura de tela da área de opções de cobrança de VM na página da web de estimativa da Calculadora de Preços do Azure. O número realçado de instâncias de VM e opções de horas por mês indicam como especificar o número de instâncias e horas por mês para uma VM dentro de uma estimativa da Calculadora de Preços do Azure.](../images/1904.png)

7. No painel **Discos gerenciados do SO**, modifique a configuração de armazenamento em VM padrão.

    | Camada | Tamanho do disco | Número de discos | Instantâneo | Transações de armazenamento |
    | ---- | --------- | --------------- | -------- | -------------------- |
    | HDD Standard | S30: 1024 GiB | 1 | Desativado | 10.000 |

   ![Captura de tela da área de opções de Discos gerenciados do SO na página da web de estimativa da Calculadora de Preços do Azure. As opções destacadas – tipo de nível, tamanho do disco, número de discos e número de transações de armazenamento – indicam como especificar uma configuração de armazenamento para uma VM dentro de uma estimativa da Calculadora de Preços do Azure.](../images/1905.png)

8. Para adicionar largura de banda de rede à sua estimativa, vá para o topo da página da web da Calculadora de Preços do Azure. Clique em **Rede** no menu do produto à esquerda e, em seguida, clique no bloco **Largura de banda**. No diálogo de mensagem **Largura de banda adicionada**, clique em **Exibir**.

   ![Captura de tela da área de produtos de rede na página da web da Calculadora de Preços do Azure. Os blocos destacados – rede, adicionar largura de banda e exibir largura de banda – indicam como adicionar e exibir detalhes de uma configuração de largura de banda de rede em uma estimativa da Calculadora de Preços do Azure.](../images/1906.png)

9. Adicione um nome para a configuração de largura de banda da VM. Este exemplo passo a passo usa o nome **Largura de banda: VM do Windows**. Modifique a configuração de largura de banda padrão adicionando os seguintes detalhes.

    | Região | Quantidade de transferência de dados de saída da zona 1 |
    | ------ | -------------------------------------- |
    | Norte da Europa | 50 GB |

   ![Captura de tela da área de configuração da largura de banda da rede na página da web de estimativa da Calculadora de Preços do Azure. Os exemplos destacados de valores de propriedade de largura de banda inseridos pelo usuário indicam como especificar uma configuração de largura de banda para uma VM dentro de uma estimativa da Calculadora de Preços do Azure.](../images/1907.png)

10. Para adicionar um Gateway de Aplicativo, volte ao início da página da web Calculadora de Preços do Azure. No menu do produto **Rede**, clique no bloco **Gateway de Aplicativo**. No diálogo de mensagem do **Gateway de Aplicativo**, clique em **Exibir**.

    ![Captura de tela da área de produtos de rede na página da web da Calculadora de Preços do Azure. Os blocos destacados – adicionar gateway de aplicativo e exibir gateway de aplicativo – indicam como adicionar e exibir detalhes de uma configuração de gateway de aplicativo em uma estimativa da Calculadora de Preços do Azure.](../images/1908.png)

11. Adicione um nome para sua configuração de Gateway de Aplicativo. Este passo a passo usa o nome **Gateway de Aplicativo: VM do Windows**. Modifique a configuração padrão do Gateway de Aplicativo adicionando os seguintes detalhes.

    | Configurações | Valor |
    | -- | -- |
    | Região | **Norte da Europa** |
    | Camada | **Basic** |
    | Tamanho | **Pequeno** |
    | Instâncias | **1** |  
    | Horas | **365** |
    | Dados processados | **50 GB** |
    | Zona 1: América do Norte, Europa | **50 GB**|

    ![Captura de tela da área de configuração do gateway de aplicativo na página da web de estimativa da Calculadora de Preços do Azure.](../images/1909.png)


# <a name="task-2-review-the-pricing-estimate"></a>Tarefa 2: Revisar a estimativa de preços

Nesta tarefa, vamos revisar os resultados da Calculadora de Preços do Azure. 

1. Role até o final da página da web da Calculadora de Preços do Azure para ver o **Custo mensal estimado total**.

    **Observação**: Explore as várias opções disponíveis na Calculadora de Preços do Azure. Por exemplo, este passo a passo requer que você atualize a moeda para Euro.

2. Altere a moeda para Euro e selecione **Exportar** para baixar uma cópia da estimativa para visualização off-line no formato Microsoft Excel (`.xlsx`).

    ![Captura de tela dos custos mensais estimados totais na página da web de estimativa da Calculadora de Preços do Azure. A opção de moeda em euro realçada indica como modificar a moeda usada em uma estimativa da Calculadora de Preços do Azure. A opção de exportação destacada ilustra como baixar uma cópia de uma estimativa para visualização off-line.](../images/1910.png)

    ![Captura de tela de um exemplo de estimativa da Calculadora de Preços do Azure no Microsoft Excel.](../images/1911.png)

Parabéns! Você baixou uma estimativa da Calculadora de Preços do Azure.
