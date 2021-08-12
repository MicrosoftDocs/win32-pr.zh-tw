---
description: 深入瞭解： EsentMultiValuedIndexViolationException 類別
title: EsentMultiValuedIndexViolationException 類別
TOCTitle: EsentMultiValuedIndexViolationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedindexviolationexception(v=EXCHG.10)
ms:contentKeyID: 55102266
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13a49ebdc4036ec4d263304a918de63c3d4a33a1bc54f94bb58630e49333520c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118264015"
---
# <a name="esentmultivaluedindexviolationexception-class"></a>EsentMultiValuedIndexViolationException 類別

JET_err 的基類。MultiValuedIndexViolation 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentUsageException （.）](./esentusageexception-class.md)  
            EsentMultiValuedIndexViolationException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedIndexViolationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentMultiValuedIndexViolationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedIndexViolationException : EsentUsageException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentMultiValuedIndexViolationException 成員](./esentmultivaluedindexviolationexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
