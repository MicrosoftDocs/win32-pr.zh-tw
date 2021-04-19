---
description: 深入瞭解： JET_ERRCAT
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: fe3f5ebad9f0838d089beb83b20b818b7faa4001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981607"
---
# <a name="jet_errcat"></a><span data-ttu-id="49e56-103">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="49e56-103">JET_ERRCAT</span></span>


<span data-ttu-id="49e56-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="49e56-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errcat"></a><span data-ttu-id="49e56-105">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="49e56-105">JET_ERRCAT</span></span>

<span data-ttu-id="49e56-106">**JET_ERRCAT** 的常數群組描述較高層級的分類或錯誤類別。</span><span class="sxs-lookup"><span data-stu-id="49e56-106">The **JET_ERRCAT** group of constants describes higher-level classifications or categories of errors.</span></span> <span data-ttu-id="49e56-107">這個常數群組可讓應用程式定義錯誤分類的預設處理方式，而不是個別處理每個錯誤案例。</span><span class="sxs-lookup"><span data-stu-id="49e56-107">This group of constants enables applications to define default treatment for a classification of errors, rather than handling each error case individually.</span></span> <span data-ttu-id="49e56-108">它也可確保應用程式不需要處理現有分類中包含的新錯誤條件。</span><span class="sxs-lookup"><span data-stu-id="49e56-108">It also ensures that the application does not have to handle new error conditions that are included in existing classifications.</span></span>

<span data-ttu-id="49e56-109">注意：本檔是以可延伸儲存引擎的初步發行版本為基礎。</span><span class="sxs-lookup"><span data-stu-id="49e56-109">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="49e56-110">此資訊可能隨時變更。</span><span class="sxs-lookup"><span data-stu-id="49e56-110">This information is subject to change.</span></span>

<span data-ttu-id="49e56-111">**JET_ERRCAT** 的常數會排列在特定的條件和 subconditions 階層中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="49e56-111">The **JET_ERRCAT** constants are arranged in a specific hierarchy of conditions and subconditions, as follows:</span></span>

<span data-ttu-id="49e56-112">|---錯誤 |---作業 (al) | |---嚴重 | |---IO | |---資源 | |---記憶體 | |---配額 | |---磁片 | |---資料 | |---損毀 | |---不一致 | |---的片段 | |---Api |---使用量 |---狀態</span><span class="sxs-lookup"><span data-stu-id="49e56-112">|--- Error |--- Operation(al) | |--- Fatal | |--- IO | |--- Resource | |--- Memory | |--- Quota | |--- Disk | |--- Data | |--- Corruption | |--- Inconsistent | |--- Fragmentation | |--- Api |--- Usage |--- State</span></span>

