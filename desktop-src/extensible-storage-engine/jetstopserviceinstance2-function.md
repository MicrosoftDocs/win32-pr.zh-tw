---
description: 深入瞭解： JetStopServiceInstance2 函數
title: JetStopServiceInstance2 函式
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690816"
---
# <a name="jetstopserviceinstance2-function"></a><span data-ttu-id="6df90-103">JetStopServiceInstance2 函式</span><span class="sxs-lookup"><span data-stu-id="6df90-103">JetStopServiceInstance2 Function</span></span>


<span data-ttu-id="6df90-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6df90-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="6df90-105">**JetStopServiceInstance2** 函式會在暫停之前準備實例，並在繼續之後準備實例。</span><span class="sxs-lookup"><span data-stu-id="6df90-105">The **JetStopServiceInstance2** function prepares an instance prior to Suspend, and prepares an instance after Resume.</span></span> <span data-ttu-id="6df90-106">暫止和繼續是 Windows Store 應用程式生命週期模型的執行狀態。</span><span class="sxs-lookup"><span data-stu-id="6df90-106">Suspend and Resume are execution states of the Windows Store App lifecycle model.</span></span>

<span data-ttu-id="6df90-107">**JetStopServiceInstance2** 函式是在 Windows 8 引進。</span><span class="sxs-lookup"><span data-stu-id="6df90-107">The **JetStopServiceInstance2** function was introduced in Windows 8.</span></span>

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a><span data-ttu-id="6df90-108">參數</span><span class="sxs-lookup"><span data-stu-id="6df90-108">Parameters</span></span>

<span data-ttu-id="6df90-109">*實例*</span><span class="sxs-lookup"><span data-stu-id="6df90-109">*instance*</span></span>

<span data-ttu-id="6df90-110">目標實例。</span><span class="sxs-lookup"><span data-stu-id="6df90-110">The target instance.</span></span> <span data-ttu-id="6df90-111">**JET_INSTANCE** 資料類型是要用於呼叫 JET API 之資料庫實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6df90-111">The **JET_INSTANCE** data type is a handle to the instance of the database to use for a call to the JET API.</span></span> <span data-ttu-id="6df90-112">當您藉由呼叫 [JetCreateInstance](./jetcreateinstance-function.md)、 [JetCreateInstance2](./jetcreateinstance2-function.md)、 [JetInit](./jetinit-function.md)或 [JetInit2](./jetinit2-function.md) 函式來建立資料庫的實例時，就會取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="6df90-112">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="6df90-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6df90-113">*grbit*</span></span>

