---
description: 深入瞭解： JET_ERRCAT 列舉
title: 'JET_ERRCAT 列舉的 (Windows8) '
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193052"
---
# <a name="jet_errcat-enumeration"></a><span data-ttu-id="07938-103">JET_ERRCAT 列舉</span><span class="sxs-lookup"><span data-stu-id="07938-103">JET_ERRCAT enumeration</span></span>

<span data-ttu-id="07938-104">錯誤類別。</span><span class="sxs-lookup"><span data-stu-id="07938-104">The error category.</span></span> <span data-ttu-id="07938-105">階層如下： JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//錯誤的 IO 問題，可能或可能不是暫時性問題。</span><span class="sxs-lookup"><span data-stu-id="07938-105">The hierarchy is as follows: JET_errcatError | |-- JET_errcatOperation | |-- JET_errcatFatal | |-- JET_errcatIO // bad IO issues, may or may not be transient.</span></span> <span data-ttu-id="07938-106">| |--JET_errcatResource | |--JET_errcatMemory//記憶體不足 (所有變體) | |--JET_errcatQuota | |--JET_errcatDisk//磁碟空間 (所有變體) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//通常是由使用者承載錯誤處理所造成 | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete</span><span class="sxs-lookup"><span data-stu-id="07938-106">| |-- JET_errcatResource | |-- JET_errcatMemory // out of memory (all variants) | |-- JET_errcatQuota | |-- JET_errcatDisk // out of disk space (all variants) |-- JET_errcatData | |-- JET_errcatCorruption | |-- JET_errcatInconsistent // typically caused by user Mishandling | |-- JET_errcatFragmentation |-- JET_errcatApi |-- JET_errcatUsage |-- JET_errcatState |-- JET_errcatObsolete</span></span>

