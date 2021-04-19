---
description: 深入瞭解： CreateIndexGrbit 列舉
title: CreateIndexGrbit 列舉
TOCTitle: CreateIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39511957
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e7a03a077262485533e29690215be1468987e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997583"
---
# <a name="createindexgrbit-enumeration"></a><span data-ttu-id="e346e-103">CreateIndexGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="e346e-103">CreateIndexGrbit enumeration</span></span>

<span data-ttu-id="e346e-104">JetCreateIndex 的選項。</span><span class="sxs-lookup"><span data-stu-id="e346e-104">Options for JetCreateIndex.</span></span>

<span data-ttu-id="e346e-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="e346e-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="e346e-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e346e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e346e-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e346e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e346e-108">語法</span><span class="sxs-lookup"><span data-stu-id="e346e-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateIndexGrbit
'Usage
Dim instance As CreateIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateIndexGrbit
```

## <a name="members"></a><span data-ttu-id="e346e-109">成員</span><span class="sxs-lookup"><span data-stu-id="e346e-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e346e-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="e346e-110">Member name</span></span></th>
<th><span data-ttu-id="e346e-111">描述</span><span class="sxs-lookup"><span data-stu-id="e346e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e346e-112">無</span><span class="sxs-lookup"><span data-stu-id="e346e-112">None</span></span></td>
<td><span data-ttu-id="e346e-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="e346e-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e346e-114">IndexUnique</span><span class="sxs-lookup"><span data-stu-id="e346e-114">IndexUnique</span></span></td>
<td><span data-ttu-id="e346e-115">不允許有重複的索引項目 (索引鍵) 。</span><span class="sxs-lookup"><span data-stu-id="e346e-115">Duplicate index entries (keys) are disallowed.</span></span> <span data-ttu-id="e346e-116">呼叫 JetUpdate 時，不會強制執行這項功能，而不是在呼叫 JetSetColumn 時強制執行。</span><span class="sxs-lookup"><span data-stu-id="e346e-116">This is enforced when JetUpdate is called, not when JetSetColumn is called.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e346e-117">IndexPrimary</span><span class="sxs-lookup"><span data-stu-id="e346e-117">IndexPrimary</span></span></td>
<td><span data-ttu-id="e346e-118">索引是主要 (叢集) 索引。</span><span class="sxs-lookup"><span data-stu-id="e346e-118">The index is a primary (clustered) index.</span></span> <span data-ttu-id="e346e-119">每個資料表都必須只有一個主要索引。</span><span class="sxs-lookup"><span data-stu-id="e346e-119">Every table must have exactly one primary index.</span></span> <span data-ttu-id="e346e-120">如果未在資料表上明確定義主要索引，則資料庫引擎會建立自己的主要索引。</span><span class="sxs-lookup"><span data-stu-id="e346e-120">If no primary index is explicitly defined over a table, then the database engine will create its own primary index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e346e-121">IndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="e346e-121">IndexDisallowNull</span></span></td>
<td><span data-ttu-id="e346e-122">建立索引的資料行都不能包含 Null 值。</span><span class="sxs-lookup"><span data-stu-id="e346e-122">None of the columns over which the index is created may contain a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e346e-123">IndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="e346e-123">IndexIgnoreNull</span></span></td>
<td><span data-ttu-id="e346e-124">如果要編制索引的所有資料行都是 Null，請勿加入資料列的索引項目。</span><span class="sxs-lookup"><span data-stu-id="e346e-124">Do not add an index entry for a row if all of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e346e-125">IndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="e346e-125">IndexIgnoreAnyNull</span></span></td>
<td><span data-ttu-id="e346e-126">如果要編制索引的任何資料行都是 Null，請勿加入資料列的索引項目。</span><span class="sxs-lookup"><span data-stu-id="e346e-126">Do not add an index entry for a row if any of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e346e-127">IndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="e346e-127">IndexIgnoreFirstNull</span></span></td>
<td><span data-ttu-id="e346e-128">如果要編制索引的第一個資料行是 Null，請勿加入資料列的索引項目。</span><span class="sxs-lookup"><span data-stu-id="e346e-128">Do not add an index entry for a row if the first column being indexed is NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e346e-129">IndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="e346e-129">IndexLazyFlush</span></span></td>
<td><span data-ttu-id="e346e-130">指定將延遲記錄索引作業。</span><span class="sxs-lookup"><span data-stu-id="e346e-130">Specifies that the index operations will be logged lazily.</span></span> <span data-ttu-id="e346e-131">JET_bitIndexLazyFlush 不會影響資料更新的酷。</span><span class="sxs-lookup"><span data-stu-id="e346e-131">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="e346e-132">如果處理常式終止時，索引作業中斷，軟復原仍能讓資料庫處於一致的狀態，但索引可能不存在。</span><span class="sxs-lookup"><span data-stu-id="e346e-132">If the indexing operations is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index may not be present.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e346e-133">IndexEmpty</span><span class="sxs-lookup"><span data-stu-id="e346e-133">IndexEmpty</span></span></td>
<td><span data-ttu-id="e346e-134">請勿嘗試建立索引，因為所有專案都會評估為 Null。</span><span class="sxs-lookup"><span data-stu-id="e346e-134">Do not attempt to build the index, because all entries would evaluate to NULL.</span></span> <span data-ttu-id="e346e-135">傳遞 JET_bitIndexEmpty 時，grbit 也必須指定 JET_bitIgnoreAnyNull。</span><span class="sxs-lookup"><span data-stu-id="e346e-135">grbit MUST also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="e346e-136">這是一項效能增強功能。</span><span class="sxs-lookup"><span data-stu-id="e346e-136">This is a performance enhancement.</span></span> <span data-ttu-id="e346e-137">例如，如果將新的資料行加入至資料表，則會在這個新加入的資料行上建立索引，但會掃描資料表中的所有記錄，即使它們永遠不會加入索引中。</span><span class="sxs-lookup"><span data-stu-id="e346e-137">For example if a new column is added to a table, then an index is created over this newly added column, all of the records in the table would be scanned even though they would never get added to the index anyway.</span></span> <span data-ttu-id="e346e-138">指定 JET_bitIndexEmpty 會略過資料表掃描，這可能會花費很長的時間。</span><span class="sxs-lookup"><span data-stu-id="e346e-138">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e346e-139">IndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="e346e-139">IndexUnversioned</span></span></td>
<td><span data-ttu-id="e346e-140">導致其他交易可以看到索引建立。</span><span class="sxs-lookup"><span data-stu-id="e346e-140">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="e346e-141">一般來說，交易中的會話將無法在另一個會話中看到索引建立作業。</span><span class="sxs-lookup"><span data-stu-id="e346e-141">Normally a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="e346e-142">如果另一個交易可能建立相同的索引，而第二個索引建立只會失敗，而不是可能導致許多不必要的資料庫作業，則此旗標很有用。</span><span class="sxs-lookup"><span data-stu-id="e346e-142">This flag can be useful if another transaction is likely to create the same index, so that the second index-create will simply fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="e346e-143">第二筆交易可能無法立即使用索引。</span><span class="sxs-lookup"><span data-stu-id="e346e-143">The second transaction may not be able to use the index immediately.</span></span> <span data-ttu-id="e346e-144">索引建立作業必須先完成，才可供使用。</span><span class="sxs-lookup"><span data-stu-id="e346e-144">The index creation operation needs to complete before it is usable.</span></span> <span data-ttu-id="e346e-145">會話目前不能在交易中建立索引，而不需要版本資訊。</span><span class="sxs-lookup"><span data-stu-id="e346e-145">The session must not currently be in a transaction to create an index without version information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e346e-146">IndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="e346e-146">IndexSortNullsHigh</span></span></td>
<td><span data-ttu-id="e346e-147">指定此旗標會在索引中的所有資料行資料之後，將 Null 值排序。</span><span class="sxs-lookup"><span data-stu-id="e346e-147">Specifying this flag causes NULL values to be sorted after data for all columns in the index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="e346e-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e346e-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e346e-149">參考</span><span class="sxs-lookup"><span data-stu-id="e346e-149">Reference</span></span>

[<span data-ttu-id="e346e-150">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e346e-150">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
