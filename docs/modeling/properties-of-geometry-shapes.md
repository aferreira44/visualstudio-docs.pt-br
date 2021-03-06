---
title: Propriedades de formas geométricas
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.dsltools.dsldesigner.geometryshape
helpviewer_keywords:
- Domain-Specific Language, geometry shape
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.technology: vs-ide-modeling
ms.openlocfilehash: f9e1febd80c060d97ec9b533a3ec1b67d0427eab
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49942173"
---
# <a name="properties-of-geometry-shapes"></a>Propriedades de formas geométricas
Você pode usar formas geométricas para especificar como as instâncias de classes de domínio são exibidas em uma linguagem específica de domínio. Para obter mais informações, consulte [como definir uma linguagem específica do domínio](../modeling/how-to-define-a-domain-specific-language.md). Para obter mais informações sobre como usar essas propriedades, consulte [personalizando e estendendo uma linguagem específica do domínio](../modeling/customizing-and-extending-a-domain-specific-language.md).

 Formas geométricas têm as propriedades que são listadas na tabela a seguir.

|Propriedade|Descrição|Padrão|
|-|-|-|
|Cor de preenchimento|A cor de preenchimento desta forma.|Branco|
|Modo de gradiente de preenchimento|O modo gradiente de preenchimento desta forma (Horizontal, Vertical, Diagonal para frente, Diagonal para trás ou nenhum).|Horizontal|
|geometria|A geometria desta forma (retângulo, retângulo arredondado, elipse ou um círculo).|Retângulo|
|Tem pontos de Conexão padrão|Se `True`, a forma usará superior, inferior, esquerda e pontos de conexão certa no designer gerado.|False|
|Cor do contorno|A cor do contorno desta forma.|Preto|
|Estilo de contorno tracejado|O estilo de contorno tracejado desta forma (sólido, traço, Dot, Traçoponto, Traçopontoponto ou personalizado).|Sólido|
|Espessura do contorno|A espessura do contorno desta forma.|0.03125|
|Cor do texto|A cor que é usada para os decoradores de texto que estão associados esta forma.|Preto|
|Modificador de acesso|O modificador de acesso da classe (público ou interno).|Público|
|Atributos personalizados|Usado para adicionar atributos para a classe de código de origem que é gerada para esta forma.|\<Nenhum >|
|Gera dupla derivado|Se `True`, serão geradas uma classe base e uma classe parcial (para dar suporte à personalização por meio de substituições). Para obter mais informações, consulte [substituindo e estendendo as Classes geradas](../modeling/overriding-and-extending-the-generated-classes.md).|False|
|Tem um construtor personalizado|Se `True`, um construtor personalizado será fornecido no código-fonte. Para obter mais informações, consulte [substituindo e estendendo as Classes geradas](../modeling/overriding-and-extending-the-generated-classes.md).|False|
|Modificador de herança|Descreve o tipo de herança da classe de código fonte que é gerado a partir da forma (`none`, `abstract` ou `sealed`).|nenhum|
|Forma geométrica base|A classe base dessa forma.|(nenhum)|
|Nome|O nome desta forma.|Nome atual|
|Namespace|O namespace que é afiliado desta forma.|Namespace atual|
|Tipo de dica de ferramenta|Como a dica de ferramenta é definida (fixo, variável ou nenhum). Se fixo, em seguida, o valor da `Fixed Tooltip Text` propriedade é usada como a dica de ferramenta; se a variável, em seguida, a dica de ferramenta é definida no código personalizado.|Nenhum|
|Observações|Observações informais associadas esse elemento.|\<Nenhum >|
|Altura inicial|Altura inicial desta forma em polegadas.|1|
|Largura inicial|Largura inicial desta forma em polegadas.|1.5|
|Cor de preenchimento expostos como propriedade<br /><br /> Modo de gradiente de preenchimento exposto<br /><br /> Exposto a cor do contorno como propriedade<br /><br /> Exposto o estilo de contorno tracejado como propriedade<br /><br /> Exposto como propriedade de espessura do contorno<br /><br /> Expõe a cor do texto|Se `True`, o usuário pode definir a propriedade indicada de uma forma. Para configurar isso, a definição de forma com o botão direito e clique em **adicionar exposto**.|False|
|Descrição|A descrição é usada para documentar o designer gerado.|\<Nenhum >|
|Nome de Exibição|O nome que será exibido no designer gerado para esta forma.|\<Nenhum >|
|Texto de dica de ferramenta fixa|O texto que é usado para uma dica de ferramenta fixa.|\<Nenhum >|
|Palavra-chave de ajuda|A palavra-chave que é usada para indexar a Ajuda de F1 para esta forma.|\<Nenhum >|

## <a name="see-also"></a>Consulte também

- [Glossário de ferramentas de linguagem específica do domínio](http://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)