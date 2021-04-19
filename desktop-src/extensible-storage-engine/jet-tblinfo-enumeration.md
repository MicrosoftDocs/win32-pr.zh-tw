---
description: 深入瞭解： JET_TblInfo 列舉
title: JET_TblInfo 列舉
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad43dcecf65fdc9fb8dd53bdf686a077e6bdfa8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981605"
---
# <a name="jet_tblinfo-enumeration"></a><span data-ttu-id="9b344-103">JET_TblInfo 列舉</span><span class="sxs-lookup"><span data-stu-id="9b344-103">JET_TblInfo enumeration</span></span>

<span data-ttu-id="9b344-104">使用 JetGetTableInfo 來抓取資料表資訊的資訊層級。</span><span class="sxs-lookup"><span data-stu-id="9b344-104">Info levels for retrieving table info with JetGetTableInfo.</span></span>

<span data-ttu-id="9b344-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9b344-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9b344-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="9b344-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9b344-107">語法</span><span class="sxs-lookup"><span data-stu-id="9b344-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
```

## <a name="members"></a><span data-ttu-id="9b344-108">成員</span><span class="sxs-lookup"><span data-stu-id="9b344-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="9b344-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="9b344-109">Member name</span></span></th>
<th><span data-ttu-id="9b344-110">描述</span><span class="sxs-lookup"><span data-stu-id="9b344-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9b344-111">預設</span><span class="sxs-lookup"><span data-stu-id="9b344-111">Default</span></span></td>
<td><span data-ttu-id="9b344-112">預設選項。</span><span class="sxs-lookup"><span data-stu-id="9b344-112">Default option.</span></span> <span data-ttu-id="9b344-113">抓取 <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> ，其中包含資料表的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b344-113">Retrieves a <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> containing information about the table.</span></span> <span data-ttu-id="9b344-114">使用這個選項搭配 <a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、JET_OBJECTINFO JET_TblInfo) </a>。</span><span class="sxs-lookup"><span data-stu-id="9b344-114">Use this option with <a href="dn292198(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9b344-115">Name</span><span class="sxs-lookup"><span data-stu-id="9b344-115">Name</span></span></td>
<td><span data-ttu-id="9b344-116">抓取資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b344-116">Retrieves the name of the table.</span></span> <span data-ttu-id="9b344-117">使用這個選項搭配 <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、字串、JET_TblInfo) </a>。</span><span class="sxs-lookup"><span data-stu-id="9b344-117">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9b344-118">Dbid</span><span class="sxs-lookup"><span data-stu-id="9b344-118">Dbid</span></span></td>
<td><span data-ttu-id="9b344-119">抓取包含資料表之資料庫的 <a href="hh596176(v=exchg.10).md">JET_DBID</a> 。</span><span class="sxs-lookup"><span data-stu-id="9b344-119">Retrieves the <a href="hh596176(v=exchg.10).md">JET_DBID</a> of the database containing the table.</span></span> <span data-ttu-id="9b344-120">使用這個選項搭配 <a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、JET_DBID JET_TblInfo) </a>。</span><span class="sxs-lookup"><span data-stu-id="9b344-120">Use this option with <a href="dn292197(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9b344-121">SpaceUsage</span><span class="sxs-lookup"><span data-stu-id="9b344-121">SpaceUsage</span></span></td>
<td><span data-ttu-id="9b344-122">方法的行為取決於傳遞給方法的陣列大小。</span><span class="sxs-lookup"><span data-stu-id="9b344-122">The behavior of the method depends on how large the array that is passed to the method is.</span></span> <span data-ttu-id="9b344-123">陣列必須至少有兩個專案。</span><span class="sxs-lookup"><span data-stu-id="9b344-123">The array must have at least two entries.</span></span> <span data-ttu-id="9b344-124">第一個專案會包含資料表中擁有的範圍數目。</span><span class="sxs-lookup"><span data-stu-id="9b344-124">The first entry will contain the number of Owned Extents in the table.</span></span> <span data-ttu-id="9b344-125">第二個專案會包含資料表中可用範圍的數目。</span><span class="sxs-lookup"><span data-stu-id="9b344-125">The second entry will contain the number of Available Extents in the table.</span></span> <span data-ttu-id="9b344-126">如果陣列有兩個以上的專案，則緩衝區的剩餘位元組將由表示範圍清單的結構陣列所組成。</span><span class="sxs-lookup"><span data-stu-id="9b344-126">If the array has more than two entries then the remaining bytes of the buffer will consist of an array of structures that represent a list of extents.</span></span> <span data-ttu-id="9b344-127">此結構包含兩個成員：範圍中的最後一個頁碼和範圍中的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="9b344-127">This structure contains two members: the last page number in the extent and the number of pages in the extent.</span></span> <span data-ttu-id="9b344-128">使用這個選項搭配 <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、[]、JET_TblInfo) </a>。</span><span class="sxs-lookup"><span data-stu-id="9b344-128">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9b344-129">SpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="9b344-129">SpaceAlloc</span></span></td>
<td><span data-ttu-id="9b344-130">傳遞至 JetGetTableInfo 的陣列必須有兩個專案。</span><span class="sxs-lookup"><span data-stu-id="9b344-130">The array passed to JetGetTableInfo must have two entries.</span></span> <span data-ttu-id="9b344-131">第一個專案會設定為數據表中的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="9b344-131">The first entry will be set to the number of pages in the table.</span></span> <span data-ttu-id="9b344-132">第二個專案將會設定為數據表之頁面的目標密度。</span><span class="sxs-lookup"><span data-stu-id="9b344-132">The second entry will be set to the target density of pages for the table.</span></span> <span data-ttu-id="9b344-133">使用這個選項搭配 <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、[]、JET_TblInfo) </a>。</span><span class="sxs-lookup"><span data-stu-id="9b344-133">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9b344-134">SpaceOwned</span><span class="sxs-lookup"><span data-stu-id="9b344-134">SpaceOwned</span></span></td>
<td><span data-ttu-id="9b344-135">取得資料表中擁有的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="9b344-135">Gets the number of owned pages in the table.</span></span> <span data-ttu-id="9b344-136">使用這個選項搭配 <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、Int32、JET_TblInfo) </a>。</span><span class="sxs-lookup"><span data-stu-id="9b344-136">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9b344-137">SpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="9b344-137">SpaceAvailable</span></span></td>
<td><span data-ttu-id="9b344-138">取得資料表中可用的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="9b344-138">Gets the number of available pages in the table.</span></span> <span data-ttu-id="9b344-139">使用這個選項搭配 <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、Int32、JET_TblInfo) </a>。</span><span class="sxs-lookup"><span data-stu-id="9b344-139">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9b344-140">TemplateTableName</span><span class="sxs-lookup"><span data-stu-id="9b344-140">TemplateTableName</span></span></td>
<td><span data-ttu-id="9b344-141">如果資料表是衍生的資料表，則會以衍生資料表繼承其 DDL 的資料表名稱填入結果。</span><span class="sxs-lookup"><span data-stu-id="9b344-141">If the table is a derived table, the result will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="9b344-142">如果資料表不是衍生的資料表，則緩衝區將會是空字串。</span><span class="sxs-lookup"><span data-stu-id="9b344-142">If the table is not a derived table, the buffer will an empty string.</span></span> <span data-ttu-id="9b344-143">使用這個選項搭配 <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、字串、JET_TblInfo) </a>。</span><span class="sxs-lookup"><span data-stu-id="9b344-143">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="9b344-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b344-144">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9b344-145">參考</span><span class="sxs-lookup"><span data-stu-id="9b344-145">Reference</span></span>

[<span data-ttu-id="9b344-146">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9b344-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
