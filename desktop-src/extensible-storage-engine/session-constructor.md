---
description: 深入瞭解：會話的函式
title: 會話的函式
TOCTitle: 'Session constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.session(v=EXCHG.10)
ms:contentKeyID: 55107728
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Session
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73d19d5ae1ba422969cd5b11f5b59ceb2811a89d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193029"
---
# <a name="session-constructor"></a>會話的函式

初始化 Session 類別的新實例。 從指定的實例配置新的 JET_SESSION。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCE

Dim instance As New Session(instance)
```

``` csharp
public Session(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a>參數

  - instance  
    類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    要在其中啟動會話的實例。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[工作階段類別](./session-class.md)

[會話成員](./session-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
