---
title: 'Como: alterar o idioma de publicação para um aplicativo ClickOnce | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- Publish language property
- ClickOnce deployment, changing publish language
- publishing, ClickOnce
ms.assetid: ef5024c4-cda1-4970-bc75-32a2a10c92c3
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 3395d0b7bbed5ec1d20e0d04894e439a9a27a15d
ms.sourcegitcommit: 0e5289414d90a314ca0d560c0c3fe9c88cb2217c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/19/2018
ms.locfileid: "39154655"
---
# <a name="how-to-change-the-publish-language-for-a-clickonce-application"></a>Como: alterar o idioma de publicação para um aplicativo ClickOnce
Ao publicar um [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] aplicativo, a interface do usuário exibida durante a instalação padrão é o idioma e cultura do computador de desenvolvimento. Se você estiver publicando um aplicativo localizado, você precisará especificar um idioma e cultura para coincidir com a versão localizada. Isso é determinado pelo `Publish language` propriedade para o seu projeto.  
  
 O `Publish language` propriedade pode ser definida **opções de publicação** caixa de diálogo, acessível a partir o **publicar** página do **Designer de projeto**.  
  
> [!NOTE]
>  As caixas de diálogo e os comandos de menu que você vê podem ser diferentes dos descritos na Ajuda, dependendo da sua edição ou das configurações ativas. Para alterar as configurações, escolha **Importar e Exportar Configurações** no menu **Ferramentas**. Para obter mais informações, confira [Personalizar o IDE do Visual Studio](../ide/personalizing-the-visual-studio-ide.md).  
  
### <a name="to-change-the-publish-language"></a>Para alterar o idioma de publicação  
  
1.  Com um projeto selecionado no **Gerenciador de Soluções**, no menu **Projeto**, clique em **Propriedades**.  
  
2.  Clique o **publicar** guia.  
  
3.  Clique o **opções** para abrir o **opções de publicação** caixa de diálogo.  
  
4.  Clique em **descrição**.  
  
5.  No **opções de publicação** diálogo caixa, selecione um idioma e cultura da **linguagem de publicação** lista suspensa e clique **Okey**.  
  
## <a name="see-also"></a>Consulte também  
 [Publicar aplicativos ClickOnce](../deployment/publishing-clickonce-applications.md)   
 [Como: publicar um aplicativo ClickOnce usando o Assistente de publicação](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)