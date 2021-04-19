---
description: 深入瞭解： SetIndexRangeGrbit 列舉
title: SetIndexRangeGrbit 列舉
TOCTitle: SetIndexRangeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setindexrangegrbit(v=EXCHG.10)
ms:contentKeyID: 39515181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cda73597f88d2c8fca911ebb96d7a3c6399ed9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974074"
---
# <a name="setindexrangegrbit-enumeration"></a><span data-ttu-id="8e544-103">SetIndexRangeGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="8e544-103">SetIndexRangeGrbit enumeration</span></span>

<span data-ttu-id="8e544-104">JetSetIndexRange 的選項。</span><span class="sxs-lookup"><span data-stu-id="8e544-104">Options for JetSetIndexRange.</span></span>

<span data-ttu-id="8e544-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="8e544-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="8e544-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e544-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8e544-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8e544-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e544-108">語法</span><span class="sxs-lookup"><span data-stu-id="8e544-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetIndexRangeGrbit
'Usage
Dim instance As SetIndexRangeGrbit
```

``` csharp
[FlagsAttribute]
public enum SetIndexRangeGrbit
```

## <a name="members"></a><span data-ttu-id="8e544-109">成員</span><span class="sxs-lookup"><span data-stu-id="8e544-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8e544-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="8e544-110">Member name</span></span></th>
<th><span data-ttu-id="8e544-111">描述</span><span class="sxs-lookup"><span data-stu-id="8e544-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8e544-112">無</span><span class="sxs-lookup"><span data-stu-id="8e544-112">None</span></span></td>
<td><span data-ttu-id="8e544-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="8e544-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8e544-114">RangeInclusive</span><span class="sxs-lookup"><span data-stu-id="8e544-114">RangeInclusive</span></span></td>
<td><span data-ttu-id="8e544-115">此選項表示索引範圍的限制為內含。</span><span class="sxs-lookup"><span data-stu-id="8e544-115">This option indicates that the limit of the index range is inclusive.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8e544-116">RangeUpperLimit</span><span class="sxs-lookup"><span data-stu-id="8e544-116">RangeUpperLimit</span></span></td>
<td><span data-ttu-id="8e544-117">資料指標中的搜尋索引鍵代表索引項目的搜尋準則，最接近索引的結尾會符合索引範圍。</span><span class="sxs-lookup"><span data-stu-id="8e544-117">The search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8e544-118">RangeInstantDuration</span><span class="sxs-lookup"><span data-stu-id="8e544-118">RangeInstantDuration</span></span></td>
<td><span data-ttu-id="8e544-119">索引範圍應在建立後立即移除。</span><span class="sxs-lookup"><span data-stu-id="8e544-119">The index range should be removed as soon as it has been established.</span></span> <span data-ttu-id="8e544-120">這適合用來測試符合搜尋準則的索引項目是否存在。</span><span class="sxs-lookup"><span data-stu-id="8e544-120">This is useful for testing for the existence of index entries that match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8e544-121">RangeRemove</span><span class="sxs-lookup"><span data-stu-id="8e544-121">RangeRemove</span></span></td>
<td><span data-ttu-id="8e544-122">取消和現有的索引範圍。</span><span class="sxs-lookup"><span data-stu-id="8e544-122">Cancel and existing index range.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8e544-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e544-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e544-124">參考</span><span class="sxs-lookup"><span data-stu-id="8e544-124">Reference</span></span>

[<span data-ttu-id="8e544-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8e544-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
