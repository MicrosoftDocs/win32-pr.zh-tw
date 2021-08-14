---
description: 深入瞭解： EsentDatabaseIncompleteIncrementalReseedException 類別
title: EsentDatabaseIncompleteIncrementalReseedException 類別
TOCTitle: EsentDatabaseIncompleteIncrementalReseedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseincompleteincrementalreseedexception(v=EXCHG.10)
ms:contentKeyID: 55101478
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fdb8219ee0759bddaa5c5258ec184bc40af5bdf207665357a648c8880cdd8f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118781249"
---
# <a name="esentdatabaseincompleteincrementalreseedexception-class"></a>EsentDatabaseIncompleteIncrementalReseedException 類別

JET_err 的基類。DatabaseIncompleteIncrementalReseed 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          [EsentInconsistentException （.）](./esentinconsistentexception-class.md)  
            EsentDatabaseIncompleteIncrementalReseedException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseIncompleteIncrementalReseedException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDatabaseIncompleteIncrementalReseedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseIncompleteIncrementalReseedException : EsentInconsistentException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentDatabaseIncompleteIncrementalReseedException 成員](./esentdatabaseincompleteincrementalreseedexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
