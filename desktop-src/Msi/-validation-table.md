---
description: '\_驗證資料表是包含資料庫中所有資料表之資料行名稱和資料行值的系統資料表。'
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: _Validation 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666f00ccccda11706dce6a8d7e04e0efea91b7cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849003"
---
# <a name="_validation-table"></a><span data-ttu-id="6d558-103">\_驗證資料表</span><span class="sxs-lookup"><span data-stu-id="6d558-103">\_Validation Table</span></span>

<span data-ttu-id="6d558-104">\_驗證資料表是包含資料庫中所有資料表之資料行名稱和資料行值的系統資料表。</span><span class="sxs-lookup"><span data-stu-id="6d558-104">The \_Validation table is a system table that contains the column names and the column values for all of the tables in the database.</span></span> <span data-ttu-id="6d558-105">在資料庫驗證過程中，會使用它來確保所有資料行都已列入考慮，而且具有正確的值。</span><span class="sxs-lookup"><span data-stu-id="6d558-105">It is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="6d558-106">此資料表並未隨附于安裝程式資料庫。</span><span class="sxs-lookup"><span data-stu-id="6d558-106">This table is not shipped with the installer database.</span></span>

<span data-ttu-id="6d558-107">\_驗證資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="6d558-107">The \_Validation table has the following columns.</span></span>



