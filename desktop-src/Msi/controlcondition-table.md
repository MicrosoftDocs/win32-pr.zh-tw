---
description: ControlCondition 資料表可讓作者根據條件陳述式的結果，指定要套用至控制項的特殊動作。 例如，使用此資料表時，作者可以選擇根據 VersionNT 屬性隱藏控制項。
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: ControlCondition 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671dcdee6e2ed1067c51a04084693c276b8db2d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944653"
---
# <a name="controlcondition-table"></a><span data-ttu-id="a409c-104">ControlCondition 資料表</span><span class="sxs-lookup"><span data-stu-id="a409c-104">ControlCondition Table</span></span>

<span data-ttu-id="a409c-105">ControlCondition 資料表可讓作者根據條件陳述式的結果，指定要套用至控制項的特殊動作。</span><span class="sxs-lookup"><span data-stu-id="a409c-105">The ControlCondition table enables an author to specify special actions to be applied to controls based on the result of a conditional statement.</span></span> <span data-ttu-id="a409c-106">例如，使用此資料表時，作者可以選擇根據 [**VersionNT**](versionnt.md) 屬性隱藏控制項。</span><span class="sxs-lookup"><span data-stu-id="a409c-106">For example, using this table the author could choose to hide a control based on the [**VersionNT**](versionnt.md) property.</span></span>

<span data-ttu-id="a409c-107">ControlCondition 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="a409c-107">The ControlCondition table has the following columns.</span></span>



