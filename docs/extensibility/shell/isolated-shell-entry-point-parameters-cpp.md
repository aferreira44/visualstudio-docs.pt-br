---
title: "Isolar os parâmetros de ponto de entrada do Shell (C++) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Shell [Visual Studio], isolated mode, Start entry point
- Visual Studio shell, isolated mode, Start entry point
ms.assetid: 18f4b18b-2173-4afa-ba0a-42fe33e61118
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 54b15d849efacb681eb8b4238cd067144bc67342
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2017
---
# <a name="isolated-shell-entry-point-parameters-c"></a>Parâmetros de ponto de entrada do Shell isolado (C++)
Quando um aplicativo baseado no shell do Visual Studio é iniciado, ele chama o ponto de entrada inicial do shell do Visual Studio. As configurações a seguir podem ser substituídas na chamada para o ponto de entrada do início do shell. Para obter uma descrição de cada configuração, consulte [. Arquivos de Pkgdef](modifying-the-isolated-shell-by-using-the-dot-pkgdef-file.md).  
  
-   AddinsAllowed  
  
-   AllowsDroppedFilesOnMainWindow  
  
-   AppName  
  
-   CommandLineLogo  
  
-   DefaultHomePage  
  
-   DefaultProjectsLocation  
  
-   DefaultSearchPage  
  
-   DefaultUserFilesFolderRoot  
  
-   DisableOutputWindow  
  
-   HideMiscellaneousFilesByDefault  
  
-   HideSolutionConcept  
  
-   NewProjDlgInstalledTemplatesHdr  
  
-   NewProjDlgSlnTreeNodeTitle  
  
-   SolutionFileCreatorIdentifier  
  
-   SolutionFileExt  
  
-   UserFilesSubFolderName  
  
-   UserOptsFileExt  
  
 O Visual Studio Shell isolado modelo cria um arquivo de origem, *solutionName*. cpp, onde *solutionName* é o nome da solução para o aplicativo. Esse arquivo define o ponto de entrada principal para o aplicativo, a função twinmain. Esta função chama o ponto de entrada do início do shell.  
  
 Você pode alterar o comportamento do aplicativo ao alterar essas configurações quando o aplicativo for iniciado.  
  
## <a name="parameters"></a>Parâmetros  
 O ponto de entrada inicial do shell do Visual Studio define cinco parâmetros. Não altere os quatro primeiros parâmetros. O quinto parâmetro usa uma lista de substituição de configurações. O ponto de entrada do início do shell é chamado de ponto de entrada principal de um aplicativo.  
  
 O ponto de entrada do início do shell tem a seguinte assinatura.  
  
```  
typedef int (__cdecl *STARTFCN)(LPSTR, LPWSTR, int, GUID *, WCHAR *pszSettings);  
```  
  
 Se você não deseja substituir as configurações de aplicativo, deixe o valor das configurações de substituir o parâmetro como um ponteiro nulo.  
  
 Para substituir uma ou mais configurações, passe uma cadeia de caracteres Unicode que contém as configurações a ser substituído. A cadeia de caracteres é uma lista separada por ponto e vírgula de pares nome-valor. Cada par contém o nome da configuração para substituir, seguido por um sinal de igual (=), seguido pelo valor para aplicar a configuração.  
  
> [!NOTE]
>  Não inclua espaços em branco em cadeias de caracteres de Unicode.  
  
 Para configurações de Boolianas, as cadeias de caracteres a seguir representam o valor true; todas as outras cadeias de caracteres que representam o valor false. Essas cadeias de caracteres diferenciam maiusculas de minúsculas.  
  
-   \+  
  
-   1  
  
-   -1  
  
-   em  
  
-   true  
  
-   sim  
  
## <a name="example"></a>Exemplo  
 Para desabilitar suplementos e alterar o local padrão dos projetos para seu aplicativo, você pode definir o último parâmetro "AddinsAllowed=false;DefaultProjectsLocation=%USERPROFILE%\temp".  
  
## <a name="see-also"></a>Consulte também  
 [Personalizando o Shell isolado](customizing-the-isolated-shell.md)   
 [. Arquivos de Pkgdef](modifying-the-isolated-shell-by-using-the-dot-pkgdef-file.md)