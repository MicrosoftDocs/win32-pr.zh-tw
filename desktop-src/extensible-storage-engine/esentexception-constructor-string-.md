---
description: 深入瞭解： EsentException (字串) 的函數
title: 'EsentException 函式 (字串)  (的函式) '
TOCTitle: EsentException constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100720
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22a93625b7becbe083a42fbd6fcc71ad801173ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980046"
---
# <a name="esentexception-constructor-string"></a>EsentException (字串) 的函式

使用指定的錯誤訊息，初始化 EsentException 類別的新實例。

**命名空間：**  [Microsoft. Isam. Esent](./microsoft.isam.esent-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Protected Sub New ( _
    message As String _
)
'Usage
Dim message As String

Dim instance As New EsentException(message)
```

``` csharp
protected EsentException(
    string message
)
```

#### <a name="parameters"></a>參數

  - message  
    類型： [system.string](/dotnet/api/system.string)  
    
    描述錯誤的訊息。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentException 類別](./esentexception-class.md)

[EsentException 成員](./esentexception-members.md)

[EsentException 多載](./esentexception-constructor.md)

[Microsoft Isam 命名空間](./microsoft.isam.esent-namespace.md)
