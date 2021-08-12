---
description: 深入瞭解： EsentInvalidLogDirectoryException 類別
title: EsentInvalidLogDirectoryException 類別
TOCTitle: EsentInvalidLogDirectoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidlogdirectoryexception(v=EXCHG.10)
ms:contentKeyID: 55101985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de0eebb1386a1d2ac7d533d85a2200a3054b4c9569dce6c4fafb9fe9fa4fd551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118265609"
---
# <a name="esentinvalidlogdirectoryexception-class"></a>EsentInvalidLogDirectoryException 類別

JET_err 的基類。InvalidLogDirectory 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentObsoleteException （.）](./esentobsoleteexception-class.md)  
            EsentInvalidLogDirectoryException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidLogDirectoryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentInvalidLogDirectoryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidLogDirectoryException : EsentObsoleteException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentInvalidLogDirectoryException 成員](./esentinvalidlogdirectoryexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
