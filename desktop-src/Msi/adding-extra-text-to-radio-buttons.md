---
description: 螢幕讀取程式只能讀取已在選項按鈕資料表的文字資料行中撰寫之 RadioButtonGroup 控制項的文字。
ms.assetid: 92ad70ec-a3a4-4ea7-8888-40c78d73e58a
title: 在選項按鈕中加入額外的文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e73ac55e300ddee603449e9ea7ce5e10f4e0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944042"
---
# <a name="adding-extra-text-to-radio-buttons"></a><span data-ttu-id="b094b-103">在選項按鈕中加入額外的文字</span><span class="sxs-lookup"><span data-stu-id="b094b-103">Adding Extra Text to Radio Buttons</span></span>

<span data-ttu-id="b094b-104">螢幕讀取程式只能讀取已在[選項按鈕資料表](radiobutton-table.md)的文字資料行中撰寫之[RadioButtonGroup 控制項](radiobuttongroup-control.md)的文字。</span><span class="sxs-lookup"><span data-stu-id="b094b-104">Screen reader programs can only read the text of a [RadioButtonGroup control](radiobuttongroup-control.md) that has been authored into the Text column of the [RadioButton table](radiobutton-table.md).</span></span> <span data-ttu-id="b094b-105">如果此文字是選項按鈕的不足描述，則可以加入重迭的 [文字控制項](text-control.md) 來提供額外的描述性文字。</span><span class="sxs-lookup"><span data-stu-id="b094b-105">If this text is an insufficient description of the radio buttons, overlapping [Text controls](text-control.md) can be added to provide extra descriptive text.</span></span> <span data-ttu-id="b094b-106">這些文字控制項應該在對話方塊中彼此重迭，並在 [ControlCondition 資料表](controlcondition-table.md) 中設定條件，如此一來，一次只會顯示一個文字控制項。</span><span class="sxs-lookup"><span data-stu-id="b094b-106">These Text controls should overlap each other in the dialog box and have conditions set in the [ControlCondition table](controlcondition-table.md) so that only one Text control is shown at a time.</span></span> <span data-ttu-id="b094b-107">文字控制項不能重迭 RadioButtonGroup 控制項或對話方塊中的其他控制項，因為這樣會讓螢幕讀取器看不到控制項。</span><span class="sxs-lookup"><span data-stu-id="b094b-107">The Text controls must not overlap the RadioButtonGroup control or other controls in the dialog because this makes the controls invisible to screen readers.</span></span> <span data-ttu-id="b094b-108">當使用者將游標停留在文字控制項上方時，螢幕讀取程式會讀取額外的文字。</span><span class="sxs-lookup"><span data-stu-id="b094b-108">When the user hovers the cursor over the Text control, the screen reader program reads the extra text.</span></span>

<span data-ttu-id="b094b-109">在下列範例中，[MySample] 對話方塊有一個名為 [色彩] 的 RadioButtonGroup 控制項，其中有兩個 [TheColor] 屬性值的選項。</span><span class="sxs-lookup"><span data-stu-id="b094b-109">In the following example the MySample dialog box has a RadioButtonGroup control named Colors with two choices for the value of the TheColor property.</span></span> <span data-ttu-id="b094b-110">針對每個選擇，都有一個具有要隱藏或顯示之條件的文字控制項，視目前針對 TheColor 選取的選擇而定。</span><span class="sxs-lookup"><span data-stu-id="b094b-110">For each choice there is a Text control with a condition to hide or show, depending on the current choice selected for TheColor.</span></span> <span data-ttu-id="b094b-111">初始 TheColor 值定義于屬性工作表中。</span><span class="sxs-lookup"><span data-stu-id="b094b-111">An initial TheColor value is defined in the Property table.</span></span> <span data-ttu-id="b094b-112">文字控制項具有在選項按鈕資料表的文字欄位中撰寫的額外描述性文字。</span><span class="sxs-lookup"><span data-stu-id="b094b-112">The Text controls have the extra descriptive text authored in the Text field of the RadioButton table.</span></span> <span data-ttu-id="b094b-113">當使用者將游標停留在對話方塊中的文字控制項上方時，螢幕讀取器可以讀取目前選擇的額外描述。</span><span class="sxs-lookup"><span data-stu-id="b094b-113">When a user hovers the cursor over the Text control in the dialog box, the screen reader can read the extra description of the current choice.</span></span>

