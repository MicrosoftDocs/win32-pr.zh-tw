---
description: 深入瞭解： JET_LS
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3300fd88c0dd1e1fca55722bf58350e28f3c3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979255"
---
# <a name="jet_ls"></a><span data-ttu-id="bb556-103">JET_LS</span><span class="sxs-lookup"><span data-stu-id="bb556-103">JET_LS</span></span>


<span data-ttu-id="bb556-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bb556-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_ls"></a><span data-ttu-id="bb556-105">JET_LS</span><span class="sxs-lookup"><span data-stu-id="bb556-105">JET_LS</span></span>

<span data-ttu-id="bb556-106">**JET_LS** 資料類型包含本機儲存體 (LS) 的內容控制碼。這個控制碼可能會與資料指標或資料表相關聯，而且可能會參考動態配置的資源。</span><span class="sxs-lookup"><span data-stu-id="bb556-106">The **JET_LS** data type contains a context handle to local storage (LS).This handle might be associated with a cursor or a table and might refer to dynamically allocated resources.</span></span>

<span data-ttu-id="bb556-107">**WINDOWS xp： JET_LS** 是在 windows xp 中引進。</span><span class="sxs-lookup"><span data-stu-id="bb556-107">**Windows XP:  JET_LS** is introduced in Windows XP.</span></span>

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a><span data-ttu-id="bb556-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="bb556-108">Data Types</span></span>

<span data-ttu-id="bb556-109">JET_LS</span><span class="sxs-lookup"><span data-stu-id="bb556-109">JET_LS</span></span>

<span data-ttu-id="bb556-110">JET_LSNil 的值表示不正確內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="bb556-110">A value of JET_LSNil indicates an invalid context handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="bb556-111">備註</span><span class="sxs-lookup"><span data-stu-id="bb556-111">Remarks</span></span>

<span data-ttu-id="bb556-112">內容控制碼一開始會與 **JET_LS** 資料類型（使用 [JetSetLS](./jetsetls-function.md)）相關聯。</span><span class="sxs-lookup"><span data-stu-id="bb556-112">A context handle is initially associated with the **JET_LS** data type, using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="bb556-113">您可以使用 [JetGetLS](./jetgetls-function.md)，從 **JET_LS** 資料類型中取出內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="bb556-113">The context handle can be retrieved from the **JET_LS** data type, using [JetGetLS](./jetgetls-function.md).</span></span>

<span data-ttu-id="bb556-114">您可以使用 [JetGetLS](./jetgetls-function.md)搭配 JET_bitLSReset，明確地將內容控制碼與 **JET_LS** 資料類型解除關聯。</span><span class="sxs-lookup"><span data-stu-id="bb556-114">The context handle can be explicitly disassociated from the **JET_LS** data type using [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="bb556-115">或者，當資料庫引擎釋出基礎物件做為應用程式直接或間接動作的結果時，內容控制碼也可以從 **JET_LS** 資料類型隱含地解除關聯。</span><span class="sxs-lookup"><span data-stu-id="bb556-115">Alternatively, the context handle can be implicitly disassociated from the **JET_LS** data type when the underlying object is released by the database engine as a result of direct or indirect action by the application.</span></span> <span data-ttu-id="bb556-116">在隱含的情況下，會將執行時間回呼發給應用程式，讓它可以清除內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="bb556-116">In the implicit case, a runtime callback is issued to the application so that it can clean up the context handle.</span></span> <span data-ttu-id="bb556-117">如需從 **JET_LS** 資料類型隱含解除關聯的詳細資訊，請參閱 [JetSetLS](./jetsetls-function.md)。</span><span class="sxs-lookup"><span data-stu-id="bb556-117">For more information on implicitly disassociating from the **JET_LS** data type, see [JetSetLS](./jetsetls-function.md).</span></span>

<span data-ttu-id="bb556-118">下列旗標會與 JET_LS 資料類型相關聯。</span><span class="sxs-lookup"><span data-stu-id="bb556-118">The following flags are associated with the JET_LS data type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb556-119">詞彙</span><span class="sxs-lookup"><span data-stu-id="bb556-119">Term</span></span></p></th>
<th><p><span data-ttu-id="bb556-120">描述</span><span class="sxs-lookup"><span data-stu-id="bb556-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb556-121">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="bb556-121">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="bb556-122">內容控制碼與物件解除關聯。</span><span class="sxs-lookup"><span data-stu-id="bb556-122">The context handle is disassociated from the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb556-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="bb556-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="bb556-124">設定或取出與資料表資料指標相關聯的本機儲存體。</span><span class="sxs-lookup"><span data-stu-id="bb556-124">Set or retrieve the local storage associated with a table cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb556-125">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="bb556-125">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="bb556-126">設定或取得與資料表相關聯的本機儲存體。</span><span class="sxs-lookup"><span data-stu-id="bb556-126">Set or retrieve the local storage associated with a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb556-127">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="bb556-127">JET_LSNil</span></span></p></td>
<td><p><span data-ttu-id="bb556-128">內容控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="bb556-128">The context handle is invalid.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="bb556-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb556-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb556-130"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="bb556-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bb556-131">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="bb556-131">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb556-132"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="bb556-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bb556-133">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="bb556-133">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb556-134"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="bb556-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bb556-135">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="bb556-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="bb556-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb556-136">See Also</span></span>

[<span data-ttu-id="bb556-137">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="bb556-137">JetSetLS</span></span>](./jetsetls-function.md)  
[<span data-ttu-id="bb556-138">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="bb556-138">JetGetLS</span></span>](./jetgetls-function.md)
