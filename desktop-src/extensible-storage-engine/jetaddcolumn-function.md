---
description: 深入瞭解： JetAddColumn 函數
title: JetAddColumn 函式
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b8c3eac113daeae43ec4a8e62b7fcda9ddbf9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979304"
---
# <a name="jetaddcolumn-function"></a><span data-ttu-id="602db-103">JetAddColumn 函式</span><span class="sxs-lookup"><span data-stu-id="602db-103">JetAddColumn Function</span></span>


<span data-ttu-id="602db-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="602db-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetaddcolumn-function"></a><span data-ttu-id="602db-105">JetAddColumn 函式</span><span class="sxs-lookup"><span data-stu-id="602db-105">JetAddColumn Function</span></span>

<span data-ttu-id="602db-106">**JetAddColumn** 函數會將新的資料行加入至 ESE 資料庫中的現有資料表。</span><span class="sxs-lookup"><span data-stu-id="602db-106">The **JetAddColumn** function adds a new column to an existing table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="602db-107">參數</span><span class="sxs-lookup"><span data-stu-id="602db-107">Parameters</span></span>

<span data-ttu-id="602db-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="602db-108">*sesid*</span></span>

<span data-ttu-id="602db-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="602db-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="602db-110">*tableid*</span><span class="sxs-lookup"><span data-stu-id="602db-110">*tableid*</span></span>

<span data-ttu-id="602db-111">要加入資料行的資料表。</span><span class="sxs-lookup"><span data-stu-id="602db-111">The table to which to add the column.</span></span>

<span data-ttu-id="602db-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="602db-112">*szColumnName*</span></span>

<span data-ttu-id="602db-113">要加入之資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="602db-113">The name of the column to add.</span></span> <span data-ttu-id="602db-114">此名稱必須符合下列準則：</span><span class="sxs-lookup"><span data-stu-id="602db-114">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="602db-115">長度必須少於 JET_cbNameMost 個字元，不包括終止的 **Null**。</span><span class="sxs-lookup"><span data-stu-id="602db-115">It must be fewer than JET_cbNameMost characters in length, not including the terminating **NULL**.</span></span>

  - <span data-ttu-id="602db-116">它必須只包含下列集合中的字元：0到9、A 到 Z、a 到 z，以及除了驚嘆號以外的所有其他標點符號 (\!) 、逗點 (、) 、左括弧 (\[) 和右括弧 () ， \] 也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c 和0x5d 至0x7f。</span><span class="sxs-lookup"><span data-stu-id="602db-116">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="602db-117">它不能以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="602db-117">It cannot begin with a space.</span></span>

  - <span data-ttu-id="602db-118">它至少必須包含一個非空白字元。</span><span class="sxs-lookup"><span data-stu-id="602db-118">It must contain at least one non-space character.</span></span>

<span data-ttu-id="602db-119">*pcolumndef*</span><span class="sxs-lookup"><span data-stu-id="602db-119">*pcolumndef*</span></span>

<span data-ttu-id="602db-120">[JET_COLUMNDEF](./jet-columndef-structure.md)結構的指標，此結構會定義可儲存在資料行中的資料。</span><span class="sxs-lookup"><span data-stu-id="602db-120">A pointer to a [JET_COLUMNDEF](./jet-columndef-structure.md) structure, which defines the data that can be stored in a column.</span></span>

<span data-ttu-id="602db-121">*pvDefault*</span><span class="sxs-lookup"><span data-stu-id="602db-121">*pvDefault*</span></span>

<span data-ttu-id="602db-122">緩衝區的指標，其中包含資料行的預設值。</span><span class="sxs-lookup"><span data-stu-id="602db-122">A pointer to a buffer that contains the default value for the column.</span></span> <span data-ttu-id="602db-123">緩衝區的長度為 **cbDefault**。</span><span class="sxs-lookup"><span data-stu-id="602db-123">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="602db-124">如果沒有預設值，請將 **pvDefault** 設定為 **Null** ，並將 **cbDefault** 設定為零。</span><span class="sxs-lookup"><span data-stu-id="602db-124">If there is no default, set **pvDefault** to **NULL** and **cbDefault** to zero.</span></span> <span data-ttu-id="602db-125">固定資料行的預設值不能大於 JET_cbColumnMost 個位元組，或 long 值的 JET_cbLVDefaultValueMost 個位元組。</span><span class="sxs-lookup"><span data-stu-id="602db-125">Default values cannot be larger than JET_cbColumnMost bytes for fixed columns or JET_cbLVDefaultValueMost bytes for long values.</span></span> <span data-ttu-id="602db-126">如果預設值大於該值，則會以無訊息模式截斷。</span><span class="sxs-lookup"><span data-stu-id="602db-126">If a default value is larger than that, it will be silently truncated.</span></span>

