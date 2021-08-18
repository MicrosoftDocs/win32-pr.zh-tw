---
description: '深入瞭解：交易. Commit 方法 (CommitTransactionGrbit、TimeSpan、JET_COMMIT_ID) '
title: '交易. Commit 方法 (CommitTransactionGrbit、TimeSpan、JET_COMMIT_ID) '
TOCTitle: Commit method (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.Commit(Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.commit(v=EXCHG.10)
ms:contentKeyID: 55104166
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.Commit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 90fd53fd7097db98ab84148b3f32710c369c948ed64c3606d0018cc8e79c877a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890511"
---
# <a name="transactioncommit-method-committransactiongrbit-timespan-jet_commit_id"></a>交易. Commit 方法 (CommitTransactionGrbit、TimeSpan、JET_COMMIT_ID) 

認可交易。 此物件應該在交易中。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Sub Commit ( _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim instance As Transaction
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_ID

instance.Commit(grbit, durableCommit, _
    commitId)
```

``` csharp
public void Commit(
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a>參數

  - grbit  
    型別： [CommitTransactionGrbit](./committransactiongrbit-enumeration.md) 。  
    
    JetCommitTransaction 選項。

<!-- end list -->

  - durableCommit  
    類型： [TimeSpan](/dotnet/api/system.timespan)  
    
    認可延遲交易的持續時間。

<!-- end list -->

  - commitId  
    類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    此認可記錄的認可識別碼。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Transaction 類別](./transaction-class.md)

[交易成員](./transaction-members.md)

[認可多載](./transaction.commit-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
