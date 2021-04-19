---
description: 深入瞭解： EsentTooManyInstancesException 類別
title: EsentTooManyInstancesException 類別
TOCTitle: EsentTooManyInstancesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyinstancesexception(v=EXCHG.10)
ms:contentKeyID: 55103084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ecd20f6a05a17d4bd21623732a4e716e82c9b1cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983827"
---
# <a name="esenttoomanyinstancesexception-class"></a>EsentTooManyInstancesException 類別

JET_err 的基類。TooManyInstances 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentOperationException （.）](./esentoperationexception-class.md)  
          [EsentResourceException （.）](./esentresourceexception-class.md)  
            [EsentQuotaException （.）](./esentquotaexception-class.md)  
              EsentTooManyInstancesException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyInstancesException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentTooManyInstancesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyInstancesException : EsentQuotaException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentTooManyInstancesException 成員](./esenttoomanyinstancesexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
