---
description: 深入瞭解： EsentConsistentTimeMismatchException 類別
title: EsentConsistentTimeMismatchException 類別
TOCTitle: EsentConsistentTimeMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentconsistenttimemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55101416
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e8980648eba45a2640ef90e899efe858cac803986db407d59a88823dfbb5590
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736668"
---
# <a name="esentconsistenttimemismatchexception-class"></a>EsentConsistentTimeMismatchException 類別

JET_err 的基類。ConsistentTimeMismatch 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          [EsentInconsistentException （.）](./esentinconsistentexception-class.md)  
            EsentConsistentTimeMismatchException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentConsistentTimeMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentConsistentTimeMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentConsistentTimeMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentConsistentTimeMismatchException 成員](./esentconsistenttimemismatchexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
