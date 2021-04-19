---
description: AdminExecuteSequence 資料表會列出安裝程式在執行最上層系統管理動作時，會依序呼叫的動作。
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: AdminExecuteSequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c62ae43f8436ab210765e5402751c5722b78b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986891"
---
# <a name="adminexecutesequence-table"></a><span data-ttu-id="1f5f7-103">AdminExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="1f5f7-103">AdminExecuteSequence Table</span></span>

<span data-ttu-id="1f5f7-104">AdminExecuteSequence 資料表會列出安裝程式在執行最上層系統 [管理動作](admin-action.md) 時，會依序呼叫的動作。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-104">The AdminExecuteSequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed.</span></span>

<span data-ttu-id="1f5f7-105">安裝順序中的系統管理動作（最多 [InstallValidate 動作](installvalidate-action.md) 和任何結束對話方塊）都位於 [AdminUISequence 資料表](adminuisequence-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-105">ADMIN actions in the install sequence, up to the [InstallValidate action](installvalidate-action.md) and any exit dialog boxes, are located in the [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="1f5f7-106">從 InstallValidate 動作到安裝順序結束的系統管理動作都位於 AdminExecuteSequence 資料表中。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-106">ADMIN actions from the InstallValidate action through the end of the install sequence are in the AdminExecuteSequence table.</span></span> <span data-ttu-id="1f5f7-107">由於 AdminExecuteSequence 資料表需要獨立，因此它也包含任何必要的初始化動作，例如 [LaunchConditions](launchconditions-action.md)、 [CostInitialize](costinitialize-action.md)、 [FileCost](filecost-action.md)和 [CostFinalize](costfinalize-action.md)。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-107">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span>

<span data-ttu-id="1f5f7-108">需要使用者介面的 [自訂動作](custom-actions.md)應使用 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) ，而不是使用 [對話方塊資料表](dialog-table.md)所建立的編寫對話方塊。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="1f5f7-109">這些資料行與 [InstallExecuteSequence 資料表](installexecutesequence-table.md)的資料行相同。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-109">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="1f5f7-110">AdminExecuteSequence 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-110">The AdminExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="1f5f7-111">Column</span><span class="sxs-lookup"><span data-stu-id="1f5f7-111">Column</span></span>    | <span data-ttu-id="1f5f7-112">類型</span><span class="sxs-lookup"><span data-stu-id="1f5f7-112">Type</span></span>                         | <span data-ttu-id="1f5f7-113">答案</span><span class="sxs-lookup"><span data-stu-id="1f5f7-113">Key</span></span> | <span data-ttu-id="1f5f7-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="1f5f7-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="1f5f7-115">動作</span><span class="sxs-lookup"><span data-stu-id="1f5f7-115">Action</span></span>    | [<span data-ttu-id="1f5f7-116">識別碼</span><span class="sxs-lookup"><span data-stu-id="1f5f7-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="1f5f7-117">Y</span><span class="sxs-lookup"><span data-stu-id="1f5f7-117">Y</span></span>   | <span data-ttu-id="1f5f7-118">N</span><span class="sxs-lookup"><span data-stu-id="1f5f7-118">N</span></span>        |
| <span data-ttu-id="1f5f7-119">條件</span><span class="sxs-lookup"><span data-stu-id="1f5f7-119">Condition</span></span> | [<span data-ttu-id="1f5f7-120">Condition</span><span class="sxs-lookup"><span data-stu-id="1f5f7-120">Condition</span></span>](condition.md)   | <span data-ttu-id="1f5f7-121">N</span><span class="sxs-lookup"><span data-stu-id="1f5f7-121">N</span></span>   | <span data-ttu-id="1f5f7-122">Y</span><span class="sxs-lookup"><span data-stu-id="1f5f7-122">Y</span></span>        |
| <span data-ttu-id="1f5f7-123">順序</span><span class="sxs-lookup"><span data-stu-id="1f5f7-123">Sequence</span></span>  | [<span data-ttu-id="1f5f7-124">整數</span><span class="sxs-lookup"><span data-stu-id="1f5f7-124">Integer</span></span>](integer.md)       | <span data-ttu-id="1f5f7-125">N</span><span class="sxs-lookup"><span data-stu-id="1f5f7-125">N</span></span>   | <span data-ttu-id="1f5f7-126">Y</span><span class="sxs-lookup"><span data-stu-id="1f5f7-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1f5f7-127">資料行</span><span class="sxs-lookup"><span data-stu-id="1f5f7-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1f5f7-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動</span><span class="sxs-lookup"><span data-stu-id="1f5f7-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="1f5f7-129">要執行之動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-129">Name of the action to execute.</span></span> <span data-ttu-id="1f5f7-130">這是 [CustomAction 資料表](customaction-table.md)中所列的標準動作或自訂動作。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-130">This is either a standard action or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="1f5f7-131">主表索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="1f5f7-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="1f5f7-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="1f5f7-133">邏輯運算式。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-133">Logical expression.</span></span> <span data-ttu-id="1f5f7-134">如果運算式評估為 false，則會略過該動作。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-134">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="1f5f7-135">如果運算式語法無效，則序列會終止，並傳回 iesBadActionData。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-135">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="1f5f7-136">如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-136">For information on the syntax of conditional statements see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f5f7-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列</span><span class="sxs-lookup"><span data-stu-id="1f5f7-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="1f5f7-138">正值表示動作的序列位置。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-138">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="1f5f7-139">下列負數值表示如果安裝程式傳回終止旗標，則會呼叫動作。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-139">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="1f5f7-140">每個終止旗標 (負數值) 可用於不超過一個動作。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-140">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="1f5f7-141">多個動作可以有終止旗標，但它們必須是不同的旗標。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-141">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="1f5f7-142">終止旗標 (負數值) 通常會與 [對話方塊](dialog-boxes.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-142">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="1f5f7-143">終止旗標</span><span class="sxs-lookup"><span data-stu-id="1f5f7-143">Termination flag</span></span>          | <span data-ttu-id="1f5f7-144">值</span><span class="sxs-lookup"><span data-stu-id="1f5f7-144">Value</span></span> | <span data-ttu-id="1f5f7-145">描述</span><span class="sxs-lookup"><span data-stu-id="1f5f7-145">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1f5f7-146">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="1f5f7-146">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="1f5f7-147">-1</span><span class="sxs-lookup"><span data-stu-id="1f5f7-147">-1</span></span>    | <span data-ttu-id="1f5f7-148">順利完成。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-148">Successful completion.</span></span> <span data-ttu-id="1f5f7-149">與 [結束] [對話方塊一起使用](exit-dialog.md) 。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-149">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="1f5f7-150">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="1f5f7-150">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="1f5f7-151">-2</span><span class="sxs-lookup"><span data-stu-id="1f5f7-151">-2</span></span>    | <span data-ttu-id="1f5f7-152">使用者終止安裝。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-152">User terminates install.</span></span> <span data-ttu-id="1f5f7-153">搭配 [UserExit](userexit-dialog.md) 對話方塊使用。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-153">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="1f5f7-154">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="1f5f7-154">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="1f5f7-155">-3</span><span class="sxs-lookup"><span data-stu-id="1f5f7-155">-3</span></span>    | <span data-ttu-id="1f5f7-156">嚴重結束終止。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-156">Fatal exit terminates.</span></span> <span data-ttu-id="1f5f7-157">搭配 [FatalError](fatalerror-dialog.md) 對話方塊使用。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-157">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="1f5f7-158">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="1f5f7-158">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="1f5f7-159">-4</span><span class="sxs-lookup"><span data-stu-id="1f5f7-159">-4</span></span>    | <span data-ttu-id="1f5f7-160">安裝已暫停。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-160">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="1f5f7-161">零、所有其他負數或 null 值表示永遠不會呼叫該動作。</span><span class="sxs-lookup"><span data-stu-id="1f5f7-161">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="1f5f7-162">驗證</span><span class="sxs-lookup"><span data-stu-id="1f5f7-162">Validation</span></span>

<dl>

[<span data-ttu-id="1f5f7-163">ICE03</span><span class="sxs-lookup"><span data-stu-id="1f5f7-163">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1f5f7-164">ICE06</span><span class="sxs-lookup"><span data-stu-id="1f5f7-164">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1f5f7-165">ICE12</span><span class="sxs-lookup"><span data-stu-id="1f5f7-165">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="1f5f7-166">ICE13</span><span class="sxs-lookup"><span data-stu-id="1f5f7-166">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="1f5f7-167">ICE26</span><span class="sxs-lookup"><span data-stu-id="1f5f7-167">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="1f5f7-168">ICE27</span><span class="sxs-lookup"><span data-stu-id="1f5f7-168">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="1f5f7-169">ICE28</span><span class="sxs-lookup"><span data-stu-id="1f5f7-169">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="1f5f7-170">ICE75</span><span class="sxs-lookup"><span data-stu-id="1f5f7-170">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="1f5f7-171">ICE77</span><span class="sxs-lookup"><span data-stu-id="1f5f7-171">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="1f5f7-172">ICE79</span><span class="sxs-lookup"><span data-stu-id="1f5f7-172">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="1f5f7-173">ICE82</span><span class="sxs-lookup"><span data-stu-id="1f5f7-173">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="1f5f7-174">ICE84</span><span class="sxs-lookup"><span data-stu-id="1f5f7-174">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="1f5f7-175">ICE86</span><span class="sxs-lookup"><span data-stu-id="1f5f7-175">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="1f5f7-176">ICEM04</span><span class="sxs-lookup"><span data-stu-id="1f5f7-176">ICEM04</span></span>](icem04.md)  
</dl>

 

 



