---
description: AdminUISequence 資料表會列出當執行最上層系統管理員動作，而內部使用者介面層級設定為完整 UI 或縮減 UI 時，安裝程式會依序呼叫的動作。
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: AdminUISequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8fb460f65d223e75ebd50a7587f5b3f4adeced8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977044"
---
# <a name="adminuisequence-table"></a><span data-ttu-id="1df21-103">AdminUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="1df21-103">AdminUISequence Table</span></span>

<span data-ttu-id="1df21-104">AdminUISequence 資料表會列出當執行最上層系統 [管理員動作](admin-action.md) ，而內部使用者介面層級設定為完整 ui 或縮減 ui 時，安裝程式會依序呼叫的動作。</span><span class="sxs-lookup"><span data-stu-id="1df21-104">The AdminUISequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="1df21-105">如果使用者介面層級設定為基本 UI 或沒有 UI，則安裝程式會略過此資料表中的動作。</span><span class="sxs-lookup"><span data-stu-id="1df21-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="1df21-106">[關於消費者介面的詳細資訊，](about-the-user-interface.md)請參閱。</span><span class="sxs-lookup"><span data-stu-id="1df21-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="1df21-107">安裝順序中的系統管理動作，直到 [InstallValidate 動作](installvalidate-action.md)和任何結束對話方塊都位於 AdminUISequence 資料表中。</span><span class="sxs-lookup"><span data-stu-id="1df21-107">ADMIN actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the AdminUISequence table.</span></span> <span data-ttu-id="1df21-108">從 InstallValidate 到安裝順序結束的所有動作都會在 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="1df21-108">All actions from the InstallValidate through the end of the install sequence are in the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="1df21-109">由於 AdminExecuteSequence 資料表需要獨立，因此它也包含任何必要的初始化動作，例如 [LaunchConditions](launchconditions-action.md)、 [CostInitialize](costinitialize-action.md)、 [FileCost](filecost-action.md)和 [CostFinalize](costfinalize-action.md)。</span><span class="sxs-lookup"><span data-stu-id="1df21-109">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span> <span data-ttu-id="1df21-110">它也有 [ExecuteAction 動作](executeaction-action.md)。</span><span class="sxs-lookup"><span data-stu-id="1df21-110">It also has the [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="1df21-111">這些資料行與 [InstallUISequence 資料表](installuisequence-table.md)的資料行相同。</span><span class="sxs-lookup"><span data-stu-id="1df21-111">The columns are identical to those of the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="1df21-112">AdminUISequence 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="1df21-112">The AdminUISequence table has the following columns.</span></span>



| <span data-ttu-id="1df21-113">Column</span><span class="sxs-lookup"><span data-stu-id="1df21-113">Column</span></span>    | <span data-ttu-id="1df21-114">類型</span><span class="sxs-lookup"><span data-stu-id="1df21-114">Type</span></span>                         | <span data-ttu-id="1df21-115">答案</span><span class="sxs-lookup"><span data-stu-id="1df21-115">Key</span></span> | <span data-ttu-id="1df21-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="1df21-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="1df21-117">動作</span><span class="sxs-lookup"><span data-stu-id="1df21-117">Action</span></span>    | [<span data-ttu-id="1df21-118">識別碼</span><span class="sxs-lookup"><span data-stu-id="1df21-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="1df21-119">Y</span><span class="sxs-lookup"><span data-stu-id="1df21-119">Y</span></span>   | <span data-ttu-id="1df21-120">N</span><span class="sxs-lookup"><span data-stu-id="1df21-120">N</span></span>        |
| <span data-ttu-id="1df21-121">條件</span><span class="sxs-lookup"><span data-stu-id="1df21-121">Condition</span></span> | [<span data-ttu-id="1df21-122">Condition</span><span class="sxs-lookup"><span data-stu-id="1df21-122">Condition</span></span>](condition.md)   | <span data-ttu-id="1df21-123">N</span><span class="sxs-lookup"><span data-stu-id="1df21-123">N</span></span>   | <span data-ttu-id="1df21-124">Y</span><span class="sxs-lookup"><span data-stu-id="1df21-124">Y</span></span>        |
| <span data-ttu-id="1df21-125">順序</span><span class="sxs-lookup"><span data-stu-id="1df21-125">Sequence</span></span>  | [<span data-ttu-id="1df21-126">整數</span><span class="sxs-lookup"><span data-stu-id="1df21-126">Integer</span></span>](integer.md)       | <span data-ttu-id="1df21-127">N</span><span class="sxs-lookup"><span data-stu-id="1df21-127">N</span></span>   | <span data-ttu-id="1df21-128">Y</span><span class="sxs-lookup"><span data-stu-id="1df21-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1df21-129">資料行</span><span class="sxs-lookup"><span data-stu-id="1df21-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1df21-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動</span><span class="sxs-lookup"><span data-stu-id="1df21-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="1df21-131">要執行之動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="1df21-131">Name of the action to execute.</span></span> <span data-ttu-id="1df21-132">這是標準動作、使用者介面 wizard 或 [CustomAction 資料表](customaction-table.md)中所列的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="1df21-132">This is either a standard action, a user interface wizard, or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="1df21-133">主表索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1df21-133">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="1df21-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="1df21-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="1df21-135">邏輯運算式。</span><span class="sxs-lookup"><span data-stu-id="1df21-135">Logical expression.</span></span> <span data-ttu-id="1df21-136">如果運算式評估為 false，則會略過該動作。</span><span class="sxs-lookup"><span data-stu-id="1df21-136">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="1df21-137">如果運算式語法無效，則序列會終止，並傳回 iesBadActionData。</span><span class="sxs-lookup"><span data-stu-id="1df21-137">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="1df21-138">如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="1df21-138">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="1df21-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列</span><span class="sxs-lookup"><span data-stu-id="1df21-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="1df21-140">正值表示動作的序列位置。</span><span class="sxs-lookup"><span data-stu-id="1df21-140">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="1df21-141">下列負數值表示如果安裝程式傳回終止旗標，則會呼叫動作。</span><span class="sxs-lookup"><span data-stu-id="1df21-141">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="1df21-142">每個終止旗標 (負數值) 可用於不超過一個動作。</span><span class="sxs-lookup"><span data-stu-id="1df21-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="1df21-143">多個動作可以有終止旗標，但它們必須是不同的旗標。</span><span class="sxs-lookup"><span data-stu-id="1df21-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="1df21-144">終止旗標 (負數值) 通常會與 [對話方塊](dialog-boxes.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="1df21-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="1df21-145">終止旗標</span><span class="sxs-lookup"><span data-stu-id="1df21-145">Termination flag</span></span>          | <span data-ttu-id="1df21-146">值</span><span class="sxs-lookup"><span data-stu-id="1df21-146">Value</span></span> | <span data-ttu-id="1df21-147">描述</span><span class="sxs-lookup"><span data-stu-id="1df21-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1df21-148">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="1df21-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="1df21-149">-1</span><span class="sxs-lookup"><span data-stu-id="1df21-149">-1</span></span>    | <span data-ttu-id="1df21-150">順利完成。</span><span class="sxs-lookup"><span data-stu-id="1df21-150">Successful completion.</span></span> <span data-ttu-id="1df21-151">與 [結束] [對話方塊一起使用](exit-dialog.md) 。</span><span class="sxs-lookup"><span data-stu-id="1df21-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="1df21-152">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="1df21-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="1df21-153">-2</span><span class="sxs-lookup"><span data-stu-id="1df21-153">-2</span></span>    | <span data-ttu-id="1df21-154">使用者終止安裝。</span><span class="sxs-lookup"><span data-stu-id="1df21-154">User terminates install.</span></span> <span data-ttu-id="1df21-155">搭配 [UserExit](userexit-dialog.md) 對話方塊使用。</span><span class="sxs-lookup"><span data-stu-id="1df21-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="1df21-156">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="1df21-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="1df21-157">-3</span><span class="sxs-lookup"><span data-stu-id="1df21-157">-3</span></span>    | <span data-ttu-id="1df21-158">嚴重結束終止。</span><span class="sxs-lookup"><span data-stu-id="1df21-158">Fatal exit terminates.</span></span> <span data-ttu-id="1df21-159">搭配 [FatalError](fatalerror-dialog.md) 對話方塊使用。</span><span class="sxs-lookup"><span data-stu-id="1df21-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="1df21-160">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="1df21-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="1df21-161">-4</span><span class="sxs-lookup"><span data-stu-id="1df21-161">-4</span></span>    | <span data-ttu-id="1df21-162">安裝已暫停。</span><span class="sxs-lookup"><span data-stu-id="1df21-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="1df21-163">零、所有其他負數或 null 值表示永遠不會呼叫該動作。</span><span class="sxs-lookup"><span data-stu-id="1df21-163">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="1df21-164">驗證</span><span class="sxs-lookup"><span data-stu-id="1df21-164">Validation</span></span>

<dl>

[<span data-ttu-id="1df21-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="1df21-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1df21-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="1df21-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1df21-167">ICE12</span><span class="sxs-lookup"><span data-stu-id="1df21-167">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="1df21-168">ICE13</span><span class="sxs-lookup"><span data-stu-id="1df21-168">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="1df21-169">ICE20</span><span class="sxs-lookup"><span data-stu-id="1df21-169">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="1df21-170">ICE26</span><span class="sxs-lookup"><span data-stu-id="1df21-170">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="1df21-171">ICE27</span><span class="sxs-lookup"><span data-stu-id="1df21-171">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="1df21-172">ICE28</span><span class="sxs-lookup"><span data-stu-id="1df21-172">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="1df21-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="1df21-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="1df21-174">ICE75</span><span class="sxs-lookup"><span data-stu-id="1df21-174">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="1df21-175">ICE79</span><span class="sxs-lookup"><span data-stu-id="1df21-175">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="1df21-176">ICE82</span><span class="sxs-lookup"><span data-stu-id="1df21-176">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="1df21-177">ICE84</span><span class="sxs-lookup"><span data-stu-id="1df21-177">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="1df21-178">ICE86</span><span class="sxs-lookup"><span data-stu-id="1df21-178">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="1df21-179">ICE96</span><span class="sxs-lookup"><span data-stu-id="1df21-179">ICE96</span></span>](ice96.md)  
[<span data-ttu-id="1df21-180">ICEM04</span><span class="sxs-lookup"><span data-stu-id="1df21-180">ICEM04</span></span>](icem04.md)  
</dl>

 

 



