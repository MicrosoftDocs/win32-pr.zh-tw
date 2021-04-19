---
description: 深入瞭解： Windows8Api. JetTryPrereadIndexRanges 方法
title: 'Windows8Api. JetTryPrereadIndexRanges 方法 (Windows8 的) '
TOCTitle: 'JetTryPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jettryprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104421
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a9664e658254de057b0e3aa8ae86813eb996a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983360"
---
# <a name="windows8apijettryprereadindexranges-method"></a><span data-ttu-id="e952c-103">Windows8Api. JetTryPrereadIndexRanges 方法</span><span class="sxs-lookup"><span data-stu-id="e952c-103">Windows8Api.JetTryPrereadIndexRanges method</span></span>

<span data-ttu-id="e952c-104">如果具有指定索引鍵範圍的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。</span><span class="sxs-lookup"><span data-stu-id="e952c-104">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="e952c-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e952c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="e952c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e952c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e952c-107">語法</span><span class="sxs-lookup"><span data-stu-id="e952c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetTryPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbit
Dim returnValue As Boolean

returnValue = Windows8Api.JetTryPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static bool JetTryPrereadIndexRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_RANGE[] indexRanges,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e952c-108">參數</span><span class="sxs-lookup"><span data-stu-id="e952c-108">Parameters</span></span>

  - <span data-ttu-id="e952c-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e952c-109">sesid</span></span>  
    <span data-ttu-id="e952c-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e952c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e952c-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="e952c-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e952c-112">tableid</span><span class="sxs-lookup"><span data-stu-id="e952c-112">tableid</span></span>  
    <span data-ttu-id="e952c-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e952c-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e952c-114">要針對其發出 prereads 的資料表。</span><span class="sxs-lookup"><span data-stu-id="e952c-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="e952c-115">indexRanges</span><span class="sxs-lookup"><span data-stu-id="e952c-115">indexRanges</span></span>  
    <span data-ttu-id="e952c-116">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="e952c-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="e952c-117">要 preread 的索引鍵範圍。</span><span class="sxs-lookup"><span data-stu-id="e952c-117">The key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e952c-118">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="e952c-118">rangeIndex</span></span>  
    <span data-ttu-id="e952c-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e952c-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e952c-120">要讀取的陣列中第一個索引鍵範圍的索引。</span><span class="sxs-lookup"><span data-stu-id="e952c-120">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="e952c-121">rangeCount</span><span class="sxs-lookup"><span data-stu-id="e952c-121">rangeCount</span></span>  
    <span data-ttu-id="e952c-122">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e952c-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e952c-123">要 preread 的索引鍵範圍的最大數目。</span><span class="sxs-lookup"><span data-stu-id="e952c-123">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e952c-124">rangesPreread</span><span class="sxs-lookup"><span data-stu-id="e952c-124">rangesPreread</span></span>  
    <span data-ttu-id="e952c-125">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e952c-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e952c-126">傳回實際 preread 的索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="e952c-126">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e952c-127">columnsPreread</span><span class="sxs-lookup"><span data-stu-id="e952c-127">columnsPreread</span></span>  
    <span data-ttu-id="e952c-128">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="e952c-128">Type: \[\]</span></span>  
    
    <span data-ttu-id="e952c-129">要 preread 之 long 值資料行的資料行識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="e952c-129">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e952c-130">grbit</span><span class="sxs-lookup"><span data-stu-id="e952c-130">grbit</span></span>  
    <span data-ttu-id="e952c-131">型別： [Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e952c-131">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e952c-132">Preread 選項。</span><span class="sxs-lookup"><span data-stu-id="e952c-132">Preread options.</span></span> <span data-ttu-id="e952c-133">用來指定 preread 的方向。</span><span class="sxs-lookup"><span data-stu-id="e952c-133">Used to specify the direction of the preread.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e952c-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="e952c-134">Return value</span></span>

<span data-ttu-id="e952c-135">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e952c-135">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="e952c-136">如果某些 preread 完成， **\[ 則為 true \]** ，否則為 **\[ false \]** 。</span><span class="sxs-lookup"><span data-stu-id="e952c-136">**\[true\]** if some preread done, **\[false\]** otherwise.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e952c-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e952c-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e952c-138">參考</span><span class="sxs-lookup"><span data-stu-id="e952c-138">Reference</span></span>

[<span data-ttu-id="e952c-139">Windows8Api 類別</span><span class="sxs-lookup"><span data-stu-id="e952c-139">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="e952c-140">Windows8Api 成員</span><span class="sxs-lookup"><span data-stu-id="e952c-140">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="e952c-141">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="e952c-141">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
