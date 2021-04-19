---
description: 深入瞭解： CommitTransactionGrbit 列舉
title: CommitTransactionGrbit 列舉
TOCTitle: CommitTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.committransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39510830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a93504d688d1eddfcde81ae23c87e62f70e0aab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997280"
---
# <a name="committransactiongrbit-enumeration"></a><span data-ttu-id="b9755-103">CommitTransactionGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="b9755-103">CommitTransactionGrbit enumeration</span></span>

<span data-ttu-id="b9755-104">JetCommitTransaction 的選項。</span><span class="sxs-lookup"><span data-stu-id="b9755-104">Options for JetCommitTransaction.</span></span>

<span data-ttu-id="b9755-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="b9755-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="b9755-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b9755-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b9755-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b9755-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b9755-108">語法</span><span class="sxs-lookup"><span data-stu-id="b9755-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CommitTransactionGrbit
'Usage
Dim instance As CommitTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum CommitTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="b9755-109">成員</span><span class="sxs-lookup"><span data-stu-id="b9755-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b9755-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="b9755-110">Member name</span></span></th>
<th><span data-ttu-id="b9755-111">描述</span><span class="sxs-lookup"><span data-stu-id="b9755-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b9755-112">無</span><span class="sxs-lookup"><span data-stu-id="b9755-112">None</span></span></td>
<td><span data-ttu-id="b9755-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="b9755-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b9755-114">LazyFlush</span><span class="sxs-lookup"><span data-stu-id="b9755-114">LazyFlush</span></span></td>
<td><span data-ttu-id="b9755-115">交易會正常認可，但此 Api 不會等到交易被排清到交易記錄檔，然後再傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="b9755-115">The transaction is committed normally but this Api does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="b9755-116">這可大幅減少認可作業的持續時間，代價是持久性。</span><span class="sxs-lookup"><span data-stu-id="b9755-116">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="b9755-117">在下次呼叫 JetInit 期間，任何未在損毀之前排清到記錄檔的交易都會自動中止。</span><span class="sxs-lookup"><span data-stu-id="b9755-117">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to JetInit.</span></span> <span data-ttu-id="b9755-118">如果指定 WaitLastLevel0Commit 或 WaitAllLevel0Commit，則會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="b9755-118">If WaitLastLevel0Commit or WaitAllLevel0Commit are specified, this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b9755-119">WaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="b9755-119">WaitLastLevel0Commit</span></span></td>
<td><span data-ttu-id="b9755-120">如果會話先前已認可任何交易，而且它們尚未排清到交易記錄檔，則應該立即排清它們。</span><span class="sxs-lookup"><span data-stu-id="b9755-120">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="b9755-121">此 Api 會等到交易已排清之後，再返回呼叫端。</span><span class="sxs-lookup"><span data-stu-id="b9755-121">This Api will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="b9755-122">如果應用程式先前已使用 JET_bitCommitLazyFlush 認可數筆交易，而現在想要將所有交易排清到磁片上，這項功能就很有用。</span><span class="sxs-lookup"><span data-stu-id="b9755-122">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span>
<p><span data-ttu-id="b9755-123">即使會話目前不在交易中，也可以使用此選項。</span><span class="sxs-lookup"><span data-stu-id="b9755-123">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="b9755-124">此選項不能與任何其他選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b9755-124">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b9755-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9755-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b9755-126">參考</span><span class="sxs-lookup"><span data-stu-id="b9755-126">Reference</span></span>

[<span data-ttu-id="b9755-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b9755-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
