---
description: 合併工具會評估 ModuleAdminUISequence 資料表，然後將計算的動作以正確的序號插入 AdminUISequence 資料表中。
ms.assetid: c71477e7-22bc-420a-9902-39bbf98b4ee5
title: ModuleAdminUISequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e128aebd6481c077827f4d1ba2b487eafe6132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979999"
---
# <a name="moduleadminuisequence-table"></a><span data-ttu-id="cb077-103">ModuleAdminUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="cb077-103">ModuleAdminUISequence Table</span></span>

<span data-ttu-id="cb077-104">合併工具會評估 ModuleAdminUISequence 資料表，然後將計算的動作以正確的序號插入 [AdminUISequence 資料表](adminuisequence-table.md) 中。</span><span class="sxs-lookup"><span data-stu-id="cb077-104">A merge tool evaluates the ModuleAdminUISequence table and then inserts the calculated actions into the [AdminUISequence table](adminuisequence-table.md) with a correct sequence number.</span></span>

<span data-ttu-id="cb077-105">ModuleAdminUISequence 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="cb077-105">The ModuleAdminUISequence table has the following columns.</span></span>



| <span data-ttu-id="cb077-106">Column</span><span class="sxs-lookup"><span data-stu-id="cb077-106">Column</span></span>     | <span data-ttu-id="cb077-107">類型</span><span class="sxs-lookup"><span data-stu-id="cb077-107">Type</span></span>                         | <span data-ttu-id="cb077-108">答案</span><span class="sxs-lookup"><span data-stu-id="cb077-108">Key</span></span> | <span data-ttu-id="cb077-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="cb077-109">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="cb077-110">動作</span><span class="sxs-lookup"><span data-stu-id="cb077-110">Action</span></span>     | [<span data-ttu-id="cb077-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="cb077-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="cb077-112">Y</span><span class="sxs-lookup"><span data-stu-id="cb077-112">Y</span></span>   | <span data-ttu-id="cb077-113">N</span><span class="sxs-lookup"><span data-stu-id="cb077-113">N</span></span>        |
| <span data-ttu-id="cb077-114">順序</span><span class="sxs-lookup"><span data-stu-id="cb077-114">Sequence</span></span>   | [<span data-ttu-id="cb077-115">整數</span><span class="sxs-lookup"><span data-stu-id="cb077-115">Integer</span></span>](integer.md)       |     | <span data-ttu-id="cb077-116">Y</span><span class="sxs-lookup"><span data-stu-id="cb077-116">Y</span></span>        |
| <span data-ttu-id="cb077-117">BaseAction</span><span class="sxs-lookup"><span data-stu-id="cb077-117">BaseAction</span></span> | [<span data-ttu-id="cb077-118">識別碼</span><span class="sxs-lookup"><span data-stu-id="cb077-118">Identifier</span></span>](identifier.md) |     | <span data-ttu-id="cb077-119">Y</span><span class="sxs-lookup"><span data-stu-id="cb077-119">Y</span></span>        |
| <span data-ttu-id="cb077-120">After</span><span class="sxs-lookup"><span data-stu-id="cb077-120">After</span></span>      | [<span data-ttu-id="cb077-121">整數</span><span class="sxs-lookup"><span data-stu-id="cb077-121">Integer</span></span>](integer.md)       |     | <span data-ttu-id="cb077-122">Y</span><span class="sxs-lookup"><span data-stu-id="cb077-122">Y</span></span>        |
| <span data-ttu-id="cb077-123">條件</span><span class="sxs-lookup"><span data-stu-id="cb077-123">Condition</span></span>  | [<span data-ttu-id="cb077-124">Condition</span><span class="sxs-lookup"><span data-stu-id="cb077-124">Condition</span></span>](condition.md)   |     | <span data-ttu-id="cb077-125">Y</span><span class="sxs-lookup"><span data-stu-id="cb077-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cb077-126">資料行</span><span class="sxs-lookup"><span data-stu-id="cb077-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cb077-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動</span><span class="sxs-lookup"><span data-stu-id="cb077-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="cb077-128">要插入順序的動作。</span><span class="sxs-lookup"><span data-stu-id="cb077-128">Action to insert into sequence.</span></span> <span data-ttu-id="cb077-129">指的是其中一個安裝程式 [標準動作](standard-actions.md)，或合併模組的 [CustomAction 資料表](customaction-table.md) 或 [對話方塊資料表](dialog-table.md)中的專案。</span><span class="sxs-lookup"><span data-stu-id="cb077-129">Refers to one of the installer [standard actions](standard-actions.md), or an entry in the merge module's [CustomAction table](customaction-table.md) or [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="cb077-130">如果在 merge module sequence 資料表的動作資料行中使用 [標準動作](standard-actions.md) ，則該記錄的 BaseAction 和 After 資料行必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="cb077-130">If a [standard action](standard-actions.md) is used in the Action column of a merge module sequence table, the BaseAction and After columns of that record must be Null.</span></span>

</dd> <dt>

<span data-ttu-id="cb077-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列</span><span class="sxs-lookup"><span data-stu-id="cb077-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="cb077-132">標準動作的序號。</span><span class="sxs-lookup"><span data-stu-id="cb077-132">The sequence number of a standard action.</span></span> <span data-ttu-id="cb077-133">如果在此資料列的 [動作] 資料行中輸入自訂動作或對話，此欄位必須設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="cb077-133">If a custom action or dialog is entered into the Action column of this row, this field must be set to Null.</span></span>

