---
description: 深入瞭解： TryMove 方法
title: TryMove 方法
TOCTitle: 'TryMove method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymove(v=EXCHG.10)
ms:contentKeyID: 55100883
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMove
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d4b3aa596bb5e813d87dcc6f278112fe1e4cbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991666"
---
# <a name="apitrymove-method"></a><span data-ttu-id="b9b00-103">TryMove 方法</span><span class="sxs-lookup"><span data-stu-id="b9b00-103">Api.TryMove method</span></span>

<span data-ttu-id="b9b00-104">嘗試流覽索引。</span><span class="sxs-lookup"><span data-stu-id="b9b00-104">Try to navigate through an index.</span></span> <span data-ttu-id="b9b00-105">如果流覽成功，這個方法會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="b9b00-105">If the navigation succeeds this method returns true.</span></span> <span data-ttu-id="b9b00-106">如果沒有任何記錄可流覽此方法，則會傳回 false;將會擲回例外狀況，以找出其他錯誤。</span><span class="sxs-lookup"><span data-stu-id="b9b00-106">If there is no record to navigate to this method returns false; an exception will be thrown for other errors.</span></span>

<span data-ttu-id="b9b00-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b9b00-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b9b00-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b9b00-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b9b00-109">語法</span><span class="sxs-lookup"><span data-stu-id="b9b00-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    move As JET_Move, _
    grbit As MoveGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim move As JET_Move
Dim grbit As MoveGrbit
Dim returnValue As Boolean

returnValue = Api.TryMove(sesid, _
    tableid, move, grbit)
```

``` csharp
public static bool TryMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move move,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b9b00-110">參數</span><span class="sxs-lookup"><span data-stu-id="b9b00-110">Parameters</span></span>

  - <span data-ttu-id="b9b00-111">sesid</span><span class="sxs-lookup"><span data-stu-id="b9b00-111">sesid</span></span>  
    <span data-ttu-id="b9b00-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b9b00-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b9b00-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="b9b00-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9b00-114">tableid</span><span class="sxs-lookup"><span data-stu-id="b9b00-114">tableid</span></span>  
    <span data-ttu-id="b9b00-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b9b00-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b9b00-116">要放置的游標。</span><span class="sxs-lookup"><span data-stu-id="b9b00-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9b00-117">移動</span><span class="sxs-lookup"><span data-stu-id="b9b00-117">move</span></span>  
    <span data-ttu-id="b9b00-118">類型： [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b9b00-118">Type: [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)</span></span>  
    
    <span data-ttu-id="b9b00-119">要移動的方向。</span><span class="sxs-lookup"><span data-stu-id="b9b00-119">The direction to move in.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9b00-120">grbit</span><span class="sxs-lookup"><span data-stu-id="b9b00-120">grbit</span></span>  
    <span data-ttu-id="b9b00-121">型別： [MoveGrbit](./movegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="b9b00-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b9b00-122">移動選項。</span><span class="sxs-lookup"><span data-stu-id="b9b00-122">Move options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b9b00-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9b00-123">Return value</span></span>

<span data-ttu-id="b9b00-124">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b9b00-124">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b9b00-125">如果移動成功則為 True。</span><span class="sxs-lookup"><span data-stu-id="b9b00-125">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b9b00-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9b00-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b9b00-127">參考</span><span class="sxs-lookup"><span data-stu-id="b9b00-127">Reference</span></span>

[<span data-ttu-id="b9b00-128">Api 類別</span><span class="sxs-lookup"><span data-stu-id="b9b00-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b9b00-129">Api 成員</span><span class="sxs-lookup"><span data-stu-id="b9b00-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b9b00-130">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b9b00-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
