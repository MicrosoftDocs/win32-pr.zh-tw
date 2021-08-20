---
description: 深入瞭解： EsentException 類別
title: 'EsentException 類別 (Microsoft 的 Isam) '
TOCTitle: EsentException class
ms:assetid: T:Microsoft.Isam.Esent.EsentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100645
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.EsentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.EsentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0f1d48827a16a44f050d8ef293217da518cfbb8eb56fa698b0458880305c1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117711017"
---
# <a name="esentexception-class"></a>EsentException 類別

ESENT 例外狀況的基類。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    EsentException。  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
      [EsentInvalidColumnException （.）](./esentinvalidcolumnexception-class.md)  

**命名空間：**  [Microsoft. Isam. Esent](./microsoft.isam.esent-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentException _
    Inherits Exception
'Usage
Dim instance As EsentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentException : Exception
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentException 成員](./esentexception-members.md)

[Microsoft Isam 命名空間](./microsoft.isam.esent-namespace.md)
