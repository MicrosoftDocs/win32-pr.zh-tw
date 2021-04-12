---
description: 深入瞭解： EsentInvalidPlaceholderColumnException 類別
title: EsentInvalidPlaceholderColumnException 類別
TOCTitle: EsentInvalidPlaceholderColumnException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidPlaceholderColumnException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidplaceholdercolumnexception(v=EXCHG.10)
ms:contentKeyID: 55102014
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidPlaceholderColumnException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidPlaceholderColumnException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e18cd4c7a5b65b8125b99b51af5b64a4673b1565
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320996"
---
# <a name="esentinvalidplaceholdercolumnexception-class"></a>EsentInvalidPlaceholderColumnException 類別

JET_err 的基類。InvalidPlaceholderColumn 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentUsageException （.）](./esentusageexception-class.md)  
            EsentInvalidPlaceholderColumnException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidPlaceholderColumnException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidPlaceholderColumnException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidPlaceholderColumnException : EsentUsageException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentInvalidPlaceholderColumnException 成員](./esentinvalidplaceholdercolumnexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
