---
description: 深入瞭解： EsentCannotMaterializeForwardOnlySortException 類別
title: EsentCannotMaterializeForwardOnlySortException 類別
TOCTitle: EsentCannotMaterializeForwardOnlySortException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotMaterializeForwardOnlySortException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotmaterializeforwardonlysortexception(v=EXCHG.10)
ms:contentKeyID: 55101164
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotMaterializeForwardOnlySortException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotMaterializeForwardOnlySortException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3f34b0f45ff3b3b552b3272827a237e71d1c1eebe571a3d56b2a587bf24eaf45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118497324"
---
# <a name="esentcannotmaterializeforwardonlysortexception-class"></a>EsentCannotMaterializeForwardOnlySortException 類別

JET_err 的基類。CannotMaterializeForwardOnlySort 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentUsageException （.）](./esentusageexception-class.md)  
            EsentCannotMaterializeForwardOnlySortException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotMaterializeForwardOnlySortException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotMaterializeForwardOnlySortException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotMaterializeForwardOnlySortException : EsentUsageException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentCannotMaterializeForwardOnlySortException 成員](./esentcannotmaterializeforwardonlysortexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
