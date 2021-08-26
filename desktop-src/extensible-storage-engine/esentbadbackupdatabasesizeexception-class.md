---
description: 深入瞭解： EsentBadBackupDatabaseSizeException 類別
title: EsentBadBackupDatabaseSizeException 類別
TOCTitle: EsentBadBackupDatabaseSizeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadBackupDatabaseSizeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadbackupdatabasesizeexception(v=EXCHG.10)
ms:contentKeyID: 55101045
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadBackupDatabaseSizeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadBackupDatabaseSizeException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ee8de11055350848dc75e55194bd76bc2b1093040f7796d822bc979c62680b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021291"
---
# <a name="esentbadbackupdatabasesizeexception-class"></a>EsentBadBackupDatabaseSizeException 類別

JET_err 的基類。BadBackupDatabaseSize 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentObsoleteException （.）](./esentobsoleteexception-class.md)  
            EsentBadBackupDatabaseSizeException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadBackupDatabaseSizeException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentBadBackupDatabaseSizeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadBackupDatabaseSizeException : EsentObsoleteException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentBadBackupDatabaseSizeException 成員](./esentbadbackupdatabasesizeexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
