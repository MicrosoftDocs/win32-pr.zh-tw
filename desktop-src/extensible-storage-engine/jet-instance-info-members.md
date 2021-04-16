---
description: 深入瞭解： JET_INSTANCE_INFO 成員
title: JET_INSTANCE_INFO 成員
TOCTitle: JET_INSTANCE_INFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info_members(v=EXCHG.10)
ms:contentKeyID: 55103693
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 42d9bcd2c078766875fc8230eaf83dc07fdb4b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565940"
---
# <a name="jet_instance_info-members"></a><span data-ttu-id="b828b-103">JET_INSTANCE_INFO 成員</span><span class="sxs-lookup"><span data-stu-id="b828b-103">JET_INSTANCE_INFO members</span></span>

<span data-ttu-id="b828b-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="b828b-104">Include protected members</span></span>  
<span data-ttu-id="b828b-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="b828b-105">Include inherited members</span></span>  

<span data-ttu-id="b828b-106">當搭配 JetGetInstanceInfo 和 JetOSSnapshotFreeze 函數使用時，接收有關執行中資料庫實例的資訊。</span><span class="sxs-lookup"><span data-stu-id="b828b-106">Receives information about running database instances when used with the JetGetInstanceInfo and JetOSSnapshotFreeze functions.</span></span>

<span data-ttu-id="b828b-107">[JET_INSTANCE_INFO](./jet-instance-info-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="b828b-107">The [JET_INSTANCE_INFO](./jet-instance-info-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="b828b-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b828b-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b828b-109">名稱</span><span class="sxs-lookup"><span data-stu-id="b828b-109">Name</span></span></th>
<th><span data-ttu-id="b828b-110">描述</span><span class="sxs-lookup"><span data-stu-id="b828b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="b828b-112"><a href="dn335189(v=exchg.10).md">cDatabases</a></span><span class="sxs-lookup"><span data-stu-id="b828b-112"><a href="dn335189(v=exchg.10).md">cDatabases</a></span></span></td>
<td><span data-ttu-id="b828b-113">取得附加至資料庫實例的資料庫數目。</span><span class="sxs-lookup"><span data-stu-id="b828b-113">Gets the number of databases that are attached to the database instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="b828b-115"><a href="dn335190(v=exchg.10).md">hInstanceId</a></span><span class="sxs-lookup"><span data-stu-id="b828b-115"><a href="dn335190(v=exchg.10).md">hInstanceId</a></span></span></td>
<td><span data-ttu-id="b828b-116">取得指定實例的 JET_INSTANCE。</span><span class="sxs-lookup"><span data-stu-id="b828b-116">Gets the JET_INSTANCE of the given instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="b828b-118"><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></span><span class="sxs-lookup"><span data-stu-id="b828b-118"><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></span></span></td>
<td><span data-ttu-id="b828b-119">取得字串的集合，每個字串都包含附加至資料庫實例的資料庫檔案名。</span><span class="sxs-lookup"><span data-stu-id="b828b-119">Gets a collection of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="b828b-120">陣列具有 cDatabases 元素。</span><span class="sxs-lookup"><span data-stu-id="b828b-120">The array has cDatabases elements.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="b828b-122"><a href="dn335194(v=exchg.10).md">szInstanceName</a></span><span class="sxs-lookup"><span data-stu-id="b828b-122"><a href="dn335194(v=exchg.10).md">szInstanceName</a></span></span></td>
<td><span data-ttu-id="b828b-123">取得資料庫實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="b828b-123">Gets the name of the database instance.</span></span> <span data-ttu-id="b828b-124">如果實例沒有名稱，這個值可以是 null。</span><span class="sxs-lookup"><span data-stu-id="b828b-124">This value can be null if the instance does not have a name.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b828b-125">頁首</span><span class="sxs-lookup"><span data-stu-id="b828b-125">Top</span></span>

## <a name="methods"></a><span data-ttu-id="b828b-126">方法</span><span class="sxs-lookup"><span data-stu-id="b828b-126">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b828b-127">名稱</span><span class="sxs-lookup"><span data-stu-id="b828b-127">Name</span></span></th>
<th><span data-ttu-id="b828b-128">描述</span><span class="sxs-lookup"><span data-stu-id="b828b-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="b828b-130"><a href="dn335184(v=exchg.10).md">等於 (物件) </a></span><span class="sxs-lookup"><span data-stu-id="b828b-130"><a href="dn335184(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="b828b-131">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="b828b-131">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="b828b-132"> (覆寫 <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_"> (物件) 的 Equals </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="b828b-132">(Overrides <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="b828b-134"><a href="dn335187(v=exchg.10).md">等於 (JET_INSTANCE_INFO) </a></span><span class="sxs-lookup"><span data-stu-id="b828b-134"><a href="dn335187(v=exchg.10).md">Equals(JET_INSTANCE_INFO)</a></span></span></td>
<td><span data-ttu-id="b828b-135">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="b828b-135">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="b828b-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="b828b-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="b828b-138"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="b828b-138">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="b828b-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="b828b-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="b828b-141">傳回這個執行個體的雜湊碼。</span><span class="sxs-lookup"><span data-stu-id="b828b-141">Returns the hash code for this instance.</span></span> <span data-ttu-id="b828b-142"> (覆寫 <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="b828b-142">(Overrides <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="b828b-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="b828b-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="b828b-145"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="b828b-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="b828b-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="b828b-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="b828b-148"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="b828b-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="b828b-150"><a href="dn335192(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="b828b-150"><a href="dn335192(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="b828b-151">產生實例的字串表示。</span><span class="sxs-lookup"><span data-stu-id="b828b-151">Generate a string representation of the instance.</span></span> <span data-ttu-id="b828b-152"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="b828b-152">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b828b-153">頁首</span><span class="sxs-lookup"><span data-stu-id="b828b-153">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="b828b-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b828b-154">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b828b-155">參考</span><span class="sxs-lookup"><span data-stu-id="b828b-155">Reference</span></span>

[<span data-ttu-id="b828b-156">JET_INSTANCE_INFO 類別</span><span class="sxs-lookup"><span data-stu-id="b828b-156">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="b828b-157">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b828b-157">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
