---
description: 深入瞭解： EsentTooManyOpenTablesAndCleanupTimedOutException 類別
title: EsentTooManyOpenTablesAndCleanupTimedOutException 類別
TOCTitle: EsentTooManyOpenTablesAndCleanupTimedOutException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopentablesandcleanuptimedoutexception(v=EXCHG.10)
ms:contentKeyID: 55103109
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 229972a3200942f2b2864aefff3d6bc1031863f7875c69bc6994a73facb7c9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017978"
---
# <a name="esenttoomanyopentablesandcleanuptimedoutexception-class"></a>EsentTooManyOpenTablesAndCleanupTimedOutException 類別

JET_err 的基類。TooManyOpenTablesAndCleanupTimedOut 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentUsageException （.）](./esentusageexception-class.md)  
            EsentTooManyOpenTablesAndCleanupTimedOutException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenTablesAndCleanupTimedOutException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyOpenTablesAndCleanupTimedOutException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenTablesAndCleanupTimedOutException : EsentUsageException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentTooManyOpenTablesAndCleanupTimedOutException 成員](./esenttoomanyopentablesandcleanuptimedoutexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
