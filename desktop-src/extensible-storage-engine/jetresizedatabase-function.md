---
description: 深入瞭解： JetResizeDatabase 函數
title: JetResizeDatabase 函式
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dadaa7eaa310c5b3a6a2730d316218bc2607d100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997255"
---
# <a name="jetresizedatabase-function"></a><span data-ttu-id="d752b-103">JetResizeDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="d752b-103">JetResizeDatabase Function</span></span>


<span data-ttu-id="d752b-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d752b-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="d752b-105">**JetResizeDatabase** 函式會擴充或縮減目前開啟之資料庫的大小。</span><span class="sxs-lookup"><span data-stu-id="d752b-105">The **JetResizeDatabase** function extends or shrinks the size of a database that is currently open.</span></span>

<span data-ttu-id="d752b-106">**JetResizeDatabase** 函式是在 Windows 8 作業系統中引進的。</span><span class="sxs-lookup"><span data-stu-id="d752b-106">The **JetResizeDatabase** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="d752b-107">參數</span><span class="sxs-lookup"><span data-stu-id="d752b-107">Parameters</span></span>

<span data-ttu-id="d752b-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d752b-108">*sesid*</span></span>

<span data-ttu-id="d752b-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="d752b-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="d752b-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="d752b-110">*dbid*</span></span>

<span data-ttu-id="d752b-111">將擴充的資料庫。</span><span class="sxs-lookup"><span data-stu-id="d752b-111">The database that will be extended.</span></span>

<span data-ttu-id="d752b-112">*Cpg*</span><span class="sxs-lookup"><span data-stu-id="d752b-112">*cpg*</span></span>

<span data-ttu-id="d752b-113">要求的資料庫大小（以頁面為限）。</span><span class="sxs-lookup"><span data-stu-id="d752b-113">The requested size of the database, in pages.</span></span>

<span data-ttu-id="d752b-114">*pcpgActual*</span><span class="sxs-lookup"><span data-stu-id="d752b-114">*pcpgActual*</span></span>

<span data-ttu-id="d752b-115">在 API 呼叫之後，接收資料庫大小（以頁面為限）的數位指標。</span><span class="sxs-lookup"><span data-stu-id="d752b-115">A pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="d752b-116">如果 API 呼叫失敗， *pcpgActual* 參數的內容會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="d752b-116">If the API call fails, the contents of *pcpgActual* parameter are undefined.</span></span>

<span data-ttu-id="d752b-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d752b-117">*grbit*</span></span>

<span data-ttu-id="d752b-118">一組位，指定下表所列的零或多個值。</span><span class="sxs-lookup"><span data-stu-id="d752b-118">A group of bits that specifies zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d752b-119">值</span><span class="sxs-lookup"><span data-stu-id="d752b-119">Value</span></span></p></th>
<th><p><span data-ttu-id="d752b-120">意義</span><span class="sxs-lookup"><span data-stu-id="d752b-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d752b-121">JET_bitResizeDatabaseOnlyGrow</span><span class="sxs-lookup"><span data-stu-id="d752b-121">JET_bitResizeDatabaseOnlyGrow</span></span></p></td>
<td><p><span data-ttu-id="d752b-122">只增加資料庫。</span><span class="sxs-lookup"><span data-stu-id="d752b-122">Only grow the database.</span></span> <span data-ttu-id="d752b-123">如果調整大小呼叫會壓縮資料庫，則不執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="d752b-123">If the resize call would shrink the database, do nothing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d752b-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="d752b-124">Return value</span></span>

<span data-ttu-id="d752b-125">此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="d752b-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="d752b-126">如需可能的可延伸儲存引擎 (ESE) 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="d752b-126">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d752b-127">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d752b-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="d752b-128">Description</span><span class="sxs-lookup"><span data-stu-id="d752b-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d752b-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d752b-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d752b-130">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="d752b-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d752b-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="d752b-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="d752b-132">磁片區上的可用空間不足，無法執行成長作業。</span><span class="sxs-lookup"><span data-stu-id="d752b-132">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d752b-133">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="d752b-133">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="d752b-134"><a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>函數傳回檔案相關的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d752b-134">A file-related error was returned by the <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> function.</span></span> <span data-ttu-id="d752b-135">如需可能傳回之其他檔案相關錯誤的詳細資訊，請參閱 <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>。</span><span class="sxs-lookup"><span data-stu-id="d752b-135">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="d752b-136">備註</span><span class="sxs-lookup"><span data-stu-id="d752b-136">Remarks</span></span>

<span data-ttu-id="d752b-137">如果在插入大量資料之前呼叫 **JetResizeDatabase** 函數，則會在一項作業中成長資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="d752b-137">If the **JetResizeDatabase** function is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="d752b-138">這樣可以減少資料庫檔案在檔案系統層級上的片段，也可以減少資料庫檔案必須成長的次數。</span><span class="sxs-lookup"><span data-stu-id="d752b-138">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="d752b-139">成長資料庫檔案一次可能會比將其成長數次快。</span><span class="sxs-lookup"><span data-stu-id="d752b-139">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="d752b-140">若要設定未開啟之資料庫的大小，請參閱 [JetSetDatabaseSize](./jetsetdatabasesize-function.md)。</span><span class="sxs-lookup"><span data-stu-id="d752b-140">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="d752b-141">檔案大小可能不符合 *pcpgReal* 參數中所傳回的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="d752b-141">The file size might not match the number of pages that are returned in the *pcpgReal* parameter.</span></span> <span data-ttu-id="d752b-142">*PcpgReal* 參數中可能不會計算兩個額外的保留頁面。</span><span class="sxs-lookup"><span data-stu-id="d752b-142">Two additional reserved pages might not be counted in the *pcpgReal* parameter.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d752b-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="d752b-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d752b-144"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="d752b-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d752b-145">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="d752b-145">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d752b-146"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="d752b-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d752b-147">需要 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="d752b-147">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d752b-148"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="d752b-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d752b-149">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="d752b-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d752b-150"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="d752b-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d752b-151">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="d752b-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d752b-152"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d752b-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d752b-153">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="d752b-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d752b-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d752b-154">See also</span></span>

[<span data-ttu-id="d752b-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d752b-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d752b-156">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d752b-156">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d752b-157">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d752b-157">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d752b-158">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d752b-158">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d752b-159">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="d752b-159">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="d752b-160">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="d752b-160">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="d752b-161">JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="d752b-161">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
