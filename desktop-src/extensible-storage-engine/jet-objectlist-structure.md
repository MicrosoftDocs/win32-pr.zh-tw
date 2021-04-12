---
description: 深入瞭解： JET_OBJECTLIST 結構
title: JET_OBJECTLIST 結構
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
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
ms.openlocfilehash: a7a66bb3b7f7dfbbfd1087d1fe0ce32c4144a8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319983"
---
# <a name="jet_objectlist-structure"></a><span data-ttu-id="06c9d-103">JET_OBJECTLIST 結構</span><span class="sxs-lookup"><span data-stu-id="06c9d-103">JET_OBJECTLIST Structure</span></span>


<span data-ttu-id="06c9d-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="06c9d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_objectlist-structure"></a><span data-ttu-id="06c9d-105">JET_OBJECTLIST 結構</span><span class="sxs-lookup"><span data-stu-id="06c9d-105">JET_OBJECTLIST Structure</span></span>

<span data-ttu-id="06c9d-106">**JET_OBJECTLIST** 結構會遍歷以 [JetGetObjectInfo](./jetgetobjectinfo-function.md)建立的臨時表。</span><span class="sxs-lookup"><span data-stu-id="06c9d-106">The **JET_OBJECTLIST** structure traverses a temporary table that was created with [JetGetObjectInfo](./jetgetobjectinfo-function.md).</span></span> <span data-ttu-id="06c9d-107">臨時表中的每個資料列都會描述資料庫中的物件。</span><span class="sxs-lookup"><span data-stu-id="06c9d-107">Each row in the temporary table describes an object in the database.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a><span data-ttu-id="06c9d-108">成員</span><span class="sxs-lookup"><span data-stu-id="06c9d-108">Members</span></span>

<span data-ttu-id="06c9d-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="06c9d-109">**cbStruct**</span></span>

<span data-ttu-id="06c9d-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="06c9d-110">The size of the structure, in bytes.</span></span> <span data-ttu-id="06c9d-111">API 呼叫會更新此欄位，因此呼叫端應確定此值符合 sizeof ( JET_INDEXLIST ) 。</span><span class="sxs-lookup"><span data-stu-id="06c9d-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="06c9d-112">**tableid**</span><span class="sxs-lookup"><span data-stu-id="06c9d-112">**tableid**</span></span>

<span data-ttu-id="06c9d-113">所建立之臨時表的資料表識別碼。</span><span class="sxs-lookup"><span data-stu-id="06c9d-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="06c9d-114">呼叫端必須包含將關閉資料表的程式碼。</span><span class="sxs-lookup"><span data-stu-id="06c9d-114">The caller must contain code that will close the table.</span></span>

<span data-ttu-id="06c9d-115">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="06c9d-115">**cRecord**</span></span>

<span data-ttu-id="06c9d-116">已建立之臨時表中的記錄數目。</span><span class="sxs-lookup"><span data-stu-id="06c9d-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="06c9d-117">**columnidcontainername**</span><span class="sxs-lookup"><span data-stu-id="06c9d-117">**columnidcontainername**</span></span>

<span data-ttu-id="06c9d-118">容器型別名稱的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="06c9d-118">The column identifier of the name of the type of container.</span></span>

