---
description: 深入瞭解： SystemParameters 屬性
title: SystemParameters 屬性
TOCTitle: SystemParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55104035
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 12e18b6c045758c8e9fd7ffb91f728c78dcf2e24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568063"
---
# <a name="systemparameters-properties"></a><span data-ttu-id="2a168-103">SystemParameters 屬性</span><span class="sxs-lookup"><span data-stu-id="2a168-103">SystemParameters properties</span></span>

<span data-ttu-id="2a168-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="2a168-104">Include protected members</span></span>  
<span data-ttu-id="2a168-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="2a168-105">Include inherited members</span></span>  

<span data-ttu-id="2a168-106">[SystemParameters](./systemparameters-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="2a168-106">The [SystemParameters](./systemparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="2a168-107">屬性</span><span class="sxs-lookup"><span data-stu-id="2a168-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2a168-108">名稱</span><span class="sxs-lookup"><span data-stu-id="2a168-108">Name</span></span></th>
<th><span data-ttu-id="2a168-109">描述</span><span class="sxs-lookup"><span data-stu-id="2a168-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-112"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span><span class="sxs-lookup"><span data-stu-id="2a168-112"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span></span></td>
<td><span data-ttu-id="2a168-113">取得書簽的大小上限。</span><span class="sxs-lookup"><span data-stu-id="2a168-113">Gets the maximum size of a bookmark.</span></span> <span data-ttu-id="2a168-114"><a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID、JET_TABLEID、[]、int32、int32) </a>。</span><span class="sxs-lookup"><span data-stu-id="2a168-114"><a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-117"><a href="dn351214(v=exchg.10).md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="2a168-117"><a href="dn351214(v=exchg.10).md">CacheSize</a></span></span></td>
<td><span data-ttu-id="2a168-118">取得或設定頁面中資料庫快取的大小。</span><span class="sxs-lookup"><span data-stu-id="2a168-118">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="2a168-119">根據預設，資料庫快取會自動調整其大小，將此屬性設定為非零值會導致快取將本身調整為目標大小。</span><span class="sxs-lookup"><span data-stu-id="2a168-119">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-122"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span><span class="sxs-lookup"><span data-stu-id="2a168-122"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span></span></td>
<td><span data-ttu-id="2a168-123">取得或設定資料庫頁面快取的大小上限。</span><span class="sxs-lookup"><span data-stu-id="2a168-123">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="2a168-124">大小是在資料庫頁面中。</span><span class="sxs-lookup"><span data-stu-id="2a168-124">The size is in database pages.</span></span> <span data-ttu-id="2a168-125">如果此參數保留為其預設值，則在呼叫 JetInit 時，會將快取的大小上限設定為實體記憶體的大小。</span><span class="sxs-lookup"><span data-stu-id="2a168-125">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-128"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span><span class="sxs-lookup"><span data-stu-id="2a168-128"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span></span></td>
<td><span data-ttu-id="2a168-129">取得或設定資料庫頁面中資料庫頁面快取的大小下限。</span><span class="sxs-lookup"><span data-stu-id="2a168-129">Gets or sets the minimum size of the database page cache, in database pages.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-132"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="2a168-132"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span></span></td>
<td><span data-ttu-id="2a168-133">取得排序或索引鍵中元件的最大數目。</span><span class="sxs-lookup"><span data-stu-id="2a168-133">Gets the maximum number of components in a sort or index key.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-136"><a href="dn351218(v=exchg.10).md">Configuration</a></span><span class="sxs-lookup"><span data-stu-id="2a168-136"><a href="dn351218(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="2a168-137">取得或設定值，這個值會指定整個系統參數集的預設值。</span><span class="sxs-lookup"><span data-stu-id="2a168-137">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="2a168-138">當此參數設定為特定設定時，所有系統參數值都會重設為該設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="2a168-138">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="2a168-139">如果設定特定實例的設定，則全域系統參數將不會重設為其預設值。</span><span class="sxs-lookup"><span data-stu-id="2a168-139">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="2a168-140">Small Configuration (0) ：資料庫引擎已針對記憶體使用量優化。</span><span class="sxs-lookup"><span data-stu-id="2a168-140">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="2a168-141">舊版設定 (1) ：資料庫引擎有其傳統預設值。</span><span class="sxs-lookup"><span data-stu-id="2a168-141">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="2a168-142">Windows Vista 和更新的支援。</span><span class="sxs-lookup"><span data-stu-id="2a168-142">Supported on Windows Vista and up.</span></span> <span data-ttu-id="2a168-143">在 Windows XP 和 Windows Server 2003 上略過。</span><span class="sxs-lookup"><span data-stu-id="2a168-143">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-146"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span><span class="sxs-lookup"><span data-stu-id="2a168-146"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span></span></td>
<td><span data-ttu-id="2a168-147">取得或設定資料庫頁面的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2a168-147">Gets or sets the size of the database pages, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-150"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span><span class="sxs-lookup"><span data-stu-id="2a168-150"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="2a168-151">取得或設定值，這個值表示資料庫引擎是否接受或拒絕系統參數子集的變更。</span><span class="sxs-lookup"><span data-stu-id="2a168-151">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="2a168-152">此參數會搭配 <a href="dn351218(v=exchg.10).md">設定使用，以防止</a> 某些系統參數從選取的設定的預設值中退出。</span><span class="sxs-lookup"><span data-stu-id="2a168-152">This parameter is used in conjunction with <a href="dn351218(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="2a168-153">Windows Vista 和更新的支援。</span><span class="sxs-lookup"><span data-stu-id="2a168-153">Supported on Windows Vista and up.</span></span> <span data-ttu-id="2a168-154">在 Windows XP 和 Windows Server 2003 上略過。</span><span class="sxs-lookup"><span data-stu-id="2a168-154">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-157"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span><span class="sxs-lookup"><span data-stu-id="2a168-157"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="2a168-158">取得或設定值，這個值表示資料庫引擎是否應使用所有 managed 檔案的 OS 檔案快取。</span><span class="sxs-lookup"><span data-stu-id="2a168-158">Gets or sets a value indicating whether the database engine should use the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-161"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span><span class="sxs-lookup"><span data-stu-id="2a168-161"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="2a168-162">取得或設定值，這個值表示資料庫引擎是否應針對資料庫檔案使用記憶體對應的檔案 i/o。</span><span class="sxs-lookup"><span data-stu-id="2a168-162">Gets or sets a value indicating whether the database engine should use memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-165"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span><span class="sxs-lookup"><span data-stu-id="2a168-165"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span></span></td>
<td><span data-ttu-id="2a168-166">取得或設定資料庫引擎發出至 eventlog 的 eventlog 訊息詳細層級。</span><span class="sxs-lookup"><span data-stu-id="2a168-166">Gets or sets the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="2a168-167">較高的數位將會產生更詳細的事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="2a168-167">Higher numbers will result in more detailed eventlog messages.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-170"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span><span class="sxs-lookup"><span data-stu-id="2a168-170"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span></span></td>
<td><span data-ttu-id="2a168-171">取得或設定在 JET 內產生之例外狀況的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="2a168-171">Gets or sets the value encoding what to do with exceptions generated within JET.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-174"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span><span class="sxs-lookup"><span data-stu-id="2a168-174"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span></span></td>
<td><span data-ttu-id="2a168-175">取得或設定要在出現無回應的 IOs 上執行的動作集合。</span><span class="sxs-lookup"><span data-stu-id="2a168-175">Gets or sets the set of actions to be taken on IOs that appear hung.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-178"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span><span class="sxs-lookup"><span data-stu-id="2a168-178"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span></span></td>
<td><span data-ttu-id="2a168-179">取得或設定視為應採取動作之無反應 IO 的臨界值。</span><span class="sxs-lookup"><span data-stu-id="2a168-179">Gets or sets the threshold for what is considered a hung IO that should be acted upon.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-182"><a href="dn351156(v=exchg.10).md">KeyMost</a></span><span class="sxs-lookup"><span data-stu-id="2a168-182"><a href="dn351156(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="2a168-183">取得最大索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="2a168-183">Gets the maximum key size.</span></span> <span data-ttu-id="2a168-184">這取決於 Esent 版本和資料庫頁面大小。</span><span class="sxs-lookup"><span data-stu-id="2a168-184">This depends on the Esent version and database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-187"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span><span class="sxs-lookup"><span data-stu-id="2a168-187"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="2a168-188">取得或設定與舊版資料庫引擎的檔案命名慣例的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="2a168-188">Gets or sets backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-191"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span><span class="sxs-lookup"><span data-stu-id="2a168-191"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span></span></td>
<td><span data-ttu-id="2a168-192">取得 lv 區塊大小。</span><span class="sxs-lookup"><span data-stu-id="2a168-192">Gets the lv chunks size.</span></span> <span data-ttu-id="2a168-193">這取決於資料庫頁面大小。</span><span class="sxs-lookup"><span data-stu-id="2a168-193">This depends on the database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-196"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span><span class="sxs-lookup"><span data-stu-id="2a168-196"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span></span></td>
<td><span data-ttu-id="2a168-197">取得或設定可建立的實例數目上限。</span><span class="sxs-lookup"><span data-stu-id="2a168-197">Gets or sets the maximum number of instances that can be created.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-200"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span><span class="sxs-lookup"><span data-stu-id="2a168-200"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span></span></td>
<td><span data-ttu-id="2a168-201">取得或設定應壓縮為 xpress 壓縮的最小資料量。</span><span class="sxs-lookup"><span data-stu-id="2a168-201">Gets or sets the smallest amount of data that should be compressed with xpress compression.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-204"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span><span class="sxs-lookup"><span data-stu-id="2a168-204"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span></span></td>
<td><span data-ttu-id="2a168-205">此參數控制一次可在主機作業系統中的每個磁片佇列的資料庫檔案 i/o 數目。</span><span class="sxs-lookup"><span data-stu-id="2a168-205">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="2a168-206">較大的參數值可大幅協助大型資料庫應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="2a168-206">A larger value for this parameter can significantly help the performance of a large database application.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-209"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span><span class="sxs-lookup"><span data-stu-id="2a168-209"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span></span></td>
<td><span data-ttu-id="2a168-210">取得或設定這個進程實例的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="2a168-210">Gets or sets the friendly name for this instance of the process.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-213"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span><span class="sxs-lookup"><span data-stu-id="2a168-213"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span></span></td>
<td><span data-ttu-id="2a168-214">取得或設定資料庫頁面快取開始從快取收回頁面的閾值，以騰出空間給未快取的頁面。</span><span class="sxs-lookup"><span data-stu-id="2a168-214">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="2a168-215">當快取中的頁面緩衝區數目降到低於此閾值時，就會啟動背景進程來補充該可用緩衝區集區。</span><span class="sxs-lookup"><span data-stu-id="2a168-215">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="2a168-216">此臨界值一律相對於 JET_paramCacheSizeMax 所設定的最大快取大小。</span><span class="sxs-lookup"><span data-stu-id="2a168-216">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="2a168-217">此臨界值也必須小於 JET_paramStopFlushThreshold 所設定的停止閾值。</span><span class="sxs-lookup"><span data-stu-id="2a168-217">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="2a168-218">開始閾值的距離高度將決定資料庫頁面快取在應用程式需要之前產生可用緩衝區所必須擁有的回應時間。</span><span class="sxs-lookup"><span data-stu-id="2a168-218">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="2a168-219">高啟動臨界值可讓背景進程更有時間回應。</span><span class="sxs-lookup"><span data-stu-id="2a168-219">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="2a168-220">不過，高啟動閾值表示較高的停止閾值，而且會減少資料庫頁面快取的有效大小。</span><span class="sxs-lookup"><span data-stu-id="2a168-220">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="2a168-223"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span><span class="sxs-lookup"><span data-stu-id="2a168-223"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span></span></td>
<td><span data-ttu-id="2a168-224">取得或設定資料庫頁面快取結束從快取收回頁面的閾值，以騰出空間給未快取的頁面。</span><span class="sxs-lookup"><span data-stu-id="2a168-224">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="2a168-225">當快取中的頁面緩衝區數目超過此臨界值時，就會停止已開始補充該可用緩衝區集區的背景進程。</span><span class="sxs-lookup"><span data-stu-id="2a168-225">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="2a168-226">此臨界值一律相對於 JET_paramCacheSizeMax 所設定的最大快取大小。</span><span class="sxs-lookup"><span data-stu-id="2a168-226">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="2a168-227">此臨界值也必須大於 JET_paramStartFlushThreshold 所設定的 [開始] 閾值。</span><span class="sxs-lookup"><span data-stu-id="2a168-227">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="2a168-228">開始閾值和停止臨界值之間的距離，會影響背景進程清除資料庫頁面的效率。</span><span class="sxs-lookup"><span data-stu-id="2a168-228">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="2a168-229">較大的間距將可讓您更有可能合併對相鄰頁面的寫入。</span><span class="sxs-lookup"><span data-stu-id="2a168-229">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="2a168-230">不過，高停止閾值將會減少資料庫頁面快取的有效大小。</span><span class="sxs-lookup"><span data-stu-id="2a168-230">However, a high stop threshold will reduce the effective size of the database page cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2a168-231">頁首</span><span class="sxs-lookup"><span data-stu-id="2a168-231">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="2a168-232">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a168-232">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2a168-233">參考</span><span class="sxs-lookup"><span data-stu-id="2a168-233">Reference</span></span>

[<span data-ttu-id="2a168-234">SystemParameters 類別</span><span class="sxs-lookup"><span data-stu-id="2a168-234">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="2a168-235">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2a168-235">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
