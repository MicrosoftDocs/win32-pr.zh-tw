---
description: 深入瞭解： EsentVersionStoreOutOfMemoryAndCleanupTimedOutException 類別
title: EsentVersionStoreOutOfMemoryAndCleanupTimedOutException 類別
TOCTitle: EsentVersionStoreOutOfMemoryAndCleanupTimedOutException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversionstoreoutofmemoryandcleanuptimedoutexception(v=EXCHG.10)
ms:contentKeyID: 55103240
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 58cfb5343bd4de471dc73cb0fa5a57729dde5b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983695"
---
# <a name="esentversionstoreoutofmemoryandcleanuptimedoutexception-class"></a>EsentVersionStoreOutOfMemoryAndCleanupTimedOutException 類別

JET_err 的基類。VersionStoreOutOfMemoryAndCleanupTimedOut 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentUsageException （.）](./esentusageexception-class.md)  
            EsentVersionStoreOutOfMemoryAndCleanupTimedOutException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentVersionStoreOutOfMemoryAndCleanupTimedOutException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
```

``` csharp
[SerializableAttribute]
public sealed class EsentVersionStoreOutOfMemoryAndCleanupTimedOutException : EsentUsageException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentVersionStoreOutOfMemoryAndCleanupTimedOutException 成員](./esentversionstoreoutofmemoryandcleanuptimedoutexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
