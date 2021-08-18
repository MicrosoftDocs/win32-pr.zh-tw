---
description: 深入瞭解： EsentTooManyTestInjectionsException 類別
title: EsentTooManyTestInjectionsException 類別
TOCTitle: EsentTooManyTestInjectionsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyTestInjectionsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanytestinjectionsexception(v=EXCHG.10)
ms:contentKeyID: 55107367
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyTestInjectionsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyTestInjectionsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e5c90ccda8585f208917447ec3b1f331b1743bdbd0be3f24800c08d50233818
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112898"
---
# <a name="esenttoomanytestinjectionsexception-class"></a>EsentTooManyTestInjectionsException 類別

JET_err 的基類。TooManyTestInjections 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentUsageException （.）](./esentusageexception-class.md)  
            EsentTooManyTestInjectionsException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyTestInjectionsException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyTestInjectionsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyTestInjectionsException : EsentUsageException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentTooManyTestInjectionsException 成員](./esenttoomanytestinjectionsexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
