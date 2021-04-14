---
description: 深入瞭解： VistaParam 欄位
title: 'VistaParam fields (的欄位) '
TOCTitle: VistaParam fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_fields(v=EXCHG.10)
ms:contentKeyID: 55104336
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 6e20c4b784b9a4421c447f24d5736d7c6ef67f41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555835"
---
# <a name="vistaparam-fields"></a><span data-ttu-id="773d2-103">VistaParam 欄位</span><span class="sxs-lookup"><span data-stu-id="773d2-103">VistaParam fields</span></span>

<span data-ttu-id="773d2-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="773d2-104">Include protected members</span></span>  
<span data-ttu-id="773d2-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="773d2-105">Include inherited members</span></span>  

<span data-ttu-id="773d2-106">[VistaParam](./vistaparam-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="773d2-106">The [VistaParam](./vistaparam-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="773d2-107">欄位</span><span class="sxs-lookup"><span data-stu-id="773d2-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="773d2-108">名稱</span><span class="sxs-lookup"><span data-stu-id="773d2-108">Name</span></span></th>
<th><span data-ttu-id="773d2-109">描述</span><span class="sxs-lookup"><span data-stu-id="773d2-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-112"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span><span class="sxs-lookup"><span data-stu-id="773d2-112"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="773d2-113">此參數會控制應用程式已關閉實例所代表的資料表之後，該實例所快取的 B + 樹系資源數目。</span><span class="sxs-lookup"><span data-stu-id="773d2-113">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="773d2-114">此參數的大型值會導致資料庫引擎使用更多記憶體，但會增加應用程式隨機開啟大量資料表的速度。</span><span class="sxs-lookup"><span data-stu-id="773d2-114">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="773d2-115">對於具有極大量資料表之架構的應用程式而言，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="773d2-115">This is useful for applications that have a schema with a very large number of tables.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-118"><a href="dn335289(v=exchg.10).md">Configuration</a></span><span class="sxs-lookup"><span data-stu-id="773d2-118"><a href="dn335289(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="773d2-119">此參數會針對整組系統參數公開多組預設值。</span><span class="sxs-lookup"><span data-stu-id="773d2-119">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="773d2-120">當此參數設定為特定設定時，所有系統參數值都會重設為該設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="773d2-120">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="773d2-121">如果設定特定實例的設定，則全域系統參數將不會重設為其預設值。</span><span class="sxs-lookup"><span data-stu-id="773d2-121">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="773d2-122">Small Configuration (0) ：資料庫引擎已針對記憶體使用量優化。</span><span class="sxs-lookup"><span data-stu-id="773d2-122">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="773d2-123">舊版設定 (1) ：資料庫引擎有其傳統預設值。</span><span class="sxs-lookup"><span data-stu-id="773d2-123">Legacy Configuration (1): The database engine has its traditional defaults.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-126"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span><span class="sxs-lookup"><span data-stu-id="773d2-126"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="773d2-127">這個參數是用來控制 database engine 接受或拒絕系統參數子集之變更的時間。</span><span class="sxs-lookup"><span data-stu-id="773d2-127">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="773d2-128">此參數會搭配 <a href="dn335289(v=exchg.10).md">設定使用，以防止</a> 某些系統參數從選取的設定的預設值中退出。</span><span class="sxs-lookup"><span data-stu-id="773d2-128">This parameter is used in conjunction with <a href="dn335289(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-131"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span><span class="sxs-lookup"><span data-stu-id="773d2-131"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="773d2-132">啟用所有受管理檔案的 OS 檔案快取。</span><span class="sxs-lookup"><span data-stu-id="773d2-132">Enable the use of the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-135"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span><span class="sxs-lookup"><span data-stu-id="773d2-135"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="773d2-136">啟用資料庫檔案的記憶體對應檔案 i/o。</span><span class="sxs-lookup"><span data-stu-id="773d2-136">Enable the use of memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-139"><a href="dn335292(v=exchg.10).md">KeyMost</a></span><span class="sxs-lookup"><span data-stu-id="773d2-139"><a href="dn335292(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="773d2-140">這個唯讀參數表示可針對目前資料庫頁面大小選取的最大可允許索引鍵長度， (如 <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>) 所設定。</span><span class="sxs-lookup"><span data-stu-id="773d2-140">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-143"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span><span class="sxs-lookup"><span data-stu-id="773d2-143"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="773d2-144">此參數提供舊版資料庫引擎的檔案命名慣例回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="773d2-144">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-147"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-147"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span></span></td>
<td><span data-ttu-id="773d2-148">設定與資料表類別10相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-148">Set the name associated with table class 10.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-151"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-151"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span></span></td>
<td><span data-ttu-id="773d2-152">設定與資料表類別11相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-152">Set the name associated with table class 11.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-155"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-155"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span></span></td>
<td><span data-ttu-id="773d2-156">設定與資料表類別12相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-156">Set the name associated with table class 12.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-159"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-159"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span></span></td>
<td><span data-ttu-id="773d2-160">設定與資料表類別13相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-160">Set the name associated with table class 13.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-163"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-163"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span></span></td>
<td><span data-ttu-id="773d2-164">設定與資料表類別14相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-164">Set the name associated with table class 14.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-167"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-167"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span></span></td>
<td><span data-ttu-id="773d2-168">設定與資料表類別15相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-168">Set the name associated with table class 15.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-171"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-171"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span></span></td>
<td><span data-ttu-id="773d2-172">設定與資料表類別1相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-172">Set the name associated with table class 1.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-175"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-175"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span></span></td>
<td><span data-ttu-id="773d2-176">設定與資料表類別2相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-176">Set the name associated with table class 2.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-179"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-179"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span></span></td>
<td><span data-ttu-id="773d2-180">設定與資料表類別3相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-180">Set the name associated with table class 3.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-183"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-183"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span></span></td>
<td><span data-ttu-id="773d2-184">設定與資料表類別4相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-184">Set the name associated with table class 4.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-187"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-187"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span></span></td>
<td><span data-ttu-id="773d2-188">設定與資料表類別5相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-188">Set the name associated with table class 5.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-191"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-191"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span></span></td>
<td><span data-ttu-id="773d2-192">設定與資料表類別6相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-192">Set the name associated with table class 6.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-195"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-195"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span></span></td>
<td><span data-ttu-id="773d2-196">設定與資料表類別7相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-196">Set the name associated with table class 7.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-199"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-199"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span></span></td>
<td><span data-ttu-id="773d2-200">設定與資料表類別8相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-200">Set the name associated with table class 8.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="773d2-203"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span><span class="sxs-lookup"><span data-stu-id="773d2-203"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span></span></td>
<td><span data-ttu-id="773d2-204">設定與資料表類別9相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="773d2-204">Set the name associated with table class 9.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="773d2-205">頁首</span><span class="sxs-lookup"><span data-stu-id="773d2-205">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="773d2-206">另請參閱</span><span class="sxs-lookup"><span data-stu-id="773d2-206">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="773d2-207">參考</span><span class="sxs-lookup"><span data-stu-id="773d2-207">Reference</span></span>

[<span data-ttu-id="773d2-208">VistaParam 類別</span><span class="sxs-lookup"><span data-stu-id="773d2-208">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="773d2-209">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="773d2-209">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
