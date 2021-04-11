---
description: 深入瞭解： JET_SESID
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 542802c806bbea55aafb4fc1a0241a92b2842878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847836"
---
# <a name="jet_sesid"></a><span data-ttu-id="9dd01-103">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9dd01-103">JET_SESID</span></span>


<span data-ttu-id="9dd01-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9dd01-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_sesid"></a><span data-ttu-id="9dd01-105">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9dd01-105">JET_SESID</span></span>

<span data-ttu-id="9dd01-106">**JET_SESID** 資料類型包含要用於呼叫 JET API 的會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="9dd01-106">The **JET_SESID** data type contains a handle to the session to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a><span data-ttu-id="9dd01-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="9dd01-107">Data Types</span></span>

<span data-ttu-id="9dd01-108">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9dd01-108">JET_SESID</span></span>

<span data-ttu-id="9dd01-109">**Null** 或 [JET_sesidNil](./invalid-handle-constants.md)可以用來表示不正確會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="9dd01-109">Either **NULL** or [JET_sesidNil](./invalid-handle-constants.md) can be used to indicate an invalid session handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="9dd01-110">備註</span><span class="sxs-lookup"><span data-stu-id="9dd01-110">Remarks</span></span>

<span data-ttu-id="9dd01-111">會話是 database engine 的交易內容。</span><span class="sxs-lookup"><span data-stu-id="9dd01-111">A session is the transaction context of the database engine.</span></span> <span data-ttu-id="9dd01-112">您可以使用它來開始、認可或中止交易，這些交易會影響此會話或其他會話所進行之變更的可見度和持久性。</span><span class="sxs-lookup"><span data-stu-id="9dd01-112">It can be used to begin, commit, or abort transactions that affect the visibility and durability of changes that are made by this or other sessions.</span></span>

<span data-ttu-id="9dd01-113">您可以使用 [JetBeginTransaction](./jetbegintransaction-function.md)來啟動交易。</span><span class="sxs-lookup"><span data-stu-id="9dd01-113">A transaction can be started using [JetBeginTransaction](./jetbegintransaction-function.md).</span></span> <span data-ttu-id="9dd01-114">您可以使用 [JetBeginSession](./jetbeginsession-function.md)來建立會話。</span><span class="sxs-lookup"><span data-stu-id="9dd01-114">A session may be created using [JetBeginSession](./jetbeginsession-function.md).</span></span> <span data-ttu-id="9dd01-115">可以在任何時間建立的會話數目上限是由 [JET_paramMaxSessions](./resource-parameters.md)所控制，可以透過 [JetSetSystemParameter](./jetsetsystemparameter-function.md)來設定。</span><span class="sxs-lookup"><span data-stu-id="9dd01-115">The maximum number of sessions that can be created at any one time is controlled by [JET_paramMaxSessions](./resource-parameters.md), which can be configured by means of [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="9dd01-116">會話是由呼叫 [JetEndSession](./jetendsession-function.md) 明確結束，或呼叫 [JetTerm](./jetterm-function.md)以隱含方式結束。</span><span class="sxs-lookup"><span data-stu-id="9dd01-116">A session is explicitly ended by a call to [JetEndSession](./jetendsession-function.md) or implicitly ended by a call to [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="9dd01-117">每個會話一次只能供一個執行緒使用。</span><span class="sxs-lookup"><span data-stu-id="9dd01-117">Each session can only be used by one thread at a time.</span></span> <span data-ttu-id="9dd01-118">此外，引擎的預設行為是在呼叫 [JetBeginTransaction](./jetbegintransaction-function.md) 的第一次呼叫時，將會話限制在相同的執行緒上，直到發出 [JetCommitTransaction](./jetcommittransaction-function.md) 或 [JetRollback](./jetrollback-function.md) 的相符呼叫為止。</span><span class="sxs-lookup"><span data-stu-id="9dd01-118">In addition, the default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to [JetBeginTransaction](./jetbegintransaction-function.md) is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="9dd01-119">您可以使用 [JetSetSessionCoNtext](./jetsetsessioncontext-function.md) 和 [JetResetSessionCoNtext](./jetresetsessioncontext-function.md)設定自訂會話內容，來變更此行為，以移除第二個限制。</span><span class="sxs-lookup"><span data-stu-id="9dd01-119">This behavior can be changed to remove this second restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="9dd01-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9dd01-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9dd01-121"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="9dd01-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9dd01-122">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="9dd01-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd01-123"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="9dd01-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9dd01-124">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="9dd01-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd01-125"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="9dd01-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9dd01-126">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="9dd01-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9dd01-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9dd01-127">See Also</span></span>

[<span data-ttu-id="9dd01-128">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="9dd01-128">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="9dd01-129">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="9dd01-129">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="9dd01-130">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="9dd01-130">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="9dd01-131">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="9dd01-131">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="9dd01-132">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="9dd01-132">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="9dd01-133">JetResetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="9dd01-133">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="9dd01-134">JetRollback</span><span class="sxs-lookup"><span data-stu-id="9dd01-134">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="9dd01-135">JetSetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="9dd01-135">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="9dd01-136">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="9dd01-136">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="9dd01-137">JetTerm</span><span class="sxs-lookup"><span data-stu-id="9dd01-137">JetTerm</span></span>](./jetterm-function.md)
