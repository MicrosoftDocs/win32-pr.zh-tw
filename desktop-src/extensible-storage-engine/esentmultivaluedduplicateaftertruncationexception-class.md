---
description: 深入瞭解： EsentMultiValuedDuplicateAfterTruncationException 類別
title: EsentMultiValuedDuplicateAfterTruncationException 類別
TOCTitle: EsentMultiValuedDuplicateAfterTruncationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedduplicateaftertruncationexception(v=EXCHG.10)
ms:contentKeyID: 55102259
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4354bc53349d7c9ee4625c085b983e90b06a747f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943594"
---
# <a name="esentmultivaluedduplicateaftertruncationexception-class"></a>EsentMultiValuedDuplicateAfterTruncationException 類別

JET_err 的基類。MultiValuedDuplicateAfterTruncation 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentStateException （.）](./esentstateexception-class.md)  
            EsentMultiValuedDuplicateAfterTruncationException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedDuplicateAfterTruncationException _
    Inherits EsentStateException
'Usage
Dim instance As EsentMultiValuedDuplicateAfterTruncationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedDuplicateAfterTruncationException : EsentStateException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentMultiValuedDuplicateAfterTruncationException 成員](./esentmultivaluedduplicateaftertruncationexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
