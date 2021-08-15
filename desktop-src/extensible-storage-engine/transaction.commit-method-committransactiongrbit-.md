---
description: 深入瞭解：交易 (CommitTransactionGrbit) 的 Commit 方法
title: Transaction (CommitTransactionGrbit) 的 Commit 方法
TOCTitle: Commit method (CommitTransactionGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.Commit(Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.commit(v=EXCHG.10)
ms:contentKeyID: 55104071
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e40bde6191759e48e59f535f672d221331fc45956e5af7bfe709d90f4573b38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484687"
---
# <a name="transactioncommit-method-committransactiongrbit"></a>Transaction (CommitTransactionGrbit) 的 Commit 方法

認可交易。 此物件應該在交易中。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Sub Commit ( _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim instance As Transaction
Dim grbit As CommitTransactionGrbit

instance.Commit(grbit)
```

``` csharp
public void Commit(
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - grbit  
    型別： [CommitTransactionGrbit](./committransactiongrbit-enumeration.md) 。  
    
    JetCommitTransaction 選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Transaction 類別](./transaction-class.md)

[交易成員](./transaction-members.md)

[認可多載](./transaction.commit-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
