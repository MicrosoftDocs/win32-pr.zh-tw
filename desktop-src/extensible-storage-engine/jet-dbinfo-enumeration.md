---
description: 深入瞭解： JET_DbInfo 列舉
title: JET_DbInfo 列舉
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39c6c3175c08e4f7644ad4f0b41137e12e84f71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972628"
---
# <a name="jet_dbinfo-enumeration"></a><span data-ttu-id="432ca-103">JET_DbInfo 列舉</span><span class="sxs-lookup"><span data-stu-id="432ca-103">JET_DbInfo enumeration</span></span>

<span data-ttu-id="432ca-104">用於抓取資料庫資訊的資訊層級。</span><span class="sxs-lookup"><span data-stu-id="432ca-104">Info levels for retrieving database info.</span></span>

<span data-ttu-id="432ca-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="432ca-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="432ca-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="432ca-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="432ca-107">語法</span><span class="sxs-lookup"><span data-stu-id="432ca-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
```

## <a name="members"></a><span data-ttu-id="432ca-108">成員</span><span class="sxs-lookup"><span data-stu-id="432ca-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="432ca-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="432ca-109">Member name</span></span></th>
<th><span data-ttu-id="432ca-110">說明</span><span class="sxs-lookup"><span data-stu-id="432ca-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="432ca-111">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="432ca-111">Filename</span></span></td>
<td><span data-ttu-id="432ca-112">傳回資料庫檔案的路徑， (字串) 。</span><span class="sxs-lookup"><span data-stu-id="432ca-112">Returns the path to the database file (string).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="432ca-113">LCID</span><span class="sxs-lookup"><span data-stu-id="432ca-113">LCID</span></span></td>
<td><span data-ttu-id="432ca-114">傳回與這個資料庫相關聯的地區設定識別碼 (LCID)  (Int32) 。</span><span class="sxs-lookup"><span data-stu-id="432ca-114">Returns the locale identifier (LCID) associated with this database (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="432ca-115">選項</span><span class="sxs-lookup"><span data-stu-id="432ca-115">Options</span></span></td>
<td><span data-ttu-id="432ca-116">傳回 <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>。</span><span class="sxs-lookup"><span data-stu-id="432ca-116">Returns a <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>.</span></span> <span data-ttu-id="432ca-117">這會指出資料庫是否在獨佔模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="432ca-117">This indicates whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="432ca-118">如果資料庫處於獨佔模式，則會傳回 <a href="hh579532(v=exchg.10).md">獨佔</a> ，否則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="432ca-118">If the database is in exclusive mode then <a href="hh579532(v=exchg.10).md">Exclusive</a> will be returned, otherwise zero is returned.</span></span> <span data-ttu-id="432ca-119">不會傳回 JetAttachDatabase 和 JetOpenDatabase 的其他資料庫 grbit 選項。</span><span class="sxs-lookup"><span data-stu-id="432ca-119">Other database grbit options for JetAttachDatabase and JetOpenDatabase are not returned.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="432ca-120">交易</span><span class="sxs-lookup"><span data-stu-id="432ca-120">Transactions</span></span></td>
<td><span data-ttu-id="432ca-121">傳回一個大於最大層級的數位，可將交易進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="432ca-121">Returns a number one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="432ca-122">如果以嵌套方式 (呼叫 <a href="dn292105(v=exchg.10).md">JetBeginTransaction (JET_SESID) </a> ，也就是在相同的會話上，如果沒有認可或復原) 與此值多次相同，則會傳回 (Int32) 的最後一個呼叫 <a href="hh564840(v=exchg.10).md">TransTooDeep</a> 。</span><span class="sxs-lookup"><span data-stu-id="432ca-122">If <a href="dn292105(v=exchg.10).md">JetBeginTransaction(JET_SESID)</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call <a href="hh564840(v=exchg.10).md">TransTooDeep</a> will be returned (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="432ca-123">版本</span><span class="sxs-lookup"><span data-stu-id="432ca-123">Version</span></span></td>
<td><span data-ttu-id="432ca-124">傳回資料庫引擎的主要版本 (Int32) 。</span><span class="sxs-lookup"><span data-stu-id="432ca-124">Returns the major version of the database engine (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="432ca-125">Filesize</span><span class="sxs-lookup"><span data-stu-id="432ca-125">Filesize</span></span></td>
<td><span data-ttu-id="432ca-126">傳回資料庫的 filesize，以 pages (Int32) 。</span><span class="sxs-lookup"><span data-stu-id="432ca-126">Returns the filesize of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="432ca-127">SpaceOwned</span><span class="sxs-lookup"><span data-stu-id="432ca-127">SpaceOwned</span></span></td>
<td><span data-ttu-id="432ca-128">傳回資料庫的擁有空間，以 pages (Int32) 。</span><span class="sxs-lookup"><span data-stu-id="432ca-128">Returns the owned space of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="432ca-129">SpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="432ca-129">SpaceAvailable</span></span></td>
<td><span data-ttu-id="432ca-130">傳回資料庫中的可用空間，以 pages (Int32) 。</span><span class="sxs-lookup"><span data-stu-id="432ca-130">Returns the available space in the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="432ca-131">其他</span><span class="sxs-lookup"><span data-stu-id="432ca-131">Misc</span></span></td>
<td><span data-ttu-id="432ca-132">傳回 <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> 物件。</span><span class="sxs-lookup"><span data-stu-id="432ca-132">Returns a <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> object.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="432ca-133">DBInUse</span><span class="sxs-lookup"><span data-stu-id="432ca-133">DBInUse</span></span></td>
<td><span data-ttu-id="432ca-134">傳回布林值，指出資料庫是否附加 (布林值) 。</span><span class="sxs-lookup"><span data-stu-id="432ca-134">Returns a boolean indicating whether the database is attached (boolean).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="432ca-135">PageSize</span><span class="sxs-lookup"><span data-stu-id="432ca-135">PageSize</span></span></td>
<td><span data-ttu-id="432ca-136">傳回資料庫 (Int32) 的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="432ca-136">Returns the page size of the database (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="432ca-137">FileType</span><span class="sxs-lookup"><span data-stu-id="432ca-137">FileType</span></span></td>
<td><span data-ttu-id="432ca-138">傳回資料庫 (<a href="hh566739(v=exchg.10).md">JET_filetype</a>) 的型別。</span><span class="sxs-lookup"><span data-stu-id="432ca-138">Returns the type of the database (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="432ca-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="432ca-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="432ca-140">參考</span><span class="sxs-lookup"><span data-stu-id="432ca-140">Reference</span></span>

[<span data-ttu-id="432ca-141">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="432ca-141">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