| <span data-ttu-id="a409c-108">Column</span><span class="sxs-lookup"><span data-stu-id="a409c-108">Column</span></span>    | <span data-ttu-id="a409c-109">類型</span><span class="sxs-lookup"><span data-stu-id="a409c-109">Type</span></span>                         | <span data-ttu-id="a409c-110">答案</span><span class="sxs-lookup"><span data-stu-id="a409c-110">Key</span></span> | <span data-ttu-id="a409c-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="a409c-111">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="a409c-112">對話\_</span><span class="sxs-lookup"><span data-stu-id="a409c-112">Dialog\_</span></span>  | [<span data-ttu-id="a409c-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="a409c-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="a409c-114">Y</span><span class="sxs-lookup"><span data-stu-id="a409c-114">Y</span></span>   | <span data-ttu-id="a409c-115">N</span><span class="sxs-lookup"><span data-stu-id="a409c-115">N</span></span>        |
| <span data-ttu-id="a409c-116">控制項\_</span><span class="sxs-lookup"><span data-stu-id="a409c-116">Control\_</span></span> | [<span data-ttu-id="a409c-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="a409c-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="a409c-118">Y</span><span class="sxs-lookup"><span data-stu-id="a409c-118">Y</span></span>   | <span data-ttu-id="a409c-119">N</span><span class="sxs-lookup"><span data-stu-id="a409c-119">N</span></span>        |
| <span data-ttu-id="a409c-120">動作</span><span class="sxs-lookup"><span data-stu-id="a409c-120">Action</span></span>    | [<span data-ttu-id="a409c-121">Text</span><span class="sxs-lookup"><span data-stu-id="a409c-121">Text</span></span>](text.md)             | <span data-ttu-id="a409c-122">Y</span><span class="sxs-lookup"><span data-stu-id="a409c-122">Y</span></span>   | <span data-ttu-id="a409c-123">N</span><span class="sxs-lookup"><span data-stu-id="a409c-123">N</span></span>        |
| <span data-ttu-id="a409c-124">條件</span><span class="sxs-lookup"><span data-stu-id="a409c-124">Condition</span></span> | [<span data-ttu-id="a409c-125">Condition</span><span class="sxs-lookup"><span data-stu-id="a409c-125">Condition</span></span>](condition.md)   | <span data-ttu-id="a409c-126">Y</span><span class="sxs-lookup"><span data-stu-id="a409c-126">Y</span></span>   | <span data-ttu-id="a409c-127">N</span><span class="sxs-lookup"><span data-stu-id="a409c-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a409c-128">資料行</span><span class="sxs-lookup"><span data-stu-id="a409c-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a409c-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>對話 框\_</span><span class="sxs-lookup"><span data-stu-id="a409c-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="a409c-130">[對話方塊資料表](dialog-table.md)第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a409c-130">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="a409c-131">結合此欄位與控制項欄位，即可 \_ 識別唯一的控制項。</span><span class="sxs-lookup"><span data-stu-id="a409c-131">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="a409c-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>控制\_</span><span class="sxs-lookup"><span data-stu-id="a409c-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="a409c-133">[控制資料表](control-table.md)第二個數據行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a409c-133">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="a409c-134">結合此欄位時，對話方塊 \_ 欄位會識別唯一的控制項。</span><span class="sxs-lookup"><span data-stu-id="a409c-134">Combining this field the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="a409c-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動</span><span class="sxs-lookup"><span data-stu-id="a409c-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="a409c-136">要在控制項上採取的動作。</span><span class="sxs-lookup"><span data-stu-id="a409c-136">The action that is to be taken on the control.</span></span> <span data-ttu-id="a409c-137">下表顯示可能的動作。</span><span class="sxs-lookup"><span data-stu-id="a409c-137">The possible actions are shown in the following table.</span></span>



| <span data-ttu-id="a409c-138">值</span><span class="sxs-lookup"><span data-stu-id="a409c-138">Value</span></span>   | <span data-ttu-id="a409c-139">意義</span><span class="sxs-lookup"><span data-stu-id="a409c-139">Meaning</span></span>                     |
|---------|-----------------------------|
| <span data-ttu-id="a409c-140">預設</span><span class="sxs-lookup"><span data-stu-id="a409c-140">Default</span></span> | <span data-ttu-id="a409c-141">將控制項設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="a409c-141">Set control as the default.</span></span> |
| <span data-ttu-id="a409c-142">停用</span><span class="sxs-lookup"><span data-stu-id="a409c-142">Disable</span></span> | <span data-ttu-id="a409c-143">停用控制項。</span><span class="sxs-lookup"><span data-stu-id="a409c-143">Disable the control.</span></span>        |
| <span data-ttu-id="a409c-144">啟用</span><span class="sxs-lookup"><span data-stu-id="a409c-144">Enable</span></span>  | <span data-ttu-id="a409c-145">啟用控制項。</span><span class="sxs-lookup"><span data-stu-id="a409c-145">Enable the control.</span></span>         |
| <span data-ttu-id="a409c-146">隱藏</span><span class="sxs-lookup"><span data-stu-id="a409c-146">Hide</span></span>    | <span data-ttu-id="a409c-147">隱藏控制項。</span><span class="sxs-lookup"><span data-stu-id="a409c-147">Hide the control.</span></span>           |
| <span data-ttu-id="a409c-148">顯示</span><span class="sxs-lookup"><span data-stu-id="a409c-148">Show</span></span>    | <span data-ttu-id="a409c-149">顯示控制項。</span><span class="sxs-lookup"><span data-stu-id="a409c-149">Display the control.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="a409c-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="a409c-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="a409c-151">條件陳述式，指定應觸發動作的條件。</span><span class="sxs-lookup"><span data-stu-id="a409c-151">A conditional statement that specifies under which conditions the action should be triggered.</span></span> <span data-ttu-id="a409c-152">此資料行可能不會保留空白。</span><span class="sxs-lookup"><span data-stu-id="a409c-152">This column may not be left blank.</span></span> <span data-ttu-id="a409c-153">如果此語句未評估為 TRUE，就不會執行此動作。</span><span class="sxs-lookup"><span data-stu-id="a409c-153">If this statement does not evaluate to TRUE, the action does not take place.</span></span> <span data-ttu-id="a409c-154">如果設定為1，則一律會套用動作。</span><span class="sxs-lookup"><span data-stu-id="a409c-154">If it is set to 1, the action is always applied.</span></span> <span data-ttu-id="a409c-155">如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="a409c-155">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a409c-156">備註</span><span class="sxs-lookup"><span data-stu-id="a409c-156">Remarks</span></span>

<span data-ttu-id="a409c-157">如果您想要根據 [ControlCondition] 資料表的 [條件] 欄位中的條件陳述式隱藏和停用 [按鈕](pushbutton-control.md) 控制項或 [核取方塊控制項](checkbox-control.md) ，您應該針對每個控制項使用四筆記錄來停用和隱藏控制項。</span><span class="sxs-lookup"><span data-stu-id="a409c-157">If you want to hide and disable a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) based on a conditional statement in the Condition field of the ControlCondition table, you should use four records for each control to disable as well as hide the control.</span></span> <span data-ttu-id="a409c-158">快速鍵仍可存取只有隱藏的按鈕或核取方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="a409c-158">PushButton or CheckBox controls that have only been hidden can still be accessed by shortcut keys.</span></span>

