---
description: 深入瞭解： JetCloseDatabase 函數
title: JetCloseDatabase 函式
TOCTitle: JetCloseDatabase Function
ms:assetid: e17a05dd-c30b-4e8f-8538-91a65e8052d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294123(v=EXCHG.10)
ms:contentKeyID: 32765737
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9088e0ebc3b4778d6968c999afc238e49fb2f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510919"
---
# <a name="jetclosedatabase-function"></a><span data-ttu-id="49ab0-103">JetCloseDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="49ab0-103">JetCloseDatabase Function</span></span>


<span data-ttu-id="49ab0-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="49ab0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosedatabase-function"></a><span data-ttu-id="49ab0-105">JetCloseDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="49ab0-105">JetCloseDatabase Function</span></span>

<span data-ttu-id="49ab0-106">**JetCloseDatabase** 函式會關閉先前以 [JetOpenDatabase](./jetopendatabase-function.md)開啟的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="49ab0-106">The **JetCloseDatabase** function closes a database file that was previously opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="49ab0-107">參數</span><span class="sxs-lookup"><span data-stu-id="49ab0-107">Parameters</span></span>

<span data-ttu-id="49ab0-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="49ab0-108">*sesid*</span></span>

<span data-ttu-id="49ab0-109">將用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="49ab0-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="49ab0-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="49ab0-110">*dbid*</span></span>

<span data-ttu-id="49ab0-111">要關閉的資料庫。</span><span class="sxs-lookup"><span data-stu-id="49ab0-111">The database to be closed.</span></span>

<span data-ttu-id="49ab0-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="49ab0-112">*grbit*</span></span>

<span data-ttu-id="49ab0-113">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="49ab0-113">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="49ab0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="49ab0-114">Return Value</span></span>

<span data-ttu-id="49ab0-115">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="49ab0-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="49ab0-116">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="49ab0-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49ab0-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="49ab0-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="49ab0-118">Description</span><span class="sxs-lookup"><span data-stu-id="49ab0-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49ab0-119">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="49ab0-119">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="49ab0-120">先前未開啟資料庫。</span><span class="sxs-lookup"><span data-stu-id="49ab0-120">The database was not previously opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ab0-121">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="49ab0-121">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="49ab0-122"><em>Dbid</em>參數不是有效的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="49ab0-122">The <em>dbid</em> parameter was not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ab0-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="49ab0-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="49ab0-124">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="49ab0-124">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="49ab0-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="49ab0-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49ab0-126"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="49ab0-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="49ab0-127">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="49ab0-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ab0-128"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="49ab0-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="49ab0-129">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="49ab0-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ab0-130"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="49ab0-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="49ab0-131">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="49ab0-131">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ab0-132"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="49ab0-132"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="49ab0-133">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="49ab0-133">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ab0-134"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="49ab0-134"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="49ab0-135">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="49ab0-135">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="49ab0-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49ab0-136">See Also</span></span>

[<span data-ttu-id="49ab0-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="49ab0-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="49ab0-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="49ab0-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="49ab0-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="49ab0-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="49ab0-140">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="49ab0-140">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="49ab0-141">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="49ab0-141">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="49ab0-142">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="49ab0-142">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="49ab0-143">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="49ab0-143">JetOpenDatabase</span></span>](./jetopendatabase-function.md)
