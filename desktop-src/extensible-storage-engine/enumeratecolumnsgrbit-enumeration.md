---
description: 深入瞭解： EnumerateColumnsGrbit 列舉
title: EnumerateColumnsGrbit 列舉
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e27e6810b37b513d550bbafce509b2815ccea2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979408"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a><span data-ttu-id="d8403-103">EnumerateColumnsGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="d8403-103">EnumerateColumnsGrbit enumeration</span></span>

<span data-ttu-id="d8403-104">JetEnumerateColumns 的選項。</span><span class="sxs-lookup"><span data-stu-id="d8403-104">Options for JetEnumerateColumns.</span></span>

<span data-ttu-id="d8403-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="d8403-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="d8403-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d8403-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d8403-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d8403-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d8403-108">語法</span><span class="sxs-lookup"><span data-stu-id="d8403-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a><span data-ttu-id="d8403-109">成員</span><span class="sxs-lookup"><span data-stu-id="d8403-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d8403-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="d8403-110">Member name</span></span></th>
<th><span data-ttu-id="d8403-111">描述</span><span class="sxs-lookup"><span data-stu-id="d8403-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d8403-112">無</span><span class="sxs-lookup"><span data-stu-id="d8403-112">None</span></span></td>
<td><span data-ttu-id="d8403-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="d8403-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d8403-114">EnumerateCompressOutput</span><span class="sxs-lookup"><span data-stu-id="d8403-114">EnumerateCompressOutput</span></span></td>
<td><span data-ttu-id="d8403-115">列舉資料行值時，我們將會以壓縮格式傳回所有資料行，而這些資料行只會傳回一個非 Null 資料行值。</span><span class="sxs-lookup"><span data-stu-id="d8403-115">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="d8403-116">這類資料行的狀態將會設定為 <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> ，而資料行值的大小和包含資料行值的記憶體則會直接傳回 <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> 結構中。</span><span class="sxs-lookup"><span data-stu-id="d8403-116">The status for such columns will be set to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> and the size of the column value and the memory containing the column value will be returned directly in the <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="d8403-117">不保證會以這種方式壓縮所有合格的資料行。</span><span class="sxs-lookup"><span data-stu-id="d8403-117">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="d8403-118">如需詳細資訊，請參閱 <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> 。</span><span class="sxs-lookup"><span data-stu-id="d8403-118">See <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d8403-119">EnumerateCopy</span><span class="sxs-lookup"><span data-stu-id="d8403-119">EnumerateCopy</span></span></td>
<td><span data-ttu-id="d8403-120">此選項表示應該列舉記錄的已修改資料行值，而不是原始資料行值。</span><span class="sxs-lookup"><span data-stu-id="d8403-120">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="d8403-121">如果資料行值尚未修改，則會列舉原始資料行值。</span><span class="sxs-lookup"><span data-stu-id="d8403-121">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="d8403-122">如此一來，插入或更新記錄時，可能會列舉尚未插入或更新的資料行值。</span><span class="sxs-lookup"><span data-stu-id="d8403-122">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span>
<p><span data-ttu-id="d8403-123">此選項與 <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>相同。</span><span class="sxs-lookup"><span data-stu-id="d8403-123">This option is identical to <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d8403-124">EnumerateIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="d8403-124">EnumerateIgnoreDefault</span></span></td>
<td><span data-ttu-id="d8403-125">如果指定的資料行不存在於記錄中，則不會傳回任何資料行值。</span><span class="sxs-lookup"><span data-stu-id="d8403-125">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="d8403-126">一般來說，在此案例中會傳回資料行的預設值（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d8403-126">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="d8403-127">如果資料行設定為與預設值不同的值，則會傳回不同的值 (也就是說，如果具有預設值的資料行明確設定為 Null，則會傳回 Null 做為該資料行的值) 。</span><span class="sxs-lookup"><span data-stu-id="d8403-127">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to NULL then a NULL will be returned as the value for that column).</span></span> <span data-ttu-id="d8403-128">即使已要求此選項，仍然可以看到剛好等於預設值的資料行值。</span><span class="sxs-lookup"><span data-stu-id="d8403-128">Even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="d8403-129">移除符合其預設值的資料行值不會進行任何工作。</span><span class="sxs-lookup"><span data-stu-id="d8403-129">No effort is made to remove column values that match their default values.</span></span> <span data-ttu-id="d8403-130">請務必記住，在搭配 EnumeratePresenceOnly 或 EnumerateTaggedOnly 使用時，此選項會影響 <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID、JET_TABLEID、Int32、[]、int32、[]、JET_PFNREALLOC、IntPtr、int32、EnumerateColumnsGrbit) </a> 的輸出。</span><span class="sxs-lookup"><span data-stu-id="d8403-130">It is important to remember that this option affects the output of <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> when used with EnumeratePresenceOnly or EnumerateTaggedOnly.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d8403-131">EnumeratePresenceOnly</span><span class="sxs-lookup"><span data-stu-id="d8403-131">EnumeratePresenceOnly</span></span></td>
<td><span data-ttu-id="d8403-132">如果要求的資料行或資料行值有非 Null 的值，則不會傳回相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="d8403-132">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="d8403-133">相反地，該資料行或資料行值的關聯狀態將會設定為 <a href="hh557250(v=exchg.10).md">ColumnPresent</a>。</span><span class="sxs-lookup"><span data-stu-id="d8403-133">Instead, the associated status for that column or column value will be set to <a href="hh557250(v=exchg.10).md">ColumnPresent</a>.</span></span> <span data-ttu-id="d8403-134">如果資料行或資料行的值為 Null，則 <a href="hh557250(v=exchg.10).md">ColumnNull</a> 會如往常般傳回。</span><span class="sxs-lookup"><span data-stu-id="d8403-134">If the column or column value is NULL then <a href="hh557250(v=exchg.10).md">ColumnNull</a> will be returned as usual.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d8403-135">EnumerateTaggedOnly</span><span class="sxs-lookup"><span data-stu-id="d8403-135">EnumerateTaggedOnly</span></span></td>
<td><span data-ttu-id="d8403-136">列舉記錄中的所有資料行值時 (例如，當 numColumnids 為零) 時，只會傳回已標記的資料行值。</span><span class="sxs-lookup"><span data-stu-id="d8403-136">When enumerating all column values in the record (for example,that is when numColumnids is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="d8403-137">列舉資料行識別碼的特定陣列時，不允許使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="d8403-137">This option is not allowed when enumerating a specific array of column IDs.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d8403-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8403-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d8403-139">參考</span><span class="sxs-lookup"><span data-stu-id="d8403-139">Reference</span></span>

[<span data-ttu-id="d8403-140">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="d8403-140">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="d8403-141">EnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="d8403-141">EnumerateIgnoreUserDefinedDefault</span></span>](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[<span data-ttu-id="d8403-142">EnumerateInRecordOnly</span><span class="sxs-lookup"><span data-stu-id="d8403-142">EnumerateInRecordOnly</span></span>](./windows7grbits.enumerateinrecordonly-field.md)
