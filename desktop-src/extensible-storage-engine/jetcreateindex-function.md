---
description: 深入瞭解： JetCreateIndex 函數
title: JetCreateIndex 函式
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988843"
---
# <a name="jetcreateindex-function"></a><span data-ttu-id="154cb-103">JetCreateIndex 函式</span><span class="sxs-lookup"><span data-stu-id="154cb-103">JetCreateIndex Function</span></span>


<span data-ttu-id="154cb-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="154cb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex-function"></a><span data-ttu-id="154cb-105">JetCreateIndex 函式</span><span class="sxs-lookup"><span data-stu-id="154cb-105">JetCreateIndex Function</span></span>

<span data-ttu-id="154cb-106">**JetCreateIndex** 函式可讓您在可延伸的儲存引擎 (ESE) 資料庫中建立資料的索引，您可以用它來快速找出特定資料。</span><span class="sxs-lookup"><span data-stu-id="154cb-106">The **JetCreateIndex** function enables you to create an index of data in an Extensible Storage Engine (ESE) database, which you can use to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a><span data-ttu-id="154cb-107">參數</span><span class="sxs-lookup"><span data-stu-id="154cb-107">Parameters</span></span>

<span data-ttu-id="154cb-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="154cb-108">*sesid*</span></span>

<span data-ttu-id="154cb-109">用於特定 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="154cb-109">The database session context to use for a particular API call.</span></span>

<span data-ttu-id="154cb-110">*tableid*</span><span class="sxs-lookup"><span data-stu-id="154cb-110">*tableid*</span></span>

<span data-ttu-id="154cb-111">將為其建立索引的資料表。</span><span class="sxs-lookup"><span data-stu-id="154cb-111">The table that an index will be created for.</span></span>

<span data-ttu-id="154cb-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="154cb-112">*szIndexName*</span></span>

<span data-ttu-id="154cb-113">以 null 結束的字串指標，指定要建立之索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="154cb-113">A pointer to a null-terminated string that specifies the name of the index to be created.</span></span>

<span data-ttu-id="154cb-114">索引名稱必須符合下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="154cb-114">The index name must conform to the following guidelines:</span></span>

  - <span data-ttu-id="154cb-115">它必須包含少於 JET_cbNameMost 的字元數，而不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="154cb-115">It must contain fewer characters than JET_cbNameMost, not including the terminating null character.</span></span>

  - <span data-ttu-id="154cb-116">它必須只包含下列類別的字元：0到9、A 到 Z、a 到 z，以及 "" 以外的所有標點符號字元 \!</span><span class="sxs-lookup"><span data-stu-id="154cb-116">It must contain only characters from the following categories: 0 through 9, A through Z, a through z, and all punctuation characters except for "\!"</span></span> <span data-ttu-id="154cb-117"> (驚嘆號) 、"、" (逗號) 、" \[ " (左括弧) 和 " \] " (右括弧) ，也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c 和0x5d 至0x7f。</span><span class="sxs-lookup"><span data-stu-id="154cb-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, the ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="154cb-118">不得以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="154cb-118">It must not begin with a space.</span></span>

  - <span data-ttu-id="154cb-119">它至少必須包含一個非空白字元。</span><span class="sxs-lookup"><span data-stu-id="154cb-119">It must contain at least one non-space character.</span></span>

<span data-ttu-id="154cb-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="154cb-120">*grbit*</span></span>

<span data-ttu-id="154cb-121">位群組，其中包含要用於特定呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="154cb-121">A group of bits that contains the options to be used for a particular call.</span></span> <span data-ttu-id="154cb-122">這個參數可以包含在 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構中找到的零或多個選項。</span><span class="sxs-lookup"><span data-stu-id="154cb-122">This parameter can include zero or more of the options found in the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="154cb-123">*szKey*</span><span class="sxs-lookup"><span data-stu-id="154cb-123">*szKey*</span></span>

<span data-ttu-id="154cb-124">Null 分隔標記的雙 null 結束字串指標。</span><span class="sxs-lookup"><span data-stu-id="154cb-124">A pointer to a double null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="154cb-125">如需此參數的詳細資訊，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="154cb-125">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="154cb-126">*cbKey*</span><span class="sxs-lookup"><span data-stu-id="154cb-126">*cbKey*</span></span>

<span data-ttu-id="154cb-127">*SzKey* 參數的長度（以位元組為單位），包括兩個終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="154cb-127">The length, in bytes, of the *szKey* parameter, including the two terminating null characters.</span></span>

