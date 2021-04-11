---
description: 深入瞭解： Windows8Api. PrereadKeyRanges 方法
title: 'Windows8Api. PrereadKeyRanges 方法 (Windows8 的) '
TOCTitle: 'PrereadKeyRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.prereadkeyranges(v=EXCHG.10)
ms:contentKeyID: 55104465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 091c1f92512fd9a55bb4acd4d824567acc19fdde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943693"
---
# <a name="windows8apiprereadkeyranges-method"></a><span data-ttu-id="f2898-103">Windows8Api. PrereadKeyRanges 方法</span><span class="sxs-lookup"><span data-stu-id="f2898-103">Windows8Api.PrereadKeyRanges method</span></span>

<span data-ttu-id="f2898-104">如果具有指定索引鍵範圍的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。</span><span class="sxs-lookup"><span data-stu-id="f2898-104">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="f2898-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f2898-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="f2898-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f2898-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f2898-107">語法</span><span class="sxs-lookup"><span data-stu-id="f2898-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub PrereadKeyRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keysStart As Byte()(), _
    keyStartLengths As Integer(), _
    keysEnd As Byte()(), _
    keyEndLengths As Integer(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keysStart As Byte()()
Dim keyStartLengths As Integer()
Dim keysEnd As Byte()()
Dim keyEndLengths As Integer()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.PrereadKeyRanges(sesid, tableid, _
    keysStart, keyStartLengths, keysEnd, _
    keyEndLengths, rangeIndex, rangeCount, _
    rangesPreread, columnsPreread, grbit)
```

``` csharp
public static void PrereadKeyRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keysStart,
    int[] keyStartLengths,
    byte[][] keysEnd,
    int[] keyEndLengths,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f2898-108">參數</span><span class="sxs-lookup"><span data-stu-id="f2898-108">Parameters</span></span>

  - <span data-ttu-id="f2898-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f2898-109">sesid</span></span>  
    <span data-ttu-id="f2898-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2898-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f2898-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="f2898-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2898-112">tableid</span><span class="sxs-lookup"><span data-stu-id="f2898-112">tableid</span></span>  
    <span data-ttu-id="f2898-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2898-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f2898-114">要針對其發出 prereads 的資料表。</span><span class="sxs-lookup"><span data-stu-id="f2898-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2898-115">keysStart</span><span class="sxs-lookup"><span data-stu-id="f2898-115">keysStart</span></span>  
    <span data-ttu-id="f2898-116">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="f2898-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="f2898-117">要 preread 的索引鍵範圍開頭。</span><span class="sxs-lookup"><span data-stu-id="f2898-117">The start of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2898-118">keyStartLengths</span><span class="sxs-lookup"><span data-stu-id="f2898-118">keyStartLengths</span></span>  
    <span data-ttu-id="f2898-119">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="f2898-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="f2898-120">要 preread 的開始索引鍵長度。</span><span class="sxs-lookup"><span data-stu-id="f2898-120">The lengths of the start keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2898-121">keysEnd</span><span class="sxs-lookup"><span data-stu-id="f2898-121">keysEnd</span></span>  
    <span data-ttu-id="f2898-122">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="f2898-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="f2898-123">要 preread 的主要 rangess 結尾。</span><span class="sxs-lookup"><span data-stu-id="f2898-123">The end of key rangess to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2898-124">keyEndLengths</span><span class="sxs-lookup"><span data-stu-id="f2898-124">keyEndLengths</span></span>  
    <span data-ttu-id="f2898-125">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="f2898-125">Type: \[\]</span></span>  
    
    <span data-ttu-id="f2898-126">要 preread 的結束金鑰長度。</span><span class="sxs-lookup"><span data-stu-id="f2898-126">The lengths of the end keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2898-127">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="f2898-127">rangeIndex</span></span>  
    <span data-ttu-id="f2898-128">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f2898-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f2898-129">要讀取的陣列中第一個索引鍵範圍的索引。</span><span class="sxs-lookup"><span data-stu-id="f2898-129">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2898-130">rangeCount</span><span class="sxs-lookup"><span data-stu-id="f2898-130">rangeCount</span></span>  
    <span data-ttu-id="f2898-131">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f2898-131">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f2898-132">要 preread 的索引鍵範圍的最大數目。</span><span class="sxs-lookup"><span data-stu-id="f2898-132">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2898-133">rangesPreread</span><span class="sxs-lookup"><span data-stu-id="f2898-133">rangesPreread</span></span>  
    <span data-ttu-id="f2898-134">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f2898-134">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f2898-135">傳回實際 preread 的索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="f2898-135">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2898-136">columnsPreread</span><span class="sxs-lookup"><span data-stu-id="f2898-136">columnsPreread</span></span>  
    <span data-ttu-id="f2898-137">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="f2898-137">Type: \[\]</span></span>  
    
    <span data-ttu-id="f2898-138">要 preread 之 long 值資料行的資料行識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="f2898-138">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2898-139">grbit</span><span class="sxs-lookup"><span data-stu-id="f2898-139">grbit</span></span>  
    <span data-ttu-id="f2898-140">型別： [Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f2898-140">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f2898-141">Preread 選項。</span><span class="sxs-lookup"><span data-stu-id="f2898-141">Preread options.</span></span> <span data-ttu-id="f2898-142">用來指定 preread 的方向。</span><span class="sxs-lookup"><span data-stu-id="f2898-142">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2898-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2898-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f2898-144">參考</span><span class="sxs-lookup"><span data-stu-id="f2898-144">Reference</span></span>

[<span data-ttu-id="f2898-145">Windows8Api 類別</span><span class="sxs-lookup"><span data-stu-id="f2898-145">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="f2898-146">Windows8Api 成員</span><span class="sxs-lookup"><span data-stu-id="f2898-146">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="f2898-147">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="f2898-147">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
