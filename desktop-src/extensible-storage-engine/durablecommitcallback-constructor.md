---
description: 深入瞭解： DurableCommitCallback 的函式
title: 'DurableCommitCallback 函式 (Windows8) '
TOCTitle: 'DurableCommitCallback constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.durablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.DurableCommitCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade1952615b98d9ea41a7a1b83d0bf1a3c6fc8d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694916"
---
# <a name="durablecommitcallback-constructor"></a>DurableCommitCallback 函式

初始化 [DurableCommitCallback](./durablecommitcallback-class.md) 類別的新實例。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE, _
    wrappedCallback As JET_PFNDURABLECOMMITCALLBACK _
)
'Usage
Dim instance As JET_INSTANCE
Dim wrappedCallback As JET_PFNDURABLECOMMITCALLBACK

Dim instance As New DurableCommitCallback(instance, _
    wrappedCallback)
```

``` csharp
public DurableCommitCallback(
    JET_INSTANCE instance,
    JET_PFNDURABLECOMMITCALLBACK wrappedCallback
)
```

#### <a name="parameters"></a>參數

  - instance  
    類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    要與回呼產生關聯的實例。

<!-- end list -->

  - wrappedCallback  
    類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK](./jet-pfndurablecommitcallback-delegate.md)  
    
    要呼叫的 managed 程式碼回呼。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[DurableCommitCallback 類別](./durablecommitcallback-class.md)

[DurableCommitCallback 成員](./durablecommitcallback-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
