---
description: 深入瞭解： TrySetIndexRange 方法
title: TrySetIndexRange 方法
TOCTitle: 'TrySetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trysetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100893
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d175fdfc931d24742d61f962a45e690a5c49c2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695355"
---
# <a name="apitrysetindexrange-method"></a><span data-ttu-id="11a10-103">TrySetIndexRange 方法</span><span class="sxs-lookup"><span data-stu-id="11a10-103">Api.TrySetIndexRange method</span></span>

<span data-ttu-id="11a10-104">暫時限制索引項目的索引項目集合，其可使用 JetMove 從目前的索引項目目開始，然後在符合該資料指標中搜尋索引鍵所指定之搜尋準則的索引項目目和指定的系結準則中結束。</span><span class="sxs-lookup"><span data-stu-id="11a10-104">Temporarily limits the set of index entries that the cursor can walk using JetMove to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="11a10-105">搜尋金鑰必須先前已使用 JetMakeKey 來建立。</span><span class="sxs-lookup"><span data-stu-id="11a10-105">A search key must have been previously constructed using JetMakeKey.</span></span> <span data-ttu-id="11a10-106">如果索引範圍不是空的，則傳回 true，否則傳回 false。</span><span class="sxs-lookup"><span data-stu-id="11a10-106">Returns true if the index range is non-empty, false otherwise.</span></span>

<span data-ttu-id="11a10-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="11a10-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="11a10-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="11a10-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="11a10-109">語法</span><span class="sxs-lookup"><span data-stu-id="11a10-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbit
Dim returnValue As Boolean

returnValue = Api.TrySetIndexRange(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="11a10-110">參數</span><span class="sxs-lookup"><span data-stu-id="11a10-110">Parameters</span></span>

  - <span data-ttu-id="11a10-111">sesid</span><span class="sxs-lookup"><span data-stu-id="11a10-111">sesid</span></span>  
    <span data-ttu-id="11a10-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="11a10-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="11a10-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="11a10-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="11a10-114">tableid</span><span class="sxs-lookup"><span data-stu-id="11a10-114">tableid</span></span>  
    <span data-ttu-id="11a10-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="11a10-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="11a10-116">要放置的游標。</span><span class="sxs-lookup"><span data-stu-id="11a10-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="11a10-117">grbit</span><span class="sxs-lookup"><span data-stu-id="11a10-117">grbit</span></span>  
    <span data-ttu-id="11a10-118">型別： [SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="11a10-118">Type: [Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="11a10-119">搜尋選項。</span><span class="sxs-lookup"><span data-stu-id="11a10-119">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="11a10-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="11a10-120">Return value</span></span>

<span data-ttu-id="11a10-121">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="11a10-121">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="11a10-122">如果搜尋成功，則為 True。</span><span class="sxs-lookup"><span data-stu-id="11a10-122">True if the seek was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="11a10-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11a10-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="11a10-124">參考</span><span class="sxs-lookup"><span data-stu-id="11a10-124">Reference</span></span>

[<span data-ttu-id="11a10-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="11a10-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="11a10-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="11a10-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="11a10-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="11a10-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
