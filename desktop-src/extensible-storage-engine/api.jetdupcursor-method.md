---
description: 深入瞭解： JetDupCursor 方法
title: JetDupCursor 方法
TOCTitle: 'JetDupCursor method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupCursor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.DupCursorGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupcursor(v=EXCHG.10)
ms:contentKeyID: 55100686
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fce19d23838f3dfeab5317bfa7ea1aaacfcb508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511139"
---
# <a name="apijetdupcursor-method"></a><span data-ttu-id="e7585-103">JetDupCursor 方法</span><span class="sxs-lookup"><span data-stu-id="e7585-103">Api.JetDupCursor method</span></span>

<span data-ttu-id="e7585-104">複製開啟的資料指標，並傳回重復資料指標的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e7585-104">Duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="e7585-105">如果複製的資料指標是唯讀資料指標，則重復資料指標也是唯讀資料指標。</span><span class="sxs-lookup"><span data-stu-id="e7585-105">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="e7585-106">任何與建立搜尋索引鍵或更新記錄相關的狀態都不會複製到重複的資料指標中。</span><span class="sxs-lookup"><span data-stu-id="e7585-106">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="e7585-107">此外，原始資料指標的位置不會複製到重複的資料指標中。</span><span class="sxs-lookup"><span data-stu-id="e7585-107">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="e7585-108">重複的資料指標一律會在叢集索引上開啟，而且其位置一律會在資料表的第一個資料列上。</span><span class="sxs-lookup"><span data-stu-id="e7585-108">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

<span data-ttu-id="e7585-109">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e7585-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e7585-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e7585-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e7585-111">語法</span><span class="sxs-lookup"><span data-stu-id="e7585-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDupCursor ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef newTableid As JET_TABLEID, _
    grbit As DupCursorGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim newTableid As JET_TABLEID
Dim grbit As DupCursorGrbitApi.JetDupCursor(sesid, tableid, _
    newTableid, grbit)
```

``` csharp
public static void JetDupCursor(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_TABLEID newTableid,
    DupCursorGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e7585-112">參數</span><span class="sxs-lookup"><span data-stu-id="e7585-112">Parameters</span></span>

  - <span data-ttu-id="e7585-113">sesid</span><span class="sxs-lookup"><span data-stu-id="e7585-113">sesid</span></span>  
    <span data-ttu-id="e7585-114">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e7585-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e7585-115">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="e7585-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e7585-116">tableid</span><span class="sxs-lookup"><span data-stu-id="e7585-116">tableid</span></span>  
    <span data-ttu-id="e7585-117">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e7585-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e7585-118">要複製的資料指標。</span><span class="sxs-lookup"><span data-stu-id="e7585-118">The cursor to duplicate.</span></span>

<!-- end list -->

  - <span data-ttu-id="e7585-119">newTableid</span><span class="sxs-lookup"><span data-stu-id="e7585-119">newTableid</span></span>  
    <span data-ttu-id="e7585-120">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e7585-120">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e7585-121">重複的資料指標。</span><span class="sxs-lookup"><span data-stu-id="e7585-121">The duplicated cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="e7585-122">grbit</span><span class="sxs-lookup"><span data-stu-id="e7585-122">grbit</span></span>  
    <span data-ttu-id="e7585-123">型別： [DupCursorGrbit](./dupcursorgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="e7585-123">Type: [Microsoft.Isam.Esent.Interop.DupCursorGrbit](./dupcursorgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e7585-124">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="e7585-124">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7585-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7585-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e7585-126">參考</span><span class="sxs-lookup"><span data-stu-id="e7585-126">Reference</span></span>

[<span data-ttu-id="e7585-127">Api 類別</span><span class="sxs-lookup"><span data-stu-id="e7585-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e7585-128">Api 成員</span><span class="sxs-lookup"><span data-stu-id="e7585-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e7585-129">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e7585-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