<span data-ttu-id="6df90-114">位群組，指定下表中列出和定義的一或多個值。</span><span class="sxs-lookup"><span data-stu-id="6df90-114">A group of bits that specifies one or more of the values listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6df90-115">值</span><span class="sxs-lookup"><span data-stu-id="6df90-115">Value</span></span></p></th>
<th><p><span data-ttu-id="6df90-116">描述</span><span class="sxs-lookup"><span data-stu-id="6df90-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6df90-117">JET_bitStopServiceAll</span><span class="sxs-lookup"><span data-stu-id="6df90-117">JET_bitStopServiceAll</span></span></p></td>
<td><p><span data-ttu-id="6df90-118">針對指定的實例停止所有可延伸的儲存引擎 (ESE) 服務。</span><span class="sxs-lookup"><span data-stu-id="6df90-118">Stops all Extensible Storage Engine (ESE) services for the specified instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df90-119">JET_bitStopServiceBackgroundUserTasks</span><span class="sxs-lookup"><span data-stu-id="6df90-119">JET_bitStopServiceBackgroundUserTasks</span></span></p></td>
<td><p><span data-ttu-id="6df90-120">停止可重新開機的用戶端指定的背景維護工作 (B + 樹狀重組，例如) 。</span><span class="sxs-lookup"><span data-stu-id="6df90-120">Stops restartable client-specified background maintenance tasks (B+ Tree Defrag, for example).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df90-121">JET_bitStopServiceQuiesceCaches</span><span class="sxs-lookup"><span data-stu-id="6df90-121">JET_bitStopServiceQuiesceCaches</span></span></p></td>
<td><p><span data-ttu-id="6df90-122">將所有中途快取 Quiesces 至磁片。</span><span class="sxs-lookup"><span data-stu-id="6df90-122">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="6df90-123">這個值是非同步，而且可以取消。</span><span class="sxs-lookup"><span data-stu-id="6df90-123">This value is asynchronous and can be canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df90-124">JET_bitStopServiceResume</span><span class="sxs-lookup"><span data-stu-id="6df90-124">JET_bitStopServiceResume</span></span></p></td>
<td><p><span data-ttu-id="6df90-125">繼續先前發行的 StopService 作業;也就是說，它會重新開機服務。</span><span class="sxs-lookup"><span data-stu-id="6df90-125">Resumes previously issued StopService operations; that is, it restarts the service.</span></span> <span data-ttu-id="6df90-126">這個值可以與 <em>grbits</em> 參數結合以繼續特定服務，或使用 JET_bitStopServiceAll 繼續所有先前停止的服務。</span><span class="sxs-lookup"><span data-stu-id="6df90-126">This value can be combined with the <em>grbits</em> parameter to resume specific services, or with JET_bitStopServiceAll to Resume all previously stopped services.</span></span> <span data-ttu-id="6df90-127">此位只能用來繼續 StopServiceBackgroundUserTasks 和 JET_bitStopServiceQuiesceCaches。</span><span class="sxs-lookup"><span data-stu-id="6df90-127">This bit can only be used to resume StopServiceBackgroundUserTasks and JET_bitStopServiceQuiesceCaches.</span></span> <span data-ttu-id="6df90-128">如果您先前已使用 JET_bitStopServiceAll 呼叫，則嘗試使用 JET_bitStopServiceResume 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="6df90-128">If you previously called with JET_bitStopServiceAll, an attempt to use JET_bitStopServiceResume will fail.</span></span> <span data-ttu-id="6df90-129">如果未呼叫第二個恢復步驟，應用程式將會降低效能。</span><span class="sxs-lookup"><span data-stu-id="6df90-129">If the second resume step does not get called, the application will have degraded performance.</span></span> <span data-ttu-id="6df90-130">在這種情況下，檢查點會保持為零。</span><span class="sxs-lookup"><span data-stu-id="6df90-130">In this situation the checkpoint is kept at zero.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6df90-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="6df90-131">Return value</span></span>

<span data-ttu-id="6df90-132">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="6df90-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="6df90-133">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="6df90-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6df90-134">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6df90-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="6df90-135">Description</span><span class="sxs-lookup"><span data-stu-id="6df90-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6df90-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6df90-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6df90-137">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="6df90-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="6df90-138">備註</span><span class="sxs-lookup"><span data-stu-id="6df90-138">Remarks</span></span>

<span data-ttu-id="6df90-139">這項功能可讓 JET 應用程式將資料庫快取移到乾淨或近乎乾淨的狀態 (使用作業系統 i/o 閒置) ，如此一來，如果要終止應用程式，復原就會很快速。</span><span class="sxs-lookup"><span data-stu-id="6df90-139">This function allows a JET application to move the database cache to a clean or nearly clean state (with the operating system I/O idle), such that if the application were to be terminated, recovery would be quick.</span></span> <span data-ttu-id="6df90-140">這種方法優於透過呼叫 [JetTerm](./jetterm-function.md) 或 [JetDetachDatabase](./jetdetachdatabase-function.md) 函式來終止 JET，因此在較常見的案例中，應用程式只是 unsuspended，稍後應用程式會有完整的快取，而且已準備好繼續進行。</span><span class="sxs-lookup"><span data-stu-id="6df90-140">This approach is preferred over terminating JET by calling the [JetTerm](./jetterm-function.md) or [JetDetachDatabase](./jetdetachdatabase-function.md) functions, so that in the more common scenario, the application is just unsuspended, and later the application has the whole cache and is ready to go as soon as possible.</span></span>

