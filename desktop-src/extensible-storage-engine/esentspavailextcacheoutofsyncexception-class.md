---
description: 深入瞭解： EsentSPAvailExtCacheOutOfSyncException 類別
title: EsentSPAvailExtCacheOutOfSyncException 類別
TOCTitle: EsentSPAvailExtCacheOutOfSyncException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfSyncException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentspavailextcacheoutofsyncexception(v=EXCHG.10)
ms:contentKeyID: 55102876
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfSyncException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfSyncException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 858646a446266f94fd218a418d94222493ea923b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996808"
---
# <a name="esentspavailextcacheoutofsyncexception-class"></a>EsentSPAvailExtCacheOutOfSyncException 類別

JET_err 的基類。SPAvailExtCacheOutOfSync 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentObsoleteException （.）](./esentobsoleteexception-class.md)  
            EsentSPAvailExtCacheOutOfSyncException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSPAvailExtCacheOutOfSyncException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentSPAvailExtCacheOutOfSyncException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSPAvailExtCacheOutOfSyncException : EsentObsoleteException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentSPAvailExtCacheOutOfSyncException 成員](./esentspavailextcacheoutofsyncexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
