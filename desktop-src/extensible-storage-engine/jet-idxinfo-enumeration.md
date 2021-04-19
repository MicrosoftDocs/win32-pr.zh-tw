---
description: 深入瞭解： JET_IdxInfo 列舉
title: JET_IdxInfo 列舉
TOCTitle: JET_IdxInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_IdxInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_idxinfo(v=EXCHG.10)
ms:contentKeyID: 39512789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1f2cb50537ed492a428c82fd9a6f6541c5fad2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988423"
---
# <a name="jet_idxinfo-enumeration"></a><span data-ttu-id="9b787-103">JET_IdxInfo 列舉</span><span class="sxs-lookup"><span data-stu-id="9b787-103">JET_IdxInfo enumeration</span></span>

<span data-ttu-id="9b787-104">使用 JetGetIndexInfo 取得索引資訊的資訊層級。</span><span class="sxs-lookup"><span data-stu-id="9b787-104">Info levels for retrieve index information with JetGetIndexInfo.</span></span> <span data-ttu-id="9b787-105">和 JetGetTableIndexInfo。</span><span class="sxs-lookup"><span data-stu-id="9b787-105">and JetGetTableIndexInfo.</span></span>

<span data-ttu-id="9b787-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9b787-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9b787-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="9b787-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9b787-108">語法</span><span class="sxs-lookup"><span data-stu-id="9b787-108">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_IdxInfo
'Usage
Dim instance As JET_IdxInfo
```

``` csharp
public enum JET_IdxInfo
```

## <a name="members"></a><span data-ttu-id="9b787-109">成員</span><span class="sxs-lookup"><span data-stu-id="9b787-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="9b787-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="9b787-110">Member name</span></span></th>
<th><span data-ttu-id="9b787-111">描述</span><span class="sxs-lookup"><span data-stu-id="9b787-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9b787-112">預設</span><span class="sxs-lookup"><span data-stu-id="9b787-112">Default</span></span></td>
<td><span data-ttu-id="9b787-113">傳回包含索引相關資訊的 <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="9b787-113">Returns a <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> structure with information about the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9b787-114">List</span><span class="sxs-lookup"><span data-stu-id="9b787-114">List</span></span></td>
<td><span data-ttu-id="9b787-115">傳回包含索引相關資訊的 <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> 結構。</span><span class="sxs-lookup"><span data-stu-id="9b787-115">Returns a <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> structure with information about the index.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9b787-116">SysTabCursor</span><span class="sxs-lookup"><span data-stu-id="9b787-116">SysTabCursor</span></span></td>
<td><span data-ttu-id="9b787-117"><strong>已淘汰。</strong></span><span class="sxs-lookup"><span data-stu-id="9b787-117"><strong>Obsolete.</strong></span></span> <span data-ttu-id="9b787-118">SysTabCursor 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="9b787-118">SysTabCursor is obsolete.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9b787-119">OLC</span><span class="sxs-lookup"><span data-stu-id="9b787-119">OLC</span></span></td>
<td><span data-ttu-id="9b787-120"><strong>已淘汰。</strong></span><span class="sxs-lookup"><span data-stu-id="9b787-120"><strong>Obsolete.</strong></span></span> <span data-ttu-id="9b787-121">OLC 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="9b787-121">OLC is obsolete.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9b787-122">ResetOLC</span><span class="sxs-lookup"><span data-stu-id="9b787-122">ResetOLC</span></span></td>
<td><span data-ttu-id="9b787-123"><strong>已淘汰。</strong></span><span class="sxs-lookup"><span data-stu-id="9b787-123"><strong>Obsolete.</strong></span></span> <span data-ttu-id="9b787-124">重設 OLC 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="9b787-124">Reset OLC is obsolete.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9b787-125">SpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="9b787-125">SpaceAlloc</span></span></td>
<td><span data-ttu-id="9b787-126">傳回具有索引空間使用量的整數。</span><span class="sxs-lookup"><span data-stu-id="9b787-126">Returns an integer with the space usage of the index.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9b787-127">LCID</span><span class="sxs-lookup"><span data-stu-id="9b787-127">LCID</span></span></td>
<td><span data-ttu-id="9b787-128">傳回具有索引 LCID 的整數。</span><span class="sxs-lookup"><span data-stu-id="9b787-128">Returns an integer with the LCID of the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9b787-129">Langid</span><span class="sxs-lookup"><span data-stu-id="9b787-129">Langid</span></span></td>
<td><span data-ttu-id="9b787-130"><strong>已淘汰。</strong></span><span class="sxs-lookup"><span data-stu-id="9b787-130"><strong>Obsolete.</strong></span></span> <span data-ttu-id="9b787-131">Langid 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="9b787-131">Langid is obsolete.</span></span> <span data-ttu-id="9b787-132">請改用 LCID。</span><span class="sxs-lookup"><span data-stu-id="9b787-132">Use LCID instead.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9b787-133">Count</span><span class="sxs-lookup"><span data-stu-id="9b787-133">Count</span></span></td>
<td><span data-ttu-id="9b787-134">傳回包含資料表中索引計數的整數。</span><span class="sxs-lookup"><span data-stu-id="9b787-134">Returns an integer with the count of indexes in the table.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9b787-135">VarSegMac</span><span class="sxs-lookup"><span data-stu-id="9b787-135">VarSegMac</span></span></td>
<td><span data-ttu-id="9b787-136">傳回具有以 cbVarSegMac 建立索引之值的 ushort。</span><span class="sxs-lookup"><span data-stu-id="9b787-136">Returns a ushort with the value of cbVarSegMac the index was created with.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9b787-137">IndexId</span><span class="sxs-lookup"><span data-stu-id="9b787-137">IndexId</span></span></td>
<td><span data-ttu-id="9b787-138">傳回識別索引的 <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> 。</span><span class="sxs-lookup"><span data-stu-id="9b787-138">Returns a <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> identifying the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9b787-139">KeyMost</span><span class="sxs-lookup"><span data-stu-id="9b787-139">KeyMost</span></span></td>
<td><span data-ttu-id="9b787-140">在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="9b787-140">Introduced in Windows Vista.</span></span> <span data-ttu-id="9b787-141">傳回具有以 cbKeyMost 建立索引之值的 ushort。</span><span class="sxs-lookup"><span data-stu-id="9b787-141">Returns a ushort with the value of cbKeyMost the index was created with.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="9b787-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b787-142">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9b787-143">參考</span><span class="sxs-lookup"><span data-stu-id="9b787-143">Reference</span></span>

[<span data-ttu-id="9b787-144">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9b787-144">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