[<span data-ttu-id="b094b-114">對話方塊資料表</span><span class="sxs-lookup"><span data-stu-id="b094b-114">Dialog table</span></span>](dialog-table.md)



| <span data-ttu-id="b094b-115">對話</span><span class="sxs-lookup"><span data-stu-id="b094b-115">Dialog</span></span>   | <span data-ttu-id="b094b-116">HCentering</span><span class="sxs-lookup"><span data-stu-id="b094b-116">HCentering</span></span> | <span data-ttu-id="b094b-117">VCentering</span><span class="sxs-lookup"><span data-stu-id="b094b-117">VCentering</span></span> | <span data-ttu-id="b094b-118">寬度</span><span class="sxs-lookup"><span data-stu-id="b094b-118">Width</span></span> | <span data-ttu-id="b094b-119">高度</span><span class="sxs-lookup"><span data-stu-id="b094b-119">Height</span></span> | <span data-ttu-id="b094b-120">屬性</span><span class="sxs-lookup"><span data-stu-id="b094b-120">Attributes</span></span> | <span data-ttu-id="b094b-121">標題</span><span class="sxs-lookup"><span data-stu-id="b094b-121">Title</span></span>                    | <span data-ttu-id="b094b-122">\_先控制項</span><span class="sxs-lookup"><span data-stu-id="b094b-122">Control\_First</span></span> | <span data-ttu-id="b094b-123">控制項 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="b094b-123">Control\_Default</span></span> | <span data-ttu-id="b094b-124">控制 \_ 取消</span><span class="sxs-lookup"><span data-stu-id="b094b-124">Control\_Cancel</span></span> |
|----------|------------|------------|-------|--------|------------|--------------------------|----------------|------------------|-----------------|
| <span data-ttu-id="b094b-125">MySample</span><span class="sxs-lookup"><span data-stu-id="b094b-125">MySample</span></span> | <span data-ttu-id="b094b-126">50</span><span class="sxs-lookup"><span data-stu-id="b094b-126">50</span></span>         | <span data-ttu-id="b094b-127">50</span><span class="sxs-lookup"><span data-stu-id="b094b-127">50</span></span>         | <span data-ttu-id="b094b-128">200</span><span class="sxs-lookup"><span data-stu-id="b094b-128">200</span></span>   | <span data-ttu-id="b094b-129">180</span><span class="sxs-lookup"><span data-stu-id="b094b-129">180</span></span>    | <span data-ttu-id="b094b-130">3</span><span class="sxs-lookup"><span data-stu-id="b094b-130">3</span></span>          | <span data-ttu-id="b094b-131">可存取的選項按鈕</span><span class="sxs-lookup"><span data-stu-id="b094b-131">Accessible radio buttons</span></span> | <span data-ttu-id="b094b-132">色彩</span><span class="sxs-lookup"><span data-stu-id="b094b-132">Colors</span></span>         | <span data-ttu-id="b094b-133">下一個</span><span class="sxs-lookup"><span data-stu-id="b094b-133">Next</span></span>             |                 |



 

[<span data-ttu-id="b094b-134">控制資料表</span><span class="sxs-lookup"><span data-stu-id="b094b-134">Control table</span></span>](control-table.md)



