---
title: Salvar logs de teste de carga no Visual Studio
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, scenarios
- load tests, logging
ms.assetid: 9ac88d8a-4777-462c-aa0e-244dadb2cfd1
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.openlocfilehash: 3464ffc1db1a757ac20e3f77d0d901ec731a7cab
ms.sourcegitcommit: 495bba1d8029646653f99ad20df2f80faad8d58b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/31/2018
ms.locfileid: "39381928"
---
# <a name="how-to-specify-how-frequently-test-logs-are-saved-using-the-load-test-editor"></a>Como especificar a frequência com que os logs de teste são salvos usando o Editor de Teste de Carga

Depois de criar seu teste de carga com o **Novo Assistente de Teste de Carga**, você poderá usar o **Editor de Teste de Carga** para alterar as propriedades dos testes de carga para que elas atendam às suas metas e necessidades de teste. Para obter mais informações, consulte [Passo a passo: criar e executar um teste de carga](../test/walkthrough-create-and-run-a-load-test.md).

> [!NOTE]
> Para obter uma lista completa das propriedades de configurações de execução e suas descrições, confira [Propriedades de configurações de execução de teste de carga](../test/load-test-run-settings-properties.md).

Você pode especificar a frequência com que o log de teste é salvo em um teste de carga usando o **Editor de Teste de Carga** para alterar a propriedade **Salvar Frequência de Logs para Testes Concluídos** na janela **Propriedades**.

## <a name="to-specify-the-frequency-for-saving-the-test-log-in-a-load-test"></a>Para especificar a frequência para salvar o log de teste em um teste de carga

1.  Abra um teste de carga.

     O **Editor de Teste de Carga** é exibido. Exibe a árvore do teste de carga.

2.  Na pasta **Configurações de Execução** da árvore de teste de carga, escolha o nó de configurações de execução para o qual deseja especificar a frequência com que o log de teste é salvo.

3.  No menu **Exibir**, selecione **Janela de Propriedades**.

     As categorias e as propriedades do cenário são exibidas na janela **Propriedades**.

4.  Na caixa de texto da propriedade **Salvar frequência de logs para testes concluídos**, digite um número para indicar a frequência com que o log de teste será gravado. O número que indica que um de cada número inserido de testes será salvo no log de teste. Por exemplo, inserindo o valor de dez especifica que o décimo, vigésimo, trigésimo etc. será gravado no log de teste.

    > [!NOTE]
    > Usar um valor de 0 para a propriedade de **Salvar frequência de logs para testes concluídos** especifica que nenhum log de teste será salvo.

5.  Depois de alterar a propriedade, escolha **Salvar** no menu **Arquivo**.

     Os dados salvos no log podem ser exibidos usando-se a exibição Tabelas do Analisador de Testes de Carga. Para obter mais informações, consulte [Analisar resultados de teste de carga e erros na exibição Tabelas](../test/analyze-load-test-results-and-errors-in-the-tables-view.md).

## <a name="see-also"></a>Consulte também

- [Editar cenários de teste de carga](../test/edit-load-test-scenarios.md)
- [Passo a passo: criar e executar um teste de carga](../test/walkthrough-create-and-run-a-load-test.md)
- [Como especificar se as falhas no teste são salvas em logs de teste](../test/how-to-specify-if-test-failures-are-saved-to-test-logs.md)
- [Como configurar a coleta de detalhes completos para habilitar o Gráfico de Atividade do Usuário Virtual](../test/how-to-configure-load-tests-to-collect-full-details.md)