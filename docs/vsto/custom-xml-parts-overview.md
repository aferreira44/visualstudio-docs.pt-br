---
title: Visão geral de partes XML personalizado
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- custom XML parts [Office development in Visual Studio], about
- Office Open XML Formats [Office development in Visual Studio]
- custom XML parts [Office development in Visual Studio]
- embedding XML data in documents [Office development in Visual Studio]
- XML parts [Office development in Visual Studio]
- XML file formats [Office development in Visual Studio]
- data [Office development in Visual Studio], custom XML parts
- Office documents [Office development in Visual Studio, custom XML parts
- XML [Office development in Visual Studio], custom XML parts
- Word [Office development in Visual Studio], custom XML parts
- Excel [Office development in Visual Studio], custom XML parts
- documents [Office development in Visual Studio], custom XML parts
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: b31ce44c458f7f376d98fac83670595b8a163d65
ms.sourcegitcommit: 48bc8492973e93612e5afaba3b47d0f98aecf97c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2018
ms.locfileid: "49324997"
---
# <a name="custom-xml-parts-overview"></a>Visão geral de partes XML personalizado
  Você pode inserir dados XML em documentos para alguns aplicativos do Microsoft Office. Quando você insere dados XML em um documento, os dados são denominados um *parte XML personalizada*.  
  
 Você pode criar e modificar partes XML personalizadas em um documento usando um suplemento do VSTO ou solução no Visual Studio de nível de documento. Você não precisa iniciar o aplicativo do Microsoft Office para criar e modificar partes XML personalizadas.  
  
 **Aplica-se a:** as informações neste tópico se aplicam a projetos no nível de documento e projetos de suplemento do VSTO para Excel, PowerPoint e Word. Para obter mais informações, consulte [recursos disponíveis por tipo de projeto e aplicativo do Office](../vsto/features-available-by-office-application-and-project-type.md).  
  
> [!NOTE]  
>  Visual Studio também permite aos objetos de dados de cache em personalizações no nível do documento. Esse recurso é diferente de partes XML personalizadas, embora haja algumas semelhanças. Para obter mais informações, consulte [armazenado em cache dados personalizações no nível do documento](../vsto/cached-data-in-document-level-customizations.md).  
  
## <a name="understand-custom-xml-parts"></a>Entender as partes XML personalizadas  
 Partes XML personalizadas foram introduzidas no 2007 Microsoft Office system, junto com os formatos XML abertos. Esses formatos incluem novos formatos de arquivo baseado em XML para o Excel, PowerPoint e Word (como *. xlsx*, *pptx*, e *. docx*). Documentos nesses formatos consistem em arquivos XML (também denominada *partes XML*) que são organizados em pastas em um arquivo ZIP. A maioria das partes XML são partes internas que ajudam a definir a estrutura e o estado do documento. No entanto, os documentos também podem conter partes XML personalizadas, o que pode ser usado para armazenar dados arbitrários do XML em documentos.  
  
 Habilitar aplicativos para trabalhar com documentos de maneiras que não são possíveis com os formatos de arquivo binário mais antigos de formatos de arquivo XML (como *. xls*, *ppt*, e *. doc*). Qualquer aplicativo que pode ler arquivos ZIP pode examinar e modificar o conteúdo dos documentos, mesmo se o Microsoft Office não está instalado.  
  
 Para obter mais informações sobre a estrutura do Open XML e partes XML personalizadas, consulte os seguintes artigos:  
  
-   [Apresentando os formatos de arquivo do Office (2007) Open XML](http://msdn.microsoft.com/96018532-f62c-4da7-bbff-16b96a483fbf)  
  
-   [Como: manipular documentos nos formatos XML abertos](http://msdn.microsoft.com/c989d4e2-053d-4e1f-83be-257c608b343f)  
  
-   [Passo a passo: Formato de XML do Word 2007](http://msdn.microsoft.com/fc1afcb2-27fb-4608-9f29-11b7bd23ea4a)  
  
-   [Criar documentos do Word 2007 usando os formatos XML abertos](http://msdn.microsoft.com/59a46f4e-5a5a-4dac-86e5-7dfd43330766)  
  
> [!NOTE]  
>  Excel, Word e PowerPoint também permitem que você usar partes XML personalizadas em documentos que são salvos nos formatos de arquivo binário. No entanto, se um documento for salvo em um formato binário, não é possível adicionar ou modificar partes XML personalizadas sem iniciar o aplicativo Microsoft Office.  
  
## <a name="create-and-modify-custom-xml-parts"></a>Criar e modificar partes XML personalizadas  
 Você pode criar ou modificar partes XML personalizadas quando o documento está aberto no aplicativo do Office, ou quando o documento é fechado, mesmo se o Microsoft Office não está instalado.  
  
### <a name="modify-xml-parts-while-the-office-application-is-running"></a>Modificar partes XML enquanto o aplicativo do Office está em execução  
 Você pode trabalhar com partes XML personalizadas, usando uma personalização no nível de documento ou um suplemento do VSTO. Se você estiver usando uma personalização no nível de documento, você normalmente irá trabalhar com partes XML personalizadas que estão no documento personalizado. Se você estiver usando um suplemento do VSTO, você pode criar ou modificar partes XML personalizadas em qualquer documento que está aberto no aplicativo.  
  
 Para criar uma parte XML personalizada usando o Visual Studio, adicione um novo <xref:Microsoft.Office.Core.CustomXMLPart> para o <xref:Microsoft.Office.Core.CustomXMLParts> coleta no documento. Para mais informações, consulte os seguintes tópicos:  
  
-   [Como: adicionar partes XML personalizadas a personalizações no nível do documento](../vsto/how-to-add-custom-xml-parts-to-document-level-customizations.md)  
  
-   [Como: adicionar partes XML personalizadas aos documentos usando suplementos VSTO](../vsto/how-to-add-custom-xml-parts-to-documents-by-using-vsto-add-ins.md)  
  
### <a name="modify-xml-parts-without-starting-the-office-application"></a>Modificar partes XML sem iniciar o aplicativo do Office  
 Você pode adicionar ou modificar uma parte XML personalizada sem iniciar o Excel, PowerPoint ou Word. Isso é útil se você quiser trabalhar com dados XML em um documento em um computador que não tenha instalados, como um servidor de aplicativos do Microsoft Office.  
  
 Para adicionar uma parte XML personalizada sem iniciar o Microsoft Office, use classes no SDK do XML aberto. Essas classes são projetadas para fornecer acesso ao conteúdo XML aberto que é específico para documentos do Office. Por exemplo, para adicionar uma parte XML personalizada para uma pasta de trabalho do Excel, use o [AddNewPart\<T >](https://msdn.microsoft.com/library/office/cc562657.aspx) método de um [WorkbookPart](https://msdn.microsoft.com/library/office/documentformat.openxml.packaging.workbookpart.aspx) objeto. Para obter mais informações, consulte [SDK do Open XML](/office/open-xml/open-xml-sdk).  
  
## <a name="bind-custom-xml-parts-to-word-content-controls"></a>Associar partes XML personalizadas aos controles de conteúdo do Word  
 Você pode associar controles de conteúdo em uma solução do Word a elementos em uma parte XML personalizada. Quando um controle de conteúdo é associado a uma parte XML personalizada, os dados na parte XML personalizada são exibidos na interface do usuário (IU) do controle de conteúdo. Se um usuário edita o texto do controle, o elemento XML correspondente é atualizado automaticamente. Da mesma forma, se os valores de elemento em que as partes XML personalizadas são alterados, os controles de conteúdo que são associados aos elementos XML exibem os novos dados. Para obter mais informações, consulte [controles de conteúdo](../vsto/content-controls.md).  
  
## <a name="see-also"></a>Consulte também  
 [Esquemas e dados em personalizações no nível de documento XML](../vsto/xml-schemas-and-data-in-document-level-customizations.md)   
 [Como: adicionar partes XML personalizadas a personalizações no nível do documento](../vsto/how-to-add-custom-xml-parts-to-document-level-customizations.md)   
 [Como: adicionar partes XML personalizadas aos documentos usando suplementos VSTO](../vsto/how-to-add-custom-xml-parts-to-documents-by-using-vsto-add-ins.md)   
 [Controles de conteúdo](../vsto/content-controls.md)   
 [Passo a passo: Associar controles de conteúdo a partes XML personalizadas](../vsto/walkthrough-binding-content-controls-to-custom-xml-parts.md)  
  
  
