---
description: 深入瞭解： JET_DBINFOUPGRADE 結構
title: JET_DBINFOUPGRADE 結構
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
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
ms.openlocfilehash: 9652b0050805ad116a7087cb2ec4cd146255b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966707"
---
# <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="a58d7-103">JET_DBINFOUPGRADE 結構</span><span class="sxs-lookup"><span data-stu-id="a58d7-103">JET_DBINFOUPGRADE Structure</span></span>


<span data-ttu-id="a58d7-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a58d7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="a58d7-105">JET_DBINFOUPGRADE 結構</span><span class="sxs-lookup"><span data-stu-id="a58d7-105">JET_DBINFOUPGRADE Structure</span></span>

<span data-ttu-id="a58d7-106">**JET_DBINFOUPGRADE** 結構會保存資料庫升級狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a58d7-106">The **JET_DBINFOUPGRADE** structure holds information about the upgrade status of the database.</span></span> <span data-ttu-id="a58d7-107">只有當 **JET_DBINFOUPGRADE** 已傳遞至 [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) 或 [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)時，才會抓取此值。</span><span class="sxs-lookup"><span data-stu-id="a58d7-107">This value is retrieved only if **JET_DBINFOUPGRADE** was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="a58d7-108">資料庫引擎目前的作業系統版本不需要此結構。</span><span class="sxs-lookup"><span data-stu-id="a58d7-108">This structure is not required for current operating system versions of the database engine.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a><span data-ttu-id="a58d7-109">成員</span><span class="sxs-lookup"><span data-stu-id="a58d7-109">Members</span></span>

<span data-ttu-id="a58d7-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="a58d7-110">**cbStruct**</span></span>

<span data-ttu-id="a58d7-111">設定為 **JET_DBINFOUPGRADE** 結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a58d7-111">Set to the size of the **JET_DBINFOUPGRADE** structure, in bytes.</span></span>

<span data-ttu-id="a58d7-112">**cbFilesizeLow**</span><span class="sxs-lookup"><span data-stu-id="a58d7-112">**cbFilesizeLow**</span></span>

<span data-ttu-id="a58d7-113">可反映資料庫目前檔案大小的低 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="a58d7-113">The low **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="a58d7-114">**cbFilesizeHigh**</span><span class="sxs-lookup"><span data-stu-id="a58d7-114">**cbFilesizeHigh**</span></span>

<span data-ttu-id="a58d7-115">會反映資料庫目前檔案大小的高 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="a58d7-115">The high **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="a58d7-116">**cbFreeSpaceRequiredLow**</span><span class="sxs-lookup"><span data-stu-id="a58d7-116">**cbFreeSpaceRequiredLow**</span></span>

<span data-ttu-id="a58d7-117">就地升級所需之估計可用磁碟空間的低 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="a58d7-117">The low **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="a58d7-118">**cbFreeSpaceRequiredHigh**</span><span class="sxs-lookup"><span data-stu-id="a58d7-118">**cbFreeSpaceRequiredHigh**</span></span>

<span data-ttu-id="a58d7-119">就地升級所需之估計可用磁碟空間的高 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="a58d7-119">The high **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="a58d7-120">**csecToUpgrade**</span><span class="sxs-lookup"><span data-stu-id="a58d7-120">**csecToUpgrade**</span></span>

<span data-ttu-id="a58d7-121">升級所需的預估時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a58d7-121">The estimated time required to upgrade, in seconds.</span></span>

<span data-ttu-id="a58d7-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a58d7-122">**ulFlags**</span></span>

<span data-ttu-id="a58d7-123">由零或多個下列旗標所組成的位欄位： **fUpgradable**、 **fAlreadyUpgraded**。</span><span class="sxs-lookup"><span data-stu-id="a58d7-123">A bit field made of zero or more of the following flags: **fUpgradable**, **fAlreadyUpgraded**.</span></span>

<span data-ttu-id="a58d7-124">**fUpgradable**</span><span class="sxs-lookup"><span data-stu-id="a58d7-124">**fUpgradable**</span></span>

<span data-ttu-id="a58d7-125">資料庫可升級。</span><span class="sxs-lookup"><span data-stu-id="a58d7-125">The database is upgradeable.</span></span>

<span data-ttu-id="a58d7-126">**fAlreadyUpgraded**</span><span class="sxs-lookup"><span data-stu-id="a58d7-126">**fAlreadyUpgraded**</span></span>

<span data-ttu-id="a58d7-127">資料庫會升級為目前的資料庫格式。</span><span class="sxs-lookup"><span data-stu-id="a58d7-127">The database is upgraded to the current database format.</span></span>

### <a name="remarks"></a><span data-ttu-id="a58d7-128">備註</span><span class="sxs-lookup"><span data-stu-id="a58d7-128">Remarks</span></span>

<span data-ttu-id="a58d7-129">[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)或 [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)的呼叫會填入 **JET_DBINFOUPGRADE** 結構。</span><span class="sxs-lookup"><span data-stu-id="a58d7-129">A **JET_DBINFOUPGRADE** structure is populated by a call to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="a58d7-130">如果函式不成功，則結構的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="a58d7-130">If the function does not succeed, the contents of the structure are undefined.</span></span>

### <a name="requirements"></a><span data-ttu-id="a58d7-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="a58d7-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a58d7-132"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="a58d7-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a58d7-133">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="a58d7-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a58d7-134"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="a58d7-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a58d7-135">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="a58d7-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a58d7-136"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="a58d7-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a58d7-137">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="a58d7-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a58d7-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a58d7-138">See Also</span></span>

[<span data-ttu-id="a58d7-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a58d7-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a58d7-140">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a58d7-140">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a58d7-141">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a58d7-141">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a58d7-142">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a58d7-142">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a58d7-143">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="a58d7-143">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="a58d7-144">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="a58d7-144">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="a58d7-145">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="a58d7-145">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="a58d7-146">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="a58d7-146">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
