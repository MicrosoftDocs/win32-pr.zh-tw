---
description: 深入瞭解： EsentLogBufferTooSmallException 類別
title: EsentLogBufferTooSmallException 類別
TOCTitle: EsentLogBufferTooSmallException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogbuffertoosmallexception(v=EXCHG.10)
ms:contentKeyID: 55102132
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d92650333d2cd787a8e7622f2e4abd70c530bff178b4fca47884003e291b68e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019578"
---
# <a name="esentlogbuffertoosmallexception-class"></a>EsentLogBufferTooSmallException 類別

JET_err 的基類。LogBufferTooSmall 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentObsoleteException （.）](./esentobsoleteexception-class.md)  
            EsentLogBufferTooSmallException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogBufferTooSmallException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentLogBufferTooSmallException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogBufferTooSmallException : EsentObsoleteException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentLogBufferTooSmallException 成員](./esentlogbuffertoosmallexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
