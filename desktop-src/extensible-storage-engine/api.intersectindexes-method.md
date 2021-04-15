---
description: 深入瞭解： IntersectIndexes 方法
title: IntersectIndexes 方法
TOCTitle: 'IntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.IntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.intersectindexes(v=EXCHG.10)
ms:contentKeyID: 55107220
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8dfe5784ecd5ab517e183f8eeeb5f79315fe585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510855"
---
# <a name="apiintersectindexes-method"></a><span data-ttu-id="f2118-103">IntersectIndexes 方法</span><span class="sxs-lookup"><span data-stu-id="f2118-103">Api.IntersectIndexes method</span></span>

<span data-ttu-id="f2118-104">交集一組索引範圍，並傳回在所有索引範圍中找到之記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="f2118-104">Intersect a group of index ranges and return the bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="f2118-105">另請參閱[JetIntersectIndexes (JET_SESID、 \[ \] 、Int32、JET_RECORDLIST、IntersectIndexesGrbit) ](./api.jetintersectindexes-method.md)。</span><span class="sxs-lookup"><span data-stu-id="f2118-105">Also see [JetIntersectIndexes(JET_SESID, \[\], Int32, JET_RECORDLIST, IntersectIndexesGrbit)](./api.jetintersectindexes-method.md).</span></span>

<span data-ttu-id="f2118-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f2118-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f2118-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f2118-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f2118-108">語法</span><span class="sxs-lookup"><span data-stu-id="f2118-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function IntersectIndexes ( _
    sesid As JET_SESID, _
    ParamArray tableids As JET_TABLEID() _
) As IEnumerable(Of Byte())
'Usage
Dim sesid As JET_SESID
Dim tableids As JET_TABLEID()
Dim returnValue As IEnumerable(Of Byte())

returnValue = Api.IntersectIndexes(sesid, _
    tableids)
```

``` csharp
public static IEnumerable<byte[]> IntersectIndexes(
    JET_SESID sesid,
    params JET_TABLEID[] tableids
)
```

#### <a name="parameters"></a><span data-ttu-id="f2118-109">參數</span><span class="sxs-lookup"><span data-stu-id="f2118-109">Parameters</span></span>

  - <span data-ttu-id="f2118-110">sesid</span><span class="sxs-lookup"><span data-stu-id="f2118-110">sesid</span></span>  
    <span data-ttu-id="f2118-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2118-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f2118-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="f2118-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2118-113">tableids</span><span class="sxs-lookup"><span data-stu-id="f2118-113">tableids</span></span>  
    <span data-ttu-id="f2118-114">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="f2118-114">Type: \[\]</span></span>  
    
    <span data-ttu-id="f2118-115">要使用的 tableids。</span><span class="sxs-lookup"><span data-stu-id="f2118-115">The tableids to use.</span></span> <span data-ttu-id="f2118-116">每個 tableid 都必須來自相同資料表上的不同索引，並具有使用中的索引範圍。</span><span class="sxs-lookup"><span data-stu-id="f2118-116">Each tableid must be from a different index on the same table and have an active index range.</span></span> <span data-ttu-id="f2118-117">使用 [JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) ](./api.jetsetindexrange-method.md) 建立索引範圍。</span><span class="sxs-lookup"><span data-stu-id="f2118-117">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f2118-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2118-118">Return value</span></span>

<span data-ttu-id="f2118-119">類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1) 。\<\[\]\></span><span class="sxs-lookup"><span data-stu-id="f2118-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span></span>  
<span data-ttu-id="f2118-120">在所有索引範圍中找到之記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="f2118-120">The bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="f2118-121">書簽會以主要索引鍵順序傳回。</span><span class="sxs-lookup"><span data-stu-id="f2118-121">The bookmarks are returned in primary key order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f2118-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2118-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f2118-123">參考</span><span class="sxs-lookup"><span data-stu-id="f2118-123">Reference</span></span>

[<span data-ttu-id="f2118-124">Api 類別</span><span class="sxs-lookup"><span data-stu-id="f2118-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f2118-125">Api 成員</span><span class="sxs-lookup"><span data-stu-id="f2118-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f2118-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f2118-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