<span data-ttu-id="602db-127">如果 *grbit* 已設定 JET_bitColumnUserDefinedDefault， **pvDefault** 將會被解釋為 [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="602db-127">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure.</span></span>

<span data-ttu-id="602db-128">*cbDefault*</span><span class="sxs-lookup"><span data-stu-id="602db-128">*cbDefault*</span></span>

<span data-ttu-id="602db-129">在 **pvDefault** 中指定的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="602db-129">The size, in bytes, of the buffer that is specified in **pvDefault**.</span></span>

<span data-ttu-id="602db-130">*>ekind*</span><span class="sxs-lookup"><span data-stu-id="602db-130">*pcolumnid*</span></span>

<span data-ttu-id="602db-131">[JET_COLUMNID](./jet-columnid.md)結構的指標，在成功的情況下，將會接收新建立之資料行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="602db-131">A pointer to a [JET_COLUMNID](./jet-columnid.md) structure, which, on success, will receive the identifier of the newly created column.</span></span> <span data-ttu-id="602db-132">失敗時，值為未定義。</span><span class="sxs-lookup"><span data-stu-id="602db-132">On failure, the value is undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="602db-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="602db-133">Return Value</span></span>

<span data-ttu-id="602db-134">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="602db-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="602db-135">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="602db-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="602db-136">傳回碼</span><span class="sxs-lookup"><span data-stu-id="602db-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="602db-137">Description</span><span class="sxs-lookup"><span data-stu-id="602db-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="602db-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="602db-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="602db-139">作業成功。</span><span class="sxs-lookup"><span data-stu-id="602db-139">The operation was successful.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-140">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="602db-140">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="602db-141">嘗試修改固定 DDL 資料表的資料定義。</span><span class="sxs-lookup"><span data-stu-id="602db-141">An attempt was made to modify the data definition of a fixed DDL table.</span></span> <span data-ttu-id="602db-142">具有固定 DDL 的資料表範例是範本資料表。</span><span class="sxs-lookup"><span data-stu-id="602db-142">An example of a table with fixed DDL is a Template Table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="602db-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="602db-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="602db-144">傳遞至 API 的參數無效。</span><span class="sxs-lookup"><span data-stu-id="602db-144">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="602db-145">以下是無效參數的一些範例：</span><span class="sxs-lookup"><span data-stu-id="602db-145">Some examples of invalid parameters are:</span></span></p>
<ul>
<li><p><span data-ttu-id="602db-146">在其<em>cbStruct</em>成員中傳遞錯誤的<a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>結構大小。</span><span class="sxs-lookup"><span data-stu-id="602db-146">Passing in the wrong size of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure in its <em>cbStruct</em> member.</span></span></p></li>
<li><p><span data-ttu-id="602db-147">傳入 JET_bitColumnUserDefinedDefault，但未將 <strong>cbDefault</strong> 設定為 sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>) 。</span><span class="sxs-lookup"><span data-stu-id="602db-147">Passing in JET_bitColumnUserDefinedDefault, but not setting <strong>cbDefault</strong> to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-148">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="602db-148">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="602db-149">嘗試加入具有 JET_bitColumnUnversioned 位集的資料行，但該會話目前位於交易中。</span><span class="sxs-lookup"><span data-stu-id="602db-149">An attempt was made to add a column with the JET_bitColumnUnversioned bit set, but the session is currently in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="602db-150">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="602db-150">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="602db-151">資料行已經存在。</span><span class="sxs-lookup"><span data-stu-id="602db-151">A column already exists.</span></span> <span data-ttu-id="602db-152">嘗試加入沒有版本資訊的資料行，而且該資料行已經存在。</span><span class="sxs-lookup"><span data-stu-id="602db-152">An attempt was made to add a column without version information, and that column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-153">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="602db-153">JET_errTableNotEmpty</span></span></p></td>
<td><p><span data-ttu-id="602db-154">資料表包含資料。</span><span class="sxs-lookup"><span data-stu-id="602db-154">The table contains data.</span></span> <span data-ttu-id="602db-155">您只能將 [保管更新] 資料行新增至空白資料表。</span><span class="sxs-lookup"><span data-stu-id="602db-155">An Escrow Update column can only be added to an empty table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="602db-156">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="602db-156">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="602db-157">記錄太大。</span><span class="sxs-lookup"><span data-stu-id="602db-157">The record is too big.</span></span> <span data-ttu-id="602db-158">固定資料行之 <strong>cbMax</strong> 參數的總和不得超過某個值。</span><span class="sxs-lookup"><span data-stu-id="602db-158">The sum of the <strong>cbMax</strong> parameter for the fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-159">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="602db-159">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="602db-160">嘗試將過多的資料行新增至資料表。</span><span class="sxs-lookup"><span data-stu-id="602db-160">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="602db-161">資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="602db-161">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="602db-162">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="602db-162">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="602db-163">嘗試加入重複的資料行。</span><span class="sxs-lookup"><span data-stu-id="602db-163">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="602db-164">應該不會有一個以上的自動遞增資料行，而且每個資料表不能有一個以上的版本資料行。</span><span class="sxs-lookup"><span data-stu-id="602db-164">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-165">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="602db-165">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="602db-166">無法解析回呼函數。</span><span class="sxs-lookup"><span data-stu-id="602db-166">The callback function could not be resolved.</span></span> <span data-ttu-id="602db-167">可能找不到 DLL，或可能找不到 DLL 中的函數。</span><span class="sxs-lookup"><span data-stu-id="602db-167">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="602db-168">如果啟用了足夠的記錄，事件記錄檔將會提供更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="602db-168">The event log will provide more details if sufficient logging is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="602db-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="602db-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="602db-170">指出固定或變數資料行 (<strong>cbMax</strong>) 長度上限大於 JET_cbColumnMost 的警告。</span><span class="sxs-lookup"><span data-stu-id="602db-170">A warning indicating that the maximum length (<strong>cbMax</strong>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="602db-171">這項限制不適用於 <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> 和 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) 的 Long 值 (。</span><span class="sxs-lookup"><span data-stu-id="602db-171">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-172">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="602db-172">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="602db-173">傳遞的名稱無效，因為 <strong>szColumnName</strong>。</span><span class="sxs-lookup"><span data-stu-id="602db-173">An invalid name was passed as <strong>szColumnName</strong>.</span></span> <span data-ttu-id="602db-174">如需有關限制的詳細資訊，請參閱 <strong>szColumnName</strong>的準則。</span><span class="sxs-lookup"><span data-stu-id="602db-174">For more information about the restrictions, see the criteria for <strong>szColumnName</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="602db-175">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="602db-175">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="602db-176"><strong>Coltyp</strong>欄位未設定為有效的資料行類型。</span><span class="sxs-lookup"><span data-stu-id="602db-176">The <strong>coltyp</strong> field was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-177">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="602db-177">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="602db-178"><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>結構的<strong>cp</strong>參數未設定為有效的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="602db-178">The <strong>cp</strong> parameter of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="602db-179">Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。</span><span class="sxs-lookup"><span data-stu-id="602db-179">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="602db-180">0值表示預設值將使用 (英文、1252) 。</span><span class="sxs-lookup"><span data-stu-id="602db-180">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="602db-181">JET_errTaggedNotNull</span><span class="sxs-lookup"><span data-stu-id="602db-181">JET_errTaggedNotNULL</span></span></p></td>
<td><p><span data-ttu-id="602db-182">JET_bitColumnNotNull 不能與加上標籤、Long 值或 SLV 資料行一起使用。</span><span class="sxs-lookup"><span data-stu-id="602db-182">JET_bitColumnNotNULL cannot be used with tagged, Long Value, or SLV columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-183">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="602db-183">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="602db-184">指定了不正確 <em>grbits</em> 組合。</span><span class="sxs-lookup"><span data-stu-id="602db-184">An invalid combination of <em>grbits</em> was specified.</span></span> <span data-ttu-id="602db-185">此錯誤的部分原因如下：</span><span class="sxs-lookup"><span data-stu-id="602db-185">Some of the reasons for this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="602db-186">JET_bitColumnFixed 用於已標記、Long 值或 SLV 資料行。</span><span class="sxs-lookup"><span data-stu-id="602db-186">JET_bitColumnFixed was used on a tagged, Long Value, or SLV column.</span></span></p></li>
<li><p><span data-ttu-id="602db-187">JET_bitColumnEscrowUpdate 用於不是 <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>類型的資料行。</span><span class="sxs-lookup"><span data-stu-id="602db-187">JET_bitColumnEscrowUpdate was used on a column that was not of type <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="602db-188">JET_bitColumnEscrowUpdate 用於 (JET_bitColumnVersion) 的版本資料行。</span><span class="sxs-lookup"><span data-stu-id="602db-188">JET_bitColumnEscrowUpdate was used on a Version column (JET_bitColumnVersion).</span></span></p></li>
<li><p><span data-ttu-id="602db-189">JET_bitColumnEscrowUpdate 用在 AutoIncrememnt 資料行上 (JET_bitColumnAutoincrement) 。</span><span class="sxs-lookup"><span data-stu-id="602db-189">JET_bitColumnEscrowUpdate was used on an AutoIncrememnt column (JET_bitColumnAutoincrement).</span></span></p></li>
<li><p><span data-ttu-id="602db-190">JET_bitColumnEscrowUpdate 在沒有預設值的資料行上使用 (<strong>cbDefault</strong> 等於零) 。</span><span class="sxs-lookup"><span data-stu-id="602db-190">JET_bitColumnEscrowUpdate was used on a column that did not have a default value (<strong>cbDefault</strong> was equal to zero).</span></span></p></li>
<li><p><span data-ttu-id="602db-191">JET_bitColumnFinalize 用在非「正在進行」更新資料行的資料行上， (JET_bitColumnEscrowUpdate 未設定) 。</span><span class="sxs-lookup"><span data-stu-id="602db-191">JET_bitColumnFinalize was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="602db-192">JET_bitColumnDeleteOnZero 用在非「正在進行」更新資料行的資料行上， (JET_bitColumnEscrowUpdate 未設定) 。</span><span class="sxs-lookup"><span data-stu-id="602db-192">JET_bitColumnDeleteOnZero was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="602db-193">JET_bitColumnAutoincrement 用於未 <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>的資料行。</span><span class="sxs-lookup"><span data-stu-id="602db-193">JET_bitColumnAutoincrement was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p>
<p><span data-ttu-id="602db-194"><strong>Windows 2000：  </strong>錯誤碼的這個原因只在 Windows 2000 中使用。</span><span class="sxs-lookup"><span data-stu-id="602db-194"><strong>Windows 2000:  </strong>This reason for the error code is used only in Windows 2000.</span></span></p>
<p><span data-ttu-id="602db-195">JET_bitColumnAutoincrement 用於不是 <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>的資料行。</span><span class="sxs-lookup"><span data-stu-id="602db-195">JET_bitColumnAutoincrement was used on a column that was neither <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> nor <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</span></span></p>
<p><span data-ttu-id="602db-196"><strong>WINDOWS XP：  </strong>此錯誤碼的原因是在 Windows XP 和更新版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="602db-196"><strong>Windows XP:  </strong>This reason for the error code is used in Windows XP and later operating systems.</span></span></p></li>
<li><p><span data-ttu-id="602db-197">JET_bitColumnVersion 用於未 <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>的資料行。</span><span class="sxs-lookup"><span data-stu-id="602db-197">JET_bitColumnVersion was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="602db-198">自動遞增資料行使用了 JET_bitColumnVersion。</span><span class="sxs-lookup"><span data-stu-id="602db-198">JET_bitColumnVersion was used on an autoincrement column.</span></span></p></li>
<li><p><span data-ttu-id="602db-199">JET_bitColumnUserDefinedDefault 與 JET_bitColumnFixed 一起使用。</span><span class="sxs-lookup"><span data-stu-id="602db-199">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFixed.</span></span></p></li>
<li><p><span data-ttu-id="602db-200">JET_bitColumnUserDefinedDefault 與 JET_bitColumnNotNull 一起使用。</span><span class="sxs-lookup"><span data-stu-id="602db-200">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnNotNULL.</span></span></p></li>
<li><p><span data-ttu-id="602db-201">JET_bitColumnUserDefinedDefault 與 JET_bitColumnVersion 一起使用。</span><span class="sxs-lookup"><span data-stu-id="602db-201">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnVersion.</span></span></p></li>
<li><p><span data-ttu-id="602db-202">JET_bitColumnUserDefinedDefault 與 JET_bitColumnAutoincrement 一起使用。</span><span class="sxs-lookup"><span data-stu-id="602db-202">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnAutoincrement.</span></span></p></li>
<li><p><span data-ttu-id="602db-203">JET_bitColumnUserDefinedDefault 與 JET_bitColumnUpdatable 一起使用。</span><span class="sxs-lookup"><span data-stu-id="602db-203">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnUpdatable.</span></span></p></li>
<li><p><span data-ttu-id="602db-204">JET_bitColumnUserDefinedDefault 與 JET_bitColumnEscrowUpdate 一起使用。</span><span class="sxs-lookup"><span data-stu-id="602db-204">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnEscrowUpdate.</span></span></p></li>
<li><p><span data-ttu-id="602db-205">JET_bitColumnUserDefinedDefault 與 JET_bitColumnFinalize 一起使用。</span><span class="sxs-lookup"><span data-stu-id="602db-205">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFinalize.</span></span></p></li>
<li><p><span data-ttu-id="602db-206">JET_bitColumnUserDefinedDefault 與 JET_bitColumnDeleteOnZero 一起使用。</span><span class="sxs-lookup"><span data-stu-id="602db-206">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnDeleteOnZero.</span></span></p></li>
<li><p><span data-ttu-id="602db-207">JET_bitColumnUserDefinedDefault 與 JET_bitColumnMaybeNull 一起使用。</span><span class="sxs-lookup"><span data-stu-id="602db-207">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnMaybeNull.</span></span></p></li>
<li><p><span data-ttu-id="602db-208">JET_bitColumnUserDefinedDefault 是用於固定或變數) 的未標記資料行 (。</span><span class="sxs-lookup"><span data-stu-id="602db-208">JET_bitColumnUserDefinedDefault was used on a non-tagged column (that is fixed or variable).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="602db-209">JET_errMultiValuedColumnMustBeTagged</span><span class="sxs-lookup"><span data-stu-id="602db-209">JET_errMultiValuedColumnMustBeTagged</span></span></p></td>
<td><p><span data-ttu-id="602db-210">多值資料行 (JET_bitColumnMultiValued) 只能用在已加上標籤或 Long 值 (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) 資料行中。</span><span class="sxs-lookup"><span data-stu-id="602db-210">A multi-valued column (JET_bitColumnMultiValued) can only be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-211">JET_errCannotBeTagged</span><span class="sxs-lookup"><span data-stu-id="602db-211">JET_errCannotBeTagged</span></span></p></td>
<td><p><span data-ttu-id="602db-212">嘗試在資料行可能未標記時使用標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="602db-212">An attempt was made to use a tagged column when the column might not be tagged.</span></span> <span data-ttu-id="602db-213">禁止標記的資料行的部分條件約束為：</span><span class="sxs-lookup"><span data-stu-id="602db-213">Some of the constraints for disallowing tagged columns are:</span></span></p>
<ul>
<li><p><span data-ttu-id="602db-214"> (JET_bitColumnEscrowUpdate) 的「保管更新資料行」不能用在已標記或長的值 (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) 資料行。</span><span class="sxs-lookup"><span data-stu-id="602db-214">An Escrow Update column (JET_bitColumnEscrowUpdate) cannot be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></li>
<li><p><span data-ttu-id="602db-215">自動遞增資料行可能未標記。</span><span class="sxs-lookup"><span data-stu-id="602db-215">An autoincrement column might not be tagged.</span></span></p></li>
<li><p><span data-ttu-id="602db-216">可能未標記版本資料行。</span><span class="sxs-lookup"><span data-stu-id="602db-216">A Version column might not be tagged.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="602db-217">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="602db-217">JET_errExclusiveTableLockRequired</span></span></p></td>
<td><p><span data-ttu-id="602db-218">此作業需要資料表的獨佔鎖定。</span><span class="sxs-lookup"><span data-stu-id="602db-218">An exclusive lock on the table was required for this operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-219">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="602db-219">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="602db-220">指出固定或變數資料行 (<em>cbMax</em>) 長度上限大於 JET_cbColumnMost 的警告。</span><span class="sxs-lookup"><span data-stu-id="602db-220">A warning indicating that the maximum length (<em>cbMax</em>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="602db-221">這項限制不適用於 <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> 和 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) 的 Long 值 (。</span><span class="sxs-lookup"><span data-stu-id="602db-221">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="602db-222">規格需求</span><span class="sxs-lookup"><span data-stu-id="602db-222">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="602db-223"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="602db-223"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="602db-224">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="602db-224">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-225"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="602db-225"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="602db-226">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="602db-226">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="602db-227"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="602db-227"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="602db-228">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="602db-228">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-229"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="602db-229"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="602db-230">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="602db-230">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="602db-231"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="602db-231"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="602db-232">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="602db-232">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="602db-233"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="602db-233"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="602db-234">實作為 <strong>JetAddColumnW</strong> (Unicode) 和 <strong>JetAddColumnA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="602db-234">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="602db-235">另請參閱</span><span class="sxs-lookup"><span data-stu-id="602db-235">See Also</span></span>

[<span data-ttu-id="602db-236">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="602db-236">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="602db-237">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="602db-237">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="602db-238">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="602db-238">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="602db-239">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="602db-239">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="602db-240">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="602db-240">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="602db-241">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="602db-241">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="602db-242">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="602db-242">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="602db-243">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="602db-243">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="602db-244">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="602db-244">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="602db-245">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="602db-245">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
