---
description: 深入瞭解：交易函數
title: 交易函數
TOCTitle: 'Transaction constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.transaction(v=EXCHG.10)
ms:contentKeyID: 55104069
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Transaction.Transaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Transaction..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a8c3214ebe3d88ce8b50aff000d64270ec50a6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193976"
---
# <a name="transaction-constructor"></a><span data-ttu-id="a2bf2-103">交易函數</span><span class="sxs-lookup"><span data-stu-id="a2bf2-103">Transaction constructor</span></span>

<span data-ttu-id="a2bf2-104">初始化 Transaction 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="a2bf2-104">Initializes a new instance of the Transaction class.</span></span> <span data-ttu-id="a2bf2-105">這會自動開始交易。</span><span class="sxs-lookup"><span data-stu-id="a2bf2-105">This automatically begins a transaction.</span></span> <span data-ttu-id="a2bf2-106">如果未明確認可，將會回復交易。</span><span class="sxs-lookup"><span data-stu-id="a2bf2-106">The transaction will be rolled back if not explicitly committed.</span></span>

<span data-ttu-id="a2bf2-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a2bf2-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a2bf2-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a2bf2-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a2bf2-109">語法</span><span class="sxs-lookup"><span data-stu-id="a2bf2-109">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESID

Dim instance As New Transaction(sesid)
```

``` csharp
public Transaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="a2bf2-110">參數</span><span class="sxs-lookup"><span data-stu-id="a2bf2-110">Parameters</span></span>

  - <span data-ttu-id="a2bf2-111">sesid</span><span class="sxs-lookup"><span data-stu-id="a2bf2-111">sesid</span></span>  
    <span data-ttu-id="a2bf2-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a2bf2-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a2bf2-113">要啟動交易的會話。</span><span class="sxs-lookup"><span data-stu-id="a2bf2-113">The session to start the transaction for.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2bf2-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2bf2-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a2bf2-115">參考</span><span class="sxs-lookup"><span data-stu-id="a2bf2-115">Reference</span></span>

[<span data-ttu-id="a2bf2-116">Transaction 類別</span><span class="sxs-lookup"><span data-stu-id="a2bf2-116">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="a2bf2-117">交易成員</span><span class="sxs-lookup"><span data-stu-id="a2bf2-117">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="a2bf2-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a2bf2-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
