---
title: Criar um adaptador de dados de diagnóstico para teste no Visual Studio
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- Diagnostic Data Adapter [Visual Studio ALM]
- Diagnostic Data Adapter
ms.assetid: b0b53fae-7007-4ad9-a604-21685937622f
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.openlocfilehash: e0a7815b57fa49239a0895e6733a13c5c83e99e1
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49860884"
---
# <a name="create-a-diagnostic-data-adapter-to-collect-custom-data-or-affect-a-test-machine"></a>Criar um adaptador de dados de diagnóstico para coletar dados personalizados ou afetar um computador de teste

É possível criar seu próprio adaptador de dados de diagnóstico para coletar dados quando você executar um teste, ou afetar o computador de teste como parte de seu teste. Por exemplo, você pode coletar os arquivos de log que são criados por seu aplicativo em teste e anexá-los aos resultados do teste, ou pode executar os testes quando há espaço limitado em disco no computador. Usando APIs fornecidas no Visual Studio Enterprise, você pode gravar código para executar tarefas em pontos específicos da execução de teste. Por exemplo, você pode executar tarefas quando um teste é iniciado, antes e depois da execução de cada teste individual, e quando o teste termina.

Você pode fornecer as informações padrão para o adaptador de dados de diagnóstico personalizado usando um arquivo de parâmetros de configuração. Por exemplo, você pode fornecer informações sobre o local do arquivo que deseja coletar e anexar aos resultados do teste, ou quanto espaço em disco você deseja deixar no sistema. Esses dados podem ser configurados para cada parâmetro de teste criado. Eles podem ser exibidos e editados usando o editor padrão fornecido com o Microsoft Test Manager ou você pode criar seu próprio controle de usuário para usar como editor. Todas as alterações feitas na configuração do adaptador no editor são armazenadas com as configurações de teste.

Se você estiver executando seus testes do Visual Studio, deverá definir essas configurações de teste como ativas. Para obter mais informações sobre as configurações de teste, confira [Coletar informações de diagnóstico usando configurações de teste](../test/collect-diagnostic-information-using-test-settings.md).

## <a name="tasks"></a>Tarefas

 Use os tópicos a seguir como auxílio para criar adaptadores de dados de diagnóstico:

|Tarefas|Tópicos associados|
|-|-----------------------|
|**Criar um adaptador de dados de diagnóstico:** você cria um adaptador de dados de diagnóstico criando uma biblioteca de classes e usa as APIs de diagnóstico do adaptador de dados para coletar informações desejadas ou afetar um sistema de teste usado para executar os testes.|-   [Como criar um adaptador de dados de diagnóstico](../test/how-to-create-a-diagnostic-data-adapter.md)|
|**Instalar um adaptador de dados de diagnóstico personalizado:** você pode instalar o adaptador de dados de diagnóstico ou um adaptador fornecido por outra pessoa copiando no diretório correto.|-   [Como instalar um adaptador de dados de diagnóstico personalizado](../test/how-to-install-a-custom-diagnostic-data-adapter.md)|
|**Selecionar um adaptador de dados de diagnóstico personalizado para usar quando testes forem executados:** você pode selecionar qual adaptador de dados de diagnóstico será usado para suas configurações de teste, de forma que o adaptador seja usado quando os testes forem executados.|-   [Coletar dados de diagnóstico durante testes (Azure Test Plans)](/azure/devops/test/collect-diagnostic-data?view=vsts)<br />-   [Coletar dados de diagnóstico em testes manuais (Azure Test Plans)](/azure/devops/test/mtm/collect-more-diagnostic-data-in-manual-tests?view=vsts)|
|**Configurar o que um adaptador de dados de diagnóstico faz:** você pode configurar os parâmetros para controlar as ações do adaptador de dados de diagnóstico nessas configurações de teste.|-   [Como criar um editor personalizado de dados para o adaptador de dados de diagnóstico](../test/how-to-create-a-custom-editor-for-data-for-your-diagnostic-data-adapter.md)|

## <a name="see-also"></a>Consulte também

- [Projeto de amostra para criar um adaptador de dados de diagnóstico](../test/sample-project-for-creating-a-diagnostic-data-adapter.md)
- [Coletar informações de diagnóstico usando configurações de teste](../test/collect-diagnostic-information-using-test-settings.md)