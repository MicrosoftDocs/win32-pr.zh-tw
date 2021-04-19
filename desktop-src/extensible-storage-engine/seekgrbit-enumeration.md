---
description: 深入瞭解： SeekGrbit 列舉
title: SeekGrbit 列舉
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e59072055710676f5f7647130f42ad5acf50527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974712"
---
# <a name="seekgrbit-enumeration"></a><span data-ttu-id="7dcc0-103">SeekGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="7dcc0-103">SeekGrbit enumeration</span></span>

<span data-ttu-id="7dcc0-104">JetSeek 的選項。</span><span class="sxs-lookup"><span data-stu-id="7dcc0-104">Options for JetSeek.</span></span>

<span data-ttu-id="7dcc0-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="7dcc0-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="7dcc0-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7dcc0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7dcc0-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7dcc0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7dcc0-108">語法</span><span class="sxs-lookup"><span data-stu-id="7dcc0-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
```

## <a name="members"></a><span data-ttu-id="7dcc0-109">成員</span><span class="sxs-lookup"><span data-stu-id="7dcc0-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="7dcc0-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="7dcc0-110">Member name</span></span></th>
<th><span data-ttu-id="7dcc0-111">說明</span><span class="sxs-lookup"><span data-stu-id="7dcc0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7dcc0-112">SeekEQ</span><span class="sxs-lookup"><span data-stu-id="7dcc0-112">SeekEQ</span></span></td>
<td><span data-ttu-id="7dcc0-113">資料指標將定位於最接近索引開頭的索引項目目，此索引項目目完全符合搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7dcc0-113">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7dcc0-114">SeekLT</span><span class="sxs-lookup"><span data-stu-id="7dcc0-114">SeekLT</span></span></td>
<td><span data-ttu-id="7dcc0-115">資料指標將放置在最接近索引結尾的索引項目目，此索引項目目小於符合搜尋條件的索引項目。</span><span class="sxs-lookup"><span data-stu-id="7dcc0-115">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7dcc0-116">SeekLE</span><span class="sxs-lookup"><span data-stu-id="7dcc0-116">SeekLE</span></span></td>
<td><span data-ttu-id="7dcc0-117">資料指標將定位於最接近索引結尾的索引項目目，這個專案小於或等於符合搜尋準則的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="7dcc0-117">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7dcc0-118">SeekGE</span><span class="sxs-lookup"><span data-stu-id="7dcc0-118">SeekGE</span></span></td>
<td><span data-ttu-id="7dcc0-119">資料指標將定位於最接近索引開頭的索引項目目，此索引項目目大於或等於符合搜尋條件的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="7dcc0-119">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7dcc0-120">SeekGT</span><span class="sxs-lookup"><span data-stu-id="7dcc0-120">SeekGT</span></span></td>
<td><span data-ttu-id="7dcc0-121">資料指標將放置在索引項目目的開頭最接近索引的開頭，而該索引項目大於符合搜尋準則的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="7dcc0-121">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7dcc0-122">SetIndexRange</span><span class="sxs-lookup"><span data-stu-id="7dcc0-122">SetIndexRange</span></span></td>
<td><span data-ttu-id="7dcc0-123">將會針對完全符合搜尋索引鍵的所有索引鍵，自動設定索引範圍。</span><span class="sxs-lookup"><span data-stu-id="7dcc0-123">An index range will automatically be setup for all keys that exactly match the search key.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="7dcc0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dcc0-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7dcc0-125">參考</span><span class="sxs-lookup"><span data-stu-id="7dcc0-125">Reference</span></span>

[<span data-ttu-id="7dcc0-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7dcc0-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
