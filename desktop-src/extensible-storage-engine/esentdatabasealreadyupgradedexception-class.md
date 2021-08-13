---
description: 深入瞭解： EsentDatabaseAlreadyUpgradedException 類別
title: EsentDatabaseAlreadyUpgradedException 類別
TOCTitle: EsentDatabaseAlreadyUpgradedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasealreadyupgradedexception(v=EXCHG.10)
ms:contentKeyID: 55101322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8a187ad99281b048616eaf3889c4dcc56c4f4ddb22463575cb44d4e1c4a2096d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118781510"
---
# <a name="esentdatabasealreadyupgradedexception-class"></a>EsentDatabaseAlreadyUpgradedException 類別

JET_err 的基類。DatabaseAlreadyUpgraded 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentStateException （.）](./esentstateexception-class.md)  
            EsentDatabaseAlreadyUpgradedException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseAlreadyUpgradedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseAlreadyUpgradedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseAlreadyUpgradedException : EsentStateException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentDatabaseAlreadyUpgradedException 成員](./esentdatabasealreadyupgradedexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
