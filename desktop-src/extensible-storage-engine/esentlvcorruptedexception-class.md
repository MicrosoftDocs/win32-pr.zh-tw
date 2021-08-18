---
description: 深入瞭解： EsentLVCorruptedException 類別
title: EsentLVCorruptedException 類別
TOCTitle: EsentLVCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLVCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlvcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102240
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLVCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLVCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d3479ee1dc9b9dfc8162b4a6adffc26798405576a6b3aa7b5a04c8999386c11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604938"
---
# <a name="esentlvcorruptedexception-class"></a>EsentLVCorruptedException 類別

JET_err 的基類。LVCorrupted 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          [EsentCorruptionException （.）](./esentcorruptionexception-class.md)  
            EsentLVCorruptedException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLVCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLVCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLVCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentLVCorruptedException 成員](./esentlvcorruptedexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
