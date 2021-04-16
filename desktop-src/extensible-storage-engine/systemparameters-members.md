---
description: 深入瞭解： SystemParameters 成員
title: SystemParameters 成員
TOCTitle: SystemParameters members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_members(v=EXCHG.10)
ms:contentKeyID: 55104101
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e317ef4e63a33951dc55e030718d226ae3eaeec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550680"
---
# <a name="systemparameters-members"></a><span data-ttu-id="a85ce-103">SystemParameters 成員</span><span class="sxs-lookup"><span data-stu-id="a85ce-103">SystemParameters members</span></span>

<span data-ttu-id="a85ce-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="a85ce-104">Include protected members</span></span>  
<span data-ttu-id="a85ce-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="a85ce-105">Include inherited members</span></span>  

<span data-ttu-id="a85ce-106">ESENT API 的常數。</span><span class="sxs-lookup"><span data-stu-id="a85ce-106">Constants for the ESENT API.</span></span> <span data-ttu-id="a85ce-107">這些都不需要透過系統參數進行查閱。</span><span class="sxs-lookup"><span data-stu-id="a85ce-107">These don't have to be looked up via system parameters.</span></span> <span data-ttu-id="a85ce-108">此類別提供靜態屬性來設定和取得全域 ESENT 系統參數。</span><span class="sxs-lookup"><span data-stu-id="a85ce-108">This class provides static properties to set and get global ESENT system parameters.</span></span> <span data-ttu-id="a85ce-109">此類別提供靜態屬性來設定和取得全域 ESENT 系統參數。</span><span class="sxs-lookup"><span data-stu-id="a85ce-109">This class provides static properties to set and get global ESENT system parameters.</span></span>

