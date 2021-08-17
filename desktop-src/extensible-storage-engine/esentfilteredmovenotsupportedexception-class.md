---
description: 深入瞭解： EsentFilteredMoveNotSupportedException 類別
title: EsentFilteredMoveNotSupportedException 類別
TOCTitle: EsentFilteredMoveNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFilteredMoveNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfilteredmovenotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55107268
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFilteredMoveNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFilteredMoveNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d22beb277546296a2c071d92e67fe502f12546749b8b8ecb08fe6c43581a154
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119364718"
---
# <a name="esentfilteredmovenotsupportedexception-class"></a>EsentFilteredMoveNotSupportedException 類別

JET_err 的基類。FilteredMoveNotSupported 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentUsageException （.）](./esentusageexception-class.md)  
            EsentFilteredMoveNotSupportedException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFilteredMoveNotSupportedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentFilteredMoveNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFilteredMoveNotSupportedException : EsentUsageException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentFilteredMoveNotSupportedException 成員](./esentfilteredmovenotsupportedexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
