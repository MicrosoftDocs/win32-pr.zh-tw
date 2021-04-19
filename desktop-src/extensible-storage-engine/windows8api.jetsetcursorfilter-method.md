---
description: 深入瞭解： Windows8Api. JetSetCursorFilter 方法
title: 'Windows8Api. JetSetCursorFilter 方法 (Windows8 的) '
TOCTitle: 'JetSetCursorFilter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN[],Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetcursorfilter(v=EXCHG.10)
ms:contentKeyID: 55104447
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0137c25ee6ab548537d797af0a00a7ffcd1f6d5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973901"
---
# <a name="windows8apijetsetcursorfilter-method"></a><span data-ttu-id="0ce4a-103">Windows8Api. JetSetCursorFilter 方法</span><span class="sxs-lookup"><span data-stu-id="0ce4a-103">Windows8Api.JetSetCursorFilter method</span></span>

<span data-ttu-id="0ce4a-104">為 [JetMove (JET_SESID、JET_TABLEID、Int32、MoveGrbit) ](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md)設定簡單篩選的陣列。</span><span class="sxs-lookup"><span data-stu-id="0ce4a-104">Set an array of simple filters for [JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md).</span></span>

<span data-ttu-id="0ce4a-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0ce4a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="0ce4a-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0ce4a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce4a-107">語法</span><span class="sxs-lookup"><span data-stu-id="0ce4a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCursorFilter ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    filters As JET_INDEX_COLUMN(), _
    grbit As CursorFilterGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim filters As JET_INDEX_COLUMN()
Dim grbit As CursorFilterGrbitWindows8Api.JetSetCursorFilter(sesid, tableid, _
    filters, grbit)
```

``` csharp
public static void JetSetCursorFilter(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_COLUMN[] filters,
    CursorFilterGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="0ce4a-108">參數</span><span class="sxs-lookup"><span data-stu-id="0ce4a-108">Parameters</span></span>

  - <span data-ttu-id="0ce4a-109">sesid</span><span class="sxs-lookup"><span data-stu-id="0ce4a-109">sesid</span></span>  
    <span data-ttu-id="0ce4a-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0ce4a-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0ce4a-111">要用於呼叫的會話。</span><span class="sxs-lookup"><span data-stu-id="0ce4a-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="0ce4a-112">tableid</span><span class="sxs-lookup"><span data-stu-id="0ce4a-112">tableid</span></span>  
    <span data-ttu-id="0ce4a-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0ce4a-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0ce4a-114">要放置的游標。</span><span class="sxs-lookup"><span data-stu-id="0ce4a-114">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="0ce4a-115">filters</span><span class="sxs-lookup"><span data-stu-id="0ce4a-115">filters</span></span>  
    <span data-ttu-id="0ce4a-116">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="0ce4a-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="0ce4a-117">簡單的記錄篩選。</span><span class="sxs-lookup"><span data-stu-id="0ce4a-117">Simple record filters.</span></span>

<!-- end list -->

  - <span data-ttu-id="0ce4a-118">grbit</span><span class="sxs-lookup"><span data-stu-id="0ce4a-118">grbit</span></span>  
    <span data-ttu-id="0ce4a-119">型別： [Windows8. CursorFilterGrbit](./cursorfiltergrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0ce4a-119">Type: [Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit](./cursorfiltergrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0ce4a-120">移動選項。</span><span class="sxs-lookup"><span data-stu-id="0ce4a-120">Move options.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ce4a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ce4a-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0ce4a-122">參考</span><span class="sxs-lookup"><span data-stu-id="0ce4a-122">Reference</span></span>

[<span data-ttu-id="0ce4a-123">Windows8Api 類別</span><span class="sxs-lookup"><span data-stu-id="0ce4a-123">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="0ce4a-124">Windows8Api 成員</span><span class="sxs-lookup"><span data-stu-id="0ce4a-124">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="0ce4a-125">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="0ce4a-125">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
