---
description: 深入瞭解： CompactGrbit 列舉
title: CompactGrbit 列舉
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7bbe6c88a0a52ab852e3cde9af8871833948949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981444"
---
# <a name="compactgrbit-enumeration"></a><span data-ttu-id="213a5-103">CompactGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="213a5-103">CompactGrbit enumeration</span></span>

<span data-ttu-id="213a5-104">[JetCompact (的選項 JET_SESID、字串、字串、JET_PFNSTATUS、JET_CONVERT、CompactGrbit) ](./api.jetcompact-method.md)。</span><span class="sxs-lookup"><span data-stu-id="213a5-104">Options for [JetCompact(JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).</span></span>

<span data-ttu-id="213a5-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="213a5-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="213a5-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="213a5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="213a5-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="213a5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="213a5-108">語法</span><span class="sxs-lookup"><span data-stu-id="213a5-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
```

## <a name="members"></a><span data-ttu-id="213a5-109">成員</span><span class="sxs-lookup"><span data-stu-id="213a5-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="213a5-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="213a5-110">Member name</span></span></th>
<th><span data-ttu-id="213a5-111">描述</span><span class="sxs-lookup"><span data-stu-id="213a5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="213a5-112">無</span><span class="sxs-lookup"><span data-stu-id="213a5-112">None</span></span></td>
<td><span data-ttu-id="213a5-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="213a5-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="213a5-114">狀態</span><span class="sxs-lookup"><span data-stu-id="213a5-114">Stats</span></span></td>
<td><span data-ttu-id="213a5-115">讓 JetCompact 將源資料庫的統計資料傾印到名為 DFRGINFO.TXT 的檔案。</span><span class="sxs-lookup"><span data-stu-id="213a5-115">Causes JetCompact to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="213a5-116">統計資料包括源資料庫中每個資料表的名稱、每個資料表中的資料列數目、每個資料表中所有資料列的總大小（以位元組為單位）、 <a href="hh577895(v=exchg.10).md">LongText</a> 或 <a href="hh577895(v=exchg.10).md">LongBinary</a> 類型的所有資料行大小總計（以位元組為單位），且足以與記錄分開儲存、叢集索引分葉頁面數目，以及 long 值分葉頁面數目。</span><span class="sxs-lookup"><span data-stu-id="213a5-116">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="hh577895(v=exchg.10).md">LongText</a> or <a href="hh577895(v=exchg.10).md">LongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="213a5-117">此外，摘要統計資料，包括源資料庫的大小、目的地資料庫、資料庫壓縮所需的時間，也會全部傾印暫存資料庫空間。</span><span class="sxs-lookup"><span data-stu-id="213a5-117">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="213a5-118">修復</span><span class="sxs-lookup"><span data-stu-id="213a5-118">Repair</span></span></td>
<td><span data-ttu-id="213a5-119"><strong>已淘汰。</strong></span><span class="sxs-lookup"><span data-stu-id="213a5-119"><strong>Obsolete.</strong></span></span> <span data-ttu-id="213a5-120">當源資料庫已知已損毀時使用。</span><span class="sxs-lookup"><span data-stu-id="213a5-120">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="213a5-121">它會啟用一組完整的新行為，以盡可能從源資料庫中回收最多的資料。</span><span class="sxs-lookup"><span data-stu-id="213a5-121">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="213a5-122">使用這個選項組的 JetCompact 可能會傳回 <a href="hh564840(v=exchg.10).md">成功</a> ，但不會複製在源資料庫中建立的所有資料。</span><span class="sxs-lookup"><span data-stu-id="213a5-122">JetCompact with this option set may return <a href="hh564840(v=exchg.10).md">Success</a> but not copy all of the data created in the source database.</span></span> <span data-ttu-id="213a5-123">將略過源資料庫中損毀部分的資料。</span><span class="sxs-lookup"><span data-stu-id="213a5-123">Data that was in damaged portions of the source database will be skipped.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="213a5-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="213a5-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="213a5-125">參考</span><span class="sxs-lookup"><span data-stu-id="213a5-125">Reference</span></span>

[<span data-ttu-id="213a5-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="213a5-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