| <span data-ttu-id="b094b-135">對話\_</span><span class="sxs-lookup"><span data-stu-id="b094b-135">Dialog\_</span></span> | <span data-ttu-id="b094b-136">控制</span><span class="sxs-lookup"><span data-stu-id="b094b-136">Control</span></span>    | <span data-ttu-id="b094b-137">類型</span><span class="sxs-lookup"><span data-stu-id="b094b-137">Type</span></span>             | <span data-ttu-id="b094b-138">X</span><span class="sxs-lookup"><span data-stu-id="b094b-138">X</span></span>   | <span data-ttu-id="b094b-139">Y</span><span class="sxs-lookup"><span data-stu-id="b094b-139">Y</span></span>   | <span data-ttu-id="b094b-140">寬度</span><span class="sxs-lookup"><span data-stu-id="b094b-140">Width</span></span> | <span data-ttu-id="b094b-141">高度</span><span class="sxs-lookup"><span data-stu-id="b094b-141">Height</span></span> | <span data-ttu-id="b094b-142">屬性</span><span class="sxs-lookup"><span data-stu-id="b094b-142">Attributes</span></span> | <span data-ttu-id="b094b-143">屬性</span><span class="sxs-lookup"><span data-stu-id="b094b-143">Property</span></span> | <span data-ttu-id="b094b-144">Text</span><span class="sxs-lookup"><span data-stu-id="b094b-144">Text</span></span>                               | <span data-ttu-id="b094b-145">控制 \_ 下一步</span><span class="sxs-lookup"><span data-stu-id="b094b-145">Control\_Next</span></span> | <span data-ttu-id="b094b-146">Help</span><span class="sxs-lookup"><span data-stu-id="b094b-146">Help</span></span> |
|----------|------------|------------------|-----|-----|-------|--------|------------|----------|------------------------------------|---------------|------|
| <span data-ttu-id="b094b-147">MySample</span><span class="sxs-lookup"><span data-stu-id="b094b-147">MySample</span></span> | <span data-ttu-id="b094b-148">色彩</span><span class="sxs-lookup"><span data-stu-id="b094b-148">Colors</span></span>     | <span data-ttu-id="b094b-149">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="b094b-149">RadioButtonGroup</span></span> | <span data-ttu-id="b094b-150">2</span><span class="sxs-lookup"><span data-stu-id="b094b-150">2</span></span>   | <span data-ttu-id="b094b-151">20</span><span class="sxs-lookup"><span data-stu-id="b094b-151">20</span></span>  | <span data-ttu-id="b094b-152">100</span><span class="sxs-lookup"><span data-stu-id="b094b-152">100</span></span>   | <span data-ttu-id="b094b-153">50</span><span class="sxs-lookup"><span data-stu-id="b094b-153">50</span></span>     | <span data-ttu-id="b094b-154">3</span><span class="sxs-lookup"><span data-stu-id="b094b-154">3</span></span>          | <span data-ttu-id="b094b-155">TheColor</span><span class="sxs-lookup"><span data-stu-id="b094b-155">TheColor</span></span> |                                    | <span data-ttu-id="b094b-156">下一個</span><span class="sxs-lookup"><span data-stu-id="b094b-156">Next</span></span>          |      |
| <span data-ttu-id="b094b-157">MySample</span><span class="sxs-lookup"><span data-stu-id="b094b-157">MySample</span></span> | <span data-ttu-id="b094b-158">HowIsBlue</span><span class="sxs-lookup"><span data-stu-id="b094b-158">HowIsBlue</span></span>  | <span data-ttu-id="b094b-159">Text</span><span class="sxs-lookup"><span data-stu-id="b094b-159">Text</span></span>             | <span data-ttu-id="b094b-160">20</span><span class="sxs-lookup"><span data-stu-id="b094b-160">20</span></span>  | <span data-ttu-id="b094b-161">80</span><span class="sxs-lookup"><span data-stu-id="b094b-161">80</span></span>  | <span data-ttu-id="b094b-162">150</span><span class="sxs-lookup"><span data-stu-id="b094b-162">150</span></span>   | <span data-ttu-id="b094b-163">15</span><span class="sxs-lookup"><span data-stu-id="b094b-163">15</span></span>     | <span data-ttu-id="b094b-164">2</span><span class="sxs-lookup"><span data-stu-id="b094b-164">2</span></span>          |          | <span data-ttu-id="b094b-165">這就像是一天的天空。</span><span class="sxs-lookup"><span data-stu-id="b094b-165">It is like the sky on a clear day.</span></span> |               |      |
| <span data-ttu-id="b094b-166">MySample</span><span class="sxs-lookup"><span data-stu-id="b094b-166">MySample</span></span> | <span data-ttu-id="b094b-167">HowIsGreen</span><span class="sxs-lookup"><span data-stu-id="b094b-167">HowIsGreen</span></span> | <span data-ttu-id="b094b-168">Text</span><span class="sxs-lookup"><span data-stu-id="b094b-168">Text</span></span>             | <span data-ttu-id="b094b-169">20</span><span class="sxs-lookup"><span data-stu-id="b094b-169">20</span></span>  | <span data-ttu-id="b094b-170">80</span><span class="sxs-lookup"><span data-stu-id="b094b-170">80</span></span>  | <span data-ttu-id="b094b-171">150</span><span class="sxs-lookup"><span data-stu-id="b094b-171">150</span></span>   | <span data-ttu-id="b094b-172">15</span><span class="sxs-lookup"><span data-stu-id="b094b-172">15</span></span>     | <span data-ttu-id="b094b-173">2</span><span class="sxs-lookup"><span data-stu-id="b094b-173">2</span></span>          |          | <span data-ttu-id="b094b-174">這就像是彈簧中的草坪一樣。</span><span class="sxs-lookup"><span data-stu-id="b094b-174">It is like grass in the spring.</span></span>    |               |      |



 

