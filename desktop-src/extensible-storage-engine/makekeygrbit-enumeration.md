---
description: 深入瞭解： MakeKeyGrbit 列舉
title: MakeKeyGrbit 列舉
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112509"
---
# <a name="makekeygrbit-enumeration"></a><span data-ttu-id="ade07-103">MakeKeyGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="ade07-103">MakeKeyGrbit enumeration</span></span>

<span data-ttu-id="ade07-104">JetMakeKey 的選項。</span><span class="sxs-lookup"><span data-stu-id="ade07-104">Options for JetMakeKey.</span></span>

<span data-ttu-id="ade07-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="ade07-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="ade07-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ade07-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ade07-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ade07-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ade07-108">語法</span><span class="sxs-lookup"><span data-stu-id="ade07-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
```

## <a name="members"></a><span data-ttu-id="ade07-109">成員</span><span class="sxs-lookup"><span data-stu-id="ade07-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ade07-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="ade07-110">Member name</span></span></th>
<th><span data-ttu-id="ade07-111">描述</span><span class="sxs-lookup"><span data-stu-id="ade07-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ade07-112">無</span><span class="sxs-lookup"><span data-stu-id="ade07-112">None</span></span></td>
<td><span data-ttu-id="ade07-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="ade07-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ade07-114">NewKey</span><span class="sxs-lookup"><span data-stu-id="ade07-114">NewKey</span></span></td>
<td><span data-ttu-id="ade07-115">應建立新的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ade07-115">A new search key should be constructed.</span></span> <span data-ttu-id="ade07-116">任何先前現有的搜尋金鑰都會被捨棄。</span><span class="sxs-lookup"><span data-stu-id="ade07-116">Any previously existing search key is discarded.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ade07-117">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="ade07-117">NormalizedKey</span></span></td>
<td><span data-ttu-id="ade07-118">指定此選項時，會忽略所有其他選項，任何先前現有的搜尋金鑰都會被捨棄，而輸入緩衝區的內容會載入為新的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ade07-118">When this option is specified, all other options are ignored, any previously existing search key is discarded, and the contents of the input buffer are loaded as the new search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ade07-119">KeyDataZeroLength</span><span class="sxs-lookup"><span data-stu-id="ade07-119">KeyDataZeroLength</span></span></td>
<td><span data-ttu-id="ade07-120">如果輸入緩衝區的大小為零，且目前的索引鍵資料行是可變長度資料行，則此選項表示輸入緩衝區包含零長度的值。</span><span class="sxs-lookup"><span data-stu-id="ade07-120">If the size of the input buffer is zero and the current key column is a variable length column, this option indicates that the input buffer contains a zero length value.</span></span> <span data-ttu-id="ade07-121">否則，輸入緩衝區大小為零會指出 Null 值。</span><span class="sxs-lookup"><span data-stu-id="ade07-121">Otherwise, an input buffer size of zero would indicate a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ade07-122">StrLimit</span><span class="sxs-lookup"><span data-stu-id="ade07-122">StrLimit</span></span></td>
<td><span data-ttu-id="ade07-123">此選項表示應建立搜尋索引鍵，以便將目前索引鍵資料行後面的任何索引鍵資料行視為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="ade07-123">This option indicates that the search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ade07-124">SubStrLimit</span><span class="sxs-lookup"><span data-stu-id="ade07-124">SubStrLimit</span></span></td>
<td><span data-ttu-id="ade07-125">此選項表示應建立搜尋索引鍵，讓目前的索引鍵資料行被視為首碼萬用字元，且在目前索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="ade07-125">This option indicates that the search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ade07-126">FullColumnStartLimit</span><span class="sxs-lookup"><span data-stu-id="ade07-126">FullColumnStartLimit</span></span></td>
<td><span data-ttu-id="ade07-127">應將搜尋索引鍵的結構化，以便在目前的索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="ade07-127">The search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ade07-128">FullColumnEndLimit</span><span class="sxs-lookup"><span data-stu-id="ade07-128">FullColumnEndLimit</span></span></td>
<td><span data-ttu-id="ade07-129">搜尋索引鍵的建立方式，是在目前的索引鍵資料行之後的任何索引鍵資料行都會被視為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="ade07-129">The search key should be constructed in such a way that any key columns that come after the current key column are considered to be wildcards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ade07-130">PartialColumnStartLimit</span><span class="sxs-lookup"><span data-stu-id="ade07-130">PartialColumnStartLimit</span></span></td>
<td><span data-ttu-id="ade07-131">應建立搜尋索引鍵，讓目前的索引鍵資料行被視為首碼萬用字元，且在目前索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="ade07-131">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ade07-132">PartialColumnEndLimit</span><span class="sxs-lookup"><span data-stu-id="ade07-132">PartialColumnEndLimit</span></span></td>
<td><span data-ttu-id="ade07-133">應建立搜尋索引鍵，讓目前的索引鍵資料行被視為首碼萬用字元，且在目前索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="ade07-133">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ade07-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ade07-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ade07-135">參考</span><span class="sxs-lookup"><span data-stu-id="ade07-135">Reference</span></span>

[<span data-ttu-id="ade07-136">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ade07-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
