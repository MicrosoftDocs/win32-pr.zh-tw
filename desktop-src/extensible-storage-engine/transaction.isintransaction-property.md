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
ms.openlocfilehash: 1d799cd008fa63aae3ba262a9c89c031e9fce9a2591e8636e120b36ab2b37e5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117701764"
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