<span data-ttu-id="07938-107">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="07938-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="07938-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="07938-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="07938-109">語法</span><span class="sxs-lookup"><span data-stu-id="07938-109">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a><span data-ttu-id="07938-110">成員</span><span class="sxs-lookup"><span data-stu-id="07938-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="07938-111">成員名稱</span><span class="sxs-lookup"><span data-stu-id="07938-111">Member name</span></span></th>
<th><span data-ttu-id="07938-112">說明</span><span class="sxs-lookup"><span data-stu-id="07938-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="07938-113">Unknown</span><span class="sxs-lookup"><span data-stu-id="07938-113">Unknown</span></span></td>
<td><span data-ttu-id="07938-114">未知的類別。</span><span class="sxs-lookup"><span data-stu-id="07938-114">Unknown category.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="07938-115">錯誤</span><span class="sxs-lookup"><span data-stu-id="07938-115">Error</span></span></td>
<td><span data-ttu-id="07938-116">泛型類別目錄。</span><span class="sxs-lookup"><span data-stu-id="07938-116">A generic category.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="07938-117">作業</span><span class="sxs-lookup"><span data-stu-id="07938-117">Operation</span></span></td>
<td><span data-ttu-id="07938-118">通常由於無法控制條件而可能發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="07938-118">Errors that can usually happen any time due to uncontrollable conditions.</span></span> <span data-ttu-id="07938-119">通常是暫時性的，但並非一律如此。</span><span class="sxs-lookup"><span data-stu-id="07938-119">Frequently temporary, but not always.</span></span> <span data-ttu-id="07938-120">復原：可能會重試，或最後通知操作員。</span><span class="sxs-lookup"><span data-stu-id="07938-120">Recovery: Probably retry, or eventually inform the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="07938-121">嚴重</span><span class="sxs-lookup"><span data-stu-id="07938-121">Fatal</span></span></td>
<td><span data-ttu-id="07938-122">只有當 ESE 遇到錯誤狀況時，才會發生這種排序錯誤，因此我們無法在安全的 (中繼續，通常是交易式) 方式，而不是損毀的資料，我們會擲回這個類別的錯誤。</span><span class="sxs-lookup"><span data-stu-id="07938-122">This sort error happens only when ESE encounters an error condition so grave, that we can not continue on in a safe (often transactional) way, and rather than corrupt data we throw errors of this category.</span></span> <span data-ttu-id="07938-123">Recovery：重新開機實例或進程。</span><span class="sxs-lookup"><span data-stu-id="07938-123">Recovery: Restart the instance or process.</span></span> <span data-ttu-id="07938-124">如果問題持續發生，請通知操作員。</span><span class="sxs-lookup"><span data-stu-id="07938-124">If the problem persists inform the operator.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="07938-125">IO</span><span class="sxs-lookup"><span data-stu-id="07938-125">IO</span></span></td>
<td><span data-ttu-id="07938-126">O 錯誤來自 OS，而且不在 ESE 的控制之下，這類錯誤可能是暫時性的，可能不是暫時性的。</span><span class="sxs-lookup"><span data-stu-id="07938-126">O errors come from the OS, and are out of ESE's control, this sort of error is possibly temporary, possibly not.</span></span> <span data-ttu-id="07938-127">復原：重試。</span><span class="sxs-lookup"><span data-stu-id="07938-127">Recovery: Retry.</span></span> <span data-ttu-id="07938-128">如果未解決，請詢問操作員有關磁片的問題。</span><span class="sxs-lookup"><span data-stu-id="07938-128">If not resolved, ask operator about disk issue.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="07938-129">資源</span><span class="sxs-lookup"><span data-stu-id="07938-129">Resource</span></span></td>
<td><span data-ttu-id="07938-130">這是表示許多可能的資源不足狀況之一的類別。</span><span class="sxs-lookup"><span data-stu-id="07938-130">This is a category that indicates one of many potential out-of-resource conditions.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="07938-131">記憶體</span><span class="sxs-lookup"><span data-stu-id="07938-131">Memory</span></span></td>
<td><span data-ttu-id="07938-132">傳統記憶體不足的狀況。</span><span class="sxs-lookup"><span data-stu-id="07938-132">Classic out of memory condition.</span></span> <span data-ttu-id="07938-133">復原：等候一段時間，然後再試一次、釋放記憶體或結束。</span><span class="sxs-lookup"><span data-stu-id="07938-133">Recovery: Wait a while and retry, free up memory, or quit.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="07938-134">Quota</span><span class="sxs-lookup"><span data-stu-id="07938-134">Quota</span></span></td>
<td><span data-ttu-id="07938-135">某些 &quot; 特殊 &quot; 資源會在特定大小的集區中，讓您更輕鬆地偵測這些資源的洩漏。</span><span class="sxs-lookup"><span data-stu-id="07938-135">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span> <span data-ttu-id="07938-136">復原：可能需要一些次要的程式碼變更。</span><span class="sxs-lookup"><span data-stu-id="07938-136">Recovery: Might require some minor code changes.</span></span> <span data-ttu-id="07938-137">在這些情況下，您的應用程式應該要有僅限 debug 的動作（例如判斷提示），才能在開發期間偵測它們。</span><span class="sxs-lookup"><span data-stu-id="07938-137">Your application should have a debug only action, such as an Assert, on these conditions in order to detect them during development.</span></span> <span data-ttu-id="07938-138">針對零售程式碼，我們建議您將此錯誤視為記憶體類別錯誤，然後重試、釋出記憶體或結束作業。</span><span class="sxs-lookup"><span data-stu-id="07938-138">For retail code, we recommend that you treat this error like the Memory category error and either retry, free up memory, or quit the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="07938-139">磁碟</span><span class="sxs-lookup"><span data-stu-id="07938-139">Disk</span></span></td>
<td><span data-ttu-id="07938-140">磁片不足的情況。</span><span class="sxs-lookup"><span data-stu-id="07938-140">Out of disk conditions.</span></span> <span data-ttu-id="07938-141">復原：稍後可以在希望有更多可用空間的情況下重試，或要求操作員釋放一些磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="07938-141">Recovery: Can retry later in the hope more space is available, or ask the operator to free some disk space.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="07938-142">資料</span><span class="sxs-lookup"><span data-stu-id="07938-142">Data</span></span></td>
<td><span data-ttu-id="07938-143">資料相關的錯誤。</span><span class="sxs-lookup"><span data-stu-id="07938-143">A data-related error.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="07938-144">腐敗</span><span class="sxs-lookup"><span data-stu-id="07938-144">Corruption</span></span></td>
<td><span data-ttu-id="07938-145">我的硬碟 ate 我的工作空間。</span><span class="sxs-lookup"><span data-stu-id="07938-145">My hard drive ate my homework.</span></span> <span data-ttu-id="07938-146">傳統的損毀問題，經常永久沒有矯正措施。</span><span class="sxs-lookup"><span data-stu-id="07938-146">Classic corruption issues, frequently permanent without corrective action.</span></span> <span data-ttu-id="07938-147">復原：從備份還原，可能是 ese 公用程式修復作業 (只會 salvages 剩下/損及) 的資料。此外，在復原 (JetInit) 可能會藉由允許資料遺失來執行修復。</span><span class="sxs-lookup"><span data-stu-id="07938-147">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy) .Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="07938-148">不一致</span><span class="sxs-lookup"><span data-stu-id="07938-148">Inconsistent</span></span></td>
<td><span data-ttu-id="07938-149">這類似于損毀，因為資料庫和/或記錄檔處於不一致的狀態，且彼此 unreconcilable。</span><span class="sxs-lookup"><span data-stu-id="07938-149">This is similar to Corruption in that the database and/or log files are in a state that is inconsistent and unreconcilable with each other.</span></span> <span data-ttu-id="07938-150">這通常是由應用程式/系統管理員承載錯誤處理所造成。</span><span class="sxs-lookup"><span data-stu-id="07938-150">Often this is caused by application/administrator mishandling.</span></span> <span data-ttu-id="07938-151">復原：從備份還原，可能是 ese 公用程式修復作業 (只會 salvages 剩下/損及) 的資料。</span><span class="sxs-lookup"><span data-stu-id="07938-151">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy).</span></span> <span data-ttu-id="07938-152">此外，在復原 (JetInit) 可能會藉由允許資料遺失來執行修復。</span><span class="sxs-lookup"><span data-stu-id="07938-152">Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="07938-153">分割</span><span class="sxs-lookup"><span data-stu-id="07938-153">Fragmentation</span></span></td>
<td><span data-ttu-id="07938-154">這是一些持續性內部資源已用盡的錯誤類別。復原：針對資料庫錯誤，離線磁碟重組會修正問題，記錄檔會 _先_ 將所有附加的資料庫復原到正常關機，然後再刪除所有記錄檔和檢查點。</span><span class="sxs-lookup"><span data-stu-id="07938-154">This is a class of errors where some persisted internal resource ran out. Recovery: For database errors, offline defragmentation will rectify the problem, for the log files _first_ recover all attached databases to a clean shutdown, and then delete all the log files and checkpoint.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="07938-155">Api</span><span class="sxs-lookup"><span data-stu-id="07938-155">Api</span></span></td>
<td><span data-ttu-id="07938-156">使用方式和狀態的容器。</span><span class="sxs-lookup"><span data-stu-id="07938-156">A container for Usage and State.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="07938-157">使用方式</span><span class="sxs-lookup"><span data-stu-id="07938-157">Usage</span></span></td>
<td><span data-ttu-id="07938-158">傳統使用方式錯誤，這表示用戶端程式代碼未傳遞正確的引數給 JET API。</span><span class="sxs-lookup"><span data-stu-id="07938-158">Classic usage error, this means the client code did not pass correct arguments to the JET API.</span></span> <span data-ttu-id="07938-159">此錯誤可能不會在重試後消失。</span><span class="sxs-lookup"><span data-stu-id="07938-159">This error will likely not go away with retry.</span></span> <span data-ttu-id="07938-160">復原：一般而言，用戶端程式代碼應該判斷提示 () 此類別的錯誤不會傳回，因此在開發期間可能會發生問題。</span><span class="sxs-lookup"><span data-stu-id="07938-160">Recovery: Generally speaking client code should Assert() this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="07938-161">在零售版中，應用程式可能會有極少的選項，但是將問題傳回給操作員。</span><span class="sxs-lookup"><span data-stu-id="07938-161">In retail, the app will probably have little option but to return the issue up to the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="07938-162">狀態</span><span class="sxs-lookup"><span data-stu-id="07938-162">State</span></span></td>
<td><span data-ttu-id="07938-163">這是 API 可能傳回的不同信號的分類，可描述資料庫的狀態，傳統案例是 JET_errRecordNotFound 當找不到您要求的記錄時，可由 JetSeek () 傳回。</span><span class="sxs-lookup"><span data-stu-id="07938-163">This is the classification for different signals the API could return describe the state of the database, a classic case is JET_errRecordNotFound which can be returned by JetSeek() when the record you asked for was not found.</span></span> <span data-ttu-id="07938-164">復原：與 API 很大的差異。</span><span class="sxs-lookup"><span data-stu-id="07938-164">Recovery: Not really relevant, depends greatly on the API.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="07938-165">已淘汰</span><span class="sxs-lookup"><span data-stu-id="07938-165">Obsolete</span></span></td>
<td><span data-ttu-id="07938-166">錯誤會被辨識為有效的錯誤，但此版本的 API 預期不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="07938-166">The error is recognized as a valid error, but is not expected to be returned by this version of the API.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="07938-167">最大值</span><span class="sxs-lookup"><span data-stu-id="07938-167">Max</span></span></td>
<td><span data-ttu-id="07938-168">列舉的最大值。</span><span class="sxs-lookup"><span data-stu-id="07938-168">The maximum value for the enum.</span></span> <span data-ttu-id="07938-169">這不應該使用。</span><span class="sxs-lookup"><span data-stu-id="07938-169">This should not be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="07938-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07938-170">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="07938-171">參考</span><span class="sxs-lookup"><span data-stu-id="07938-171">Reference</span></span>

[<span data-ttu-id="07938-172">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="07938-172">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
