---
description: AdvtExecuteSequence 資料表會列出安裝程式在執行最上層通告動作時所呼叫的動作。
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: AdvtExecuteSequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b68a3f69cc7473b2364f169545743941d752f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848984"
---
# <a name="advtexecutesequence-table"></a><span data-ttu-id="66803-103">AdvtExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="66803-103">AdvtExecuteSequence Table</span></span>

<span data-ttu-id="66803-104">AdvtExecuteSequence 資料表會列出安裝程式在執行最上層 [通告動作](advertise-action.md) 時所呼叫的動作。</span><span class="sxs-lookup"><span data-stu-id="66803-104">The AdvtExecuteSequence table lists actions the installer calls when the top-level [ADVERTISE action](advertise-action.md) is executed.</span></span>

<span data-ttu-id="66803-105">只有下列動作可以在 AdvtExecuteSequence 資料表中使用。</span><span class="sxs-lookup"><span data-stu-id="66803-105">Only the following actions can be used in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="66803-106">自訂動作不能用在此資料表中。</span><span class="sxs-lookup"><span data-stu-id="66803-106">Custom actions cannot be used in this table.</span></span>

[<span data-ttu-id="66803-107">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="66803-107">CostFinalize</span></span>](costfinalize-action.md)

[<span data-ttu-id="66803-108">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="66803-108">CostInitialize</span></span>](costinitialize-action.md)

[<span data-ttu-id="66803-109">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="66803-109">CreateShortcuts</span></span>](createshortcuts-action.md)

[<span data-ttu-id="66803-110">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="66803-110">InstallFinalize</span></span>](installfinalize-action.md)

[<span data-ttu-id="66803-111">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="66803-111">InstallInitialize</span></span>](installinitialize-action.md)

[<span data-ttu-id="66803-112">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="66803-112">InstallValidate</span></span>](installvalidate-action.md)

[<span data-ttu-id="66803-113">MsiPublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="66803-113">MsiPublishAssemblies</span></span>](msipublishassemblies-action.md)

[<span data-ttu-id="66803-114">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="66803-114">PublishComponents</span></span>](publishcomponents-action.md)

[<span data-ttu-id="66803-115">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="66803-115">PublishFeatures</span></span>](publishfeatures-action.md)

[<span data-ttu-id="66803-116">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="66803-116">PublishProduct</span></span>](publishproduct-action.md)

[<span data-ttu-id="66803-117">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="66803-117">RegisterClassInfo</span></span>](registerclassinfo-action.md)

[<span data-ttu-id="66803-118">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="66803-118">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)

