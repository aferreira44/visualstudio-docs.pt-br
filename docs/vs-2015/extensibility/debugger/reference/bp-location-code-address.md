---
title: BP_LOCATION_CODE_ADDRESS | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- BP_LOCATION_CODE_ADDRESS
helpviewer_keywords:
- BP_LOCATION_CODE_ADDRESS structure
ms.assetid: 83c9da8b-19d9-4be5-b225-854543654901
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: e0f3264dd61f4f5a125e83eb80552c4d6e550123
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49862782"
---
# <a name="bplocationcodeaddress"></a>BP_LOCATION_CODE_ADDRESS
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Descreve o local de um ponto de interrupção em um endereço no código.  
  
## <a name="syntax"></a>Sintaxe  
  
```cpp#  
typedef struct _BP_LOCATION_CODE_ADDRESS {   
   BSTR bstrContext;  
   BSTR bstrModuleUrl;  
   BSTR bstrFunction;  
   BSTR bstrAddress;  
} BP_LOCATION_CODE_ADDRESS;  
```  
  
## <a name="members"></a>Membros  
 `bstrContext`  
 O contexto do ponto de interrupção, normalmente um nome de método ou função, como visto em uma pilha de chamadas.  
  
 `bstrModuleUrl`  
 A URL do módulo que contém o ponto de interrupção.  
  
 `bstrFunction`  
 O nome da função que contém o ponto de interrupção.  
  
 `bstrAddress`  
 O endereço do ponto de interrupção, que é analisada por um avaliador de expressão para associá-lo para um [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) objeto.  
  
## <a name="remarks"></a>Comentários  
 Essa estrutura é um membro do [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md) estrutura como parte de uma união.  
  
## <a name="requirements"></a>Requisitos  
 Cabeçalho: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Consulte também  
 [Estruturas e uniões](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)   
 [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)

