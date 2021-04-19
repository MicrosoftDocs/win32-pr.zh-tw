---
description: InstallUISequence 資料表會列出執行最上層安裝動作時所執行的動作，以及將內部使用者介面層級設定為完整 UI 或縮減 UI 的動作。
ms.assetid: 076d7c14-e302-4465-aed5-27a4b1f70ac8
title: InstallUISequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a4d8d3033645ac1f414e3aff67be2a26d7a6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998157"
---
# <a name="installuisequence-table"></a><span data-ttu-id="e8907-103">InstallUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="e8907-103">InstallUISequence Table</span></span>

<span data-ttu-id="e8907-104">InstallUISequence 資料表會列出執行最上層 [安裝動作](install-action.md) 時所執行的動作，以及將內部使用者介面層級設定為完整 ui 或縮減 ui 的動作。</span><span class="sxs-lookup"><span data-stu-id="e8907-104">The InstallUISequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="e8907-105">如果使用者介面層級設定為基本 UI 或沒有 UI，則安裝程式會略過此資料表中的動作。</span><span class="sxs-lookup"><span data-stu-id="e8907-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="e8907-106">[關於消費者介面的詳細資訊，](about-the-user-interface.md)請參閱。</span><span class="sxs-lookup"><span data-stu-id="e8907-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="e8907-107">安裝順序中的動作（直到 [InstallValidate 動作](installvalidate-action.md)）和結束對話方塊都位於 InstallUISequence 資料表中。</span><span class="sxs-lookup"><span data-stu-id="e8907-107">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and the exit dialog boxes, are located in the InstallUISequence table.</span></span> <span data-ttu-id="e8907-108">從 InstallValidate 到安裝順序結束的所有動作都會在 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="e8907-108">All actions from the InstallValidate through the end of the install sequence are in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="e8907-109">由於 InstallExecuteSequence 資料表需要獨立，因此它具有任何必要的初始化動作，例如[LaunchConditions](launchconditions-action.md)、 [CostInitialize](costinitialize-action.md)、 [FileCost](filecost-action.md)和 CostFinalize，以及[ExecuteAction 動作](executeaction-action.md)。 [](costfinalize-action.md)</span><span class="sxs-lookup"><span data-stu-id="e8907-109">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and the [CostFinalize](costfinalize-action.md), and [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="e8907-110">InstallUISequence 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="e8907-110">The InstallUISequence table has the following columns.</span></span>



| <span data-ttu-id="e8907-111">Column</span><span class="sxs-lookup"><span data-stu-id="e8907-111">Column</span></span>    | <span data-ttu-id="e8907-112">類型</span><span class="sxs-lookup"><span data-stu-id="e8907-112">Type</span></span>                         | <span data-ttu-id="e8907-113">答案</span><span class="sxs-lookup"><span data-stu-id="e8907-113">Key</span></span> | <span data-ttu-id="e8907-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="e8907-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="e8907-115">動作</span><span class="sxs-lookup"><span data-stu-id="e8907-115">Action</span></span>    | [<span data-ttu-id="e8907-116">識別碼</span><span class="sxs-lookup"><span data-stu-id="e8907-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="e8907-117">Y</span><span class="sxs-lookup"><span data-stu-id="e8907-117">Y</span></span>   | <span data-ttu-id="e8907-118">N</span><span class="sxs-lookup"><span data-stu-id="e8907-118">N</span></span>        |
| <span data-ttu-id="e8907-119">條件</span><span class="sxs-lookup"><span data-stu-id="e8907-119">Condition</span></span> | [<span data-ttu-id="e8907-120">Condition</span><span class="sxs-lookup"><span data-stu-id="e8907-120">Condition</span></span>](condition.md)   | <span data-ttu-id="e8907-121">N</span><span class="sxs-lookup"><span data-stu-id="e8907-121">N</span></span>   | <span data-ttu-id="e8907-122">Y</span><span class="sxs-lookup"><span data-stu-id="e8907-122">Y</span></span>        |
| <span data-ttu-id="e8907-123">順序</span><span class="sxs-lookup"><span data-stu-id="e8907-123">Sequence</span></span>  | [<span data-ttu-id="e8907-124">整數</span><span class="sxs-lookup"><span data-stu-id="e8907-124">Integer</span></span>](integer.md)       | <span data-ttu-id="e8907-125">N</span><span class="sxs-lookup"><span data-stu-id="e8907-125">N</span></span>   | <span data-ttu-id="e8907-126">Y</span><span class="sxs-lookup"><span data-stu-id="e8907-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e8907-127">資料行</span><span class="sxs-lookup"><span data-stu-id="e8907-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e8907-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動</span><span class="sxs-lookup"><span data-stu-id="e8907-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="e8907-129">要執行之動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8907-129">Name of the action to execute.</span></span> <span data-ttu-id="e8907-130">這可能是內建動作、自訂動作或使用者介面 wizard。</span><span class="sxs-lookup"><span data-stu-id="e8907-130">This is either a built-in action, a custom action, or a user interface wizard.</span></span>

<span data-ttu-id="e8907-131">主表索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e8907-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="e8907-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="e8907-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="e8907-133">此欄位包含條件運算式。</span><span class="sxs-lookup"><span data-stu-id="e8907-133">This field contains a conditional expression.</span></span> <span data-ttu-id="e8907-134">如果運算式評估為 False，則會略過該動作。</span><span class="sxs-lookup"><span data-stu-id="e8907-134">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="e8907-135">如果運算式語法無效，則序列會終止，並傳回 iesBadActionData。</span><span class="sxs-lookup"><span data-stu-id="e8907-135">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="e8907-136">如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="e8907-136">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8907-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列</span><span class="sxs-lookup"><span data-stu-id="e8907-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="e8907-138">此資料行中的數位決定執行此動作的順序位置。</span><span class="sxs-lookup"><span data-stu-id="e8907-138">The number in this column determines the sequence position in which this action is run.</span></span>

<span data-ttu-id="e8907-139">正值表示序列位置。</span><span class="sxs-lookup"><span data-stu-id="e8907-139">A positive value represents the sequence position.</span></span> <span data-ttu-id="e8907-140">Null 值表示永遠不會執行動作。</span><span class="sxs-lookup"><span data-stu-id="e8907-140">A Null value indicates that the action is never run.</span></span> <span data-ttu-id="e8907-141">下列負數值表示如果安裝程式傳回相關聯的終止旗標，則會執行此動作。</span><span class="sxs-lookup"><span data-stu-id="e8907-141">The following negative values indicate that this action is executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="e8907-142">每個終止旗標 (負數值) 可用於不超過一個動作。</span><span class="sxs-lookup"><span data-stu-id="e8907-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="e8907-143">多個動作可以有終止旗標，但它們必須是不同的旗標。</span><span class="sxs-lookup"><span data-stu-id="e8907-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="e8907-144">終止旗標 (負數值) 通常會與 [對話方塊](dialog-boxes.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="e8907-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="e8907-145">終止旗標</span><span class="sxs-lookup"><span data-stu-id="e8907-145">Termination flag</span></span>          | <span data-ttu-id="e8907-146">值</span><span class="sxs-lookup"><span data-stu-id="e8907-146">Value</span></span> | <span data-ttu-id="e8907-147">描述</span><span class="sxs-lookup"><span data-stu-id="e8907-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8907-148">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="e8907-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="e8907-149">-1</span><span class="sxs-lookup"><span data-stu-id="e8907-149">-1</span></span>    | <span data-ttu-id="e8907-150">順利完成。</span><span class="sxs-lookup"><span data-stu-id="e8907-150">Successful completion.</span></span> <span data-ttu-id="e8907-151">與 [結束] [對話方塊一起使用](exit-dialog.md) 。</span><span class="sxs-lookup"><span data-stu-id="e8907-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="e8907-152">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="e8907-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="e8907-153">-2</span><span class="sxs-lookup"><span data-stu-id="e8907-153">-2</span></span>    | <span data-ttu-id="e8907-154">使用者終止安裝。</span><span class="sxs-lookup"><span data-stu-id="e8907-154">User terminates install.</span></span> <span data-ttu-id="e8907-155">搭配 [UserExit](userexit-dialog.md) 對話方塊使用。</span><span class="sxs-lookup"><span data-stu-id="e8907-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="e8907-156">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="e8907-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="e8907-157">-3</span><span class="sxs-lookup"><span data-stu-id="e8907-157">-3</span></span>    | <span data-ttu-id="e8907-158">嚴重結束終止。</span><span class="sxs-lookup"><span data-stu-id="e8907-158">Fatal exit terminates.</span></span> <span data-ttu-id="e8907-159">搭配 [FatalError](fatalerror-dialog.md) 對話方塊使用。</span><span class="sxs-lookup"><span data-stu-id="e8907-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="e8907-160">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="e8907-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="e8907-161">-4</span><span class="sxs-lookup"><span data-stu-id="e8907-161">-4</span></span>    | <span data-ttu-id="e8907-162">安裝已暫停。</span><span class="sxs-lookup"><span data-stu-id="e8907-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="e8907-163">零、所有其他負數或 Null 值表示永遠不會執行動作。</span><span class="sxs-lookup"><span data-stu-id="e8907-163">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8907-164">備註</span><span class="sxs-lookup"><span data-stu-id="e8907-164">Remarks</span></span>

<span data-ttu-id="e8907-165">進度顯示或記錄的相關當地語系化文字會在 [ActionText 資料表](actiontext-table.md)中指定。</span><span class="sxs-lookup"><span data-stu-id="e8907-165">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="e8907-166">如需順序資料表的範例，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="e8907-166">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="e8907-167">驗證</span><span class="sxs-lookup"><span data-stu-id="e8907-167">Validation</span></span>

<dl>

[<span data-ttu-id="e8907-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="e8907-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e8907-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="e8907-169">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e8907-170">ICE12</span><span class="sxs-lookup"><span data-stu-id="e8907-170">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="e8907-171">ICE13</span><span class="sxs-lookup"><span data-stu-id="e8907-171">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="e8907-172">ICE20</span><span class="sxs-lookup"><span data-stu-id="e8907-172">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="e8907-173">ICE26</span><span class="sxs-lookup"><span data-stu-id="e8907-173">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="e8907-174">ICE27</span><span class="sxs-lookup"><span data-stu-id="e8907-174">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="e8907-175">ICE28</span><span class="sxs-lookup"><span data-stu-id="e8907-175">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="e8907-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="e8907-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="e8907-177">ICE75</span><span class="sxs-lookup"><span data-stu-id="e8907-177">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="e8907-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="e8907-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="e8907-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="e8907-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="e8907-180">ICE86</span><span class="sxs-lookup"><span data-stu-id="e8907-180">ICE86</span></span>](ice86.md)  
</dl>

 

 



