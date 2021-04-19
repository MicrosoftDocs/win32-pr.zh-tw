---
description: 深入瞭解： PrereadIndexRangesGrbit 列舉
title: PrereadIndexRangesGrbit 列舉 (Windows8) 的列舉
TOCTitle: PrereadIndexRangesGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.prereadindexrangesgrbit(v=EXCHG.10)
ms:contentKeyID: 55104328
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Backwards
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.FirstPageOnly
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Forward
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.NormalizedKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.FirstPageOnly
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Forward
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Backwards
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.NormalizedKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4bc1b9877d4548a68aa71ea4def536af09d9693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979187"
---
# <a name="prereadindexrangesgrbit-enumeration"></a><span data-ttu-id="ada7d-103">PrereadIndexRangesGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="ada7d-103">PrereadIndexRangesGrbit enumeration</span></span>

<span data-ttu-id="ada7d-104">[JetPrereadIndexRanges (JET_SESID、JET_TABLEID、 \[ \] 、int32、int32、int32、 \[ \] 、PrereadIndexRangesGrbit) ](./windows8api.jetprereadindexranges-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="ada7d-104">Options for [JetPrereadIndexRanges(JET_SESID, JET_TABLEID, \[\], Int32, Int32, Int32, \[\], PrereadIndexRangesGrbit)](./windows8api.jetprereadindexranges-method.md).</span></span>

<span data-ttu-id="ada7d-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="ada7d-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="ada7d-106">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ada7d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="ada7d-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ada7d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ada7d-108">語法</span><span class="sxs-lookup"><span data-stu-id="ada7d-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration PrereadIndexRangesGrbit
'Usage
Dim instance As PrereadIndexRangesGrbit
```

``` csharp
[FlagsAttribute]
public enum PrereadIndexRangesGrbit
```

## <a name="members"></a><span data-ttu-id="ada7d-109">成員</span><span class="sxs-lookup"><span data-stu-id="ada7d-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ada7d-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="ada7d-110">Member name</span></span></th>
<th><span data-ttu-id="ada7d-111">說明</span><span class="sxs-lookup"><span data-stu-id="ada7d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ada7d-112">轉寄</span><span class="sxs-lookup"><span data-stu-id="ada7d-112">Forward</span></span></td>
<td><span data-ttu-id="ada7d-113">向前 Preread。</span><span class="sxs-lookup"><span data-stu-id="ada7d-113">Preread forward.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ada7d-114">向後</span><span class="sxs-lookup"><span data-stu-id="ada7d-114">Backwards</span></span></td>
<td><span data-ttu-id="ada7d-115">向後 Preread。</span><span class="sxs-lookup"><span data-stu-id="ada7d-115">Preread backwards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ada7d-116">FirstPageOnly</span><span class="sxs-lookup"><span data-stu-id="ada7d-116">FirstPageOnly</span></span></td>
<td><span data-ttu-id="ada7d-117">Preread 任何長時間資料行的第一頁。</span><span class="sxs-lookup"><span data-stu-id="ada7d-117">Preread only first page of any long column.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ada7d-118">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="ada7d-118">NormalizedKey</span></span></td>
<td><span data-ttu-id="ada7d-119">提供正規化的索引鍵/書簽，而不是資料行值。</span><span class="sxs-lookup"><span data-stu-id="ada7d-119">Normalized key/bookmark provided instead of column value.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ada7d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ada7d-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ada7d-121">參考</span><span class="sxs-lookup"><span data-stu-id="ada7d-121">Reference</span></span>

[<span data-ttu-id="ada7d-122">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="ada7d-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