<span data-ttu-id="a85ce-110">[SystemParameters](./systemparameters-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="a85ce-110">The [SystemParameters](./systemparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="a85ce-111">屬性</span><span class="sxs-lookup"><span data-stu-id="a85ce-111">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a85ce-112">名稱</span><span class="sxs-lookup"><span data-stu-id="a85ce-112">Name</span></span></th>
<th><span data-ttu-id="a85ce-113">描述</span><span class="sxs-lookup"><span data-stu-id="a85ce-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-116"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-116"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span></span></td>
<td><span data-ttu-id="a85ce-117">取得書簽的大小上限。</span><span class="sxs-lookup"><span data-stu-id="a85ce-117">Gets the maximum size of a bookmark.</span></span> <span data-ttu-id="a85ce-118"><a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID、JET_TABLEID、[]、int32、int32) </a>。</span><span class="sxs-lookup"><span data-stu-id="a85ce-118"><a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-121"><a href="dn351214(v=exchg.10).md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-121"><a href="dn351214(v=exchg.10).md">CacheSize</a></span></span></td>
<td><span data-ttu-id="a85ce-122">取得或設定頁面中資料庫快取的大小。</span><span class="sxs-lookup"><span data-stu-id="a85ce-122">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="a85ce-123">根據預設，資料庫快取會自動調整其大小，將此屬性設定為非零值會導致快取將本身調整為目標大小。</span><span class="sxs-lookup"><span data-stu-id="a85ce-123">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-126"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-126"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span></span></td>
<td><span data-ttu-id="a85ce-127">取得或設定資料庫頁面快取的大小上限。</span><span class="sxs-lookup"><span data-stu-id="a85ce-127">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="a85ce-128">大小是在資料庫頁面中。</span><span class="sxs-lookup"><span data-stu-id="a85ce-128">The size is in database pages.</span></span> <span data-ttu-id="a85ce-129">如果此參數保留為其預設值，則在呼叫 JetInit 時，會將快取的大小上限設定為實體記憶體的大小。</span><span class="sxs-lookup"><span data-stu-id="a85ce-129">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-132"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-132"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span></span></td>
<td><span data-ttu-id="a85ce-133">取得或設定資料庫頁面中資料庫頁面快取的大小下限。</span><span class="sxs-lookup"><span data-stu-id="a85ce-133">Gets or sets the minimum size of the database page cache, in database pages.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-136"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-136"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span></span></td>
<td><span data-ttu-id="a85ce-137">取得排序或索引鍵中元件的最大數目。</span><span class="sxs-lookup"><span data-stu-id="a85ce-137">Gets the maximum number of components in a sort or index key.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-140"><a href="dn351218(v=exchg.10).md">Configuration</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-140"><a href="dn351218(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="a85ce-141">取得或設定值，這個值會指定整個系統參數集的預設值。</span><span class="sxs-lookup"><span data-stu-id="a85ce-141">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="a85ce-142">當此參數設定為特定設定時，所有系統參數值都會重設為該設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="a85ce-142">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="a85ce-143">如果設定特定實例的設定，則全域系統參數將不會重設為其預設值。</span><span class="sxs-lookup"><span data-stu-id="a85ce-143">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="a85ce-144">Small Configuration (0) ：資料庫引擎已針對記憶體使用量優化。</span><span class="sxs-lookup"><span data-stu-id="a85ce-144">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="a85ce-145">舊版設定 (1) ：資料庫引擎有其傳統預設值。</span><span class="sxs-lookup"><span data-stu-id="a85ce-145">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="a85ce-146">Windows Vista 和更新的支援。</span><span class="sxs-lookup"><span data-stu-id="a85ce-146">Supported on Windows Vista and up.</span></span> <span data-ttu-id="a85ce-147">在 Windows XP 和 Windows Server 2003 上略過。</span><span class="sxs-lookup"><span data-stu-id="a85ce-147">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-150"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-150"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span></span></td>
<td><span data-ttu-id="a85ce-151">取得或設定資料庫頁面的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a85ce-151">Gets or sets the size of the database pages, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-154"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-154"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="a85ce-155">取得或設定值，這個值表示資料庫引擎是否接受或拒絕系統參數子集的變更。</span><span class="sxs-lookup"><span data-stu-id="a85ce-155">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="a85ce-156">此參數會搭配 <a href="dn351218(v=exchg.10).md">設定使用，以防止</a> 某些系統參數從選取的設定的預設值中退出。</span><span class="sxs-lookup"><span data-stu-id="a85ce-156">This parameter is used in conjunction with <a href="dn351218(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="a85ce-157">Windows Vista 和更新的支援。</span><span class="sxs-lookup"><span data-stu-id="a85ce-157">Supported on Windows Vista and up.</span></span> <span data-ttu-id="a85ce-158">在 Windows XP 和 Windows Server 2003 上略過。</span><span class="sxs-lookup"><span data-stu-id="a85ce-158">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-161"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-161"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="a85ce-162">取得或設定值，這個值表示資料庫引擎是否應使用所有 managed 檔案的 OS 檔案快取。</span><span class="sxs-lookup"><span data-stu-id="a85ce-162">Gets or sets a value indicating whether the database engine should use the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-165"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-165"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="a85ce-166">取得或設定值，這個值表示資料庫引擎是否應針對資料庫檔案使用記憶體對應的檔案 i/o。</span><span class="sxs-lookup"><span data-stu-id="a85ce-166">Gets or sets a value indicating whether the database engine should use memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-169"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-169"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span></span></td>
<td><span data-ttu-id="a85ce-170">取得或設定資料庫引擎發出至 eventlog 的 eventlog 訊息詳細層級。</span><span class="sxs-lookup"><span data-stu-id="a85ce-170">Gets or sets the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="a85ce-171">較高的數位將會產生更詳細的事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="a85ce-171">Higher numbers will result in more detailed eventlog messages.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-174"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-174"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span></span></td>
<td><span data-ttu-id="a85ce-175">取得或設定在 JET 內產生之例外狀況的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="a85ce-175">Gets or sets the value encoding what to do with exceptions generated within JET.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-178"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-178"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span></span></td>
<td><span data-ttu-id="a85ce-179">取得或設定要在出現無回應的 IOs 上執行的動作集合。</span><span class="sxs-lookup"><span data-stu-id="a85ce-179">Gets or sets the set of actions to be taken on IOs that appear hung.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-182"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-182"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span></span></td>
<td><span data-ttu-id="a85ce-183">取得或設定視為應採取動作之無反應 IO 的臨界值。</span><span class="sxs-lookup"><span data-stu-id="a85ce-183">Gets or sets the threshold for what is considered a hung IO that should be acted upon.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-186"><a href="dn351156(v=exchg.10).md">KeyMost</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-186"><a href="dn351156(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="a85ce-187">取得最大索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="a85ce-187">Gets the maximum key size.</span></span> <span data-ttu-id="a85ce-188">這取決於 Esent 版本和資料庫頁面大小。</span><span class="sxs-lookup"><span data-stu-id="a85ce-188">This depends on the Esent version and database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-191"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-191"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="a85ce-192">取得或設定與舊版資料庫引擎的檔案命名慣例的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="a85ce-192">Gets or sets backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-195"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-195"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span></span></td>
<td><span data-ttu-id="a85ce-196">取得 lv 區塊大小。</span><span class="sxs-lookup"><span data-stu-id="a85ce-196">Gets the lv chunks size.</span></span> <span data-ttu-id="a85ce-197">這取決於資料庫頁面大小。</span><span class="sxs-lookup"><span data-stu-id="a85ce-197">This depends on the database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-200"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-200"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span></span></td>
<td><span data-ttu-id="a85ce-201">取得或設定可建立的實例數目上限。</span><span class="sxs-lookup"><span data-stu-id="a85ce-201">Gets or sets the maximum number of instances that can be created.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-204"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-204"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span></span></td>
<td><span data-ttu-id="a85ce-205">取得或設定應壓縮為 xpress 壓縮的最小資料量。</span><span class="sxs-lookup"><span data-stu-id="a85ce-205">Gets or sets the smallest amount of data that should be compressed with xpress compression.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-208"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-208"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span></span></td>
<td><span data-ttu-id="a85ce-209">此參數控制一次可在主機作業系統中的每個磁片佇列的資料庫檔案 i/o 數目。</span><span class="sxs-lookup"><span data-stu-id="a85ce-209">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="a85ce-210">較大的參數值可大幅協助大型資料庫應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="a85ce-210">A larger value for this parameter can significantly help the performance of a large database application.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-213"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-213"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span></span></td>
<td><span data-ttu-id="a85ce-214">取得或設定這個進程實例的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="a85ce-214">Gets or sets the friendly name for this instance of the process.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-217"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-217"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span></span></td>
<td><span data-ttu-id="a85ce-218">取得或設定資料庫頁面快取開始從快取收回頁面的閾值，以騰出空間給未快取的頁面。</span><span class="sxs-lookup"><span data-stu-id="a85ce-218">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="a85ce-219">當快取中的頁面緩衝區數目降到低於此閾值時，就會啟動背景進程來補充該可用緩衝區集區。</span><span class="sxs-lookup"><span data-stu-id="a85ce-219">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="a85ce-220">此臨界值一律相對於 JET_paramCacheSizeMax 所設定的最大快取大小。</span><span class="sxs-lookup"><span data-stu-id="a85ce-220">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="a85ce-221">此臨界值也必須小於 JET_paramStopFlushThreshold 所設定的停止閾值。</span><span class="sxs-lookup"><span data-stu-id="a85ce-221">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="a85ce-222">開始閾值的距離高度將決定資料庫頁面快取在應用程式需要之前產生可用緩衝區所必須擁有的回應時間。</span><span class="sxs-lookup"><span data-stu-id="a85ce-222">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="a85ce-223">高啟動臨界值可讓背景進程更有時間回應。</span><span class="sxs-lookup"><span data-stu-id="a85ce-223">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="a85ce-224">不過，高啟動閾值表示較高的停止閾值，而且會減少資料庫頁面快取的有效大小。</span><span class="sxs-lookup"><span data-stu-id="a85ce-224">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-227"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-227"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span></span></td>
<td><span data-ttu-id="a85ce-228">取得或設定資料庫頁面快取結束從快取收回頁面的閾值，以騰出空間給未快取的頁面。</span><span class="sxs-lookup"><span data-stu-id="a85ce-228">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="a85ce-229">當快取中的頁面緩衝區數目超過此臨界值時，就會停止已開始補充該可用緩衝區集區的背景進程。</span><span class="sxs-lookup"><span data-stu-id="a85ce-229">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="a85ce-230">此臨界值一律相對於 JET_paramCacheSizeMax 所設定的最大快取大小。</span><span class="sxs-lookup"><span data-stu-id="a85ce-230">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="a85ce-231">此臨界值也必須大於 JET_paramStartFlushThreshold 所設定的 [開始] 閾值。</span><span class="sxs-lookup"><span data-stu-id="a85ce-231">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="a85ce-232">開始閾值和停止臨界值之間的距離，會影響背景進程清除資料庫頁面的效率。</span><span class="sxs-lookup"><span data-stu-id="a85ce-232">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="a85ce-233">較大的間距將可讓您更有可能合併對相鄰頁面的寫入。</span><span class="sxs-lookup"><span data-stu-id="a85ce-233">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="a85ce-234">不過，高停止閾值將會減少資料庫頁面快取的有效大小。</span><span class="sxs-lookup"><span data-stu-id="a85ce-234">However, a high stop threshold will reduce the effective size of the database page cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a85ce-235">頁首</span><span class="sxs-lookup"><span data-stu-id="a85ce-235">Top</span></span>

## <a name="fields"></a><span data-ttu-id="a85ce-236">欄位</span><span class="sxs-lookup"><span data-stu-id="a85ce-236">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a85ce-237">名稱</span><span class="sxs-lookup"><span data-stu-id="a85ce-237">Name</span></span></th>
<th><span data-ttu-id="a85ce-238">描述</span><span class="sxs-lookup"><span data-stu-id="a85ce-238">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-241"><a href="dn351208(v=exchg.10).md">BaseNameLength</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-241"><a href="dn351208(v=exchg.10).md">BaseNameLength</a></span></span></td>
<td><span data-ttu-id="a85ce-242">用來命名資料庫引擎所使用之檔案的前置詞長度。</span><span class="sxs-lookup"><span data-stu-id="a85ce-242">The length of the prefix used to name files used by the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-245"><a href="dn351146(v=exchg.10).md">ColumnMost</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-245"><a href="dn351146(v=exchg.10).md">ColumnMost</a></span></span></td>
<td><span data-ttu-id="a85ce-246">未 JET_coltyp 資料行的大小上限。LongBinary 或 JET_coltyp。LongText.</span><span class="sxs-lookup"><span data-stu-id="a85ce-246">Maximum size for columns which are not JET_coltyp.LongBinary or JET_coltyp.LongText.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-249"><a href="dn351210(v=exchg.10).md">ColumnsFixedMost</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-249"><a href="dn351210(v=exchg.10).md">ColumnsFixedMost</a></span></span></td>
<td><span data-ttu-id="a85ce-250">資料表中允許的固定資料行數目上限。</span><span class="sxs-lookup"><span data-stu-id="a85ce-250">Maximum number of fixed columns allowed in a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-253"><a href="dn351140(v=exchg.10).md">ColumnsMost</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-253"><a href="dn351140(v=exchg.10).md">ColumnsMost</a></span></span></td>
<td><span data-ttu-id="a85ce-254">資料表中允許的資料行數目上限。</span><span class="sxs-lookup"><span data-stu-id="a85ce-254">Maximum number of columns allowed in a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-257"><a href="dn351148(v=exchg.10).md">ColumnsTaggedMost</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-257"><a href="dn351148(v=exchg.10).md">ColumnsTaggedMost</a></span></span></td>
<td><span data-ttu-id="a85ce-258">資料表中允許的標記資料行數目上限。</span><span class="sxs-lookup"><span data-stu-id="a85ce-258">Maximum number of tagged columns allowed in a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-261"><a href="dn351212(v=exchg.10).md">ColumnsVarMost</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-261"><a href="dn351212(v=exchg.10).md">ColumnsVarMost</a></span></span></td>
<td><span data-ttu-id="a85ce-262">資料表中允許的可變長度資料行數目上限。</span><span class="sxs-lookup"><span data-stu-id="a85ce-262">Maximum number of variable-length columns allowed in a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-265"><a href="dn351141(v=exchg.10).md">LocaleNameMaxLength</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-265"><a href="dn351141(v=exchg.10).md">LocaleNameMaxLength</a></span></span></td>
<td><span data-ttu-id="a85ce-266">地區設定名稱的最大長度 (從 winnt. h) LOCALE_NAME_MAX_LENGTH。</span><span class="sxs-lookup"><span data-stu-id="a85ce-266">The maximum length of a locale name (LOCALE_NAME_MAX_LENGTH from winnt.h).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-269"><a href="dn351213(v=exchg.10).md">NameMost</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-269"><a href="dn351213(v=exchg.10).md">NameMost</a></span></span></td>
<td><span data-ttu-id="a85ce-270">資料表/資料行/索引名稱的大小上限。</span><span class="sxs-lookup"><span data-stu-id="a85ce-270">Maximum size of a table/column/index name.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a85ce-273"><a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a></span><span class="sxs-lookup"><span data-stu-id="a85ce-273"><a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a></span></span></td>
<td><span data-ttu-id="a85ce-274">提供最小可能暫存資料庫的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="a85ce-274">The number of pages that gives the smallest possible temporary database.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a85ce-275">頁首</span><span class="sxs-lookup"><span data-stu-id="a85ce-275">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a85ce-276">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a85ce-276">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a85ce-277">參考</span><span class="sxs-lookup"><span data-stu-id="a85ce-277">Reference</span></span>

[<span data-ttu-id="a85ce-278">SystemParameters 類別</span><span class="sxs-lookup"><span data-stu-id="a85ce-278">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="a85ce-279">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a85ce-279">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
