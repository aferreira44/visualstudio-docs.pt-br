---
title: BeginCapture | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 9edbb52d-ee0b-4cc4-a382-972bcee067d3
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c8580283e19b61356746ecca8a707369abc45355
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49299293"
---
# <a name="begincapture"></a>BeginCapture
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Inicia um intervalo de captura que terminará com `EndCapture`.  
  
## <a name="syntax"></a>Sintaxe  
  
```cpp  
void BeginCapture();  
```  
  
## <a name="remarks"></a>Comentários  
 Normalmente, um intervalo de captura abrange um subconjunto de um quadro, como quando você deseja capturar informações gráficas trata apenas de um determinado tipo de chamada de desenho. Se o intervalo de captura abrange uma chamada para apresentar, dois quadros de informações de gráficos são capturados. O primeiro quadro abrange o intervalo entre a chamada para `BeginCapture` e a chamada para apresentar; o segundo quadro abrange o intervalo entre o primeiro evento do Direct3D após a chamada para apresentar e a chamada para `EndCapture`.  
  
 Para capturar um intervalo, você deve preparar seu aplicativo para capturar e registrar informações de gráficos — ou seja, você deve ter chamado [Init](../debugger/init.md) por meio de uma instância das `VsgDbg` classe antes de chamar `BeginCapture` ou `EndCapture`.  
  
## <a name="see-also"></a>Consulte também  
 [EndCapture](../debugger/endcapture.md)   
 [CaptureCurrentFrame](../debugger/capturecurrentframe.md)



