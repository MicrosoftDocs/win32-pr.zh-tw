---
description: 深入瞭解： EsentStopwatch 成員
title: EsentStopwatch 成員
TOCTitle: EsentStopwatch members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.EsentStopwatch
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch_members(v=EXCHG.10)
ms:contentKeyID: 55102990
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 36f9d619e104b7d271782c3765adea744beb950e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693967"
---
# <a name="esentstopwatch-members"></a><span data-ttu-id="0f7fe-103">EsentStopwatch 成員</span><span class="sxs-lookup"><span data-stu-id="0f7fe-103">EsentStopwatch members</span></span>

<span data-ttu-id="0f7fe-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="0f7fe-104">Include protected members</span></span>  
<span data-ttu-id="0f7fe-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="0f7fe-105">Include inherited members</span></span>  

<span data-ttu-id="0f7fe-106">提供一組方法和屬性，您可以使用這些方法和屬性來測量執行緒的 ESENT 工作統計資料。</span><span class="sxs-lookup"><span data-stu-id="0f7fe-106">Provides a set of methods and properties that you can use to measure ESENT work statistics for a thread.</span></span> <span data-ttu-id="0f7fe-107">如果最新版本的 ESENT 不支援 [JetGetThreadStats (JET_THREADSTATS) ](./vistaapi.jetgetthreadstats-method.md) 那麼所有 ESENT 統計資料都會是0。</span><span class="sxs-lookup"><span data-stu-id="0f7fe-107">If the current version of ESENT doesn't support [JetGetThreadStats(JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) then all ESENT statistics will be 0.</span></span>

<span data-ttu-id="0f7fe-108">[EsentStopwatch](./esentstopwatch-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="0f7fe-108">The [EsentStopwatch](./esentstopwatch-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="0f7fe-109">建構函式</span><span class="sxs-lookup"><span data-stu-id="0f7fe-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0f7fe-110">名稱</span><span class="sxs-lookup"><span data-stu-id="0f7fe-110">Name</span></span></th>
<th><span data-ttu-id="0f7fe-111">描述</span><span class="sxs-lookup"><span data-stu-id="0f7fe-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0f7fe-113"><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-113"><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0f7fe-114">頁首</span><span class="sxs-lookup"><span data-stu-id="0f7fe-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="0f7fe-115">屬性</span><span class="sxs-lookup"><span data-stu-id="0f7fe-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0f7fe-116">名稱</span><span class="sxs-lookup"><span data-stu-id="0f7fe-116">Name</span></span></th>
<th><span data-ttu-id="0f7fe-117">描述</span><span class="sxs-lookup"><span data-stu-id="0f7fe-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0f7fe-119"><a href="dn334934(v=exchg.10).md">過去了</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-119"><a href="dn334934(v=exchg.10).md">Elapsed</a></span></span></td>
<td><span data-ttu-id="0f7fe-120">取得目前執行個體所測量的已耗用時間總和。</span><span class="sxs-lookup"><span data-stu-id="0f7fe-120">Gets the total elapsed time measured by the current instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0f7fe-122"><a href="dn334933(v=exchg.10).md">IsRunning</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-122"><a href="dn334933(v=exchg.10).md">IsRunning</a></span></span></td>
<td><span data-ttu-id="0f7fe-123">取得值，指出 EsentStopwatch 計時器是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="0f7fe-123">Gets a value indicating whether the EsentStopwatch timer is running.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0f7fe-125"><a href="dn334930(v=exchg.10).md">ThreadStats</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-125"><a href="dn334930(v=exchg.10).md">ThreadStats</a></span></span></td>
<td><span data-ttu-id="0f7fe-126">取得目前實例所測量的總 ESENT 工作統計資料。</span><span class="sxs-lookup"><span data-stu-id="0f7fe-126">Gets the total ESENT work stats measured by the current instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0f7fe-127">頁首</span><span class="sxs-lookup"><span data-stu-id="0f7fe-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="0f7fe-128">方法</span><span class="sxs-lookup"><span data-stu-id="0f7fe-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0f7fe-129">名稱</span><span class="sxs-lookup"><span data-stu-id="0f7fe-129">Name</span></span></th>
<th><span data-ttu-id="0f7fe-130">描述</span><span class="sxs-lookup"><span data-stu-id="0f7fe-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0f7fe-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="0f7fe-133"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="0f7fe-133">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="0f7fe-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="0f7fe-136"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="0f7fe-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0f7fe-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="0f7fe-139"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="0f7fe-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0f7fe-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="0f7fe-142"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="0f7fe-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="0f7fe-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="0f7fe-145"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="0f7fe-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0f7fe-147"><a href="dn334869(v=exchg.10).md">重設</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-147"><a href="dn334869(v=exchg.10).md">Reset</a></span></span></td>
<td><span data-ttu-id="0f7fe-148">停止時間間隔測量，並重設執行緒統計資料。</span><span class="sxs-lookup"><span data-stu-id="0f7fe-148">Stops time interval measurement and resets the thread statistics.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0f7fe-150"><a href="dn334931(v=exchg.10).md">開始</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-150"><a href="dn334931(v=exchg.10).md">Start</a></span></span></td>
<td><span data-ttu-id="0f7fe-151">開始測量 ESENT 工作。</span><span class="sxs-lookup"><span data-stu-id="0f7fe-151">Starts measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="0f7fe-154"><a href="dn334877(v=exchg.10).md">System.threading.tasks.taskfactory.startnew</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span></span></td>
<td><span data-ttu-id="0f7fe-155">初始化新的 EsentStopwatch 實例，並開始測量經過的時間。</span><span class="sxs-lookup"><span data-stu-id="0f7fe-155">Initializes a new EsentStopwatch instance and starts measuring elapsed time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0f7fe-157"><a href="dn334932(v=exchg.10).md">停止</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-157"><a href="dn334932(v=exchg.10).md">Stop</a></span></span></td>
<td><span data-ttu-id="0f7fe-158">停止測量 ESENT 工作。</span><span class="sxs-lookup"><span data-stu-id="0f7fe-158">Stops measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0f7fe-160"><a href="dn334873(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="0f7fe-160"><a href="dn334873(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="0f7fe-161">傳回 <a href="/dotnet/api/system.string">字串</a> ， <a href="/dotnet/api/system.diagnostics.stopwatch">表示目前的</a>馬錶。</span><span class="sxs-lookup"><span data-stu-id="0f7fe-161">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="/dotnet/api/system.diagnostics.stopwatch">Stopwatch</a>.</span></span> <span data-ttu-id="0f7fe-162"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="0f7fe-162">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0f7fe-163">頁首</span><span class="sxs-lookup"><span data-stu-id="0f7fe-163">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="0f7fe-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f7fe-164">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0f7fe-165">參考</span><span class="sxs-lookup"><span data-stu-id="0f7fe-165">Reference</span></span>

[<span data-ttu-id="0f7fe-166">EsentStopwatch 類別</span><span class="sxs-lookup"><span data-stu-id="0f7fe-166">EsentStopwatch class</span></span>](./esentstopwatch-class.md)

[<span data-ttu-id="0f7fe-167">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0f7fe-167">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
