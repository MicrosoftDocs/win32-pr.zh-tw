---
description: 深入瞭解： ResetIndexRange 方法
title: ResetIndexRange 方法
TOCTitle: 'ResetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.ResetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.resetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100832
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.ResetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.ResetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 434740a549fa83d4601bf88ab09f307f4d19f189
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195397"
---
# <a name="apiresetindexrange-method"></a><span data-ttu-id="ed76d-103">ResetIndexRange 方法</span><span class="sxs-lookup"><span data-stu-id="ed76d-103">Api.ResetIndexRange method</span></span>

<span data-ttu-id="ed76d-104">移除以 [JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) ](./api.jetsetindexrange-method.md) 或 [TrySetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) ](./api.trysetindexrange-method.md)建立的索引範圍。</span><span class="sxs-lookup"><span data-stu-id="ed76d-104">Removes an index range created with [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) or [TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span></span> <span data-ttu-id="ed76d-105">如果沒有索引範圍存在，這個方法不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="ed76d-105">If no index range is present this method does nothing.</span></span>

<span data-ttu-id="ed76d-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ed76d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ed76d-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ed76d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ed76d-108">語法</span><span class="sxs-lookup"><span data-stu-id="ed76d-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub ResetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.ResetIndexRange(sesid, tableid)
```

``` csharp
public static void ResetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="ed76d-109">參數</span><span class="sxs-lookup"><span data-stu-id="ed76d-109">Parameters</span></span>

  - <span data-ttu-id="ed76d-110">sesid</span><span class="sxs-lookup"><span data-stu-id="ed76d-110">sesid</span></span>  
    <span data-ttu-id="ed76d-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ed76d-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ed76d-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="ed76d-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ed76d-113">tableid</span><span class="sxs-lookup"><span data-stu-id="ed76d-113">tableid</span></span>  
    <span data-ttu-id="ed76d-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ed76d-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ed76d-115">要移除索引範圍的資料指標。</span><span class="sxs-lookup"><span data-stu-id="ed76d-115">The cursor to remove the index range on.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed76d-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed76d-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ed76d-117">參考</span><span class="sxs-lookup"><span data-stu-id="ed76d-117">Reference</span></span>

[<span data-ttu-id="ed76d-118">Api 類別</span><span class="sxs-lookup"><span data-stu-id="ed76d-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ed76d-119">Api 成員</span><span class="sxs-lookup"><span data-stu-id="ed76d-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ed76d-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ed76d-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