<span data-ttu-id="a409c-159">例如，下列記錄會在安裝產品時，隱藏和停用 DialogA 上的 ControlA。</span><span class="sxs-lookup"><span data-stu-id="a409c-159">For example, the following records hide and disable ControlA on DialogA when the product is installed.</span></span> <span data-ttu-id="a409c-160">未安裝產品時，會顯示並啟用此控制項。</span><span class="sxs-lookup"><span data-stu-id="a409c-160">The control will be visible and enabled when the product is not installed.</span></span>



| <span data-ttu-id="a409c-161">對話</span><span class="sxs-lookup"><span data-stu-id="a409c-161">Dialog</span></span>  | <span data-ttu-id="a409c-162">控制</span><span class="sxs-lookup"><span data-stu-id="a409c-162">Control</span></span>  | <span data-ttu-id="a409c-163">動作</span><span class="sxs-lookup"><span data-stu-id="a409c-163">Action</span></span>  | <span data-ttu-id="a409c-164">條件</span><span class="sxs-lookup"><span data-stu-id="a409c-164">Condition</span></span>                      |
|---------|----------|---------|--------------------------------|
| <span data-ttu-id="a409c-165">DialogA</span><span class="sxs-lookup"><span data-stu-id="a409c-165">DialogA</span></span> | <span data-ttu-id="a409c-166">ControlA</span><span class="sxs-lookup"><span data-stu-id="a409c-166">ControlA</span></span> | <span data-ttu-id="a409c-167">隱藏</span><span class="sxs-lookup"><span data-stu-id="a409c-167">Hide</span></span>    | [<span data-ttu-id="a409c-168">**安裝**</span><span class="sxs-lookup"><span data-stu-id="a409c-168">**Installed**</span></span>](installed.md) |
| <span data-ttu-id="a409c-169">DialogA</span><span class="sxs-lookup"><span data-stu-id="a409c-169">DialogA</span></span> | <span data-ttu-id="a409c-170">ControlA</span><span class="sxs-lookup"><span data-stu-id="a409c-170">ControlA</span></span> | <span data-ttu-id="a409c-171">停用</span><span class="sxs-lookup"><span data-stu-id="a409c-171">Disable</span></span> | <span data-ttu-id="a409c-172">已安裝</span><span class="sxs-lookup"><span data-stu-id="a409c-172">Installed</span></span>                      |
| <span data-ttu-id="a409c-173">DialogA</span><span class="sxs-lookup"><span data-stu-id="a409c-173">DialogA</span></span> | <span data-ttu-id="a409c-174">ControlA</span><span class="sxs-lookup"><span data-stu-id="a409c-174">ControlA</span></span> | <span data-ttu-id="a409c-175">顯示</span><span class="sxs-lookup"><span data-stu-id="a409c-175">Show</span></span>    | <span data-ttu-id="a409c-176">未安裝</span><span class="sxs-lookup"><span data-stu-id="a409c-176">NOT Installed</span></span>                  |
| <span data-ttu-id="a409c-177">DialogA</span><span class="sxs-lookup"><span data-stu-id="a409c-177">DialogA</span></span> | <span data-ttu-id="a409c-178">ControlA</span><span class="sxs-lookup"><span data-stu-id="a409c-178">ControlA</span></span> | <span data-ttu-id="a409c-179">啟用</span><span class="sxs-lookup"><span data-stu-id="a409c-179">Enable</span></span>  | <span data-ttu-id="a409c-180">未安裝</span><span class="sxs-lookup"><span data-stu-id="a409c-180">NOT Installed</span></span>                  |



 

## <a name="validation"></a><span data-ttu-id="a409c-181">驗證</span><span class="sxs-lookup"><span data-stu-id="a409c-181">Validation</span></span>

<dl>

[<span data-ttu-id="a409c-182">ICE03</span><span class="sxs-lookup"><span data-stu-id="a409c-182">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a409c-183">ICE06</span><span class="sxs-lookup"><span data-stu-id="a409c-183">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a409c-184">ICE17</span><span class="sxs-lookup"><span data-stu-id="a409c-184">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="a409c-185">ICE32</span><span class="sxs-lookup"><span data-stu-id="a409c-185">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="a409c-186">ICE46</span><span class="sxs-lookup"><span data-stu-id="a409c-186">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="a409c-187">ICE79</span><span class="sxs-lookup"><span data-stu-id="a409c-187">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="a409c-188">ICE86</span><span class="sxs-lookup"><span data-stu-id="a409c-188">ICE86</span></span>](ice86.md)  
</dl>

 

 



