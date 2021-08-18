---
description: 深入瞭解： EsentSurrogateBackupInProgressException 類別
title: EsentSurrogateBackupInProgressException 類別
TOCTitle: EsentSurrogateBackupInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsurrogatebackupinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55102946
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a3b6539504866b3a0a156072b3da71ff91367f57c9b0bdc878823b45ec0dc27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835078"
---
# <a name="esentsurrogatebackupinprogressexception-class"></a>EsentSurrogateBackupInProgressException 類別

JET_err 的基類。SurrogateBackupInProgress 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentStateException （.）](./esentstateexception-class.md)  
            EsentSurrogateBackupInProgressException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSurrogateBackupInProgressException _
    Inherits EsentStateException
'Usage
Dim instance As EsentSurrogateBackupInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSurrogateBackupInProgressException : EsentStateException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentSurrogateBackupInProgressException 成員](./esentsurrogatebackupinprogressexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