<span data-ttu-id="154cb-128">*lDensity*</span><span class="sxs-lookup"><span data-stu-id="154cb-128">*lDensity*</span></span>

<span data-ttu-id="154cb-129">初始索引 B + 樹狀結構的百分比密度。</span><span class="sxs-lookup"><span data-stu-id="154cb-129">The percentage density of the initial index B+ tree.</span></span>

<span data-ttu-id="154cb-130">如需此參數的詳細資訊，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="154cb-130">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

### <a name="return-value"></a><span data-ttu-id="154cb-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="154cb-131">Return Value</span></span>

<span data-ttu-id="154cb-132">此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="154cb-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="154cb-133">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="154cb-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="154cb-134">傳回碼</span><span class="sxs-lookup"><span data-stu-id="154cb-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="154cb-135">意義</span><span class="sxs-lookup"><span data-stu-id="154cb-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="154cb-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="154cb-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="154cb-137">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="154cb-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="154cb-138">如需 **JetCreateIndex** 函數可傳回的其他錯誤清單，請參閱 [JetCreateIndex2](./jetcreateindex2-function.md)。</span><span class="sxs-lookup"><span data-stu-id="154cb-138">For a list of additional errors that can be returned by the **JetCreateIndex** function, see [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="154cb-139">備註</span><span class="sxs-lookup"><span data-stu-id="154cb-139">Remarks</span></span>

<span data-ttu-id="154cb-140">呼叫 **JetCreateIndex** 函數等同于呼叫具有 [JET_INDEXCREATE](./jet-indexcreate-structure.md)結構的 [JetCreateIndex2](./jetcreateindex2-function.md)函式，其中包含與 **JetCreateIndex** 參數相同的設定，以及等於1的 *cIndexCreate* 參數。</span><span class="sxs-lookup"><span data-stu-id="154cb-140">Calling the **JetCreateIndex** function is identical to calling the [JetCreateIndex2](./jetcreateindex2-function.md) function with a [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure containing the same settings as the parameters of **JetCreateIndex**, and a *cIndexCreate* parameter equal to 1.</span></span> <span data-ttu-id="154cb-141">如果 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構的欄位在 **JetCreateIndex** 中沒有對應的參數，則會假設為0值。</span><span class="sxs-lookup"><span data-stu-id="154cb-141">For the fields of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure that do not have corresponding parameters in **JetCreateIndex**, a value of 0 is assumed.</span></span>

<span data-ttu-id="154cb-142">請注意， **JetCreateIndex** 已被 [JetCreateIndex2](./jetcreateindex2-function.md)取代。</span><span class="sxs-lookup"><span data-stu-id="154cb-142">Note that **JetCreateIndex** has been superseded by [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="154cb-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="154cb-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="154cb-144">用戶端</span><span class="sxs-lookup"><span data-stu-id="154cb-144">Client</span></span></p></td>
<td><p><span data-ttu-id="154cb-145">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="154cb-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="154cb-146">伺服器</span><span class="sxs-lookup"><span data-stu-id="154cb-146">Server</span></span></p></td>
<td><p><span data-ttu-id="154cb-147">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="154cb-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="154cb-148">標頭</span><span class="sxs-lookup"><span data-stu-id="154cb-148">Header</span></span></p></td>
<td><p><span data-ttu-id="154cb-149">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="154cb-149">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="154cb-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="154cb-150">Library</span></span></p></td>
<td><p><span data-ttu-id="154cb-151">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="154cb-151">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="154cb-152">DLL</span><span class="sxs-lookup"><span data-stu-id="154cb-152">DLL</span></span></p></td>
<td><p><span data-ttu-id="154cb-153">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="154cb-153">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="154cb-154">Unicode</span><span class="sxs-lookup"><span data-stu-id="154cb-154">Unicode</span></span></p></td>
<td><p><span data-ttu-id="154cb-155">會實作為 <strong>JetCreateIndexW</strong> (Unicode) 和 <strong>JetCreateIndexA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="154cb-155">Is implemented as <strong>JetCreateIndexW</strong> (Unicode) and <strong>JetCreateIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="154cb-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="154cb-156">See Also</span></span>

[<span data-ttu-id="154cb-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="154cb-157">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="154cb-158">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="154cb-158">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="154cb-159">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="154cb-159">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="154cb-160">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="154cb-160">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="154cb-161">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="154cb-161">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="154cb-162">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="154cb-162">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="154cb-163">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="154cb-163">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="154cb-164">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="154cb-164">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
