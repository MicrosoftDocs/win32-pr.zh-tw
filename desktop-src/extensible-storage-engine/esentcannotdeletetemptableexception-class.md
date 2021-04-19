---
description: 深入瞭解： EsentCannotDeleteTempTableException 類別
title: EsentCannotDeleteTempTableException 類別
TOCTitle: EsentCannotDeleteTempTableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotdeletetemptableexception(v=EXCHG.10)
ms:contentKeyID: 55101145
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f333798a6b151b63cbd40c69fab438ecdff68ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994472"
---
# <a name="esentcannotdeletetemptableexception-class"></a>EsentCannotDeleteTempTableException 類別

JET_err 的基類。CannotDeleteTempTable 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentUsageException （.）](./esentusageexception-class.md)  
            EsentCannotDeleteTempTableException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotDeleteTempTableException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotDeleteTempTableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotDeleteTempTableException : EsentUsageException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentCannotDeleteTempTableException 成員](./esentcannotdeletetemptableexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