[<span data-ttu-id="b094b-175">選項按鈕資料表</span><span class="sxs-lookup"><span data-stu-id="b094b-175">RadioButton table</span></span>](radiobutton-table.md)



| <span data-ttu-id="b094b-176">屬性</span><span class="sxs-lookup"><span data-stu-id="b094b-176">Property</span></span> | <span data-ttu-id="b094b-177">單</span><span class="sxs-lookup"><span data-stu-id="b094b-177">Order</span></span> | <span data-ttu-id="b094b-178">值</span><span class="sxs-lookup"><span data-stu-id="b094b-178">Value</span></span> | <span data-ttu-id="b094b-179">X</span><span class="sxs-lookup"><span data-stu-id="b094b-179">X</span></span>   | <span data-ttu-id="b094b-180">Y</span><span class="sxs-lookup"><span data-stu-id="b094b-180">Y</span></span>   | <span data-ttu-id="b094b-181">寬度</span><span class="sxs-lookup"><span data-stu-id="b094b-181">Width</span></span> | <span data-ttu-id="b094b-182">高度</span><span class="sxs-lookup"><span data-stu-id="b094b-182">Height</span></span> | <span data-ttu-id="b094b-183">Text</span><span class="sxs-lookup"><span data-stu-id="b094b-183">Text</span></span>   | <span data-ttu-id="b094b-184">Help</span><span class="sxs-lookup"><span data-stu-id="b094b-184">Help</span></span> |
|----------|-------|-------|-----|-----|-------|--------|--------|------|
| <span data-ttu-id="b094b-185">TheColor</span><span class="sxs-lookup"><span data-stu-id="b094b-185">TheColor</span></span> | <span data-ttu-id="b094b-186">1</span><span class="sxs-lookup"><span data-stu-id="b094b-186">1</span></span>     | <span data-ttu-id="b094b-187">藍色</span><span class="sxs-lookup"><span data-stu-id="b094b-187">Blue</span></span>  | <span data-ttu-id="b094b-188">10</span><span class="sxs-lookup"><span data-stu-id="b094b-188">10</span></span>  | <span data-ttu-id="b094b-189">10</span><span class="sxs-lookup"><span data-stu-id="b094b-189">10</span></span>  | <span data-ttu-id="b094b-190">80</span><span class="sxs-lookup"><span data-stu-id="b094b-190">80</span></span>    | <span data-ttu-id="b094b-191">15</span><span class="sxs-lookup"><span data-stu-id="b094b-191">15</span></span>     | <span data-ttu-id="b094b-192">&藍色</span><span class="sxs-lookup"><span data-stu-id="b094b-192">&Blue</span></span>  |      |
| <span data-ttu-id="b094b-193">TheColor</span><span class="sxs-lookup"><span data-stu-id="b094b-193">TheColor</span></span> | <span data-ttu-id="b094b-194">2</span><span class="sxs-lookup"><span data-stu-id="b094b-194">2</span></span>     | <span data-ttu-id="b094b-195">綠色</span><span class="sxs-lookup"><span data-stu-id="b094b-195">Green</span></span> | <span data-ttu-id="b094b-196">10</span><span class="sxs-lookup"><span data-stu-id="b094b-196">10</span></span>  | <span data-ttu-id="b094b-197">30</span><span class="sxs-lookup"><span data-stu-id="b094b-197">30</span></span>  | <span data-ttu-id="b094b-198">80</span><span class="sxs-lookup"><span data-stu-id="b094b-198">80</span></span>    | <span data-ttu-id="b094b-199">15</span><span class="sxs-lookup"><span data-stu-id="b094b-199">15</span></span>     | <span data-ttu-id="b094b-200">&綠色</span><span class="sxs-lookup"><span data-stu-id="b094b-200">&Green</span></span> |      |



 

