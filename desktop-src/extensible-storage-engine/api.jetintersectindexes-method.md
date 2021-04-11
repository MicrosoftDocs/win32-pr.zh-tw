---
description: 深入瞭解： JetIntersectIndexes 方法
title: JetIntersectIndexes 方法
TOCTitle: 'JetIntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_INDEXRANGE[],System.Int32,Microsoft.Isam.Esent.Interop.JET_RECORDLIST@,Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetintersectindexes(v=EXCHG.10)
ms:contentKeyID: 55100761
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3bae632f386ef944e79a17813d1cc86451441e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945388"
---
# <a name="apijetintersectindexes-method"></a><span data-ttu-id="29215-103">JetIntersectIndexes 方法</span><span class="sxs-lookup"><span data-stu-id="29215-103">Api.JetIntersectIndexes method</span></span>

<span data-ttu-id="29215-104">計算相同資料表上不同次要索引的多個索引項目目集合之間的交集。</span><span class="sxs-lookup"><span data-stu-id="29215-104">Computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="29215-105">這項作業適用于在資料表中尋找符合可使用索引範圍表示之兩個或多個準則的一組記錄。</span><span class="sxs-lookup"><span data-stu-id="29215-105">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span> <span data-ttu-id="29215-106">另請參閱[IntersectIndexes (JET_SESID \[ \]) ](./api.intersectindexes-method.md)。</span><span class="sxs-lookup"><span data-stu-id="29215-106">Also see [IntersectIndexes(JET_SESID, \[\])](./api.intersectindexes-method.md).</span></span>

<span data-ttu-id="29215-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="29215-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="29215-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="29215-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="29215-109">語法</span><span class="sxs-lookup"><span data-stu-id="29215-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIntersectIndexes ( _
    sesid As JET_SESID, _
    ranges As JET_INDEXRANGE(), _
    numRanges As Integer, _
    <OutAttribute> ByRef recordlist As JET_RECORDLIST, _
    grbit As IntersectIndexesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim ranges As JET_INDEXRANGE()
Dim numRanges As Integer
Dim recordlist As JET_RECORDLIST
Dim grbit As IntersectIndexesGrbitApi.JetIntersectIndexes(sesid, _
    ranges, numRanges, recordlist, grbit)
```

``` csharp
public static void JetIntersectIndexes(
    JET_SESID sesid,
    JET_INDEXRANGE[] ranges,
    int numRanges,
    out JET_RECORDLIST recordlist,
    IntersectIndexesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="29215-110">參數</span><span class="sxs-lookup"><span data-stu-id="29215-110">Parameters</span></span>

  - <span data-ttu-id="29215-111">sesid</span><span class="sxs-lookup"><span data-stu-id="29215-111">sesid</span></span>  
    <span data-ttu-id="29215-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="29215-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="29215-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="29215-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="29215-114">範圍</span><span class="sxs-lookup"><span data-stu-id="29215-114">ranges</span></span>  
    <span data-ttu-id="29215-115">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="29215-115">Type: \[\]</span></span>  
    
    <span data-ttu-id="29215-116">要交集的索引範圍。</span><span class="sxs-lookup"><span data-stu-id="29215-116">An the index ranges to intersect.</span></span> <span data-ttu-id="29215-117">範圍中的 tableids 必須在其上設定索引範圍。</span><span class="sxs-lookup"><span data-stu-id="29215-117">The tableids in the ranges must have index ranges set on them.</span></span> <span data-ttu-id="29215-118">使用 [JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) ](./api.jetsetindexrange-method.md) 建立索引範圍。</span><span class="sxs-lookup"><span data-stu-id="29215-118">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

<!-- end list -->

  - <span data-ttu-id="29215-119">numRanges</span><span class="sxs-lookup"><span data-stu-id="29215-119">numRanges</span></span>  
    <span data-ttu-id="29215-120">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="29215-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="29215-121">索引範圍的數目。</span><span class="sxs-lookup"><span data-stu-id="29215-121">The number of index ranges.</span></span>

<!-- end list -->

  - <span data-ttu-id="29215-122">recordlist</span><span class="sxs-lookup"><span data-stu-id="29215-122">recordlist</span></span>  
    <span data-ttu-id="29215-123">類型： [Microsoft.Isam.Esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="29215-123">Type: [Microsoft.Isam.Esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span></span>  
    
    <span data-ttu-id="29215-124">傳回包含交集結果之臨時表的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="29215-124">Returns information about the temporary table containing the intersection results.</span></span>

<!-- end list -->

  - <span data-ttu-id="29215-125">grbit</span><span class="sxs-lookup"><span data-stu-id="29215-125">grbit</span></span>  
    <span data-ttu-id="29215-126">型別： [IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="29215-126">Type: [Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="29215-127">交集選項。</span><span class="sxs-lookup"><span data-stu-id="29215-127">Intersection options.</span></span>

## <a name="see-also"></a><span data-ttu-id="29215-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29215-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="29215-129">參考</span><span class="sxs-lookup"><span data-stu-id="29215-129">Reference</span></span>

[<span data-ttu-id="29215-130">Api 類別</span><span class="sxs-lookup"><span data-stu-id="29215-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="29215-131">Api 成員</span><span class="sxs-lookup"><span data-stu-id="29215-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="29215-132">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="29215-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
