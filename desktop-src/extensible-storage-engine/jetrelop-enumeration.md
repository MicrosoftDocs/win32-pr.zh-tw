---
description: 深入瞭解： JetRelop 列舉
title: JetRelop 列舉 (Windows8) 的列舉
TOCTitle: JetRelop enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JetRelop
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jetrelop(v=EXCHG.10)
ms:contentKeyID: 55104456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7839e0223eb9dd773ca9a5d10b5210b10b0a944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321143"
---
# <a name="jetrelop-enumeration"></a><span data-ttu-id="13793-103">JetRelop 列舉</span><span class="sxs-lookup"><span data-stu-id="13793-103">JetRelop enumeration</span></span>

<span data-ttu-id="13793-104">篩選準則定義為 [JET_INDEX_COLUMN](./jet-index-column-class.md)的比較作業。</span><span class="sxs-lookup"><span data-stu-id="13793-104">Comparison operation for filter defined as [JET_INDEX_COLUMN](./jet-index-column-class.md).</span></span>

<span data-ttu-id="13793-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="13793-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="13793-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="13793-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="13793-107">語法</span><span class="sxs-lookup"><span data-stu-id="13793-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JetRelop
'Usage
Dim instance As JetRelop
```

``` csharp
public enum JetRelop
```

## <a name="members"></a><span data-ttu-id="13793-108">成員</span><span class="sxs-lookup"><span data-stu-id="13793-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="13793-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="13793-109">Member name</span></span></th>
<th><span data-ttu-id="13793-110">說明</span><span class="sxs-lookup"><span data-stu-id="13793-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="13793-111">等於</span><span class="sxs-lookup"><span data-stu-id="13793-111">Equals</span></span></td>
<td><span data-ttu-id="13793-112">只接受資料行值等於指定值的資料列。</span><span class="sxs-lookup"><span data-stu-id="13793-112">Accept only rows which have column value equal to the given value.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="13793-113">PrefixEquals</span><span class="sxs-lookup"><span data-stu-id="13793-113">PrefixEquals</span></span></td>
<td><span data-ttu-id="13793-114">只接受具有符合指定值之資料行的資料列。</span><span class="sxs-lookup"><span data-stu-id="13793-114">Accept only rows which have columns whose prefix matches the given value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="13793-115">NotEquals</span><span class="sxs-lookup"><span data-stu-id="13793-115">NotEquals</span></span></td>
<td><span data-ttu-id="13793-116">只接受資料行值不等於指定值的資料列。</span><span class="sxs-lookup"><span data-stu-id="13793-116">Accept only rows which have column value not equal to the given value.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="13793-117">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="13793-117">LessThanOrEqual</span></span></td>
<td><span data-ttu-id="13793-118">只接受資料行值小於或等於指定值的資料列。</span><span class="sxs-lookup"><span data-stu-id="13793-118">Accept only rows which have column value less than or equal a given value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="13793-119">LessThan</span><span class="sxs-lookup"><span data-stu-id="13793-119">LessThan</span></span></td>
<td><span data-ttu-id="13793-120">只接受資料行值小於指定值的資料列。</span><span class="sxs-lookup"><span data-stu-id="13793-120">Accept only rows which have column value less than a given value.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="13793-121">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="13793-121">GreaterThanOrEqual</span></span></td>
<td><span data-ttu-id="13793-122">只接受資料行值大於或等於指定值的資料列。</span><span class="sxs-lookup"><span data-stu-id="13793-122">Accept only rows which have column value greater than or equal a given value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="13793-123">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="13793-123">GreaterThan</span></span></td>
<td><span data-ttu-id="13793-124">只接受資料行值大於指定值的資料列。</span><span class="sxs-lookup"><span data-stu-id="13793-124">Accept only rows which have column value greater than a given value.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="13793-125">BitmaskEqualsZero</span><span class="sxs-lookup"><span data-stu-id="13793-125">BitmaskEqualsZero</span></span></td>
<td><span data-ttu-id="13793-126">只接受資料行值以 and 連結且指定的位元遮罩產生零的資料列。</span><span class="sxs-lookup"><span data-stu-id="13793-126">Accept only rows which have column value ANDed with a given bitmask yielding zero.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="13793-127">BitmaskNotEqualsZero</span><span class="sxs-lookup"><span data-stu-id="13793-127">BitmaskNotEqualsZero</span></span></td>
<td><span data-ttu-id="13793-128">只接受資料行值為以 and 連結且指定的位元遮罩為非零的資料列。</span><span class="sxs-lookup"><span data-stu-id="13793-128">Accept only rows which have column value ANDed with a given bitmask yielding non-zero.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="13793-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13793-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="13793-130">參考</span><span class="sxs-lookup"><span data-stu-id="13793-130">Reference</span></span>

[<span data-ttu-id="13793-131">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="13793-131">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
