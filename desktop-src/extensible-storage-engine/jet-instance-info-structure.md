---
description: 深入瞭解： JET_INSTANCE_INFO 結構
title: JET_INSTANCE_INFO 結構
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd07d11a8b30e75f30bc5bfcaa3aca665baf1209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852264"
---
# <a name="jet_instance_info-structure"></a><span data-ttu-id="5f279-103">JET_INSTANCE_INFO 結構</span><span class="sxs-lookup"><span data-stu-id="5f279-103">JET_INSTANCE_INFO Structure</span></span>


<span data-ttu-id="5f279-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5f279-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance_info-structure"></a><span data-ttu-id="5f279-105">JET_INSTANCE_INFO 結構</span><span class="sxs-lookup"><span data-stu-id="5f279-105">JET_INSTANCE_INFO Structure</span></span>

<span data-ttu-id="5f279-106">當搭配 [JetGetInstanceInfo](./jetgetinstanceinfo-function.md)和 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)函數使用時， **JET_INSTANCE_INFO** 結構會接收有關執行中資料庫實例的資訊。</span><span class="sxs-lookup"><span data-stu-id="5f279-106">The **JET_INSTANCE_INFO** structure receives information about running database instances when used with the [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) and [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) functions.</span></span>

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a><span data-ttu-id="5f279-107">成員</span><span class="sxs-lookup"><span data-stu-id="5f279-107">Members</span></span>

<span data-ttu-id="5f279-108">**hInstanceId**</span><span class="sxs-lookup"><span data-stu-id="5f279-108">**hInstanceId**</span></span>

<span data-ttu-id="5f279-109">給定實例的 [JET_INSTANCE](./jet-instance.md) 。</span><span class="sxs-lookup"><span data-stu-id="5f279-109">The [JET_INSTANCE](./jet-instance.md) of the given instance.</span></span>

<span data-ttu-id="5f279-110">**szInstanceName**</span><span class="sxs-lookup"><span data-stu-id="5f279-110">**szInstanceName**</span></span>

<span data-ttu-id="5f279-111">資料庫執行個體的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f279-111">The name of the database instance.</span></span> <span data-ttu-id="5f279-112">如果實例沒有名稱，這個值可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="5f279-112">This value can be **NULL** if the instance does not have a name.</span></span>

<span data-ttu-id="5f279-113">**cDatabases**</span><span class="sxs-lookup"><span data-stu-id="5f279-113">**cDatabases**</span></span>

<span data-ttu-id="5f279-114">附加至資料庫實例的資料庫數目。</span><span class="sxs-lookup"><span data-stu-id="5f279-114">The number of databases that are attached to the database instance.</span></span> <span data-ttu-id="5f279-115">**cDatabases** 也會保留 **szDatabaseFileName**、 **szDatabaseDisplayName** 和 **szDatabaseSLVFileName** 中所傳回之字串陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="5f279-115">**cDatabases** also holds the size of the arrays of strings that are returned in **szDatabaseFileName**, **szDatabaseDisplayName**, and **szDatabaseSLVFileName**.</span></span>

<span data-ttu-id="5f279-116">**szDatabaseFileName**</span><span class="sxs-lookup"><span data-stu-id="5f279-116">**szDatabaseFileName**</span></span>

<span data-ttu-id="5f279-117">字串的陣列，每個字串都包含附加至資料庫實例的資料庫檔案名。</span><span class="sxs-lookup"><span data-stu-id="5f279-117">An array of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="5f279-118">陣列具有 **cDatabases** 元素。</span><span class="sxs-lookup"><span data-stu-id="5f279-118">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="5f279-119">**szDatabaseDisplayName**</span><span class="sxs-lookup"><span data-stu-id="5f279-119">**szDatabaseDisplayName**</span></span>

<span data-ttu-id="5f279-120">字串的陣列，每個字串都會保存資料庫的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5f279-120">An array of strings, each holding the display name of a database.</span></span> <span data-ttu-id="5f279-121">字串目前可以是 Null。</span><span class="sxs-lookup"><span data-stu-id="5f279-121">Currently the string can be NULL.</span></span> <span data-ttu-id="5f279-122">陣列具有 **cDatabases** 元素。</span><span class="sxs-lookup"><span data-stu-id="5f279-122">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="5f279-123">**szDatabaseSLVFileName**</span><span class="sxs-lookup"><span data-stu-id="5f279-123">**szDatabaseSLVFileName**</span></span>

<span data-ttu-id="5f279-124">字串的陣列，每個字串都包含附加至資料庫實例之 SLV 檔的檔案名。</span><span class="sxs-lookup"><span data-stu-id="5f279-124">An array of strings, each holding the file name of the SLV file that is attached to the database instance.</span></span> <span data-ttu-id="5f279-125">陣列具有 **cDatabases** 元素。</span><span class="sxs-lookup"><span data-stu-id="5f279-125">The array has **cDatabases** elements.</span></span> <span data-ttu-id="5f279-126">不支援 SLV 檔案，因此應忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="5f279-126">SLV files are not supported, so this field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="5f279-127">備註</span><span class="sxs-lookup"><span data-stu-id="5f279-127">Remarks</span></span>

<span data-ttu-id="5f279-128">每個資料庫實例都可以有多個附加的資料庫。</span><span class="sxs-lookup"><span data-stu-id="5f279-128">Each database instance can have several databases attached to it.</span></span>

<span data-ttu-id="5f279-129">針對給定的 **JET_INSTANCE_INFO** 結構，針對資料庫所傳回的字串陣列會採用相同的順序。</span><span class="sxs-lookup"><span data-stu-id="5f279-129">For a given **JET_INSTANCE_INFO** structure, the array of strings that is returned for the databases are in the same order.</span></span> <span data-ttu-id="5f279-130">例如，"szDatabaseDisplayName \[ i \] " 和 "szDatabaseFileName \[ i \] " 都會參考相同的資料庫。</span><span class="sxs-lookup"><span data-stu-id="5f279-130">For example, "szDatabaseDisplayName\[ i \]" and "szDatabaseFileName\[ i \]" both refer to the same database.</span></span>

### <a name="requirements"></a><span data-ttu-id="5f279-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f279-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f279-132"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="5f279-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5f279-133">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="5f279-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f279-134"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="5f279-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5f279-135">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="5f279-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f279-136"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="5f279-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5f279-137">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="5f279-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f279-138"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5f279-138"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5f279-139">實作為 <strong>JET_INSTANCE_INFO_W</strong> (Unicode) 和 <strong>JET_INSTANCE_INFO _A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="5f279-139">Implemented as <strong>JET_INSTANCE_INFO_W</strong> (Unicode) and <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5f279-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f279-140">See Also</span></span>

[<span data-ttu-id="5f279-141">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="5f279-141">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="5f279-142">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="5f279-142">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="5f279-143">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="5f279-143">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="5f279-144">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="5f279-144">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)
