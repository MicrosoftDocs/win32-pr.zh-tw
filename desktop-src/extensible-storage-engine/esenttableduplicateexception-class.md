---
description: 深入瞭解： EsentTableDuplicateException 類別
title: EsentTableDuplicateException 類別
TOCTitle: EsentTableDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTableDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttableduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55103013
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTableDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTableDuplicateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c8a5245394d177fe7378bba11fbd1e76413b4257db565f9990109f0434673ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119363288"
---
# <a name="esenttableduplicateexception-class"></a>EsentTableDuplicateException 類別

JET_err 的基類。TableDuplicate 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentStateException （.）](./esentstateexception-class.md)  
            EsentTableDuplicateException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTableDuplicateException _
    Inherits EsentStateException
'Usage
Dim instance As EsentTableDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTableDuplicateException : EsentStateException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentTableDuplicateException 成員](./esenttableduplicateexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
