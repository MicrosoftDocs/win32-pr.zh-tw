---
description: 深入瞭解： EsentDatabaseLogSetMismatchException 類別
title: EsentDatabaseLogSetMismatchException 類別
TOCTitle: EsentDatabaseLogSetMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaselogsetmismatchexception(v=EXCHG.10)
ms:contentKeyID: 55101422
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 31cb9142c45955de7d826c540f77f1aaf893116d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983548"
---
# <a name="esentdatabaselogsetmismatchexception-class"></a>EsentDatabaseLogSetMismatchException 類別

JET_err 的基類。DatabaseLogSetMismatch 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          [EsentInconsistentException （.）](./esentinconsistentexception-class.md)  
            EsentDatabaseLogSetMismatchException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseLogSetMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDatabaseLogSetMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseLogSetMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentDatabaseLogSetMismatchException 成員](./esentdatabaselogsetmismatchexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
