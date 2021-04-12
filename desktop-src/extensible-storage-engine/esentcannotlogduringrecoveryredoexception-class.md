---
description: 深入瞭解： EsentCannotLogDuringRecoveryRedoException 類別
title: EsentCannotLogDuringRecoveryRedoException 類別
TOCTitle: EsentCannotLogDuringRecoveryRedoException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotLogDuringRecoveryRedoException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotlogduringrecoveryredoexception(v=EXCHG.10)
ms:contentKeyID: 55101221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotLogDuringRecoveryRedoException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotLogDuringRecoveryRedoException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ae0e3b6bf805b6913abba5eb5bb59c5013672d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468665"
---
# <a name="esentcannotlogduringrecoveryredoexception-class"></a>EsentCannotLogDuringRecoveryRedoException 類別

JET_err 的基類。CannotLogDuringRecoveryRedo 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        EsentCannotLogDuringRecoveryRedoException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotLogDuringRecoveryRedoException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentCannotLogDuringRecoveryRedoException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotLogDuringRecoveryRedoException : EsentErrorException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentCannotLogDuringRecoveryRedoException 成員](./esentcannotlogduringrecoveryredoexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