<span data-ttu-id="06c9d-119">目前唯一支援的容器是資料表。</span><span class="sxs-lookup"><span data-stu-id="06c9d-119">The only containers that are currently supported are tables.</span></span> <span data-ttu-id="06c9d-120">此資料行是 [JET_coltypText](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="06c9d-120">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="06c9d-121">**columnidobjectname**</span><span class="sxs-lookup"><span data-stu-id="06c9d-121">**columnidobjectname**</span></span>

<span data-ttu-id="06c9d-122">物件名稱的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="06c9d-122">The column identifier of the name of the object.</span></span>

<span data-ttu-id="06c9d-123">此資料行是 [JET_coltypText](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="06c9d-123">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="06c9d-124">**columnidobjtyp**</span><span class="sxs-lookup"><span data-stu-id="06c9d-124">**columnidobjtyp**</span></span>

<span data-ttu-id="06c9d-125">物件之類型的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="06c9d-125">The column identifier of the type of the object.</span></span> <span data-ttu-id="06c9d-126">目前唯一支援的容器是資料表，因此此欄位將會 JET_objtypTable。</span><span class="sxs-lookup"><span data-stu-id="06c9d-126">The only containers that are currently supported are tables, so this field will be JET_objtypTable.</span></span>

<span data-ttu-id="06c9d-127">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="06c9d-127">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="06c9d-128">**columniddtCreate**</span><span class="sxs-lookup"><span data-stu-id="06c9d-128">**columniddtCreate**</span></span>

<span data-ttu-id="06c9d-129">已過時。</span><span class="sxs-lookup"><span data-stu-id="06c9d-129">Obsolete.</span></span> <span data-ttu-id="06c9d-130">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="06c9d-130">Do not use.</span></span>

<span data-ttu-id="06c9d-131">**columniddtUpdate**</span><span class="sxs-lookup"><span data-stu-id="06c9d-131">**columniddtUpdate**</span></span>

<span data-ttu-id="06c9d-132">已過時。</span><span class="sxs-lookup"><span data-stu-id="06c9d-132">Obsolete.</span></span> <span data-ttu-id="06c9d-133">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="06c9d-133">Do not use.</span></span>

<span data-ttu-id="06c9d-134">**columnidgrbit**</span><span class="sxs-lookup"><span data-stu-id="06c9d-134">**columnidgrbit**</span></span>

<span data-ttu-id="06c9d-135">適用于物件之 **grbits** 的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="06c9d-135">The column identifier of the **grbits** that are applicable to the object.</span></span> <span data-ttu-id="06c9d-136">如需適用 **grbits** 的清單，請參閱 [JET_TABLECREATE](./jet-tablecreate-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="06c9d-136">For a list of applicable **grbits**, see [JET_TABLECREATE](./jet-tablecreate-structure.md).</span></span>

<span data-ttu-id="06c9d-137">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="06c9d-137">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="06c9d-138">**columnidflags**</span><span class="sxs-lookup"><span data-stu-id="06c9d-138">**columnidflags**</span></span>

<span data-ttu-id="06c9d-139">適用于物件之旗標的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="06c9d-139">The column identifier of the flags that are applicable to the object.</span></span> <span data-ttu-id="06c9d-140">如需適用旗標的清單，請參閱 [JET_OBJECTINFO](./jet-objectinfo-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="06c9d-140">For a list of applicable flags, see [JET_OBJECTINFO](./jet-objectinfo-structure.md).</span></span>

<span data-ttu-id="06c9d-141">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="06c9d-141">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="06c9d-142">**columnidcRecord**</span><span class="sxs-lookup"><span data-stu-id="06c9d-142">**columnidcRecord**</span></span>

<span data-ttu-id="06c9d-143">存在於資料表中，以 **columnidobjectname** 命名的記錄數目的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="06c9d-143">The column identifier of the number of records that are present in the table that is named in **columnidobjectname**.</span></span>

<span data-ttu-id="06c9d-144">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="06c9d-144">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="06c9d-145">**columnidcPage**</span><span class="sxs-lookup"><span data-stu-id="06c9d-145">**columnidcPage**</span></span>

<span data-ttu-id="06c9d-146">物件所使用之頁面數目的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="06c9d-146">The column identifier of the number of pages the object uses.</span></span>

<span data-ttu-id="06c9d-147">此資料行是 [JET_coltypLong](./jet-coltyp.md)。</span><span class="sxs-lookup"><span data-stu-id="06c9d-147">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="06c9d-148">備註</span><span class="sxs-lookup"><span data-stu-id="06c9d-148">Remarks</span></span>

<span data-ttu-id="06c9d-149">臨時表中的每個資料列都會對應至資料庫中的物件。</span><span class="sxs-lookup"><span data-stu-id="06c9d-149">Each row in the temporary table corresponds to an object in the database.</span></span>

<span data-ttu-id="06c9d-150">當使用 [JetGetObjectInfo](./jetgetobjectinfo-function.md)函數中的 *InfoLevel* 參數來建立臨時表時，設定為 JET_ObjInfoListNoStats 時， **columnidcRecord** 和 **columnidcPage** 所識別的資料行將不會包含有意義的資訊。</span><span class="sxs-lookup"><span data-stu-id="06c9d-150">When the temporary table is created with the *InfoLevel* parameter in the [JetGetObjectInfo](./jetgetobjectinfo-function.md) function set to JET_ObjInfoListNoStats, the columns identified by **columnidcRecord** and **columnidcPage** will not contain meaningful information.</span></span>

<span data-ttu-id="06c9d-151">目前，只有資料表的相關資訊會在臨時表中。</span><span class="sxs-lookup"><span data-stu-id="06c9d-151">Currently, only information about tables will be in the temporary table.</span></span>

### <a name="requirements"></a><span data-ttu-id="06c9d-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="06c9d-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06c9d-153"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="06c9d-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="06c9d-154">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="06c9d-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06c9d-155"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="06c9d-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="06c9d-156">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="06c9d-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06c9d-157"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="06c9d-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="06c9d-158">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="06c9d-158">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="06c9d-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06c9d-159">See Also</span></span>

[<span data-ttu-id="06c9d-160">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="06c9d-160">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="06c9d-161">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="06c9d-161">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="06c9d-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="06c9d-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="06c9d-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="06c9d-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="06c9d-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="06c9d-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="06c9d-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="06c9d-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="06c9d-166">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="06c9d-166">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="06c9d-167">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="06c9d-167">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="06c9d-168">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="06c9d-168">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)
