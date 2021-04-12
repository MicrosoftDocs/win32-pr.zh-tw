---
description: '深入瞭解： JetUpdate 方法 (JET_SESID、JET_TABLEID) '
title: 'JetUpdate 方法 (JET_SESID，JET_TABLEID) '
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100831
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
ms.openlocfilehash: f1875353e8a5b4a23302a5f008af2cfa42a89b11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320811"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid"></a><span data-ttu-id="e5356-103">JetUpdate 方法 (JET_SESID，JET_TABLEID) </span><span class="sxs-lookup"><span data-stu-id="e5356-103">Api.JetUpdate method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="e5356-104">JetUpdate 函式會執行更新作業，包括將新的資料列插入資料表或更新現有的資料列。</span><span class="sxs-lookup"><span data-stu-id="e5356-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="e5356-105">藉由呼叫 [JetDelete (JET_SESID JET_TABLEID) ](./api.jetdelete-method.md)來執行刪除資料表資料列。</span><span class="sxs-lookup"><span data-stu-id="e5356-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="e5356-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e5356-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e5356-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e5356-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e5356-108">語法</span><span class="sxs-lookup"><span data-stu-id="e5356-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetUpdate(sesid, tableid)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="e5356-109">參數</span><span class="sxs-lookup"><span data-stu-id="e5356-109">Parameters</span></span>

  - <span data-ttu-id="e5356-110">sesid</span><span class="sxs-lookup"><span data-stu-id="e5356-110">sesid</span></span>  
    <span data-ttu-id="e5356-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e5356-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e5356-112">啟動更新的會話。</span><span class="sxs-lookup"><span data-stu-id="e5356-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="e5356-113">tableid</span><span class="sxs-lookup"><span data-stu-id="e5356-113">tableid</span></span>  
    <span data-ttu-id="e5356-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e5356-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e5356-115">要更新的資料指標。</span><span class="sxs-lookup"><span data-stu-id="e5356-115">The cursor to update.</span></span> <span data-ttu-id="e5356-116">應備妥更新。</span><span class="sxs-lookup"><span data-stu-id="e5356-116">An update should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5356-117">備註</span><span class="sxs-lookup"><span data-stu-id="e5356-117">Remarks</span></span>

<span data-ttu-id="e5356-118">JetUpdate 是執行插入或更新的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="e5356-118">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="e5356-119">更新的開始方式是呼叫[JetPrepareUpdate (JET_SESID、JET_TABLEID、JET_prep) ](./api.jetprepareupdate-method.md) ，然後藉由呼叫[JetSetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、 \[ \] 、Int32、SetColumnGrbit、JET_SETINFO) ](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md)一或多個時間來設定記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="e5356-119">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="e5356-120">最後，會呼叫[JetUpdate (JET_SESID、JET_TABLEID、 \[ \] 、int32、int32) ](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) ，以完成更新作業。</span><span class="sxs-lookup"><span data-stu-id="e5356-120">Finally, [JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) is called to complete the update operation.</span></span> <span data-ttu-id="e5356-121">只有 JetUpdate 或而不是在 JetSetColumn 期間更新索引。</span><span class="sxs-lookup"><span data-stu-id="e5356-121">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5356-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5356-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e5356-123">參考</span><span class="sxs-lookup"><span data-stu-id="e5356-123">Reference</span></span>

[<span data-ttu-id="e5356-124">Api 類別</span><span class="sxs-lookup"><span data-stu-id="e5356-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e5356-125">Api 成員</span><span class="sxs-lookup"><span data-stu-id="e5356-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e5356-126">JetUpdate 多載</span><span class="sxs-lookup"><span data-stu-id="e5356-126">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="e5356-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e5356-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