<span data-ttu-id="6df90-141">如果此函式成功，它會準備資料庫快取以供即將暫停。</span><span class="sxs-lookup"><span data-stu-id="6df90-141">If this function succeeds, it prepares the database cache for an imminent suspension.</span></span> <span data-ttu-id="6df90-142">此函式會將工作排入背景工作者執行緒，並立即返回呼叫端。</span><span class="sxs-lookup"><span data-stu-id="6df90-142">This function queues work to a background worker thread and returns to the caller immediately.</span></span> <span data-ttu-id="6df90-143">應該根據 PLM VisibilityNotice 來呼叫函式，而不是從應用程式的暫止事件處理常式呼叫，以確保 JET 有時間在 PLM 暫停或終止進程之前排清中途緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6df90-143">The function should be called based on the PLM VisibilityNotice as opposed to calling from the application's suspension event handler to ensure that JET has time to flush dirty buffers before PLM suspends/terminates the process.</span></span> <span data-ttu-id="6df90-144">就內部而言，JET 會在設定變更時立即觸發檢查點維護 (檢查點更新或這個新的靜止快取位) 。</span><span class="sxs-lookup"><span data-stu-id="6df90-144">Internally, JET triggers an immediate dispatch of checkpoint maintenance upon configuration change (either checkpoint update or this new quiesce caches bit).</span></span> <span data-ttu-id="6df90-145">如需 VisibilityNotice 事件的詳細資訊，請參閱 [VisibilityChangedEventArgs 類別](/uwp/api/windows.ui.core.visibilitychangedeventargs)。</span><span class="sxs-lookup"><span data-stu-id="6df90-145">For more information about VisibilityNotice events, see [VisibilityChangedEventArgs class](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span></span>

<span data-ttu-id="6df90-146">您必須呼叫此函式兩次。</span><span class="sxs-lookup"><span data-stu-id="6df90-146">This function must be called twice.</span></span> <span data-ttu-id="6df90-147">它會在應用程式從作業系統收到暫停通知之後，但在應用程式暫停之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="6df90-147">It is called after the application receives the suspension notice from the operating system, but before the application has been suspended.</span></span> <span data-ttu-id="6df90-148">然後在作業系統繼續應用程式之後，再次呼叫它。</span><span class="sxs-lookup"><span data-stu-id="6df90-148">Then it is called again after the operating system resumes the application.</span></span> <span data-ttu-id="6df90-149">例如：</span><span class="sxs-lookup"><span data-stu-id="6df90-149">For example:</span></span>

<span data-ttu-id="6df90-150">當呼叫以暫停： JET_ERR JET_API JetStopServiceInstance2 ( 實例，JET_bitStopServiceQuiesceCaches) ;</span><span class="sxs-lookup"><span data-stu-id="6df90-150">When called to Suspend: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches);</span></span>

<span data-ttu-id="6df90-151">繼續時： JET_ERR JET_API JetStopServiceInstance2 ( 實例，JET_bitStopServiceQuiesceCaches |JET_bitStopServiceResume ) ;</span><span class="sxs-lookup"><span data-stu-id="6df90-151">When Resumed: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches|JET_bitStopServiceResume );</span></span>

#### <a name="requirements"></a><span data-ttu-id="6df90-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="6df90-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6df90-153"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="6df90-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6df90-154">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="6df90-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df90-155"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="6df90-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6df90-156">需要 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="6df90-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df90-157"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="6df90-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6df90-158">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="6df90-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6df90-159"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="6df90-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6df90-160">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="6df90-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6df90-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6df90-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6df90-162">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="6df90-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6df90-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6df90-163">See also</span></span>

[<span data-ttu-id="6df90-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6df90-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6df90-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="6df90-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="6df90-166">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="6df90-166">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="6df90-167">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="6df90-167">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="6df90-168">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="6df90-168">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="6df90-169">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="6df90-169">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="6df90-170">JetResetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="6df90-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="6df90-171">JetRollback</span><span class="sxs-lookup"><span data-stu-id="6df90-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="6df90-172">JetTerm</span><span class="sxs-lookup"><span data-stu-id="6df90-172">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="6df90-173">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="6df90-173">JetTerm2</span></span>](./jetterm2-function.md)
