---
title: Incluir gravações de tela e de voz durante testes usando configurações de teste no Visual Studio | Microsoft Docs
ms.date: 10/03/2016
ms.topic: article
helpviewer_keywords:
- test settings, recording desktop video
ms.assetid: 2cefe8c2-430a-4cb4-bbe0-f3edb2e5bc03
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-ide-test
ms.openlocfilehash: ed05f037bbc1450e33a904f1b35a84bfaa6645be
ms.sourcegitcommit: 900ed1e299cd5bba56249cef8f5cf3981b10cb1c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2018
---
# <a name="how-to-include-recordings-of-the-screen-and-voice-during-tests-using-test-settings"></a>Como incluir gravações da tela e voz durante testes usando as configurações do teste s

No editor de configuração do Visual Studio, é possível configurar o adaptador de dados de diagnóstico que grava a tela e a voz do usuário que está executando o teste. Esse adaptador de dados de diagnóstico salva uma gravação de voz e tela da sessão da área de trabalho durante o teste. A gravação é salva com o resultado do teste ou pode ser anexada a um bug. Outros membros da equipe podem usar a gravação para isolar defeitos no aplicativo que sejam difíceis de reproduzir.

> [!WARNING]
> As gravações de tela e voz não dão suporte a várias configurações de monitor.

O gravador de tela e voz pode ser usado com testes manuais ou automatizados. Por exemplo, se executar um teste de IU codificado remotamente, você talvez queira gravar a área de trabalho para ver o teste de IU codificado à medida que ele é executado. Para obter informações sobre como capturar uma tela e a vez gravando remotamente, consulte [How to: Set Up Your Test Agent to Run Tests that Interact with the Desktop](../test/how-to-set-up-your-test-agent-to-run-tests-that-interact-with-the-desktop.md) (Como configurar seu agente de teste para executar testes que interagem com a área de trabalho).

## <a name="to-configure-screen-and-voice-recording-for-your-test-settings"></a>Para configurar a gravação de voz e tela para suas configurações de teste

1.  Abra as configurações de teste que você deseja definir para registrar a tela e a voz. Para obter mais informações, consulte [Coletar dados de diagnóstico durante testes (VSTS)](/vsts/manual-test/collect-diagnostic-data) e [Coletar informações de diagnóstico usando configurações de teste](../test/collect-diagnostic-information-using-test-settings.md).

2.  Nas configurações de teste, selecione a **Função** a ser usada para gravar a tela e a voz.

    > [!NOTE]
    > Para testes manuais e testes automatizados, essa seria a máquina que executa os testes.

3.  Selecione **Gravador de Tela e Voz** e escolha **Configurar**.

     A caixa de diálogo Adaptador de Dados de Diagnóstico de Configuração – Gravador de Tela e Voz é exibida.

     ![Configuração de vídeo](../test/media/testsettingvideoconfiggdr.png "TestSettingVideoConfigGDR")

4.  (Opcional) Selecione **Habilitar registro de voz** para capturar o conteúdo de áudio em sua gravação.

5.  (Opcional) Marque a caixa de seleção ao lado de **Salvar a gravação se o caso de teste passar** para especificar que a tela e as gravações de voz sejam salvas independentemente dos testes serem aprovados ou reprovados.

    > [!WARNING]
    > Se você selecionar **Salvar a gravação se o caso de teste passar**, a gravação será armazenada com os resultados de teste, o que usará espaço de armazenamento no servidor. Você pode usar a ferramenta de limpeza de anexo de teste para limpar esses anexos.

6.  Em **Qualidade de Gravação da Tela**, configure as seguintes opções da lista suspensa:

    1.  **Taxa de quadros:** especifique quantos quadros por segundo você deseja usar na gravação de voz e tela. O valor padrão é 4 quadros por segundo. Valores entre 2 e 20 podem ser especificados.

    2.  **Taxa de bits:** especifique quantos quilobytes serão usados por segundo na gravação de voz e tela. O valor padrão é 512. Valores entre 512 e 10.000 podem ser especificados.

    3.  **Qualidade (1-100):** você pode especificar a qualidade da gravação de voz e tela selecionando um intervalo entre 1 e 100. O padrão é 50 (intermediário).

7.  Escolha **OK**. As configurações do coletor de rastreamento de diagnóstico agora estão definidas e salvas em suas configurações de teste.

    > [!TIP]
    > Para redefinir a configuração desse adaptador de dados de diagnóstico, escolha **Restaurar configuração padrão** para o Visual Studio e **Redefinir como padrão** para o Microsoft Test Manager.

## <a name="see-also"></a>Consulte também

- [Coletar dados de diagnóstico durante testes (VSTS)](/vsts/manual-test/collect-diagnostic-data)
- [Coletar dados de diagnóstico em testes manuais (VSTS)](/vsts/manual-test/mtm/collect-more-diagnostic-data-in-manual-tests)
- [Coletar informações de diagnóstico usando configurações de teste](../test/collect-diagnostic-information-using-test-settings.md)
- [Executar testes manuais (VSTS)](/vsts/manual-test/getting-started/run-manual-tests)