[<span data-ttu-id="b094b-201">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="b094b-201">Property table</span></span>](property-table.md)



| <span data-ttu-id="b094b-202">屬性</span><span class="sxs-lookup"><span data-stu-id="b094b-202">Property</span></span> | <span data-ttu-id="b094b-203">值</span><span class="sxs-lookup"><span data-stu-id="b094b-203">Value</span></span> |
|----------|-------|
| <span data-ttu-id="b094b-204">TheColor</span><span class="sxs-lookup"><span data-stu-id="b094b-204">TheColor</span></span> | <span data-ttu-id="b094b-205">藍色</span><span class="sxs-lookup"><span data-stu-id="b094b-205">Blue</span></span>  |



 

[<span data-ttu-id="b094b-206">ControlCondition 資料表</span><span class="sxs-lookup"><span data-stu-id="b094b-206">ControlCondition table</span></span>](controlcondition-table.md)



| <span data-ttu-id="b094b-207">對話\_</span><span class="sxs-lookup"><span data-stu-id="b094b-207">Dialog\_</span></span> | <span data-ttu-id="b094b-208">控制項\_</span><span class="sxs-lookup"><span data-stu-id="b094b-208">Control\_</span></span>  | <span data-ttu-id="b094b-209">動作</span><span class="sxs-lookup"><span data-stu-id="b094b-209">Action</span></span> | <span data-ttu-id="b094b-210">條件</span><span class="sxs-lookup"><span data-stu-id="b094b-210">Condition</span></span>                 |
|----------|------------|--------|---------------------------|
| <span data-ttu-id="b094b-211">MySample</span><span class="sxs-lookup"><span data-stu-id="b094b-211">MySample</span></span> | <span data-ttu-id="b094b-212">HowIsBlue</span><span class="sxs-lookup"><span data-stu-id="b094b-212">HowIsBlue</span></span>  | <span data-ttu-id="b094b-213">隱藏</span><span class="sxs-lookup"><span data-stu-id="b094b-213">Hide</span></span>   | <span data-ttu-id="b094b-214">TheColor <>  "Blue"</span><span class="sxs-lookup"><span data-stu-id="b094b-214">TheColor <> "Blue"</span></span>  |
| <span data-ttu-id="b094b-215">MySample</span><span class="sxs-lookup"><span data-stu-id="b094b-215">MySample</span></span> | <span data-ttu-id="b094b-216">HowIsBlue</span><span class="sxs-lookup"><span data-stu-id="b094b-216">HowIsBlue</span></span>  | <span data-ttu-id="b094b-217">顯示</span><span class="sxs-lookup"><span data-stu-id="b094b-217">Show</span></span>   | <span data-ttu-id="b094b-218">TheColor = "Blue"</span><span class="sxs-lookup"><span data-stu-id="b094b-218">TheColor = "Blue"</span></span>         |
| <span data-ttu-id="b094b-219">MySample</span><span class="sxs-lookup"><span data-stu-id="b094b-219">MySample</span></span> | <span data-ttu-id="b094b-220">HowIsGreen</span><span class="sxs-lookup"><span data-stu-id="b094b-220">HowIsGreen</span></span> | <span data-ttu-id="b094b-221">隱藏</span><span class="sxs-lookup"><span data-stu-id="b094b-221">Hide</span></span>   | <span data-ttu-id="b094b-222">TheColor <>  "綠"</span><span class="sxs-lookup"><span data-stu-id="b094b-222">TheColor <> "Green"</span></span> |
| <span data-ttu-id="b094b-223">MySample</span><span class="sxs-lookup"><span data-stu-id="b094b-223">MySample</span></span> | <span data-ttu-id="b094b-224">HowIsGreen</span><span class="sxs-lookup"><span data-stu-id="b094b-224">HowIsGreen</span></span> | <span data-ttu-id="b094b-225">顯示</span><span class="sxs-lookup"><span data-stu-id="b094b-225">Show</span></span>   | <span data-ttu-id="b094b-226">TheColor = "綠"</span><span class="sxs-lookup"><span data-stu-id="b094b-226">TheColor = "Green"</span></span>        |



 

<span data-ttu-id="b094b-227">如需詳細資訊，請參閱 [協助工具](accessibility.md)。</span><span class="sxs-lookup"><span data-stu-id="b094b-227">For more information, see [Accessibility](accessibility.md).</span></span>

 

 



