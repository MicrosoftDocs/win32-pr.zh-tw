---
description: 深入瞭解： EsentInstanceUnavailableDueToFatalLogDiskFullException 類別
title: EsentInstanceUnavailableDueToFatalLogDiskFullException 類別
TOCTitle: EsentInstanceUnavailableDueToFatalLogDiskFullException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableDueToFatalLogDiskFullException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinstanceunavailableduetofatallogdiskfullexception(v=EXCHG.10)
ms:contentKeyID: 55101825
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableDueToFatalLogDiskFullException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableDueToFatalLogDiskFullException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f7e263678bc6c6b56e851f928210be59ebd3d9a0fa3cfd764043061f26bd82ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118494885"
---
# <a name="esentinstanceunavailableduetofatallogdiskfullexception-class"></a>EsentInstanceUnavailableDueToFatalLogDiskFullException 類別

JET_err 的基類。InstanceUnavailableDueToFatalLogDiskFull 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentOperationException （.）](./esentoperationexception-class.md)  
          [EsentFatalException （.）](./esentfatalexception-class.md)  
            EsentInstanceUnavailableDueToFatalLogDiskFullException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInstanceUnavailableDueToFatalLogDiskFullException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentInstanceUnavailableDueToFatalLogDiskFullException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInstanceUnavailableDueToFatalLogDiskFullException : EsentFatalException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentInstanceUnavailableDueToFatalLogDiskFullException 成員](./esentinstanceunavailableduetofatallogdiskfullexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