[<span data-ttu-id="66803-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="66803-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

[<span data-ttu-id="66803-120">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="66803-120">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="66803-121">這些資料行與 [InstallExecuteSequence 資料表](installexecutesequence-table.md)的資料行相同。</span><span class="sxs-lookup"><span data-stu-id="66803-121">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="66803-122">AdvtExecuteSequence 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="66803-122">The AdvtExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="66803-123">Column</span><span class="sxs-lookup"><span data-stu-id="66803-123">Column</span></span>    | <span data-ttu-id="66803-124">類型</span><span class="sxs-lookup"><span data-stu-id="66803-124">Type</span></span>                         | <span data-ttu-id="66803-125">答案</span><span class="sxs-lookup"><span data-stu-id="66803-125">Key</span></span> | <span data-ttu-id="66803-126">Nullable</span><span class="sxs-lookup"><span data-stu-id="66803-126">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="66803-127">動作</span><span class="sxs-lookup"><span data-stu-id="66803-127">Action</span></span>    | [<span data-ttu-id="66803-128">識別碼</span><span class="sxs-lookup"><span data-stu-id="66803-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="66803-129">Y</span><span class="sxs-lookup"><span data-stu-id="66803-129">Y</span></span>   | <span data-ttu-id="66803-130">N</span><span class="sxs-lookup"><span data-stu-id="66803-130">N</span></span>        |
| <span data-ttu-id="66803-131">條件</span><span class="sxs-lookup"><span data-stu-id="66803-131">Condition</span></span> | [<span data-ttu-id="66803-132">Condition</span><span class="sxs-lookup"><span data-stu-id="66803-132">Condition</span></span>](condition.md)   | <span data-ttu-id="66803-133">N</span><span class="sxs-lookup"><span data-stu-id="66803-133">N</span></span>   | <span data-ttu-id="66803-134">Y</span><span class="sxs-lookup"><span data-stu-id="66803-134">Y</span></span>        |
| <span data-ttu-id="66803-135">順序</span><span class="sxs-lookup"><span data-stu-id="66803-135">Sequence</span></span>  | [<span data-ttu-id="66803-136">整數</span><span class="sxs-lookup"><span data-stu-id="66803-136">Integer</span></span>](integer.md)       | <span data-ttu-id="66803-137">N</span><span class="sxs-lookup"><span data-stu-id="66803-137">N</span></span>   | <span data-ttu-id="66803-138">Y</span><span class="sxs-lookup"><span data-stu-id="66803-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="66803-139">資料行</span><span class="sxs-lookup"><span data-stu-id="66803-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="66803-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動</span><span class="sxs-lookup"><span data-stu-id="66803-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="66803-141">安裝程式要執行的 [標準動作](standard-actions.md) 名稱。</span><span class="sxs-lookup"><span data-stu-id="66803-141">Name of the [standard action](standard-actions.md) the installer is to execute.</span></span> <span data-ttu-id="66803-142">這是資料表的主鍵。</span><span class="sxs-lookup"><span data-stu-id="66803-142">This is the primary key of the table.</span></span>

</dd> <dt>

<span data-ttu-id="66803-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="66803-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="66803-144">邏輯運算式。</span><span class="sxs-lookup"><span data-stu-id="66803-144">Logical expression.</span></span> <span data-ttu-id="66803-145">如果運算式評估為 false，則會略過該動作。</span><span class="sxs-lookup"><span data-stu-id="66803-145">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="66803-146">如果運算式語法無效，則序列會終止，並傳回 iesBadActionData。</span><span class="sxs-lookup"><span data-stu-id="66803-146">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="66803-147">如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="66803-147">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="66803-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列</span><span class="sxs-lookup"><span data-stu-id="66803-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="66803-149">正值表示動作的序列位置。</span><span class="sxs-lookup"><span data-stu-id="66803-149">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="66803-150">下列負數值表示如果安裝程式傳回終止旗標，則會呼叫動作。</span><span class="sxs-lookup"><span data-stu-id="66803-150">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="66803-151">每個終止旗標 (負數值) 可用於不超過一個動作。</span><span class="sxs-lookup"><span data-stu-id="66803-151">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="66803-152">多個動作可以有終止旗標，但它們必須是不同的旗標。</span><span class="sxs-lookup"><span data-stu-id="66803-152">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="66803-153">終止旗標 (負數值) 通常會與 [對話方塊](dialog-boxes.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="66803-153">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="66803-154">終止旗標</span><span class="sxs-lookup"><span data-stu-id="66803-154">Termination flag</span></span>          | <span data-ttu-id="66803-155">值</span><span class="sxs-lookup"><span data-stu-id="66803-155">Value</span></span> | <span data-ttu-id="66803-156">描述</span><span class="sxs-lookup"><span data-stu-id="66803-156">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66803-157">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="66803-157">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="66803-158">-1</span><span class="sxs-lookup"><span data-stu-id="66803-158">-1</span></span>    | <span data-ttu-id="66803-159">順利完成。</span><span class="sxs-lookup"><span data-stu-id="66803-159">Successful completion.</span></span> <span data-ttu-id="66803-160">與 [結束] [對話方塊一起使用](exit-dialog.md) 。</span><span class="sxs-lookup"><span data-stu-id="66803-160">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="66803-161">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="66803-161">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="66803-162">-2</span><span class="sxs-lookup"><span data-stu-id="66803-162">-2</span></span>    | <span data-ttu-id="66803-163">使用者終止安裝。</span><span class="sxs-lookup"><span data-stu-id="66803-163">User terminates install.</span></span> <span data-ttu-id="66803-164">搭配 [UserExit](userexit-dialog.md) 對話方塊使用。</span><span class="sxs-lookup"><span data-stu-id="66803-164">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="66803-165">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="66803-165">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="66803-166">-3</span><span class="sxs-lookup"><span data-stu-id="66803-166">-3</span></span>    | <span data-ttu-id="66803-167">嚴重結束終止。</span><span class="sxs-lookup"><span data-stu-id="66803-167">Fatal exit terminates.</span></span> <span data-ttu-id="66803-168">搭配 [FatalError](fatalerror-dialog.md) 對話方塊使用。</span><span class="sxs-lookup"><span data-stu-id="66803-168">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="66803-169">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="66803-169">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="66803-170">-4</span><span class="sxs-lookup"><span data-stu-id="66803-170">-4</span></span>    | <span data-ttu-id="66803-171">安裝已暫停。</span><span class="sxs-lookup"><span data-stu-id="66803-171">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="66803-172">零、所有其他負數或 null 值表示永遠不會呼叫該動作。</span><span class="sxs-lookup"><span data-stu-id="66803-172">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="66803-173">驗證</span><span class="sxs-lookup"><span data-stu-id="66803-173">Validation</span></span>

<dl>

[<span data-ttu-id="66803-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="66803-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="66803-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="66803-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="66803-176">ICE12</span><span class="sxs-lookup"><span data-stu-id="66803-176">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="66803-177">ICE13</span><span class="sxs-lookup"><span data-stu-id="66803-177">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="66803-178">ICE27</span><span class="sxs-lookup"><span data-stu-id="66803-178">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="66803-179">ICE46</span><span class="sxs-lookup"><span data-stu-id="66803-179">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="66803-180">ICE72</span><span class="sxs-lookup"><span data-stu-id="66803-180">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="66803-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="66803-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="66803-182">ICE82</span><span class="sxs-lookup"><span data-stu-id="66803-182">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="66803-183">ICE83</span><span class="sxs-lookup"><span data-stu-id="66803-183">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="66803-184">ICE84</span><span class="sxs-lookup"><span data-stu-id="66803-184">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="66803-185">ICE86</span><span class="sxs-lookup"><span data-stu-id="66803-185">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="66803-186">ICEM04</span><span class="sxs-lookup"><span data-stu-id="66803-186">ICEM04</span></span>](icem04.md)  
</dl>

 

 



