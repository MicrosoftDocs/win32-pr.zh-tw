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
ms.openlocfilehash: 18df363e4320a4b1a53c34e15fcf68939fce96ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027215"
---
# <a name="transactioncommit-method-committransactiongrbit-timespan-jet_commit_id"></a><span data-ttu-id="b0a90-103">交易. Commit 方法 (CommitTransactionGrbit、TimeSpan、JET_COMMIT_ID) </span><span class="sxs-lookup"><span data-stu-id="b0a90-103">Transaction.Commit method (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</span></span>

<span data-ttu-id="b0a90-104">認可交易。</span><span class="sxs-lookup"><span data-stu-id="b0a90-104">Commit a transaction.</span></span> <span data-ttu-id="b0a90-105">此物件應該在交易中。</span><span class="sxs-lookup"><span data-stu-id="b0a90-105">This object should be in a transaction.</span></span>

<span data-ttu-id="b0a90-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b0a90-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b0a90-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b0a90-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a90-108">語法</span><span class="sxs-lookup"><span data-stu-id="b0a90-108">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="b0a90-109">參數</span><span class="sxs-lookup"><span data-stu-id="b0a90-109">Parameters</span></span>

  - <span data-ttu-id="b0a90-110">grbit</span><span class="sxs-lookup"><span data-stu-id="b0a90-110">grbit</span></span>  
    <span data-ttu-id="b0a90-111">型別： [CommitTransactionGrbit](./committransactiongrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="b0a90-111">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b0a90-112">JetCommitTransaction 選項。</span><span class="sxs-lookup"><span data-stu-id="b0a90-112">JetCommitTransaction options.</span></span>

<!-- end list -->

  - <span data-ttu-id="b0a90-113">durableCommit</span><span class="sxs-lookup"><span data-stu-id="b0a90-113">durableCommit</span></span>  
    <span data-ttu-id="b0a90-114">類型： [TimeSpan](/dotnet/api/system.timespan)</span><span class="sxs-lookup"><span data-stu-id="b0a90-114">Type: [System.TimeSpan](/dotnet/api/system.timespan)</span></span>  
    
    <span data-ttu-id="b0a90-115">認可延遲交易的持續時間。</span><span class="sxs-lookup"><span data-stu-id="b0a90-115">Duration for committing lazy transactions.</span></span>

<!-- end list -->

  - <span data-ttu-id="b0a90-116">commitId</span><span class="sxs-lookup"><span data-stu-id="b0a90-116">commitId</span></span>  
    <span data-ttu-id="b0a90-117">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="b0a90-117">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="b0a90-118">此認可記錄的認可識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0a90-118">Commit-id for this commit record.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0a90-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0a90-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b0a90-120">參考</span><span class="sxs-lookup"><span data-stu-id="b0a90-120">Reference</span></span>

[<span data-ttu-id="b0a90-121">Transaction 類別</span><span class="sxs-lookup"><span data-stu-id="b0a90-121">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="b0a90-122">交易成員</span><span class="sxs-lookup"><span data-stu-id="b0a90-122">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="b0a90-123">認可多載</span><span class="sxs-lookup"><span data-stu-id="b0a90-123">Commit overload</span></span>](./transaction.commit-method.md)

[<span data-ttu-id="b0a90-124">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b0a90-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
