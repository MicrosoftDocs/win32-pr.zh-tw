---
description: 深入瞭解： Server2003Api. JetUpdate2 方法
title: 'Server2003Api. JetUpdate2 方法 (Server2003 的) '
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fff3687d42160df331bfe52660be232fe3b41d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112040"
---
# <a name="server2003apijetupdate2-method"></a><span data-ttu-id="d50ef-103">Server2003Api. JetUpdate2 方法</span><span class="sxs-lookup"><span data-stu-id="d50ef-103">Server2003Api.JetUpdate2 method</span></span>

<span data-ttu-id="d50ef-104">JetUpdate 函式會執行更新作業，包括將新的資料列插入資料表或更新現有的資料列。</span><span class="sxs-lookup"><span data-stu-id="d50ef-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="d50ef-105">藉由呼叫 [JetDelete (JET_SESID JET_TABLEID) ](./api.jetdelete-method.md)來執行刪除資料表資料列。</span><span class="sxs-lookup"><span data-stu-id="d50ef-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="d50ef-106">**命名空間：**  [Microsoft Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d50ef-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="d50ef-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d50ef-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d50ef-108">語法</span><span class="sxs-lookup"><span data-stu-id="d50ef-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d50ef-109">參數</span><span class="sxs-lookup"><span data-stu-id="d50ef-109">Parameters</span></span>

  - <span data-ttu-id="d50ef-110">sesid</span><span class="sxs-lookup"><span data-stu-id="d50ef-110">sesid</span></span>  
    <span data-ttu-id="d50ef-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d50ef-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d50ef-112">啟動更新的會話。</span><span class="sxs-lookup"><span data-stu-id="d50ef-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="d50ef-113">tableid</span><span class="sxs-lookup"><span data-stu-id="d50ef-113">tableid</span></span>  
    <span data-ttu-id="d50ef-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d50ef-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d50ef-115">要更新的資料指標。</span><span class="sxs-lookup"><span data-stu-id="d50ef-115">The cursor to update.</span></span> <span data-ttu-id="d50ef-116">應備妥更新。</span><span class="sxs-lookup"><span data-stu-id="d50ef-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="d50ef-117">書籤 (bookmark)</span><span class="sxs-lookup"><span data-stu-id="d50ef-117">bookmark</span></span>  
    <span data-ttu-id="d50ef-118">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="d50ef-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="d50ef-119">傳回已更新之記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="d50ef-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="d50ef-120">這個可以是 null。</span><span class="sxs-lookup"><span data-stu-id="d50ef-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="d50ef-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="d50ef-121">bookmarkSize</span></span>  
    <span data-ttu-id="d50ef-122">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d50ef-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d50ef-123">書簽緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="d50ef-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="d50ef-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="d50ef-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="d50ef-125">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d50ef-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d50ef-126">傳回書簽的實際大小。</span><span class="sxs-lookup"><span data-stu-id="d50ef-126">Returns the actual size of the bookmark.</span></span>

<!-- end list -->

  - <span data-ttu-id="d50ef-127">grbit</span><span class="sxs-lookup"><span data-stu-id="d50ef-127">grbit</span></span>  
    <span data-ttu-id="d50ef-128">型別： [Server2003. UpdateGrbit](./updategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d50ef-128">Type: [Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit](./updategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d50ef-129">更新選項。</span><span class="sxs-lookup"><span data-stu-id="d50ef-129">Update options.</span></span>

## <a name="remarks"></a><span data-ttu-id="d50ef-130">備註</span><span class="sxs-lookup"><span data-stu-id="d50ef-130">Remarks</span></span>

<span data-ttu-id="d50ef-131">JetUpdate 是執行插入或更新的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="d50ef-131">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="d50ef-132">更新的開始方式是呼叫[JetPrepareUpdate (JET_SESID、JET_TABLEID、JET_prep) ](./api.jetprepareupdate-method.md) ，然後藉由呼叫[JetSetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、 \[ \] 、Int32、SetColumnGrbit、JET_SETINFO) ](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md)一或多個時間來設定記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="d50ef-132">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="d50ef-133">最後，會呼叫 JetUpdate2 (JET_SESID、JET_TABLEID、 \[ \] 、Int32、Int32、UpdateGrbit) ，以完成更新作業。</span><span class="sxs-lookup"><span data-stu-id="d50ef-133">Finally, JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit) is called to complete the update operation.</span></span> <span data-ttu-id="d50ef-134">只有 JetUpdate 或而不是在 JetSetColumn 期間更新索引。</span><span class="sxs-lookup"><span data-stu-id="d50ef-134">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="d50ef-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d50ef-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d50ef-136">參考</span><span class="sxs-lookup"><span data-stu-id="d50ef-136">Reference</span></span>

[<span data-ttu-id="d50ef-137">Server2003Api 類別</span><span class="sxs-lookup"><span data-stu-id="d50ef-137">Server2003Api class</span></span>](./server2003api-class.md)

[<span data-ttu-id="d50ef-138">Server2003Api 成員</span><span class="sxs-lookup"><span data-stu-id="d50ef-138">Server2003Api members</span></span>](./server2003api-members.md)

[<span data-ttu-id="d50ef-139">Server2003 命名空間。</span><span class="sxs-lookup"><span data-stu-id="d50ef-139">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
