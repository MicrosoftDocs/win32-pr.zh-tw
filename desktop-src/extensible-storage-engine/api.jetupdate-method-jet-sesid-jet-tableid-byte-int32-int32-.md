---
description: '深入瞭解： JetUpdate 方法 (JET_SESID、JET_TABLEID、位元組、Int32、Int32) '
title: 'JetUpdate 方法 (JET_SESID、JET_TABLEID、Byte、Int32、Int32) '
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c85e424fc9b672944801da3d03cbaff0ca48017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848341"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a><span data-ttu-id="25490-103">JetUpdate 方法 (JET_SESID、JET_TABLEID、Byte、Int32、Int32) </span><span class="sxs-lookup"><span data-stu-id="25490-103">Api.JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)</span></span>

<span data-ttu-id="25490-104">JetUpdate 函式會執行更新作業，包括將新的資料列插入資料表或更新現有的資料列。</span><span class="sxs-lookup"><span data-stu-id="25490-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="25490-105">藉由呼叫 [JetDelete (JET_SESID JET_TABLEID) ](./api.jetdelete-method.md)來執行刪除資料表資料列。</span><span class="sxs-lookup"><span data-stu-id="25490-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="25490-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25490-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25490-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="25490-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25490-108">語法</span><span class="sxs-lookup"><span data-stu-id="25490-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="25490-109">參數</span><span class="sxs-lookup"><span data-stu-id="25490-109">Parameters</span></span>

  - <span data-ttu-id="25490-110">sesid</span><span class="sxs-lookup"><span data-stu-id="25490-110">sesid</span></span>  
    <span data-ttu-id="25490-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25490-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="25490-112">啟動更新的會話。</span><span class="sxs-lookup"><span data-stu-id="25490-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="25490-113">tableid</span><span class="sxs-lookup"><span data-stu-id="25490-113">tableid</span></span>  
    <span data-ttu-id="25490-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25490-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="25490-115">要更新的資料指標。</span><span class="sxs-lookup"><span data-stu-id="25490-115">The cursor to update.</span></span> <span data-ttu-id="25490-116">應備妥更新。</span><span class="sxs-lookup"><span data-stu-id="25490-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="25490-117">書籤 (bookmark)</span><span class="sxs-lookup"><span data-stu-id="25490-117">bookmark</span></span>  
    <span data-ttu-id="25490-118">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="25490-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="25490-119">傳回已更新之記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="25490-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="25490-120">這個可以是 null。</span><span class="sxs-lookup"><span data-stu-id="25490-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="25490-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="25490-121">bookmarkSize</span></span>  
    <span data-ttu-id="25490-122">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="25490-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="25490-123">書簽緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="25490-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="25490-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="25490-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="25490-125">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="25490-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="25490-126">傳回書簽的實際大小。</span><span class="sxs-lookup"><span data-stu-id="25490-126">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="25490-127">備註</span><span class="sxs-lookup"><span data-stu-id="25490-127">Remarks</span></span>

<span data-ttu-id="25490-128">JetUpdate 是執行插入或更新的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="25490-128">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="25490-129">更新的開始方式是呼叫[JetPrepareUpdate (JET_SESID、JET_TABLEID、JET_prep) ](./api.jetprepareupdate-method.md) ，然後藉由呼叫[JetSetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、 \[ \] 、Int32、SetColumnGrbit、JET_SETINFO) ](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md)一或多個時間來設定記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="25490-129">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="25490-130">最後，會呼叫 JetUpdate (JET_SESID、JET_TABLEID、 \[ \] 、Int32、int32) ，以完成更新作業。</span><span class="sxs-lookup"><span data-stu-id="25490-130">Finally, JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32) is called to complete the update operation.</span></span> <span data-ttu-id="25490-131">只有 JetUpdate 或而不是在 JetSetColumn 期間更新索引。</span><span class="sxs-lookup"><span data-stu-id="25490-131">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="25490-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25490-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25490-133">參考</span><span class="sxs-lookup"><span data-stu-id="25490-133">Reference</span></span>

[<span data-ttu-id="25490-134">Api 類別</span><span class="sxs-lookup"><span data-stu-id="25490-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="25490-135">Api 成員</span><span class="sxs-lookup"><span data-stu-id="25490-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="25490-136">JetUpdate 多載</span><span class="sxs-lookup"><span data-stu-id="25490-136">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="25490-137">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="25490-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
