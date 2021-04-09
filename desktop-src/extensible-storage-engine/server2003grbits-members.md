---
description: 深入瞭解： Server2003Grbits 成員
title: Server2003Grbits 成員 (Server2003) 的成員
TOCTitle: Server2003Grbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_members(v=EXCHG.10)
ms:contentKeyID: 55107767
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 21008153606a6c35c76daf3c2758211f3fcdd42e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849538"
---
# <a name="server2003grbits-members"></a><span data-ttu-id="e94bd-103">Server2003Grbits 成員</span><span class="sxs-lookup"><span data-stu-id="e94bd-103">Server2003Grbits members</span></span>

<span data-ttu-id="e94bd-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="e94bd-104">Include protected members</span></span>  
<span data-ttu-id="e94bd-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="e94bd-105">Include inherited members</span></span>  

<span data-ttu-id="e94bd-106">已新增至 Windows Server 2003 版 ESENT 的 Grbits。</span><span class="sxs-lookup"><span data-stu-id="e94bd-106">Grbits that have been added to the Windows Server 2003 version of ESENT.</span></span>

<span data-ttu-id="e94bd-107">[Server2003Grbits](./server2003grbits-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="e94bd-107">The [Server2003Grbits](./server2003grbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="e94bd-108">欄位</span><span class="sxs-lookup"><span data-stu-id="e94bd-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e94bd-109">名稱</span><span class="sxs-lookup"><span data-stu-id="e94bd-109">Name</span></span></th>
<th><span data-ttu-id="e94bd-110">描述</span><span class="sxs-lookup"><span data-stu-id="e94bd-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="e94bd-113"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span><span class="sxs-lookup"><span data-stu-id="e94bd-113"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span></span></td>
<td><span data-ttu-id="e94bd-114">如果指定的資料行不存在於記錄中，而且它具有使用者定義的預設值，則不會傳回任何資料行值。</span><span class="sxs-lookup"><span data-stu-id="e94bd-114">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="e94bd-115">此選項可防止在列舉該資料行的值時，計算資料行之使用者定義預設值的回呼。</span><span class="sxs-lookup"><span data-stu-id="e94bd-115">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="e94bd-118"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span><span class="sxs-lookup"><span data-stu-id="e94bd-118"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span></span></td>
<td><span data-ttu-id="e94bd-119">如果臨時表管理員可以使用針對中繼查詢結果優化的執行，此選項會要求只建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="e94bd-119">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="e94bd-120">如果臨時表的任何特性會防止使用這項優化，則作業會失敗並 JET_errCannotMaterializeForwardOnlySort。</span><span class="sxs-lookup"><span data-stu-id="e94bd-120">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="e94bd-121">此選項的副作用是允許臨時表包含具有重複索引鍵的記錄。</span><span class="sxs-lookup"><span data-stu-id="e94bd-121">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="e94bd-122">如需詳細資訊，請參閱 <a href="hh558517(v=exchg.10).md">唯一</a> 的。</span><span class="sxs-lookup"><span data-stu-id="e94bd-122">See <a href="hh558517(v=exchg.10).md">Unique</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="e94bd-125"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span><span class="sxs-lookup"><span data-stu-id="e94bd-125"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span></span></td>
<td><span data-ttu-id="e94bd-126">所有先前由尚未排清至交易記錄檔的會話所認可的交易，都會立即進行清除。</span><span class="sxs-lookup"><span data-stu-id="e94bd-126">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="e94bd-127">此 API 會等到交易已排清之後，再返回呼叫端。</span><span class="sxs-lookup"><span data-stu-id="e94bd-127">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="e94bd-128">即使會話目前不在交易中，也可以使用此選項。</span><span class="sxs-lookup"><span data-stu-id="e94bd-128">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="e94bd-129">此選項不能與任何其他選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="e94bd-129">This option cannot be used in combination with any other option.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e94bd-130">頁首</span><span class="sxs-lookup"><span data-stu-id="e94bd-130">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="e94bd-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e94bd-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e94bd-132">參考</span><span class="sxs-lookup"><span data-stu-id="e94bd-132">Reference</span></span>

[<span data-ttu-id="e94bd-133">Server2003Grbits 類別</span><span class="sxs-lookup"><span data-stu-id="e94bd-133">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="e94bd-134">Server2003 命名空間。</span><span class="sxs-lookup"><span data-stu-id="e94bd-134">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
