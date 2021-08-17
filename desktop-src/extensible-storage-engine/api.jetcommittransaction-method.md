---
description: 深入瞭解： JetCommitTransaction 方法
title: JetCommitTransaction 方法
TOCTitle: 'JetCommitTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcommittransaction(v=EXCHG.10)
ms:contentKeyID: 55100665
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 496faad81ef16a91c05c7d77fb29ea1536a67cfd39fabab2901c19f83162dc74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983468"
---
# <a name="apijetcommittransaction-method"></a>JetCommitTransaction 方法

認可目前儲存點期間對資料庫狀態所做的變更，並將其遷移至先前的儲存點。 如果已認可最外層的儲存點，則在該儲存點期間所做的變更將會認可至資料庫的狀態，而會話將會結束交易。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetCommitTransaction ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbitApi.JetCommitTransaction(sesid, _
    grbit)
```

``` csharp
public static void JetCommitTransaction(
    JET_SESID sesid,
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    認可交易的會話。

<!-- end list -->

  - grbit  
    型別： [CommitTransactionGrbit](./committransactiongrbit-enumeration.md) 。  
    
    認可選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