<span data-ttu-id="cb077-134">在合併模組順序資料表中使用 [標準動作](standard-actions.md) 時，[順序] 資料行中的值應該是建議的動作序號。</span><span class="sxs-lookup"><span data-stu-id="cb077-134">When using [standard actions](standard-actions.md) in merge module sequence tables, the value in the Sequence column should be the recommended action sequence number.</span></span> <span data-ttu-id="cb077-135">如果合併模組中的序號與 .msi 檔案順序資料表中相同動作的序號不同，則合併工具會使用 .msi 檔案中的序號。</span><span class="sxs-lookup"><span data-stu-id="cb077-135">If the sequence number in the merge module differs from that for the same action in the .msi file sequence table, the merge tool uses the sequence number from the .msi file.</span></span> <span data-ttu-id="cb077-136">如需標準動作的建議序號，請參閱 [使用順序表](using-a-sequence-table.md) 中的建議序列。</span><span class="sxs-lookup"><span data-stu-id="cb077-136">See the suggested sequences in [Using a Sequence Table](using-a-sequence-table.md) for the recommended sequence numbers of standard actions.</span></span>

</dd> <dt>

<span data-ttu-id="cb077-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span><span class="sxs-lookup"><span data-stu-id="cb077-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span></span>
</dt> <dd>

<span data-ttu-id="cb077-138">BaseAction 資料行可包含標準動作、在合併模組的自訂動作資料表中指定的自訂動作，或在模組的對話方塊資料表中指定的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cb077-138">The BaseAction column can contain a standard action, a custom action specified in the merge module's custom action table, or a dialog specified in the module's dialog table.</span></span> <span data-ttu-id="cb077-139">BaseAction 資料行是此資料表之 [動作] 資料行中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="cb077-139">The BaseAction column is a key into the Action column of this table.</span></span> <span data-ttu-id="cb077-140">它不能是 .msi 檔案中其他合併資料表或資料表的外鍵。</span><span class="sxs-lookup"><span data-stu-id="cb077-140">It cannot be a foreign key into another merge table or table in the .msi file.</span></span> <span data-ttu-id="cb077-141">這表示 BaseAction 資料行中所列的每個標準動作、自訂動作或對話方塊，也必須列在此資料表中另一筆記錄的 [動作] 資料行中。</span><span class="sxs-lookup"><span data-stu-id="cb077-141">This means that every standard action, custom action, or dialog listed in the BaseAction column must also be listed in the Action column of another record in this table.</span></span>

</dd> <dt>

<span data-ttu-id="cb077-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>後</span><span class="sxs-lookup"><span data-stu-id="cb077-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>After</span></span>
</dt> <dd>

<span data-ttu-id="cb077-143">在 BaseAction 之前或之後的動作是否為布林值。</span><span class="sxs-lookup"><span data-stu-id="cb077-143">Boolean for whether Action comes before or after BaseAction.</span></span>



| <span data-ttu-id="cb077-144">值</span><span class="sxs-lookup"><span data-stu-id="cb077-144">Value</span></span> | <span data-ttu-id="cb077-145">意義</span><span class="sxs-lookup"><span data-stu-id="cb077-145">Meaning</span></span>                          |
|-------|----------------------------------|
| <span data-ttu-id="cb077-146">0</span><span class="sxs-lookup"><span data-stu-id="cb077-146">0</span></span>     | <span data-ttu-id="cb077-147">BaseAction 前的動作</span><span class="sxs-lookup"><span data-stu-id="cb077-147">Action to come before BaseAction</span></span> |
| <span data-ttu-id="cb077-148">1</span><span class="sxs-lookup"><span data-stu-id="cb077-148">1</span></span>     | <span data-ttu-id="cb077-149">BaseAction 之後的動作</span><span class="sxs-lookup"><span data-stu-id="cb077-149">Action to come after BaseAction</span></span>  |



 

</dd> <dt>

<span data-ttu-id="cb077-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="cb077-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="cb077-151">指出是否要執行動作的條件陳述式。</span><span class="sxs-lookup"><span data-stu-id="cb077-151">A conditional statement that indicates if the action is be executed.</span></span> <span data-ttu-id="cb077-152">Null 評估為 true。</span><span class="sxs-lookup"><span data-stu-id="cb077-152">Null evaluates to true.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb077-153">備註</span><span class="sxs-lookup"><span data-stu-id="cb077-153">Remarks</span></span>

<dl> <dt>

<span data-ttu-id="cb077-154"><span id="If_this_table_is_present_the__AdminUISequence_Table_must_also_be_present_in_the_merge_module."></span><span id="if_this_table_is_present_the__adminuisequence_table_must_also_be_present_in_the_merge_module."></span><span id="IF_THIS_TABLE_IS_PRESENT_THE__ADMINUISEQUENCE_TABLE_MUST_ALSO_BE_PRESENT_IN_THE_MERGE_MODULE."></span>如果這個資料表存在，則 [AdminUISequence 資料表](adminuisequence-table.md) 也必須存在於合併模組中。</span><span class="sxs-lookup"><span data-stu-id="cb077-154"><span id="If_this_table_is_present_the__AdminUISequence_Table_must_also_be_present_in_the_merge_module."></span><span id="if_this_table_is_present_the__adminuisequence_table_must_also_be_present_in_the_merge_module."></span><span id="IF_THIS_TABLE_IS_PRESENT_THE__ADMINUISEQUENCE_TABLE_MUST_ALSO_BE_PRESENT_IN_THE_MERGE_MODULE."></span>If this table is present the [AdminUISequence Table](adminuisequence-table.md) must also be present in the merge module.</span></span>
<span data-ttu-id="cb077-155"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cb077-155"></dt> <dd></dd> </dl></span></span>

 

 



