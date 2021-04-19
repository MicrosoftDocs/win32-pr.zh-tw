---
description: 深入瞭解： JetGrowDatabase 函數
title: JetGrowDatabase 函式
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ed8ee9888a2e4ab7908b72cc071f7b8143ca6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975136"
---
# <a name="jetgrowdatabase-function"></a><span data-ttu-id="b9afc-103">JetGrowDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="b9afc-103">JetGrowDatabase Function</span></span>


<span data-ttu-id="b9afc-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b9afc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgrowdatabase-function"></a><span data-ttu-id="b9afc-105">JetGrowDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="b9afc-105">JetGrowDatabase Function</span></span>

<span data-ttu-id="b9afc-106">**JetGrowDatabase** 函數會擴充目前開啟之資料庫的大小。</span><span class="sxs-lookup"><span data-stu-id="b9afc-106">The **JetGrowDatabase** function extends the size of a database that is currently open.</span></span>

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="b9afc-107">參數</span><span class="sxs-lookup"><span data-stu-id="b9afc-107">Parameters</span></span>

<span data-ttu-id="b9afc-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b9afc-108">*sesid*</span></span>

<span data-ttu-id="b9afc-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="b9afc-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="b9afc-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="b9afc-110">*dbid*</span></span>

<span data-ttu-id="b9afc-111">將擴充的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b9afc-111">The database that will be extended.</span></span>

<span data-ttu-id="b9afc-112">*Cpg*</span><span class="sxs-lookup"><span data-stu-id="b9afc-112">*cpg*</span></span>

<span data-ttu-id="b9afc-113">所需的資料庫大小（以頁面為限）。</span><span class="sxs-lookup"><span data-stu-id="b9afc-113">The desired size of the database, in pages.</span></span>

<span data-ttu-id="b9afc-114">*pcpgReal*</span><span class="sxs-lookup"><span data-stu-id="b9afc-114">*pcpgReal*</span></span>

<span data-ttu-id="b9afc-115">在 API 呼叫之後，接收資料庫大小（以頁面為限）的數位指標。</span><span class="sxs-lookup"><span data-stu-id="b9afc-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="b9afc-116">如果 API 呼叫失敗， *pcpgReal* 的內容會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="b9afc-116">If the API call fails, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="b9afc-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9afc-117">Return Value</span></span>

<span data-ttu-id="b9afc-118">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="b9afc-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b9afc-119">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="b9afc-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9afc-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b9afc-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="b9afc-121">Description</span><span class="sxs-lookup"><span data-stu-id="b9afc-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9afc-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b9afc-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b9afc-123">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="b9afc-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9afc-124">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="b9afc-124">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="b9afc-125">磁片區上的可用空間不足，無法執行成長作業。</span><span class="sxs-lookup"><span data-stu-id="b9afc-125">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9afc-126">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="b9afc-126">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="b9afc-127"><a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>傳回檔案相關的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b9afc-127">A file-related error was returned by <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span> <span data-ttu-id="b9afc-128">如需可能傳回之其他檔案相關錯誤的詳細資訊，請參閱 <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>。</span><span class="sxs-lookup"><span data-stu-id="b9afc-128">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="b9afc-129">備註</span><span class="sxs-lookup"><span data-stu-id="b9afc-129">Remarks</span></span>

<span data-ttu-id="b9afc-130">如果在插入大量資料之前呼叫 **JetGrowDatabase** ，資料庫檔案將會在一項作業中成長。</span><span class="sxs-lookup"><span data-stu-id="b9afc-130">If **JetGrowDatabase** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="b9afc-131">這樣可以減少資料庫檔案在檔案系統層級上的片段，也可以減少資料庫檔案必須成長的次數。</span><span class="sxs-lookup"><span data-stu-id="b9afc-131">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="b9afc-132">成長資料庫檔案一次可能會比將其成長數次快。</span><span class="sxs-lookup"><span data-stu-id="b9afc-132">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="b9afc-133">目前只支援成長盤案。</span><span class="sxs-lookup"><span data-stu-id="b9afc-133">Only growing the file is currently supported.</span></span> <span data-ttu-id="b9afc-134">若要壓縮檔案，請使用 **esentutl.exe** 公用程式的磁碟重組功能。</span><span class="sxs-lookup"><span data-stu-id="b9afc-134">To shrink a file, use the defragmentation feature of the **esentutl.exe** utility program.</span></span>

<span data-ttu-id="b9afc-135">若要設定未開啟之資料庫的大小，請參閱 [JetSetDatabaseSize](./jetsetdatabasesize-function.md)。</span><span class="sxs-lookup"><span data-stu-id="b9afc-135">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="b9afc-136">檔案大小可能不符合 *pcpgReal* 中傳回的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="b9afc-136">The file size might not match the number of pages that are returned in *pcpgReal*.</span></span> <span data-ttu-id="b9afc-137">有兩個額外的保留頁面可能不會在 *pcpgReal* 中計算。</span><span class="sxs-lookup"><span data-stu-id="b9afc-137">There are two additional reserved pages that might not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b9afc-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9afc-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9afc-139"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="b9afc-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b9afc-140">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="b9afc-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9afc-141"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="b9afc-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b9afc-142">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="b9afc-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9afc-143"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="b9afc-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b9afc-144">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="b9afc-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9afc-145"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="b9afc-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b9afc-146">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="b9afc-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9afc-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b9afc-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b9afc-148">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="b9afc-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b9afc-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9afc-149">See Also</span></span>

[<span data-ttu-id="b9afc-150">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b9afc-150">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b9afc-151">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b9afc-151">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b9afc-152">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b9afc-152">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b9afc-153">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b9afc-153">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b9afc-154">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="b9afc-154">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="b9afc-155">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="b9afc-155">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="b9afc-156">JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="b9afc-156">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
