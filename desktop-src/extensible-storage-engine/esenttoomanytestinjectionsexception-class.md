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
ms.openlocfilehash: 9dbf35aebeace7c4384dc254211f5ed061029449
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945371"
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
