---
description: '深入瞭解： JetMove 方法 (JET_SESID、JET_TABLEID、Int32、MoveGrbit) '
title: 'JetMove 方法 (JET_SESID、JET_TABLEID、Int32、MoveGrbit) '
TOCTitle: JetMove method (JET_SESID, JET_TABLEID, Int32, MoveGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmove(v=EXCHG.10)
ms:contentKeyID: 55100765
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMove
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f6d77914a3dc4728626db8e4ffe271851099e5e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000330"
---
# <a name="apijetmove-method-jet_sesid-jet_tableid-int32-movegrbit"></a><span data-ttu-id="0ec1e-103">JetMove 方法 (JET_SESID、JET_TABLEID、Int32、MoveGrbit) </span><span class="sxs-lookup"><span data-stu-id="0ec1e-103">Api.JetMove method (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</span></span>

<span data-ttu-id="0ec1e-104">流覽索引。</span><span class="sxs-lookup"><span data-stu-id="0ec1e-104">Navigate through an index.</span></span> <span data-ttu-id="0ec1e-105">資料指標可放置在索引的開頭或結尾，並以指定的索引項目數目向前移動和轉寄。</span><span class="sxs-lookup"><span data-stu-id="0ec1e-105">The cursor can be positioned at the start or end of the index and moved backwards and forwards by a specified number of index entries.</span></span> <span data-ttu-id="0ec1e-106">另請參閱 [TryMoveFirst (JET_SESID、JET_TABLEID) ](./api.trymovefirst-method.md)、 [TryMoveLast (JET_SESID、JET_TABLEID) ](./api.trymovelast-method.md)、 [TryMoveNext (JET_SESID、JET_TABLEID) ](./api.trymovenext-method.md)、 [TryMovePrevious (JET_SESID JET_TABLEID) ](./api.trymoveprevious-method.md)。</span><span class="sxs-lookup"><span data-stu-id="0ec1e-106">Also see [TryMoveFirst(JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [TryMoveLast(JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [TryMoveNext(JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [TryMovePrevious(JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).</span></span>

<span data-ttu-id="0ec1e-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0ec1e-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0ec1e-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0ec1e-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0ec1e-109">語法</span><span class="sxs-lookup"><span data-stu-id="0ec1e-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numRows As Integer, _
    grbit As MoveGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRows As Integer
Dim grbit As MoveGrbitApi.JetMove(sesid, tableid, numRows, _
    grbit)
```

``` csharp
public static void JetMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numRows,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="0ec1e-110">參數</span><span class="sxs-lookup"><span data-stu-id="0ec1e-110">Parameters</span></span>

  - <span data-ttu-id="0ec1e-111">sesid</span><span class="sxs-lookup"><span data-stu-id="0ec1e-111">sesid</span></span>  
    <span data-ttu-id="0ec1e-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0ec1e-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0ec1e-113">要用於呼叫的會話。</span><span class="sxs-lookup"><span data-stu-id="0ec1e-113">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="0ec1e-114">tableid</span><span class="sxs-lookup"><span data-stu-id="0ec1e-114">tableid</span></span>  
    <span data-ttu-id="0ec1e-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0ec1e-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0ec1e-116">要放置的游標。</span><span class="sxs-lookup"><span data-stu-id="0ec1e-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="0ec1e-117">numRows</span><span class="sxs-lookup"><span data-stu-id="0ec1e-117">numRows</span></span>  
    <span data-ttu-id="0ec1e-118">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0ec1e-118">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0ec1e-119">位移，表示移動游標的距離。</span><span class="sxs-lookup"><span data-stu-id="0ec1e-119">An offset which indicates how far to move the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="0ec1e-120">grbit</span><span class="sxs-lookup"><span data-stu-id="0ec1e-120">grbit</span></span>  
    <span data-ttu-id="0ec1e-121">型別： [MoveGrbit](./movegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="0ec1e-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0ec1e-122">移動選項。</span><span class="sxs-lookup"><span data-stu-id="0ec1e-122">Move options.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ec1e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ec1e-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0ec1e-124">參考</span><span class="sxs-lookup"><span data-stu-id="0ec1e-124">Reference</span></span>

[<span data-ttu-id="0ec1e-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="0ec1e-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0ec1e-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="0ec1e-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0ec1e-127">JetMove 多載</span><span class="sxs-lookup"><span data-stu-id="0ec1e-127">JetMove overload</span></span>](./api.jetmove-method.md)

[<span data-ttu-id="0ec1e-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0ec1e-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