| <span data-ttu-id="6d558-108">Column</span><span class="sxs-lookup"><span data-stu-id="6d558-108">Column</span></span>      | <span data-ttu-id="6d558-109">類型</span><span class="sxs-lookup"><span data-stu-id="6d558-109">Type</span></span>                               | <span data-ttu-id="6d558-110">答案</span><span class="sxs-lookup"><span data-stu-id="6d558-110">Key</span></span> | <span data-ttu-id="6d558-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="6d558-111">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="6d558-112">資料表</span><span class="sxs-lookup"><span data-stu-id="6d558-112">Table</span></span>       | [<span data-ttu-id="6d558-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="6d558-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="6d558-114">Y</span><span class="sxs-lookup"><span data-stu-id="6d558-114">Y</span></span>   | <span data-ttu-id="6d558-115">N</span><span class="sxs-lookup"><span data-stu-id="6d558-115">N</span></span>        |
| <span data-ttu-id="6d558-116">Column</span><span class="sxs-lookup"><span data-stu-id="6d558-116">Column</span></span>      | [<span data-ttu-id="6d558-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="6d558-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="6d558-118">Y</span><span class="sxs-lookup"><span data-stu-id="6d558-118">Y</span></span>   | <span data-ttu-id="6d558-119">N</span><span class="sxs-lookup"><span data-stu-id="6d558-119">N</span></span>        |
| <span data-ttu-id="6d558-120">Nullable</span><span class="sxs-lookup"><span data-stu-id="6d558-120">Nullable</span></span>    | [<span data-ttu-id="6d558-121">Text</span><span class="sxs-lookup"><span data-stu-id="6d558-121">Text</span></span>](text.md)                   | <span data-ttu-id="6d558-122">N</span><span class="sxs-lookup"><span data-stu-id="6d558-122">N</span></span>   | <span data-ttu-id="6d558-123">N</span><span class="sxs-lookup"><span data-stu-id="6d558-123">N</span></span>        |
| <span data-ttu-id="6d558-124">MinValue</span><span class="sxs-lookup"><span data-stu-id="6d558-124">MinValue</span></span>    | [<span data-ttu-id="6d558-125">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="6d558-125">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="6d558-126">N</span><span class="sxs-lookup"><span data-stu-id="6d558-126">N</span></span>   | <span data-ttu-id="6d558-127">Y</span><span class="sxs-lookup"><span data-stu-id="6d558-127">Y</span></span>        |
| <span data-ttu-id="6d558-128">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6d558-128">MaxValue</span></span>    | [<span data-ttu-id="6d558-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="6d558-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="6d558-130">N</span><span class="sxs-lookup"><span data-stu-id="6d558-130">N</span></span>   | <span data-ttu-id="6d558-131">Y</span><span class="sxs-lookup"><span data-stu-id="6d558-131">Y</span></span>        |
| <span data-ttu-id="6d558-132">KeyTable</span><span class="sxs-lookup"><span data-stu-id="6d558-132">KeyTable</span></span>    | [<span data-ttu-id="6d558-133">識別碼</span><span class="sxs-lookup"><span data-stu-id="6d558-133">Identifier</span></span>](identifier.md)       | <span data-ttu-id="6d558-134">N</span><span class="sxs-lookup"><span data-stu-id="6d558-134">N</span></span>   | <span data-ttu-id="6d558-135">Y</span><span class="sxs-lookup"><span data-stu-id="6d558-135">Y</span></span>        |
| <span data-ttu-id="6d558-136">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="6d558-136">KeyColumn</span></span>   | [<span data-ttu-id="6d558-137">整數</span><span class="sxs-lookup"><span data-stu-id="6d558-137">Integer</span></span>](integer.md)             | <span data-ttu-id="6d558-138">N</span><span class="sxs-lookup"><span data-stu-id="6d558-138">N</span></span>   | <span data-ttu-id="6d558-139">Y</span><span class="sxs-lookup"><span data-stu-id="6d558-139">Y</span></span>        |
| <span data-ttu-id="6d558-140">類別</span><span class="sxs-lookup"><span data-stu-id="6d558-140">Category</span></span>    | [<span data-ttu-id="6d558-141">Text</span><span class="sxs-lookup"><span data-stu-id="6d558-141">Text</span></span>](text.md)                   | <span data-ttu-id="6d558-142">N</span><span class="sxs-lookup"><span data-stu-id="6d558-142">N</span></span>   | <span data-ttu-id="6d558-143">Y</span><span class="sxs-lookup"><span data-stu-id="6d558-143">Y</span></span>        |
| <span data-ttu-id="6d558-144">設定</span><span class="sxs-lookup"><span data-stu-id="6d558-144">Set</span></span>         | [<span data-ttu-id="6d558-145">Text</span><span class="sxs-lookup"><span data-stu-id="6d558-145">Text</span></span>](text.md)                   | <span data-ttu-id="6d558-146">N</span><span class="sxs-lookup"><span data-stu-id="6d558-146">N</span></span>   | <span data-ttu-id="6d558-147">Y</span><span class="sxs-lookup"><span data-stu-id="6d558-147">Y</span></span>        |
| <span data-ttu-id="6d558-148">Description</span><span class="sxs-lookup"><span data-stu-id="6d558-148">Description</span></span> | [<span data-ttu-id="6d558-149">Text</span><span class="sxs-lookup"><span data-stu-id="6d558-149">Text</span></span>](text.md)                   | <span data-ttu-id="6d558-150">N</span><span class="sxs-lookup"><span data-stu-id="6d558-150">N</span></span>   | <span data-ttu-id="6d558-151">Y</span><span class="sxs-lookup"><span data-stu-id="6d558-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6d558-152">資料行</span><span class="sxs-lookup"><span data-stu-id="6d558-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6d558-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>表</span><span class="sxs-lookup"><span data-stu-id="6d558-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="6d558-154">用來識別特定的資料表。</span><span class="sxs-lookup"><span data-stu-id="6d558-154">Used to identify a particular table.</span></span> <span data-ttu-id="6d558-155">此索引鍵和資料行索引鍵會形成驗證資料表的主要索引鍵 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6d558-155">This key and the Column key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="6d558-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>列</span><span class="sxs-lookup"><span data-stu-id="6d558-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="6d558-157">用來識別資料表的特定資料行。</span><span class="sxs-lookup"><span data-stu-id="6d558-157">Used to identify a particular column of the table.</span></span> <span data-ttu-id="6d558-158">此索引鍵和資料表索引鍵會形成驗證資料表的主要索引鍵 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6d558-158">This key and the Table key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="6d558-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>空</span><span class="sxs-lookup"><span data-stu-id="6d558-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable</span></span>
</dt> <dd>

<span data-ttu-id="6d558-160">識別資料行是否可包含 Null 值。</span><span class="sxs-lookup"><span data-stu-id="6d558-160">Identifies whether the column may contain a Null value.</span></span>

<span data-ttu-id="6d558-161">此資料行可能會有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6d558-161">This column may have one of the following values.</span></span>



| <span data-ttu-id="6d558-162">String</span><span class="sxs-lookup"><span data-stu-id="6d558-162">String</span></span> | <span data-ttu-id="6d558-163">意義</span><span class="sxs-lookup"><span data-stu-id="6d558-163">Meaning</span></span>                                   |
|--------|-------------------------------------------|
| <span data-ttu-id="6d558-164">Y</span><span class="sxs-lookup"><span data-stu-id="6d558-164">Y</span></span>      | <span data-ttu-id="6d558-165">是，資料行可能會有 Null 值。</span><span class="sxs-lookup"><span data-stu-id="6d558-165">Yes, the column may have a Null value.</span></span>    |
| <span data-ttu-id="6d558-166">N</span><span class="sxs-lookup"><span data-stu-id="6d558-166">N</span></span>      | <span data-ttu-id="6d558-167">否，資料行的值不能是 Null。</span><span class="sxs-lookup"><span data-stu-id="6d558-167">No, the column may not have a Null value.</span></span> |



 

</dd> <dt>

<span data-ttu-id="6d558-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span><span class="sxs-lookup"><span data-stu-id="6d558-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span></span>
</dt> <dd>

<span data-ttu-id="6d558-169">此欄位適用于具有數值的資料行。</span><span class="sxs-lookup"><span data-stu-id="6d558-169">This field applies to columns having numeric value.</span></span> <span data-ttu-id="6d558-170">欄位包含允許的最小值。</span><span class="sxs-lookup"><span data-stu-id="6d558-170">The field contains the minimum permissible value.</span></span> <span data-ttu-id="6d558-171">這可以是整數的最小值或日期或版本字串的最小值。</span><span class="sxs-lookup"><span data-stu-id="6d558-171">This can be the minimum value for an integer or the minimum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="6d558-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>Timespan.maxvalue</span><span class="sxs-lookup"><span data-stu-id="6d558-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span></span>
</dt> <dd>

<span data-ttu-id="6d558-173">此欄位適用于具有數值的資料行。</span><span class="sxs-lookup"><span data-stu-id="6d558-173">This field applies to columns having numeric value.</span></span> <span data-ttu-id="6d558-174">欄位是允許的最大值。</span><span class="sxs-lookup"><span data-stu-id="6d558-174">The field is the maximum permissible value.</span></span> <span data-ttu-id="6d558-175">這可能是整數的最大值或日期或版本字串的最大值。</span><span class="sxs-lookup"><span data-stu-id="6d558-175">This may be the maximum value for an integer or the maximum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="6d558-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable</span><span class="sxs-lookup"><span data-stu-id="6d558-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable</span></span>
</dt> <dd>

<span data-ttu-id="6d558-177">此欄位會套用至屬於外部索引鍵的資料行。</span><span class="sxs-lookup"><span data-stu-id="6d558-177">This field applies to columns that are external keys.</span></span> <span data-ttu-id="6d558-178">在資料行中識別的欄位必須連結至在 KeyTable 中名為的資料表中，KeyColumn 所指定的資料行編號。</span><span class="sxs-lookup"><span data-stu-id="6d558-178">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="6d558-179">這可以是以分號分隔的資料表清單。</span><span class="sxs-lookup"><span data-stu-id="6d558-179">This can be a list of tables separated by semicolons.</span></span>

</dd> <dt>

<span data-ttu-id="6d558-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span><span class="sxs-lookup"><span data-stu-id="6d558-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span></span>
</dt> <dd>

<span data-ttu-id="6d558-181">此欄位適用于外部索引鍵的資料表資料行。</span><span class="sxs-lookup"><span data-stu-id="6d558-181">This field applies to table columns that are external keys.</span></span> <span data-ttu-id="6d558-182">在資料行中識別的欄位必須連結至在 KeyTable 中名為的資料表中，KeyColumn 所指定的資料行編號。</span><span class="sxs-lookup"><span data-stu-id="6d558-182">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="6d558-183">KeyColumn 欄位允許的範圍是1-32。</span><span class="sxs-lookup"><span data-stu-id="6d558-183">The permissible range of the KeyColumn field is 1-32.</span></span>

</dd> <dt>

<span data-ttu-id="6d558-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>類別</span><span class="sxs-lookup"><span data-stu-id="6d558-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="6d558-185">這是由驗證資料表之資料表和資料行資料行所指定的資料庫欄位所包含的資料類型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6d558-185">This is the type of data contained by the database field specified by the Table and Column columns of the \_Validation table.</span></span> <span data-ttu-id="6d558-186">如果這是具有數值的類型（例如 [整數](integer.md)、 [DoubleInteger](doubleinteger.md) 或 [時間/日期](time-date.md)），請在此欄位中輸入 null，然後使用 MinValue 和 int32.maxvalue 資料行來指定值的範圍。</span><span class="sxs-lookup"><span data-stu-id="6d558-186">If this is a type having a numeric value, such as [Integer](integer.md), [DoubleInteger](doubleinteger.md) or [Time/Date](time-date.md), then enter null into this field and specify the value's range using the MinValue and MaxValue columns.</span></span> <span data-ttu-id="6d558-187">您可以使用 [類別] 資料行來指定資料 [行資料類型](column-data-types.md)中所描述的非數值資料類型。</span><span class="sxs-lookup"><span data-stu-id="6d558-187">Use the Category column to specify the non-numeric data types described in [Column Data Types](column-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d558-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>設置</span><span class="sxs-lookup"><span data-stu-id="6d558-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Set</span></span>
</dt> <dd>

<span data-ttu-id="6d558-189">這是此欄位允許的值清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="6d558-189">This is a list of permissible values for this field separated by semicolons.</span></span> <span data-ttu-id="6d558-190">此欄位通常用於列舉。</span><span class="sxs-lookup"><span data-stu-id="6d558-190">This field is usually used for enumerations.</span></span>

</dd> <dt>

<span data-ttu-id="6d558-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="6d558-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="6d558-192">儲存在資料行中之資料的描述。</span><span class="sxs-lookup"><span data-stu-id="6d558-192">A description of the data that is stored in the column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="6d558-193">驗證</span><span class="sxs-lookup"><span data-stu-id="6d558-193">Validation</span></span>

<dl>

[<span data-ttu-id="6d558-194">ICE03</span><span class="sxs-lookup"><span data-stu-id="6d558-194">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6d558-195">ICE06</span><span class="sxs-lookup"><span data-stu-id="6d558-195">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6d558-196">ICE32</span><span class="sxs-lookup"><span data-stu-id="6d558-196">ICE32</span></span>](ice32.md)  
</dl>

## <a name="remarks"></a><span data-ttu-id="6d558-197">備註</span><span class="sxs-lookup"><span data-stu-id="6d558-197">Remarks</span></span>

<span data-ttu-id="6d558-198">此資料表的 [類別目錄] 欄位僅適用于字串資料。</span><span class="sxs-lookup"><span data-stu-id="6d558-198">The Category field of this table only applies to string data.</span></span> <span data-ttu-id="6d558-199">如果資料列欄位參考了具有二進位資料的資料行，則必須在 [類別目錄] 欄位中指定二進位資料類型。</span><span class="sxs-lookup"><span data-stu-id="6d558-199">If the Column field refers to a column with binary data, the binary data type must be specified in the Category field.</span></span> <span data-ttu-id="6d558-200">整數資料行類型在驗證期間會忽略類別目錄欄位。</span><span class="sxs-lookup"><span data-stu-id="6d558-200">Integer data Column types ignore the Category field during validation.</span></span>

 

 



