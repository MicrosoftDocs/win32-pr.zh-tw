---
description: 深入瞭解： EsentOSSnapshotInvalidSnapIdException 類別
title: EsentOSSnapshotInvalidSnapIdException 類別
TOCTitle: EsentOSSnapshotInvalidSnapIdException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOSSnapshotInvalidSnapIdException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentossnapshotinvalidsnapidexception(v=EXCHG.10)
ms:contentKeyID: 55102431
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOSSnapshotInvalidSnapIdException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOSSnapshotInvalidSnapIdException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbbd15d8962bb711e359d66bc3413bc18b8d18121464cc6a19777348e0cbcbe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947338"
---
# <a name="esentossnapshotinvalidsnapidexception-class"></a>EsentOSSnapshotInvalidSnapIdException 類別

JET_err 的基類。OSSnapshotInvalidSnapId 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentUsageException （.）](./esentusageexception-class.md)  
            EsentOSSnapshotInvalidSnapIdException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOSSnapshotInvalidSnapIdException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentOSSnapshotInvalidSnapIdException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOSSnapshotInvalidSnapIdException : EsentUsageException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentOSSnapshotInvalidSnapIdException 成員](./esentossnapshotinvalidsnapidexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
