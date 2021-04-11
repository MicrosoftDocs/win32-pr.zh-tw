---
description: 深入瞭解： EsentDatabaseAlreadyRunningMaintenanceException 類別
title: EsentDatabaseAlreadyRunningMaintenanceException 類別
TOCTitle: EsentDatabaseAlreadyRunningMaintenanceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasealreadyrunningmaintenanceexception(v=EXCHG.10)
ms:contentKeyID: 55101317
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c9f9f65df8db69762f6ec6bca72ad3903cd72ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112140"
---
# <a name="esentdatabasealreadyrunningmaintenanceexception-class"></a>EsentDatabaseAlreadyRunningMaintenanceException 類別

JET_err 的基類。DatabaseAlreadyRunningMaintenance 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentUsageException （.）](./esentusageexception-class.md)  
            EsentDatabaseAlreadyRunningMaintenanceException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseAlreadyRunningMaintenanceException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseAlreadyRunningMaintenanceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseAlreadyRunningMaintenanceException : EsentUsageException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentDatabaseAlreadyRunningMaintenanceException 成員](./esentdatabasealreadyrunningmaintenanceexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
