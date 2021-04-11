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
ms.openlocfilehash: 048071a08d1211d6091fb6c2c23f9cfe302f8872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193970"
---
# <a name="transactioncommit-method-committransactiongrbit"></a><span data-ttu-id="6f652-103">Transaction (CommitTransactionGrbit) 的 Commit 方法</span><span class="sxs-lookup"><span data-stu-id="6f652-103">Transaction.Commit method (CommitTransactionGrbit)</span></span>

<span data-ttu-id="6f652-104">認可交易。</span><span class="sxs-lookup"><span data-stu-id="6f652-104">Commit a transaction.</span></span> <span data-ttu-id="6f652-105">此物件應該在交易中。</span><span class="sxs-lookup"><span data-stu-id="6f652-105">This object should be in a transaction.</span></span>

<span data-ttu-id="6f652-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6f652-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6f652-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6f652-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6f652-108">語法</span><span class="sxs-lookup"><span data-stu-id="6f652-108">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="6f652-109">參數</span><span class="sxs-lookup"><span data-stu-id="6f652-109">Parameters</span></span>

  - <span data-ttu-id="6f652-110">grbit</span><span class="sxs-lookup"><span data-stu-id="6f652-110">grbit</span></span>  
    <span data-ttu-id="6f652-111">型別： [CommitTransactionGrbit](./committransactiongrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="6f652-111">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6f652-112">JetCommitTransaction 選項。</span><span class="sxs-lookup"><span data-stu-id="6f652-112">JetCommitTransaction options.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f652-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f652-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6f652-114">參考</span><span class="sxs-lookup"><span data-stu-id="6f652-114">Reference</span></span>

[<span data-ttu-id="6f652-115">Transaction 類別</span><span class="sxs-lookup"><span data-stu-id="6f652-115">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="6f652-116">交易成員</span><span class="sxs-lookup"><span data-stu-id="6f652-116">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="6f652-117">認可多載</span><span class="sxs-lookup"><span data-stu-id="6f652-117">Commit overload</span></span>](./transaction.commit-method.md)

[<span data-ttu-id="6f652-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6f652-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
