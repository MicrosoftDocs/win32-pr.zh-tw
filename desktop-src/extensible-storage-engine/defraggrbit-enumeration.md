---
description: 深入瞭解： DefragGrbit 列舉
title: DefragGrbit 列舉
TOCTitle: DefragGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DefragGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.defraggrbit(v=EXCHG.10)
ms:contentKeyID: 39516122
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5da047fbdad20ac40d780dc5b0bba9e986e7672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991371"
---
# <a name="defraggrbit-enumeration"></a><span data-ttu-id="ff043-103">DefragGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="ff043-103">DefragGrbit enumeration</span></span>

<span data-ttu-id="ff043-104">[JetDefragment (JET_SESID、JET_DBID、String、int32、int32、DefragGrbit) ](./api.jetdefragment-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="ff043-104">Options for [JetDefragment(JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).</span></span>

<span data-ttu-id="ff043-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="ff043-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="ff043-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ff043-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ff043-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ff043-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ff043-108">語法</span><span class="sxs-lookup"><span data-stu-id="ff043-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DefragGrbit
'Usage
Dim instance As DefragGrbit
```

``` csharp
[FlagsAttribute]
public enum DefragGrbit
```

## <a name="members"></a><span data-ttu-id="ff043-109">成員</span><span class="sxs-lookup"><span data-stu-id="ff043-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ff043-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="ff043-110">Member name</span></span></th>
<th><span data-ttu-id="ff043-111">說明</span><span class="sxs-lookup"><span data-stu-id="ff043-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ff043-112">AvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="ff043-112">AvailSpaceTreesOnly</span></span></td>
<td><span data-ttu-id="ff043-113">重組 ESE 資料庫空間配置的可用空間部分。</span><span class="sxs-lookup"><span data-stu-id="ff043-113">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="ff043-114">資料庫空間分為兩種類型：擁有的空間和可用空間。</span><span class="sxs-lookup"><span data-stu-id="ff043-114">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="ff043-115">擁有的空間會配置給資料表或索引，而可用空間可供在資料表或索引內使用。</span><span class="sxs-lookup"><span data-stu-id="ff043-115">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="ff043-116">可用空間的行為更動態，而且需要進行線上磁碟重組，而非擁有的空間或資料表或索引資料。</span><span class="sxs-lookup"><span data-stu-id="ff043-116">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ff043-117">BatchStart</span><span class="sxs-lookup"><span data-stu-id="ff043-117">BatchStart</span></span></td>
<td><span data-ttu-id="ff043-118">開始新的磁碟重組工作。</span><span class="sxs-lookup"><span data-stu-id="ff043-118">Starts a new defragmentation task.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ff043-119">BatchStop</span><span class="sxs-lookup"><span data-stu-id="ff043-119">BatchStop</span></span></td>
<td><span data-ttu-id="ff043-120">停止磁碟重組工作。</span><span class="sxs-lookup"><span data-stu-id="ff043-120">Stops a defragmentation task.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ff043-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff043-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ff043-122">參考</span><span class="sxs-lookup"><span data-stu-id="ff043-122">Reference</span></span>

[<span data-ttu-id="ff043-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ff043-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
