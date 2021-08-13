---
description: 深入瞭解： EsentDatabaseIncompleteUpgradeException 類別
title: EsentDatabaseIncompleteUpgradeException 類別
TOCTitle: EsentDatabaseIncompleteUpgradeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseincompleteupgradeexception(v=EXCHG.10)
ms:contentKeyID: 55101371
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: adf061a556c4afe7f6cd593b5cf9123f9450c049318a54b168d3f2521916cad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118781060"
---
# <a name="esentdatabaseincompleteupgradeexception-class"></a>EsentDatabaseIncompleteUpgradeException 類別

JET_err 的基類。DatabaseIncompleteUpgrade 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentStateException （.）](./esentstateexception-class.md)  
            EsentDatabaseIncompleteUpgradeException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseIncompleteUpgradeException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseIncompleteUpgradeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseIncompleteUpgradeException : EsentStateException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentDatabaseIncompleteUpgradeException 成員](./esentdatabaseincompleteupgradeexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
