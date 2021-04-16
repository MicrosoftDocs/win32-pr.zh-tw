---
description: 深入瞭解： InstanceParameters 屬性
title: InstanceParameters 屬性
TOCTitle: InstanceParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.InstanceParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55103291
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 0ac2b8aa959b8fa07f06e2de86dcfc173bab15ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550899"
---
# <a name="instanceparameters-properties"></a><span data-ttu-id="9a519-103">InstanceParameters 屬性</span><span class="sxs-lookup"><span data-stu-id="9a519-103">InstanceParameters properties</span></span>

<span data-ttu-id="9a519-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="9a519-104">Include protected members</span></span>  
<span data-ttu-id="9a519-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="9a519-105">Include inherited members</span></span>  

<span data-ttu-id="9a519-106">[InstanceParameters](./instanceparameters-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="9a519-106">The [InstanceParameters](./instanceparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="9a519-107">屬性</span><span class="sxs-lookup"><span data-stu-id="9a519-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9a519-108">名稱</span><span class="sxs-lookup"><span data-stu-id="9a519-108">Name</span></span></th>
<th><span data-ttu-id="9a519-109">描述</span><span class="sxs-lookup"><span data-stu-id="9a519-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-111"><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></span><span class="sxs-lookup"><span data-stu-id="9a519-111"><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></span></span></td>
<td><span data-ttu-id="9a519-112">取得或設定資料夾的相對或絕對檔案系統路徑，其中損毀復原或還原作業可以在指定資料夾的交易記錄中找到參考的資料庫。</span><span class="sxs-lookup"><span data-stu-id="9a519-112">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-114"><a href="dn350972(v=exchg.10).md">BaseName</a></span><span class="sxs-lookup"><span data-stu-id="9a519-114"><a href="dn350972(v=exchg.10).md">BaseName</a></span></span></td>
<td><span data-ttu-id="9a519-115">取得或設定用於資料庫引擎所使用之許多檔案的三個字母前置詞。</span><span class="sxs-lookup"><span data-stu-id="9a519-115">Gets or sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="9a519-116">例如，檢查點檔案稱為「EDB」。因為 EDB 是預設的基底名稱，所以預設為使用 .CHK。</span><span class="sxs-lookup"><span data-stu-id="9a519-116">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-118"><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></span><span class="sxs-lookup"><span data-stu-id="9a519-118"><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="9a519-119">取得或設定值，這個值會在應用程式關閉實例所代表的資料表之後，提供實例快取的 B + 樹狀資源數目。</span><span class="sxs-lookup"><span data-stu-id="9a519-119">Gets or sets a value giving the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="9a519-120">此參數的大型值會導致資料庫引擎使用更多記憶體，但會增加應用程式隨機開啟大量資料表的速度。</span><span class="sxs-lookup"><span data-stu-id="9a519-120">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="9a519-121">對於具有極大量資料表之架構的應用程式而言，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="9a519-121">This is useful for applications that have a schema with a very large number of tables.</span></span> <span data-ttu-id="9a519-122">Windows Vista 和更新的支援。</span><span class="sxs-lookup"><span data-stu-id="9a519-122">Supported on Windows Vista and up.</span></span> <span data-ttu-id="9a519-123">在 Windows XP 和 Windows Server 2003 上略過。</span><span class="sxs-lookup"><span data-stu-id="9a519-123">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-125"><a href="dn350974(v=exchg.10).md">CachePriority</a></span><span class="sxs-lookup"><span data-stu-id="9a519-125"><a href="dn350974(v=exchg.10).md">CachePriority</a></span></span></td>
<td><span data-ttu-id="9a519-126">取得或設定相對快取優先權 (預設 = 100) 的每個實例屬性。</span><span class="sxs-lookup"><span data-stu-id="9a519-126">Gets or sets the per-instance property for relative cache priorities (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-128"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span><span class="sxs-lookup"><span data-stu-id="9a519-128"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span></span></td>
<td><span data-ttu-id="9a519-129">取得或設定在損毀之後，需要重新執行多少個交易記錄檔的閾值（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9a519-129">Gets or sets the threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span> <span data-ttu-id="9a519-130">如果使用 CircularLog 來啟用迴圈記錄，此參數也會控制要保留在磁片上的大約交易記錄檔量。</span><span class="sxs-lookup"><span data-stu-id="9a519-130">If circular logging is enabled using CircularLog then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-132"><a href="dn350977(v=exchg.10).md">CircularLog</a></span><span class="sxs-lookup"><span data-stu-id="9a519-132"><a href="dn350977(v=exchg.10).md">CircularLog</a></span></span></td>
<td><span data-ttu-id="9a519-133">取得或設定值，指出是否開啟迴圈記錄。</span><span class="sxs-lookup"><span data-stu-id="9a519-133">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="9a519-134">當迴圈記錄關閉時，所產生的所有交易記錄檔都會保留在磁片上，直到不再需要該檔案，因為已執行資料庫的完整備份。</span><span class="sxs-lookup"><span data-stu-id="9a519-134">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="9a519-135">當迴圈記錄開啟時，只有小於目前檢查點的交易記錄檔會保留在磁片上。</span><span class="sxs-lookup"><span data-stu-id="9a519-135">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="9a519-136">這種模式的好處是，備份不需要淘汰舊的交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="9a519-136">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-138"><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></span><span class="sxs-lookup"><span data-stu-id="9a519-138"><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></span></span></td>
<td><span data-ttu-id="9a519-139">取得或設定值，這個值表示當資料庫引擎設定為開始使用磁片上的交易記錄檔時，如果磁片上的交易記錄檔的大小與所設定的不同，JetInit 是否會失敗。</span><span class="sxs-lookup"><span data-stu-id="9a519-139">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="9a519-140">一般來說， <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE) </a> 會成功復原資料庫，但會失敗並出現 <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> ，指出記錄檔的大小設定不正確。</span><span class="sxs-lookup"><span data-stu-id="9a519-140">Normally, <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> will successfully recover the databases but will fail with <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="9a519-141">但是，當這個參數設定為 true 時，database engine 就會以無訊息模式刪除所有舊的記錄檔，並使用所設定的記錄檔大小來啟動一組新的交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="9a519-141">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="9a519-142">當應用程式希望以透明的方式變更其交易記錄檔大小，但在升級和還原案例中仍可正常運作時，此參數很有用。</span><span class="sxs-lookup"><span data-stu-id="9a519-142">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-144"><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></span><span class="sxs-lookup"><span data-stu-id="9a519-144"><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></span></span></td>
<td><span data-ttu-id="9a519-145">取得或設定值，這個值表示 ESENT 是否會以無訊息方式建立檔案系統路徑中遺失的資料夾。</span><span class="sxs-lookup"><span data-stu-id="9a519-145">Gets or sets a value indicating whether ESENT will silently create folders that are missing in its filesystem paths.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-147"><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></span><span class="sxs-lookup"><span data-stu-id="9a519-147"><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></span></span></td>
<td><span data-ttu-id="9a519-148">取得或設定每次需要成長以容納更多資料時，資料庫檔案中加入的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="9a519-148">Gets or sets the number of pages that are added to a database file each time it needs to grow to accommodate more data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-150"><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></span><span class="sxs-lookup"><span data-stu-id="9a519-150"><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></span></span></td>
<td><span data-ttu-id="9a519-151">取得或設定允許資料庫掃描完成的最大間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9a519-151">Gets or sets the maximum interval to allow the database scan to finish, in seconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-153"><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></span><span class="sxs-lookup"><span data-stu-id="9a519-153"><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></span></span></td>
<td><span data-ttu-id="9a519-154">取得或設定重複資料庫掃描的最小間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9a519-154">Gets or sets the minimum interval to repeat the database scan, in seconds.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-156"><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></span><span class="sxs-lookup"><span data-stu-id="9a519-156"><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></span></span></td>
<td><span data-ttu-id="9a519-157">取得或設定資料庫掃描的節流（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9a519-157">Gets or sets the throttling of the database scan, in milliseconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-159"><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></span><span class="sxs-lookup"><span data-stu-id="9a519-159"><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></span></span></td>
<td><span data-ttu-id="9a519-160">取得或設定值，指出是否應在復原期間執行資料庫維護。</span><span class="sxs-lookup"><span data-stu-id="9a519-160">Gets or sets a value indicating whether Database Maintenance should run during recovery.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-162"><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></span><span class="sxs-lookup"><span data-stu-id="9a519-162"><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></span></span></td>
<td><span data-ttu-id="9a519-163">取得或設定值，指出是否為共用相同磁片的資料庫啟用資料庫維護序列化。</span><span class="sxs-lookup"><span data-stu-id="9a519-163">Gets or sets a value indicating whether database Maintenance serialization is enabled for databases sharing the same disk.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-165"><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></span><span class="sxs-lookup"><span data-stu-id="9a519-165"><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></span></span></td>
<td><span data-ttu-id="9a519-166">取得或設定值，指出 <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID、String、AttachDatabaseGrbit) </a> 是否將檢查在作業系統中使用舊版 NLS 程式庫所建立的索引。</span><span class="sxs-lookup"><span data-stu-id="9a519-166">Gets or sets a value indicating whether <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a> will check for indexes that were build using an older version of the NLS library in the operating system.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-168"><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></span><span class="sxs-lookup"><span data-stu-id="9a519-168"><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></span></span></td>
<td><span data-ttu-id="9a519-169">取得或設定值，這個值表示是否已啟用線上磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="9a519-169">Gets or sets a value indicating whether online defragmentation is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-171"><a href="dn350988(v=exchg.10).md">EventSource</a></span><span class="sxs-lookup"><span data-stu-id="9a519-171"><a href="dn350988(v=exchg.10).md">EventSource</a></span></span></td>
<td><span data-ttu-id="9a519-172">取得或設定應用程式特定的字串，這個字串將加入 database engine 所發出的任何事件記錄檔訊息中。</span><span class="sxs-lookup"><span data-stu-id="9a519-172">Gets or sets an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="9a519-173">這可讓事件記錄檔訊息與來源應用程式輕鬆相互關聯。</span><span class="sxs-lookup"><span data-stu-id="9a519-173">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="9a519-174">預設會使用主應用程式的可執行檔名稱。</span><span class="sxs-lookup"><span data-stu-id="9a519-174">By default the host application executable name will be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-176"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span><span class="sxs-lookup"><span data-stu-id="9a519-176"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span></span></td>
<td><span data-ttu-id="9a519-177">取得或設定資料庫引擎為其事件記錄檔訊息所使用的事件記錄檔名稱。</span><span class="sxs-lookup"><span data-stu-id="9a519-177">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="9a519-178">依預設，所有事件記錄檔訊息都會移至應用程式事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="9a519-178">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="9a519-179">如果已設定另一個事件記錄檔的登錄機碼名稱，則會改為將事件記錄檔訊息移至該處。</span><span class="sxs-lookup"><span data-stu-id="9a519-179">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-181"><a href="dn350968(v=exchg.10).md">LogBuffers</a></span><span class="sxs-lookup"><span data-stu-id="9a519-181"><a href="dn350968(v=exchg.10).md">LogBuffers</a></span></span></td>
<td><span data-ttu-id="9a519-182">取得或設定在將記錄寫入交易記錄檔之前，用來快取記錄檔記錄的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="9a519-182">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="9a519-183">此參數的單位是保存交易記錄檔之磁片區的磁區大小。</span><span class="sxs-lookup"><span data-stu-id="9a519-183">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="9a519-184">磁區大小幾乎一律為512個位元組，因此可以安全地假設該單位的大小。</span><span class="sxs-lookup"><span data-stu-id="9a519-184">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="9a519-185">此參數會對效能造成影響。</span><span class="sxs-lookup"><span data-stu-id="9a519-185">This parameter has an impact on performance.</span></span> <span data-ttu-id="9a519-186">當資料庫引擎處於大量更新負載時，此緩衝區可能會非常快速地完成。</span><span class="sxs-lookup"><span data-stu-id="9a519-186">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="9a519-187">交易記錄檔較大的快取大小，對於在這種高負載狀況下的良好更新效能來說非常重要。</span><span class="sxs-lookup"><span data-stu-id="9a519-187">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="9a519-188">在此情況下，已知的預設值太小。</span><span class="sxs-lookup"><span data-stu-id="9a519-188">The default is known to be too small for this case.</span></span> <span data-ttu-id="9a519-189">請勿將此參數設定為大於交易記錄檔大小一半的緩衝區數 (以位元組為單位) 。</span><span class="sxs-lookup"><span data-stu-id="9a519-189">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-191"><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></span><span class="sxs-lookup"><span data-stu-id="9a519-191"><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></span></span></td>
<td><span data-ttu-id="9a519-192">取得或設定將包含實例之交易記錄之資料夾的相對或絕對檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="9a519-192">Gets or sets the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-194"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span><span class="sxs-lookup"><span data-stu-id="9a519-194"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span></span></td>
<td><span data-ttu-id="9a519-195">取得或設定交易記錄檔的大小。</span><span class="sxs-lookup"><span data-stu-id="9a519-195">Gets or sets the size of the transaction log files.</span></span> <span data-ttu-id="9a519-196">此參數應以1024個位元組的單位來設定 (例如，2048的設定會提供2MB 的記錄檔) 。</span><span class="sxs-lookup"><span data-stu-id="9a519-196">This parameter should be set in units of 1024 bytes (e.g. a setting of 2048 will give 2MB logfiles).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-198"><a href="dn350993(v=exchg.10).md">MaxCursors</a></span><span class="sxs-lookup"><span data-stu-id="9a519-198"><a href="dn350993(v=exchg.10).md">MaxCursors</a></span></span></td>
<td><span data-ttu-id="9a519-199">取得或設定保留給這個實例的資料指標資源數目。</span><span class="sxs-lookup"><span data-stu-id="9a519-199">Gets or sets the number of cursor resources reserved for this instance.</span></span> <span data-ttu-id="9a519-200">資料指標資源會直接對應至 JET_TABLEID。</span><span class="sxs-lookup"><span data-stu-id="9a519-200">A cursor resource directly corresponds to a JET_TABLEID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-202"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span><span class="sxs-lookup"><span data-stu-id="9a519-202"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span></span></td>
<td><span data-ttu-id="9a519-203">取得或設定保留給此實例的 B + 樹系資源數目。</span><span class="sxs-lookup"><span data-stu-id="9a519-203">Gets or sets the number of B+ Tree resources reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-205"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span><span class="sxs-lookup"><span data-stu-id="9a519-205"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span></span></td>
<td><span data-ttu-id="9a519-206">取得或設定保留給此實例的會話資源數目。</span><span class="sxs-lookup"><span data-stu-id="9a519-206">Gets or sets the number of sessions resources reserved for this instance.</span></span> <span data-ttu-id="9a519-207">會話資源直接對應至 JET_SESID。</span><span class="sxs-lookup"><span data-stu-id="9a519-207">A session resource directly corresponds to a JET_SESID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-209"><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></span><span class="sxs-lookup"><span data-stu-id="9a519-209"><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></span></span></td>
<td><span data-ttu-id="9a519-210">取得或設定實例所使用之臨時表資源的數目。</span><span class="sxs-lookup"><span data-stu-id="9a519-210">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="9a519-211">此設定會影響可同時使用的臨時表數目。</span><span class="sxs-lookup"><span data-stu-id="9a519-211">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="9a519-212">如果這個系統參數設定為零，則不會建立暫存資料庫，而且任何需要使用暫存資料庫的活動都將會失敗。</span><span class="sxs-lookup"><span data-stu-id="9a519-212">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="9a519-213">這項設定有助於避免建立暫存資料庫所需的 i/o （如果已知不會使用）。</span><span class="sxs-lookup"><span data-stu-id="9a519-213">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-215"><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></span><span class="sxs-lookup"><span data-stu-id="9a519-215"><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></span></span></td>
<td><span data-ttu-id="9a519-216">取得或設定在 <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (預設值 = 100) 之前，可供最舊交易使用的版本存放區百分比。</span><span class="sxs-lookup"><span data-stu-id="9a519-216">Gets or sets the percentage of version store that can be used by oldest transaction before <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-218"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span><span class="sxs-lookup"><span data-stu-id="9a519-218"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span></span></td>
<td><span data-ttu-id="9a519-219">取得或設定保留給此實例的版本存放區頁面數目上限。</span><span class="sxs-lookup"><span data-stu-id="9a519-219">Gets or sets the maximum number of version store pages reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-221"><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></span><span class="sxs-lookup"><span data-stu-id="9a519-221"><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></span></span></td>
<td><span data-ttu-id="9a519-222">取得或設定值，這個值表示是否會隱藏資料庫引擎通常會產生的資訊事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="9a519-222">Gets or sets a value indicating whether informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-224"><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></span><span class="sxs-lookup"><span data-stu-id="9a519-224"><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></span></span></td>
<td><span data-ttu-id="9a519-225">取得或設定值，這個值表示一次是否允許指定的會話使用 JetOpenDatabase 來開啟單一資料庫。</span><span class="sxs-lookup"><span data-stu-id="9a519-225">Gets or sets a value indicating whether only one database is allowed to be opened using JetOpenDatabase by a given session at one time.</span></span> <span data-ttu-id="9a519-226">這項限制會排除暫存資料庫。</span><span class="sxs-lookup"><span data-stu-id="9a519-226">The temporary database is excluded from this restriction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-228"><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></span><span class="sxs-lookup"><span data-stu-id="9a519-228"><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></span></span></td>
<td><span data-ttu-id="9a519-229">取得或設定暫存資料庫的初始大小。</span><span class="sxs-lookup"><span data-stu-id="9a519-229">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="9a519-230">大小是在資料庫頁面中。</span><span class="sxs-lookup"><span data-stu-id="9a519-230">The size is in database pages.</span></span> <span data-ttu-id="9a519-231">大小為零表示應該使用一般資料庫的預設大小。</span><span class="sxs-lookup"><span data-stu-id="9a519-231">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="9a519-232">小型應用程式通常需要將暫存資料庫設定為盡可能小。</span><span class="sxs-lookup"><span data-stu-id="9a519-232">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="9a519-233">將此參數設定為 <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> ，可以達到最小的暫存資料庫。</span><span class="sxs-lookup"><span data-stu-id="9a519-233">Setting this parameter to <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> will achieve the smallest temporary database possible.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-235"><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></span><span class="sxs-lookup"><span data-stu-id="9a519-235"><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></span></span></td>
<td><span data-ttu-id="9a519-236">取得或設定保留給此實例之版本存放區頁面的慣用數目。</span><span class="sxs-lookup"><span data-stu-id="9a519-236">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="9a519-237">如果版本存放區的大小超過此臨界值，則只會針對選擇性的背景工作（例如回收資料庫中已刪除的空間）使用任何資訊，而不會犧牲保存交易資訊的空間。</span><span class="sxs-lookup"><span data-stu-id="9a519-237">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-239"><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></span><span class="sxs-lookup"><span data-stu-id="9a519-239"><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></span></span></td>
<td><span data-ttu-id="9a519-240">取得或設定針對指定用途分派的 i/o 作業數目上限。</span><span class="sxs-lookup"><span data-stu-id="9a519-240">Gets or sets the maximum number of I/O operations dispatched for a given purpose.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-242"><a href="dn350981(v=exchg.10).md">復原</a></span><span class="sxs-lookup"><span data-stu-id="9a519-242"><a href="dn350981(v=exchg.10).md">Recovery</a></span></span></td>
<td><span data-ttu-id="9a519-243">取得或設定值，指出是否開啟損毀復原。</span><span class="sxs-lookup"><span data-stu-id="9a519-243">Gets or sets a value indicating whether crash recovery is on.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-245"><a href="dn351007(v=exchg.10).md">SystemDirectory</a></span><span class="sxs-lookup"><span data-stu-id="9a519-245"><a href="dn351007(v=exchg.10).md">SystemDirectory</a></span></span></td>
<td><span data-ttu-id="9a519-246">取得或設定資料夾的相對或絕對檔案系統路徑，其中將包含實例的檢查點檔案。</span><span class="sxs-lookup"><span data-stu-id="9a519-246">Gets or sets the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-248"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span><span class="sxs-lookup"><span data-stu-id="9a519-248"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span></span></td>
<td><span data-ttu-id="9a519-249">取得或設定資料夾的相對或絕對檔案系統路徑，其中將包含實例的暫存資料庫。</span><span class="sxs-lookup"><span data-stu-id="9a519-249">Gets or sets the relative or absolute file system path of the folder that will contain the temporary database for the instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-251"><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></span><span class="sxs-lookup"><span data-stu-id="9a519-251"><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></span></span></td>
<td><span data-ttu-id="9a519-252">取得或設定可在任何時間佇列至資料庫引擎執行緒集區的背景清除工作專案數目。</span><span class="sxs-lookup"><span data-stu-id="9a519-252">Gets or sets the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9a519-254"><a href="dn350985(v=exchg.10).md">WaypointLatency</a></span><span class="sxs-lookup"><span data-stu-id="9a519-254"><a href="dn350985(v=exchg.10).md">WaypointLatency</a></span></span></td>
<td><span data-ttu-id="9a519-255">取得或設定 esent 將延遲資料庫排清之記錄檔的數目。</span><span class="sxs-lookup"><span data-stu-id="9a519-255">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="9a519-256">如果失敗導致記錄檔遺失，這可以用來提高資料庫復原能力。</span><span class="sxs-lookup"><span data-stu-id="9a519-256">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="9a519-257">Windows 7 和更新的支援。</span><span class="sxs-lookup"><span data-stu-id="9a519-257">Supported on Windows 7 and up.</span></span> <span data-ttu-id="9a519-258">在 Windows XP、Windows Server 2003、Windows Vista 和 Windows Server 2008 上略過。</span><span class="sxs-lookup"><span data-stu-id="9a519-258">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9a519-259">頁首</span><span class="sxs-lookup"><span data-stu-id="9a519-259">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="9a519-260">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a519-260">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9a519-261">參考</span><span class="sxs-lookup"><span data-stu-id="9a519-261">Reference</span></span>

[<span data-ttu-id="9a519-262">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="9a519-262">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="9a519-263">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9a519-263">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
