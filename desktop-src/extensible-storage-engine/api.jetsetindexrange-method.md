---
description: 深入瞭解： JetSetIndexRange 方法
title: JetSetIndexRange 方法
TOCTitle: 'JetSetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100817
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ad13e04674de60aa1c0f55cf4cd4570f8b7ddaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026140"
---
# <a name="apijetsetindexrange-method"></a><span data-ttu-id="c4937-103">JetSetIndexRange 方法</span><span class="sxs-lookup"><span data-stu-id="c4937-103">Api.JetSetIndexRange method</span></span>

<span data-ttu-id="c4937-104">暫時限制資料指標可以使用 [JetMove (JET_SESID、JET_TABLEID、Int32、MoveGrbit) ](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md) 的索引項目集合，以從目前索引項目目開始，然後在符合該資料指標中搜尋索引鍵所指定的搜尋準則和指定的系結準則的索引項目目結束。</span><span class="sxs-lookup"><span data-stu-id="c4937-104">Temporarily limits the set of index entries that the cursor can walk using [JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="c4937-105">您先前必須使用[JetMakeKey (JET_SESID、JET_TABLEID、 \[ \] 、Int32、MakeKeyGrbit) ](./api.jetmakekey-method.md)來建立搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c4937-105">A search key must have been previously constructed using [JetMakeKey(JET_SESID, JET_TABLEID, \[\], Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span></span> <span data-ttu-id="c4937-106">另請參閱 [TrySetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) ](./api.trysetindexrange-method.md)。</span><span class="sxs-lookup"><span data-stu-id="c4937-106">Also see [TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span></span>

<span data-ttu-id="c4937-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c4937-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c4937-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c4937-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c4937-109">語法</span><span class="sxs-lookup"><span data-stu-id="c4937-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbitApi.JetSetIndexRange(sesid, tableid, _
    grbit)
```

``` csharp
public static void JetSetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c4937-110">參數</span><span class="sxs-lookup"><span data-stu-id="c4937-110">Parameters</span></span>

  - <span data-ttu-id="c4937-111">sesid</span><span class="sxs-lookup"><span data-stu-id="c4937-111">sesid</span></span>  
    <span data-ttu-id="c4937-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c4937-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c4937-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="c4937-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4937-114">tableid</span><span class="sxs-lookup"><span data-stu-id="c4937-114">tableid</span></span>  
    <span data-ttu-id="c4937-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c4937-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c4937-116">要在其上設定索引範圍的資料指標。</span><span class="sxs-lookup"><span data-stu-id="c4937-116">The cursor to set the index range on.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4937-117">grbit</span><span class="sxs-lookup"><span data-stu-id="c4937-117">grbit</span></span>  
    <span data-ttu-id="c4937-118">型別： [SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="c4937-118">Type: [Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c4937-119">索引範圍選項。</span><span class="sxs-lookup"><span data-stu-id="c4937-119">Index range options.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4937-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4937-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c4937-121">參考</span><span class="sxs-lookup"><span data-stu-id="c4937-121">Reference</span></span>

[<span data-ttu-id="c4937-122">Api 類別</span><span class="sxs-lookup"><span data-stu-id="c4937-122">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c4937-123">Api 成員</span><span class="sxs-lookup"><span data-stu-id="c4937-123">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c4937-124">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c4937-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
