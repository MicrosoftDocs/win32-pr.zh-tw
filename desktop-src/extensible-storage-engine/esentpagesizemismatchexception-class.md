---
description: 深入瞭解： EsentPageSizeMismatchException 類別
title: EsentPageSizeMismatchException 類別
TOCTitle: EsentPageSizeMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpagesizemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55102466
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0573603fae445e1e5ae9d9768c3a0ffcf38f283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978211"
---
# <a name="esentpagesizemismatchexception-class"></a>EsentPageSizeMismatchException 類別

JET_err 的基類。PageSizeMismatch 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          [EsentInconsistentException （.）](./esentinconsistentexception-class.md)  
            EsentPageSizeMismatchException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPageSizeMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentPageSizeMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPageSizeMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentPageSizeMismatchException 成員](./esentpagesizemismatchexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
