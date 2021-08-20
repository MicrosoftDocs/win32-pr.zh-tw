---
description: 深入瞭解： EsentSoftRecoveryOnSnapshotException 類別
title: EsentSoftRecoveryOnSnapshotException 類別
TOCTitle: EsentSoftRecoveryOnSnapshotException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsoftrecoveryonsnapshotexception(v=EXCHG.10)
ms:contentKeyID: 55102866
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 711595f8fcd3025376e2fbf5ab88aca1cd3eed22a461a20e449e9d8ad5caf755
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039666"
---
# <a name="esentsoftrecoveryonsnapshotexception-class"></a>EsentSoftRecoveryOnSnapshotException 類別

JET_err 的基類。SoftRecoveryOnSnapshot 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentObsoleteException （.）](./esentobsoleteexception-class.md)  
            EsentSoftRecoveryOnSnapshotException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSoftRecoveryOnSnapshotException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentSoftRecoveryOnSnapshotException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSoftRecoveryOnSnapshotException : EsentObsoleteException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentSoftRecoveryOnSnapshotException 成員](./esentsoftrecoveryonsnapshotexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