<span data-ttu-id="49e56-113">下表列出 **JET_ERRCAT** 常數，並提供適用的描述和修復資訊。</span><span class="sxs-lookup"><span data-stu-id="49e56-113">The following table lists the **JET_ERRCAT** constants and provides a description and recovery information, as applicable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49e56-114">常數/值</span><span class="sxs-lookup"><span data-stu-id="49e56-114">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="49e56-115">Description</span><span class="sxs-lookup"><span data-stu-id="49e56-115">Description</span></span></p></th>
<th><p><span data-ttu-id="49e56-116">復原</span><span class="sxs-lookup"><span data-stu-id="49e56-116">Recovery</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49e56-117">JET_errcatUnknown 0</span><span class="sxs-lookup"><span data-stu-id="49e56-117">JET_errcatUnknown 0</span></span></p></td>
<td><p><span data-ttu-id="49e56-118">不正確錯誤類別。</span><span class="sxs-lookup"><span data-stu-id="49e56-118">An invalid error category.</span></span></p></td>
<td><p><span data-ttu-id="49e56-119">N/A。</span><span class="sxs-lookup"><span data-stu-id="49e56-119">N/A.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e56-120">JET_errcatError 1</span><span class="sxs-lookup"><span data-stu-id="49e56-120">JET_errcatError 1</span></span></p></td>
<td><p><span data-ttu-id="49e56-121">最上層類別 (此類別) 不會有任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="49e56-121">The top level category (no errors should be of this class).</span></span></p></td>
<td><p><span data-ttu-id="49e56-122">請參閱特定的錯誤常數。</span><span class="sxs-lookup"><span data-stu-id="49e56-122">See the specific error constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e56-123">JET_errcatOperation 2</span><span class="sxs-lookup"><span data-stu-id="49e56-123">JET_errcatOperation 2</span></span></p></td>
<td><p><span data-ttu-id="49e56-124">代表可能因為無法控制條件而發生的錯誤，而且通常是暫時性的。</span><span class="sxs-lookup"><span data-stu-id="49e56-124">Represents errors that can happen at any time due to uncontrollable conditions and are often temporary.</span></span> <span data-ttu-id="49e56-125">如果有指定，請參閱子類別。</span><span class="sxs-lookup"><span data-stu-id="49e56-125">See subcategories if specified.</span></span></p></td>
<td><p><span data-ttu-id="49e56-126">請重試一次，如果錯誤持續發生，請通知操作員。</span><span class="sxs-lookup"><span data-stu-id="49e56-126">Retry and if the error continues, inform the operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e56-127">JET_errcatFatal 3</span><span class="sxs-lookup"><span data-stu-id="49e56-127">JET_errcatFatal 3</span></span></p></td>
<td><p><span data-ttu-id="49e56-128">表示發生嚴重錯誤，當發生時，會產生一個風險，指出 ESE 無法在安全的 (（通常是交易式) 方式）中繼續，而且資料可能會損毀。</span><span class="sxs-lookup"><span data-stu-id="49e56-128">Represents fatal errors that, when they occur, create a risk that ESE cannot continue in a safe (often transactional) way, and data may become corrupted.</span></span></p></td>
<td><p><span data-ttu-id="49e56-129">重新開機實例或進程。</span><span class="sxs-lookup"><span data-stu-id="49e56-129">Restart the instance or process.</span></span> <span data-ttu-id="49e56-130">如果問題持續發生，請通知操作員。</span><span class="sxs-lookup"><span data-stu-id="49e56-130">If the problem persists, inform the operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e56-131">JET_errcatIO 4</span><span class="sxs-lookup"><span data-stu-id="49e56-131">JET_errcatIO 4</span></span></p></td>
<td><p><span data-ttu-id="49e56-132">代表來自作業系統的 IO 錯誤，而不是 ESE 的控制權。</span><span class="sxs-lookup"><span data-stu-id="49e56-132">Represents IO errors, which come from the operating system, and are out of ESE's control.</span></span> <span data-ttu-id="49e56-133">這種類型的錯誤可能是暫時性的。</span><span class="sxs-lookup"><span data-stu-id="49e56-133">This type of error may be temporary.</span></span></p></td>
<td><p><span data-ttu-id="49e56-134">請重試一次，如果錯誤持續發生，請要求操作員檢查磁片。</span><span class="sxs-lookup"><span data-stu-id="49e56-134">Retry, and if the error continues, ask the operator to check the disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e56-135">JET_errcatResource 5</span><span class="sxs-lookup"><span data-stu-id="49e56-135">JET_errcatResource 5</span></span></p></td>
<td><p><span data-ttu-id="49e56-136">表示與缺乏資源條件相關的錯誤類別。</span><span class="sxs-lookup"><span data-stu-id="49e56-136">Represents a category of errors related to lack of resource conditions.</span></span></p></td>
<td><p><span data-ttu-id="49e56-137">請參閱子類別。</span><span class="sxs-lookup"><span data-stu-id="49e56-137">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e56-138">JET_errcatMemory 6</span><span class="sxs-lookup"><span data-stu-id="49e56-138">JET_errcatMemory 6</span></span></p></td>
<td><p><span data-ttu-id="49e56-139">代表記憶體不足所造成的錯誤。</span><span class="sxs-lookup"><span data-stu-id="49e56-139">Represents an error caused by lack of memory.</span></span></p></td>
<td><p><span data-ttu-id="49e56-140">請在一段時間後重試，釋出記憶體或結束。</span><span class="sxs-lookup"><span data-stu-id="49e56-140">Retry after a period of time, free up memory, or quit.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e56-141">JET_errcatQuota 7</span><span class="sxs-lookup"><span data-stu-id="49e56-141">JET_errcatQuota 7</span></span></p></td>
<td><p><span data-ttu-id="49e56-142">某些 &quot; 特殊 &quot; 資源會在特定大小的集區中，讓您更輕鬆地偵測這些資源的洩漏。</span><span class="sxs-lookup"><span data-stu-id="49e56-142">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span></p></td>
<td><p><span data-ttu-id="49e56-143">應用程式應該判斷提示 <strong> () </strong> 在開發期間偵測這些問題。</span><span class="sxs-lookup"><span data-stu-id="49e56-143">The application should <strong>Assert()</strong> to detect these issues during development .</span></span> <span data-ttu-id="49e56-144">不過，在零售程式碼中，應用程式應該將此視為記憶體錯誤。</span><span class="sxs-lookup"><span data-stu-id="49e56-144">However, in retail code, the application should treat this as a memory error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e56-145">JET_errcatDisk 8</span><span class="sxs-lookup"><span data-stu-id="49e56-145">JET_errcatDisk 8</span></span></p></td>
<td><p><span data-ttu-id="49e56-146">代表因磁碟空間不足而造成的錯誤。</span><span class="sxs-lookup"><span data-stu-id="49e56-146">Represents an error caused by lack of disk space.</span></span></p></td>
<td><p><span data-ttu-id="49e56-147">請稍後再試一次，以判斷是否有更多可用的磁碟空間，或要求操作員釋放一些磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="49e56-147">Retry later to determine whether more disk space is available, or ask the operator to free some disk space.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e56-148">JET_errcatData 9</span><span class="sxs-lookup"><span data-stu-id="49e56-148">JET_errcatData 9</span></span></p></td>
<td><p><span data-ttu-id="49e56-149">表示與資料相關之錯誤的最上層類別。</span><span class="sxs-lookup"><span data-stu-id="49e56-149">Represents a top-level category for errors related to data.</span></span></p></td>
<td><p><span data-ttu-id="49e56-150">請參閱子類別。</span><span class="sxs-lookup"><span data-stu-id="49e56-150">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e56-151">JET_errcatCorruption 10</span><span class="sxs-lookup"><span data-stu-id="49e56-151">JET_errcatCorruption 10</span></span></p></td>
<td><p><span data-ttu-id="49e56-152">代表損毀問題，這通常不會有矯正措施的永久問題。</span><span class="sxs-lookup"><span data-stu-id="49e56-152">Represents a corruption issue, which is often permanent without corrective action.</span></span></p></td>
<td><p><span data-ttu-id="49e56-153">使用 ESE 公用程式修復作業從備份還原 (此作業只會還原) 的資料。</span><span class="sxs-lookup"><span data-stu-id="49e56-153">Restore from backup by using the ESE utilities repair operation (this operation restores only the data that is left/lossy).</span></span> <span data-ttu-id="49e56-154">此外，當使用 recovery (JetInit) 方法時，您可以藉由允許資料遺失來執行復原 (如需詳細資訊，請參閱 <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>。</span><span class="sxs-lookup"><span data-stu-id="49e56-154">Also when the recovery(JetInit) method is used, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e56-155">JET_errcatInconsistent 11</span><span class="sxs-lookup"><span data-stu-id="49e56-155">JET_errcatInconsistent 11</span></span></p></td>
<td><p><span data-ttu-id="49e56-156">表示資料庫和/或記錄檔處於不一致且無法進行協調的狀態錯誤。</span><span class="sxs-lookup"><span data-stu-id="49e56-156">Represents an error in which the database and/or log files are in a state that is inconsistent and cannot be reconciled.</span></span> <span data-ttu-id="49e56-157">此錯誤可能是由應用程式/系統管理員承載錯誤處理所造成。</span><span class="sxs-lookup"><span data-stu-id="49e56-157">This error might be caused by application/administrator mishandling.</span></span></p></td>
<td><p><span data-ttu-id="49e56-158">使用 ESE 公用程式修復作業從備份還原，這 (只會還原保持) 的資料。</span><span class="sxs-lookup"><span data-stu-id="49e56-158">Restore from backup by using the ESE utilities repair operation (which only restores the data that is left/lossy).</span></span> <span data-ttu-id="49e56-159">此外，在復原 <strong> (JetInit) </strong> 作業的情況下，您可以藉由允許資料遺失來執行復原 (如需詳細資訊，請參閱 <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>。</span><span class="sxs-lookup"><span data-stu-id="49e56-159">Also in the case of the <strong>recovery(JetInit)</strong> operation, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e56-160">JET_errcatFragmentation 12</span><span class="sxs-lookup"><span data-stu-id="49e56-160">JET_errcatFragmentation 12</span></span></p></td>
<td><p><span data-ttu-id="49e56-161">代表某些持續性內部資源已用盡的錯誤類別。</span><span class="sxs-lookup"><span data-stu-id="49e56-161">Represents a class of errors in which some persisted internal resource ran out.</span></span></p></td>
<td><p><span data-ttu-id="49e56-162">針對資料庫錯誤，離線磁碟重組將會修正此問題。</span><span class="sxs-lookup"><span data-stu-id="49e56-162">For database errors, offline defragmentation will fix the problem.</span></span> <span data-ttu-id="49e56-163">針對記錄檔，先將所有附加的資料庫復原至正常關機，然後刪除所有記錄檔和檢查點。</span><span class="sxs-lookup"><span data-stu-id="49e56-163">For the log files, first recover all attached databases to a clean shutdown, and then delete all the log files and the checkpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e56-164">JET_errcatApi 13</span><span class="sxs-lookup"><span data-stu-id="49e56-164">JET_errcatApi 13</span></span></p></td>
<td><p><span data-ttu-id="49e56-165">請參閱子類別。</span><span class="sxs-lookup"><span data-stu-id="49e56-165">See subcategories.</span></span></p></td>
<td><p><span data-ttu-id="49e56-166">請參閱子類別。</span><span class="sxs-lookup"><span data-stu-id="49e56-166">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e56-167">JET_errcatUsage 14</span><span class="sxs-lookup"><span data-stu-id="49e56-167">JET_errcatUsage 14</span></span></p></td>
<td><p><span data-ttu-id="49e56-168">表示使用錯誤。</span><span class="sxs-lookup"><span data-stu-id="49e56-168">Represents a usage error.</span></span> <span data-ttu-id="49e56-169">用戶端程式代碼未將正確的引數傳遞至 <strong>JET</strong> API。</span><span class="sxs-lookup"><span data-stu-id="49e56-169">The client code did not pass the correct arguments to the <strong>JET</strong> API.</span></span> <span data-ttu-id="49e56-170">此錯誤會在重試期間持續。</span><span class="sxs-lookup"><span data-stu-id="49e56-170">This error will persist with retry.</span></span></p></td>
<td><p><span data-ttu-id="49e56-171">用戶端程式代碼應該使用 <strong>Assert () </strong> 方法來確保不會傳回這個錯誤類別，因此可能會在開發期間攔截問題。</span><span class="sxs-lookup"><span data-stu-id="49e56-171">Client code should use the <strong>Assert()</strong> method to ensure that this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="49e56-172">在零售版中，應用程式應該通知操作員有關錯誤。</span><span class="sxs-lookup"><span data-stu-id="49e56-172">In retail, the application should notify the operator about the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e56-173">JET_errcatState 15</span><span class="sxs-lookup"><span data-stu-id="49e56-173">JET_errcatState 15</span></span></p></td>
<td><p><span data-ttu-id="49e56-174">表示 API 可傳回的訊息類別，以描述資料庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="49e56-174">Represents a class of messages that the API can return to describe the state of the database.</span></span> <span data-ttu-id="49e56-175">例如，當找不到要求的記錄時， <a href="gg294103(v=exchg.10).md">JetSeek () </a> 方法可能會傳回 <strong>JET_errRecordNotFound</strong> 。</span><span class="sxs-lookup"><span data-stu-id="49e56-175">For example, the <a href="gg294103(v=exchg.10).md">JetSeek()</a> method might return <strong>JET_errRecordNotFound</strong> when the requested record was not found.</span></span></p></td>
<td><p><span data-ttu-id="49e56-176">根據 API 而有所不同。</span><span class="sxs-lookup"><span data-stu-id="49e56-176">Varies based on the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e56-177">JET_errcatObsolete 16</span><span class="sxs-lookup"><span data-stu-id="49e56-177">JET_errcatObsolete 16</span></span></p></td>
<td><p><span data-ttu-id="49e56-178">表示來自舊版引擎的錯誤。</span><span class="sxs-lookup"><span data-stu-id="49e56-178">Represents errors that are from a previous version of the engine.</span></span> <span data-ttu-id="49e56-179">目前的引擎不應傳回這些錯誤。</span><span class="sxs-lookup"><span data-stu-id="49e56-179">These errors should not be returned by the current engine.</span></span></p></td>
<td><p><span data-ttu-id="49e56-180">不明。</span><span class="sxs-lookup"><span data-stu-id="49e56-180">Unknown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e56-181">JET_errcatMax 17</span><span class="sxs-lookup"><span data-stu-id="49e56-181">JET_errcatMax 17</span></span></p></td>
<td><p><span data-ttu-id="49e56-182">常數，表示列舉的結尾。</span><span class="sxs-lookup"><span data-stu-id="49e56-182">A constant that indicates the end of the enumeration.</span></span></p></td>
<td><p><span data-ttu-id="49e56-183">N/A。</span><span class="sxs-lookup"><span data-stu-id="49e56-183">N/A.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="49e56-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="49e56-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49e56-185"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="49e56-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="49e56-186">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="49e56-186">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e56-187"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="49e56-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="49e56-188">需要 Windows 8 Server。</span><span class="sxs-lookup"><span data-stu-id="49e56-188">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e56-189"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="49e56-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="49e56-190">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="49e56-190">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

