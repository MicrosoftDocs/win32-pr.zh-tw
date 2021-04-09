---
description: InstallExecuteSequence 資料表會列出執行最上層安裝動作時所執行的動作。
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: InstallExecuteSequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d110debacab19739c3da69abf3948d11bb7aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847903"
---
# <a name="installexecutesequence-table"></a><span data-ttu-id="907de-103">InstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="907de-103">InstallExecuteSequence Table</span></span>

<span data-ttu-id="907de-104">InstallExecuteSequence 資料表會列出執行最上層 [安裝動作](install-action.md) 時所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="907de-104">The InstallExecuteSequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed.</span></span>

<span data-ttu-id="907de-105">安裝順序中的動作，直到 [InstallValidate 動作](installvalidate-action.md)和任何結束對話方塊都位於 [InstallUISequence 資料表](installuisequence-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="907de-105">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="907de-106">從 InstallValidate 到安裝順序結束的所有動作都會在 InstallExecuteSequence 資料表中。</span><span class="sxs-lookup"><span data-stu-id="907de-106">All actions from the InstallValidate through the end of the install sequence are in the InstallExecuteSequence table.</span></span> <span data-ttu-id="907de-107">由於 InstallExecuteSequence 資料表需要獨立，因此它具有任何必要的初始化動作，例如 [LaunchConditions](launchconditions-action.md)、 [CostInitialize](costinitialize-action.md)、 [FileCost](filecost-action.md)和 [CostFinalize](costfinalize-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="907de-107">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="907de-108">需要使用者介面的 [自訂動作](custom-actions.md)應使用 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) ，而不是使用 [對話方塊資料表](dialog-table.md)所建立的編寫對話方塊。</span><span class="sxs-lookup"><span data-stu-id="907de-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="907de-109">InstallExecuteSequence 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="907de-109">The InstallExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="907de-110">Column</span><span class="sxs-lookup"><span data-stu-id="907de-110">Column</span></span>    | <span data-ttu-id="907de-111">類型</span><span class="sxs-lookup"><span data-stu-id="907de-111">Type</span></span>                         | <span data-ttu-id="907de-112">答案</span><span class="sxs-lookup"><span data-stu-id="907de-112">Key</span></span> | <span data-ttu-id="907de-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="907de-113">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="907de-114">動作</span><span class="sxs-lookup"><span data-stu-id="907de-114">Action</span></span>    | [<span data-ttu-id="907de-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="907de-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="907de-116">Y</span><span class="sxs-lookup"><span data-stu-id="907de-116">Y</span></span>   | <span data-ttu-id="907de-117">N</span><span class="sxs-lookup"><span data-stu-id="907de-117">N</span></span>        |
| <span data-ttu-id="907de-118">條件</span><span class="sxs-lookup"><span data-stu-id="907de-118">Condition</span></span> | [<span data-ttu-id="907de-119">Condition</span><span class="sxs-lookup"><span data-stu-id="907de-119">Condition</span></span>](condition.md)   | <span data-ttu-id="907de-120">N</span><span class="sxs-lookup"><span data-stu-id="907de-120">N</span></span>   | <span data-ttu-id="907de-121">Y</span><span class="sxs-lookup"><span data-stu-id="907de-121">Y</span></span>        |
| <span data-ttu-id="907de-122">順序</span><span class="sxs-lookup"><span data-stu-id="907de-122">Sequence</span></span>  | [<span data-ttu-id="907de-123">整數</span><span class="sxs-lookup"><span data-stu-id="907de-123">Integer</span></span>](integer.md)       | <span data-ttu-id="907de-124">N</span><span class="sxs-lookup"><span data-stu-id="907de-124">N</span></span>   | <span data-ttu-id="907de-125">Y</span><span class="sxs-lookup"><span data-stu-id="907de-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="907de-126">資料行</span><span class="sxs-lookup"><span data-stu-id="907de-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="907de-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動</span><span class="sxs-lookup"><span data-stu-id="907de-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="907de-128">要執行之動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="907de-128">Name of the action to execute.</span></span> <span data-ttu-id="907de-129">這可能是內建動作或自訂動作。</span><span class="sxs-lookup"><span data-stu-id="907de-129">This is either a built-in action or a custom action.</span></span>

<span data-ttu-id="907de-130">主表索引鍵。</span><span class="sxs-lookup"><span data-stu-id="907de-130">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="907de-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="907de-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="907de-132">此欄位包含條件運算式。</span><span class="sxs-lookup"><span data-stu-id="907de-132">This field contains a conditional expression.</span></span> <span data-ttu-id="907de-133">如果運算式評估為 False，則會略過該動作。</span><span class="sxs-lookup"><span data-stu-id="907de-133">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="907de-134">如果運算式語法無效，則序列會終止，並傳回 iesBadActionData。</span><span class="sxs-lookup"><span data-stu-id="907de-134">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="907de-135">如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="907de-135">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="907de-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列</span><span class="sxs-lookup"><span data-stu-id="907de-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="907de-137">決定執行此動作之順序位置的數位。</span><span class="sxs-lookup"><span data-stu-id="907de-137">Number that determines the sequence position in which this action is to be executed.</span></span>

<span data-ttu-id="907de-138">正值表示序列位置。</span><span class="sxs-lookup"><span data-stu-id="907de-138">A positive value represents the sequence position.</span></span> <span data-ttu-id="907de-139">Null 值表示不執行動作。</span><span class="sxs-lookup"><span data-stu-id="907de-139">A Null value indicates that the action is not executed.</span></span> <span data-ttu-id="907de-140">下列負數值表示如果安裝程式傳回相關聯的終止旗標，則會執行此動作。</span><span class="sxs-lookup"><span data-stu-id="907de-140">The following negative values indicate that this action is to be executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="907de-141">每個終止旗標 (負數值) 可用於不超過一個動作。</span><span class="sxs-lookup"><span data-stu-id="907de-141">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="907de-142">多個動作可以有終止旗標，但它們必須是不同的旗標。</span><span class="sxs-lookup"><span data-stu-id="907de-142">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="907de-143">終止旗標 (負數值) 通常會與 [對話方塊](dialog-boxes.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="907de-143">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="907de-144">終止旗標</span><span class="sxs-lookup"><span data-stu-id="907de-144">Termination flag</span></span>          | <span data-ttu-id="907de-145">值</span><span class="sxs-lookup"><span data-stu-id="907de-145">Value</span></span> | <span data-ttu-id="907de-146">描述</span><span class="sxs-lookup"><span data-stu-id="907de-146">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="907de-147">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="907de-147">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="907de-148">-1</span><span class="sxs-lookup"><span data-stu-id="907de-148">-1</span></span>    | <span data-ttu-id="907de-149">順利完成。</span><span class="sxs-lookup"><span data-stu-id="907de-149">Successful completion.</span></span> <span data-ttu-id="907de-150">與 [結束] [對話方塊一起使用](exit-dialog.md) 。</span><span class="sxs-lookup"><span data-stu-id="907de-150">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="907de-151">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="907de-151">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="907de-152">-2</span><span class="sxs-lookup"><span data-stu-id="907de-152">-2</span></span>    | <span data-ttu-id="907de-153">使用者終止安裝。</span><span class="sxs-lookup"><span data-stu-id="907de-153">User terminates install.</span></span> <span data-ttu-id="907de-154">搭配 [UserExit](userexit-dialog.md) 對話方塊使用。</span><span class="sxs-lookup"><span data-stu-id="907de-154">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="907de-155">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="907de-155">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="907de-156">-3</span><span class="sxs-lookup"><span data-stu-id="907de-156">-3</span></span>    | <span data-ttu-id="907de-157">嚴重結束終止。</span><span class="sxs-lookup"><span data-stu-id="907de-157">Fatal exit terminates.</span></span> <span data-ttu-id="907de-158">搭配 [FatalError](fatalerror-dialog.md) 對話方塊使用。</span><span class="sxs-lookup"><span data-stu-id="907de-158">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="907de-159">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="907de-159">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="907de-160">-4</span><span class="sxs-lookup"><span data-stu-id="907de-160">-4</span></span>    | <span data-ttu-id="907de-161">安裝已暫停。</span><span class="sxs-lookup"><span data-stu-id="907de-161">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="907de-162">零、所有其他負數或 Null 值表示永遠不會執行動作。</span><span class="sxs-lookup"><span data-stu-id="907de-162">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="907de-163">備註</span><span class="sxs-lookup"><span data-stu-id="907de-163">Remarks</span></span>

<span data-ttu-id="907de-164">進度顯示或記錄的當地語系化文字是在 [ActionText 資料表](actiontext-table.md)中指定的。</span><span class="sxs-lookup"><span data-stu-id="907de-164">Localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="907de-165">如需順序資料表的範例，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="907de-165">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="907de-166">驗證</span><span class="sxs-lookup"><span data-stu-id="907de-166">Validation</span></span>

<dl>

[<span data-ttu-id="907de-167">ICE03</span><span class="sxs-lookup"><span data-stu-id="907de-167">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="907de-168">ICE06</span><span class="sxs-lookup"><span data-stu-id="907de-168">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="907de-169">ICE12</span><span class="sxs-lookup"><span data-stu-id="907de-169">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="907de-170">ICE13</span><span class="sxs-lookup"><span data-stu-id="907de-170">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="907de-171">ICE26</span><span class="sxs-lookup"><span data-stu-id="907de-171">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="907de-172">ICE27</span><span class="sxs-lookup"><span data-stu-id="907de-172">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="907de-173">ICE28</span><span class="sxs-lookup"><span data-stu-id="907de-173">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="907de-174">ICE46</span><span class="sxs-lookup"><span data-stu-id="907de-174">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="907de-175">ICE63</span><span class="sxs-lookup"><span data-stu-id="907de-175">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="907de-176">ICE75</span><span class="sxs-lookup"><span data-stu-id="907de-176">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="907de-177">ICE77</span><span class="sxs-lookup"><span data-stu-id="907de-177">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="907de-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="907de-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="907de-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="907de-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="907de-180">ICE83</span><span class="sxs-lookup"><span data-stu-id="907de-180">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="907de-181">ICE84</span><span class="sxs-lookup"><span data-stu-id="907de-181">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="907de-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="907de-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



