---
title: 'Como: adicionar um painel de ações a documentos do Word ou pastas de trabalho do Excel'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- smart documents [Office development in Visual Studio], creating in Word
- smart documents [Office development in Visual Studio], adding controls
- actions panes [Office development in Visual Studio], creating in Word
- actions panes [Office development in Visual Studio], adding controls
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: ebf4896411a46b2c75edd8216bd61623bc9b728f
ms.sourcegitcommit: 697162f54d3c4e30df702fd0289e447e211e3a85
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2018
ms.locfileid: "34548551"
---
# <a name="how-to-add-an-actions-pane-to-word-documents-or-excel-workbooks"></a>Como adicionar um painel Ações a documentos do Word ou pastas de trabalho do Excel
  Para adicionar um painel de ações para um documento do Microsoft Office Word ou uma pasta de trabalho do Microsoft Excel, primeiro crie um controle de usuário do Windows Forms. Em seguida, adicione o controle de usuário para o <xref:Microsoft.Office.Tools.ActionsPane.Controls%2A> propriedade o `ThisDocument.ActionsPane` campo (Word) ou `ThisWorkbook.ActionsPane` campo (Excel) em seu projeto.  
  
 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]  
  
> [!NOTE]  
>  Seu computador pode mostrar diferentes nomes ou locais para alguns dos elementos de interface do usuário do Visual Studio nas instruções a seguir. A edição do Visual Studio que você possui e as configurações que você usa determinam esses elementos. Para obter mais informações, confira [Personalizar o IDE do Visual Studio](../ide/personalizing-the-visual-studio-ide.md).  
  
## <a name="creating-the-user-control"></a>Criando o controle de usuário  
 O procedimento a seguir mostra como criar o controle de usuário em uma palavra ou um projeto do Excel. Ele também adiciona um botão para o controle de usuário que escreve o texto para o documento ou a pasta de trabalho quando ele for clicado.  
  
#### <a name="to-create-the-user-control"></a>Para criar o controle de usuário  
  
1.  Abra seu projeto de nível de documento do Word ou Excel no Visual Studio.  
  
2.  No menu **Projeto**, clique em **Adicionar Novo Item**.  
  
3.  No **Adicionar Novo Item** caixa de diálogo, selecione **controle do painel Ações**, nomeie-o **HelloControl**e clique em **adicionar**.  
  
    > [!NOTE]  
    >  Como alternativa, você pode adicionar uma **controle de usuário** item ao seu projeto. As classes geradas pelo **controle do painel Ações** e **controle de usuário** itens são funcionalmente equivalentes.  
  
4.  Do **Windows Forms** guia do **caixa de ferramentas,** arrastar um **botão** controle para o controle.  
  
    > [!NOTE]  
    >  Se o controle não estiver visível no designer, clique duas vezes em **HelloControl** na **Gerenciador de soluções**.  
  
5.  Adicione o código para o <xref:System.Windows.Forms.Control.Click> manipulador de eventos do botão. O exemplo a seguir mostra o código para um documento do Microsoft Office Word.  
  
     [!code-csharp[Trin_VstcoreActionsPaneWord#12](../vsto/codesnippet/CSharp/Trin_VstcoreActionsPaneWordCS/HelloControl.cs#12)]
     [!code-vb[Trin_VstcoreActionsPaneWord#12](../vsto/codesnippet/VisualBasic/Trin_VstcoreActionsPaneWordVB/HelloControl.vb#12)]  
  
6.  Em c#, você deve adicionar um manipulador de eventos para o clique do botão. Você pode colocar esse código no `HelloControl` construtor após a chamada a `IntializeComponent`.  
  
     Para obter informações sobre como criar manipuladores de eventos, consulte [como: criar manipuladores de eventos em projetos do Office](../vsto/how-to-create-event-handlers-in-office-projects.md).  
  
     [!code-csharp[Trin_VstcoreActionsPaneWord#13](../vsto/codesnippet/CSharp/Trin_VstcoreActionsPaneWordCS/HelloControl.cs#13)]  
  
## <a name="add-the-user-control-to-the-actions-pane"></a>Adicione o controle de usuário para o painel de ações  
 Para mostrar o painel de ações, adicione o controle de usuário para o <xref:Microsoft.Office.Tools.ActionsPane.Controls%2A> propriedade o `ThisDocument.ActionsPane` campo (Word) ou `ThisWorkbook.ActionsPane` campo (Excel).  
  
### <a name="to-add-the-user-control-to-the-actions-pane"></a>Para adicionar o controle de usuário para o painel de ações  
  
1.  Adicione o seguinte código para o `ThisDocument` ou `ThisWorkbook` classe como uma declaração de nível de classe (não adicione este código para um método).  
  
     [!code-csharp[Trin_VstcoreActionsPaneWord#14](../vsto/codesnippet/CSharp/Trin_VstcoreActionsPaneWordCS/ThisDocument.cs#14)]
     [!code-vb[Trin_VstcoreActionsPaneWord#14](../vsto/codesnippet/VisualBasic/Trin_VstcoreActionsPaneWordVB/ThisDocument.vb#14)]  
  
2.  Adicione o seguinte código para o `ThisDocument_Startup` manipulador de eventos do `ThisDocument` classe ou o `ThisWorkbook_Startup` manipulador de eventos do `ThisWorkbook` classe.  
  
     [!code-csharp[Trin_VstcoreActionsPaneWord#15](../vsto/codesnippet/CSharp/Trin_VstcoreActionsPaneWordCS/ThisDocument.cs#15)]
     [!code-vb[Trin_VstcoreActionsPaneWord#15](../vsto/codesnippet/VisualBasic/Trin_VstcoreActionsPaneWordVB/ThisDocument.vb#15)]  
  
## <a name="see-also"></a>Consulte também  
 [Visão geral do painel de ações](../vsto/actions-pane-overview.md)   
 [Passo a passo: Inserir texto em um documento de um painel de ações](../vsto/walkthrough-inserting-text-into-a-document-from-an-actions-pane.md)   
 [Como: gerenciar o controle layout em painéis de ações](../vsto/how-to-manage-control-layout-on-actions-panes.md)   
 [Passo a passo: Inserir texto em um documento de um painel de ações](../vsto/walkthrough-inserting-text-into-a-document-from-an-actions-pane.md)  
  
  