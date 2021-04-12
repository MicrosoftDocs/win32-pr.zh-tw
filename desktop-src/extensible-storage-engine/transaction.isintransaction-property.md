---
description: 深入瞭解： IsInTransaction 屬性
title: IsInTransaction 屬性
TOCTitle: 'IsInTransaction property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Transaction.IsInTransaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.isintransaction(v=EXCHG.10)
ms:contentKeyID: 55104073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Transaction.IsInTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.IsInTransaction
- Microsoft.Isam.Esent.Interop.Transaction.get_IsInTransaction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: db9755c952e346f5c08c0bd74caa9bf8b90fe252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513781"
---
# <a name="transactionisintransaction-property"></a>IsInTransaction 屬性

取得值，指出這個物件目前是否在交易中。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public ReadOnly Property IsInTransaction As Boolean
    Get
'Usage
Dim instance As Transaction
Dim value As Boolean

value = instance.IsInTransaction
```

``` csharp
public bool IsInTransaction { get; }
```

#### <a name="property-value"></a>屬性值

型別： [system.object](/dotnet/api/system.boolean)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Transaction 類別](./transaction-class.md)

[交易成員](./transaction-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
