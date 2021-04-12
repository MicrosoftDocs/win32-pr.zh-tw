---
description: '深入瞭解： JetMove 方法 (JET_SESID、JET_TABLEID、JET_Move、MoveGrbit) '
title: 'JetMove 方法 (JET_SESID、JET_TABLEID、JET_Move、MoveGrbit) '
TOCTitle: JetMove method (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmove(v=EXCHG.10)
ms:contentKeyID: 55100766
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5b6eeaf8d728cf63304141614caaf9598bcc6c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695144"
---
# <a name="apijetmove-method-jet_sesid-jet_tableid-jet_move-movegrbit"></a><span data-ttu-id="fbafc-103">JetMove 方法 (JET_SESID、JET_TABLEID、JET_Move、MoveGrbit) </span><span class="sxs-lookup"><span data-stu-id="fbafc-103">Api.JetMove method (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)</span></span>

<span data-ttu-id="fbafc-104">流覽索引。</span><span class="sxs-lookup"><span data-stu-id="fbafc-104">Navigate through an index.</span></span> <span data-ttu-id="fbafc-105">資料指標可放置在索引的開頭或結尾，並以指定的索引項目數目向前移動和轉寄。</span><span class="sxs-lookup"><span data-stu-id="fbafc-105">The cursor can be positioned at the start or end of the index and moved backwards and forwards by a specified number of index entries.</span></span> <span data-ttu-id="fbafc-106">另請參閱 [TryMoveFirst (JET_SESID、JET_TABLEID) ](./api.trymovefirst-method.md)、 [TryMoveLast (JET_SESID、JET_TABLEID) ](./api.trymovelast-method.md)、 [TryMoveNext (JET_SESID、JET_TABLEID) ](./api.trymovenext-method.md)、 [TryMovePrevious (JET_SESID JET_TABLEID) ](./api.trymoveprevious-method.md)。</span><span class="sxs-lookup"><span data-stu-id="fbafc-106">Also see [TryMoveFirst(JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [TryMoveLast(JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [TryMoveNext(JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [TryMovePrevious(JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).</span></span>

<span data-ttu-id="fbafc-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fbafc-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fbafc-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fbafc-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fbafc-109">語法</span><span class="sxs-lookup"><span data-stu-id="fbafc-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numRows As JET_Move, _
    grbit As MoveGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRows As JET_Move
Dim grbit As MoveGrbitApi.JetMove(sesid, tableid, numRows, _
    grbit)
```

``` csharp
public static void JetMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move numRows,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="fbafc-110">參數</span><span class="sxs-lookup"><span data-stu-id="fbafc-110">Parameters</span></span>

  - <span data-ttu-id="fbafc-111">sesid</span><span class="sxs-lookup"><span data-stu-id="fbafc-111">sesid</span></span>  
    <span data-ttu-id="fbafc-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fbafc-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fbafc-113">要用於呼叫的會話。</span><span class="sxs-lookup"><span data-stu-id="fbafc-113">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="fbafc-114">tableid</span><span class="sxs-lookup"><span data-stu-id="fbafc-114">tableid</span></span>  
    <span data-ttu-id="fbafc-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fbafc-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fbafc-116">要放置的游標。</span><span class="sxs-lookup"><span data-stu-id="fbafc-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="fbafc-117">numRows</span><span class="sxs-lookup"><span data-stu-id="fbafc-117">numRows</span></span>  
    <span data-ttu-id="fbafc-118">類型： [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fbafc-118">Type: [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)</span></span>  
    
    <span data-ttu-id="fbafc-119">位移，表示移動游標的距離。</span><span class="sxs-lookup"><span data-stu-id="fbafc-119">An offset which indicates how far to move the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="fbafc-120">grbit</span><span class="sxs-lookup"><span data-stu-id="fbafc-120">grbit</span></span>  
    <span data-ttu-id="fbafc-121">型別： [MoveGrbit](./movegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="fbafc-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="fbafc-122">移動選項。</span><span class="sxs-lookup"><span data-stu-id="fbafc-122">Move options.</span></span>

## <a name="see-also"></a><span data-ttu-id="fbafc-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbafc-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fbafc-124">參考</span><span class="sxs-lookup"><span data-stu-id="fbafc-124">Reference</span></span>

[<span data-ttu-id="fbafc-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="fbafc-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fbafc-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="fbafc-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fbafc-127">JetMove 多載</span><span class="sxs-lookup"><span data-stu-id="fbafc-127">JetMove overload</span></span>](./api.jetmove-method.md)

[<span data-ttu-id="fbafc-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="fbafc-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
