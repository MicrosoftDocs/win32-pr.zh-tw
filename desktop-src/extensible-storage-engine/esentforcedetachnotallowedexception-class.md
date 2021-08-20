---
description: 深入瞭解： EsentForceDetachNotAllowedException 類別
title: EsentForceDetachNotAllowedException 類別
TOCTitle: EsentForceDetachNotAllowedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentforcedetachnotallowedexception(v=EXCHG.10)
ms:contentKeyID: 55101772
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9178f0aca962e72575c6a66ad26f5c73a601b47615ecd74cc6d5653fcd2412c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118081589"
---
# <a name="esentforcedetachnotallowedexception-class"></a>EsentForceDetachNotAllowedException 類別

JET_err 的基類。ForceDetachNotAllowed 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentUsageException （.）](./esentusageexception-class.md)  
            EsentForceDetachNotAllowedException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentForceDetachNotAllowedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentForceDetachNotAllowedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentForceDetachNotAllowedException : EsentUsageException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentForceDetachNotAllowedException 成員](./esentforcedetachnotallowedexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
