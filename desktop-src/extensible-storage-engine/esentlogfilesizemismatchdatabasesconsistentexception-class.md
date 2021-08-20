---
description: 深入瞭解： EsentLogFileSizeMismatchDatabasesConsistentException 類別
title: EsentLogFileSizeMismatchDatabasesConsistentException 類別
TOCTitle: EsentLogFileSizeMismatchDatabasesConsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogfilesizemismatchdatabasesconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55102114
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 12d7e18149f2082fb55c0a6e6dc871952e3dd3a296bb30906ba470c3c275618a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117900243"
---
# <a name="esentlogfilesizemismatchdatabasesconsistentexception-class"></a>EsentLogFileSizeMismatchDatabasesConsistentException 類別

JET_err 的基類。LogFileSizeMismatchDatabasesConsistent 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentStateException （.）](./esentstateexception-class.md)  
            EsentLogFileSizeMismatchDatabasesConsistentException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogFileSizeMismatchDatabasesConsistentException _
    Inherits EsentStateException
'Usage
Dim instance As EsentLogFileSizeMismatchDatabasesConsistentException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogFileSizeMismatchDatabasesConsistentException : EsentStateException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentLogFileSizeMismatchDatabasesConsistentException 成員](./esentlogfilesizemismatchdatabasesconsistentexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
