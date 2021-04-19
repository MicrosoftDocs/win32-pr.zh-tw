---
description: ICE34 會驗證每個 RadioButtonGroup 控制項上的每個選項按鈕，在選項按鈕資料表的屬性資料行中都有一個屬性，該屬性會指定其選項按鈕群組。
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979901"
---
# <a name="ice34"></a><span data-ttu-id="34989-103">ICE34</span><span class="sxs-lookup"><span data-stu-id="34989-103">ICE34</span></span>

<span data-ttu-id="34989-104">ICE34 會驗證每個 [RadioButtonGroup 控制項](radiobuttongroup-control.md) 上的每個選項按鈕，在選項按鈕 [資料表](radiobutton-table.md) 的屬性資料行中都有一個屬性，該屬性會指定其選項按鈕群組。</span><span class="sxs-lookup"><span data-stu-id="34989-104">ICE34 validates that each radio button on every [RadioButtonGroup Control](radiobuttongroup-control.md) has a property in the Property column of the [RadioButton table](radiobutton-table.md) that specifies its radio button group.</span></span> <span data-ttu-id="34989-105">ICE34 會驗證這個屬性是否存在，並設定為 [屬性工作表](property-table.md) 中的預設值，此值等於選項按鈕資料表之 [值] 資料行中的其中一個群組選項按鈕值。</span><span class="sxs-lookup"><span data-stu-id="34989-105">ICE34 validates that this property exists and is set to a default value in the [Property table](property-table.md) which is equal to one of the group's radio button values in the Value column of the RadioButton table.</span></span>

<span data-ttu-id="34989-106">選項按鈕群組必須有預設值，使用者才能使用 TAB 鍵來選取選擇。</span><span class="sxs-lookup"><span data-stu-id="34989-106">A radio button group must have a default for users to be able to select a choice using the TAB key.</span></span> <span data-ttu-id="34989-107">這是適當的使用者協助工具所需的。</span><span class="sxs-lookup"><span data-stu-id="34989-107">This is required for proper user accessibility.</span></span>

<span data-ttu-id="34989-108">ICE34 報告遺漏的資料表。</span><span class="sxs-lookup"><span data-stu-id="34989-108">ICE34 reports missing tables.</span></span>

## <a name="result"></a><span data-ttu-id="34989-109">結果</span><span class="sxs-lookup"><span data-stu-id="34989-109">Result</span></span>

<span data-ttu-id="34989-110">如果有指定無效屬性的選項按鈕，ICE34 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="34989-110">ICE34 post an error message if there is a radio button that specifies an invalid property.</span></span>

## <a name="example"></a><span data-ttu-id="34989-111">範例</span><span class="sxs-lookup"><span data-stu-id="34989-111">Example</span></span>

<span data-ttu-id="34989-112">ICE34 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="34989-112">ICE34 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="34989-113">ICE34 錯誤</span><span class="sxs-lookup"><span data-stu-id="34989-113">ICE34 error</span></span>                                                                                                                                                                | <span data-ttu-id="34989-114">Description</span><span class="sxs-lookup"><span data-stu-id="34989-114">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34989-115">控制項 DialogA。 Control2 必須有屬性，因為它的類型是 RadioButtonGroup。</span><span class="sxs-lookup"><span data-stu-id="34989-115">Control DialogA.Control2 must have a property because it is of type RadioButtonGroup.</span></span>                                                                                      | <span data-ttu-id="34989-116">有一個[RadioButtonGroup 控制項](radiobuttongroup-control.md)，沒有在[控制資料表](control-table.md)的 [屬性] 資料行中設定[間接控制](indirect-control-attribute.md)位，而且沒有在 [屬性] 資料行中列出屬性。</span><span class="sxs-lookup"><span data-stu-id="34989-116">There is a [RadioButtonGroup control](radiobuttongroup-control.md), without the [Indirect control](indirect-control-attribute.md) bit set in the Attributes column of the [Control table](control-table.md), that does not have a property listed in the Property column.</span></span> |
| <span data-ttu-id="34989-117">可能不是使用屬性 Property3 之 RadioButtonGroup 的有效預設值。</span><span class="sxs-lookup"><span data-stu-id="34989-117">Maybe is not a valid default value for the RadioButtonGroup using property Property3.</span></span> <span data-ttu-id="34989-118">值必須列為 RadioButtonGroup 資料表中的選項。</span><span class="sxs-lookup"><span data-stu-id="34989-118">The value must be listed as an option in the RadioButtonGroup table.</span></span>                 | <span data-ttu-id="34989-119">在 [屬性工作表](property-table.md) 的 [值] 資料行中指定的屬性預設值，不是 [選項按鈕] [資料表](radiobutton-table.md)的 [值] 資料行中所指定之選項按鈕群組的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="34989-119">There is a default value for a property specified in the Value column of the [Property table](property-table.md) that is not one of the values for the radio button group specified in the Value column of the [RadioButton table](radiobutton-table.md).</span></span>                  |
| <span data-ttu-id="34989-120">必須定義屬性 PropertyB，因為它是 RadioButtonGroup 控制項 DialogA 的間接屬性。 Control4</span><span class="sxs-lookup"><span data-stu-id="34989-120">Property PropertyB must be defined because it is an indirect property of a RadioButtonGroup control DialogA.Control4</span></span>                                                       | <span data-ttu-id="34989-121">這個選項按鈕群組參考的屬性是間接屬性，而間接屬性的值不是選項按鈕群組的其中一個選項。</span><span class="sxs-lookup"><span data-stu-id="34989-121">The property referenced by this RadioButton group is an indirect property, and the value of the indirect property is not one of the choices for the RadioButton group.</span></span>                                                                                                       |
| <span data-ttu-id="34989-122">可能不是屬性 PropertyA 的有效預設值。</span><span class="sxs-lookup"><span data-stu-id="34989-122">Maybe is not a valid default value for the property PropertyA.</span></span> <span data-ttu-id="34989-123">屬性是控制項 DialogA. Control5 (的間接 RadioButtonGroup 屬性（透過屬性 Property5) ）。</span><span class="sxs-lookup"><span data-stu-id="34989-123">The property is an indirect RadioButtonGroup property of control DialogA.Control5 (via property Property5).</span></span> | <span data-ttu-id="34989-124">透過控制項參考的間接屬性值不是該 RadioButtonGroup 的其中一個預設值。</span><span class="sxs-lookup"><span data-stu-id="34989-124">The value of the indirect property referenced via the control is not one of the default values for that RadioButtonGroup.</span></span>                                                                                                                                                    |



 

<span data-ttu-id="34989-125">[控制資料表](control-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="34989-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="34989-126">對話</span><span class="sxs-lookup"><span data-stu-id="34989-126">Dialog</span></span>  | <span data-ttu-id="34989-127">控制</span><span class="sxs-lookup"><span data-stu-id="34989-127">Control</span></span>  | <span data-ttu-id="34989-128">類型</span><span class="sxs-lookup"><span data-stu-id="34989-128">Type</span></span>             | <span data-ttu-id="34989-129">屬性</span><span class="sxs-lookup"><span data-stu-id="34989-129">Attributes</span></span> | <span data-ttu-id="34989-130">屬性</span><span class="sxs-lookup"><span data-stu-id="34989-130">Property</span></span>  |
|---------|----------|------------------|------------|-----------|
| <span data-ttu-id="34989-131">DialogA</span><span class="sxs-lookup"><span data-stu-id="34989-131">DialogA</span></span> | <span data-ttu-id="34989-132">Control1</span><span class="sxs-lookup"><span data-stu-id="34989-132">Control1</span></span> | <span data-ttu-id="34989-133">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="34989-133">RadioButtonGroup</span></span> | <span data-ttu-id="34989-134">0</span><span class="sxs-lookup"><span data-stu-id="34989-134">0</span></span>          | <span data-ttu-id="34989-135">Property1</span><span class="sxs-lookup"><span data-stu-id="34989-135">Property1</span></span> |
| <span data-ttu-id="34989-136">DialogA</span><span class="sxs-lookup"><span data-stu-id="34989-136">DialogA</span></span> | <span data-ttu-id="34989-137">Control2</span><span class="sxs-lookup"><span data-stu-id="34989-137">Control2</span></span> | <span data-ttu-id="34989-138">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="34989-138">RadioButtonGroup</span></span> | <span data-ttu-id="34989-139">0</span><span class="sxs-lookup"><span data-stu-id="34989-139">0</span></span>          |           |
| <span data-ttu-id="34989-140">DialogA</span><span class="sxs-lookup"><span data-stu-id="34989-140">DialogA</span></span> | <span data-ttu-id="34989-141">Control3</span><span class="sxs-lookup"><span data-stu-id="34989-141">Control3</span></span> | <span data-ttu-id="34989-142">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="34989-142">RadioButtonGroup</span></span> | <span data-ttu-id="34989-143">0</span><span class="sxs-lookup"><span data-stu-id="34989-143">0</span></span>          | <span data-ttu-id="34989-144">Property3</span><span class="sxs-lookup"><span data-stu-id="34989-144">Property3</span></span> |
| <span data-ttu-id="34989-145">DialogA</span><span class="sxs-lookup"><span data-stu-id="34989-145">DialogA</span></span> | <span data-ttu-id="34989-146">Control4</span><span class="sxs-lookup"><span data-stu-id="34989-146">Control4</span></span> | <span data-ttu-id="34989-147">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="34989-147">RadioButtonGroup</span></span> | <span data-ttu-id="34989-148">8</span><span class="sxs-lookup"><span data-stu-id="34989-148">8</span></span>          | <span data-ttu-id="34989-149">Property4</span><span class="sxs-lookup"><span data-stu-id="34989-149">Property4</span></span> |
| <span data-ttu-id="34989-150">DialogA</span><span class="sxs-lookup"><span data-stu-id="34989-150">DialogA</span></span> | <span data-ttu-id="34989-151">Control5</span><span class="sxs-lookup"><span data-stu-id="34989-151">Control5</span></span> | <span data-ttu-id="34989-152">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="34989-152">RadioButtonGroup</span></span> | <span data-ttu-id="34989-153">8</span><span class="sxs-lookup"><span data-stu-id="34989-153">8</span></span>          | <span data-ttu-id="34989-154">Property5</span><span class="sxs-lookup"><span data-stu-id="34989-154">Property5</span></span> |



 

<span data-ttu-id="34989-155">[屬性工作表](property-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="34989-155">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="34989-156">屬性</span><span class="sxs-lookup"><span data-stu-id="34989-156">Property</span></span>  | <span data-ttu-id="34989-157">值</span><span class="sxs-lookup"><span data-stu-id="34989-157">Value</span></span>     |
|-----------|-----------|
| <span data-ttu-id="34989-158">Property1</span><span class="sxs-lookup"><span data-stu-id="34989-158">Property1</span></span> | <span data-ttu-id="34989-159">Yes</span><span class="sxs-lookup"><span data-stu-id="34989-159">Yes</span></span>       |
| <span data-ttu-id="34989-160">Property3</span><span class="sxs-lookup"><span data-stu-id="34989-160">Property3</span></span> | <span data-ttu-id="34989-161">可能</span><span class="sxs-lookup"><span data-stu-id="34989-161">Maybe</span></span>     |
| <span data-ttu-id="34989-162">Property4</span><span class="sxs-lookup"><span data-stu-id="34989-162">Property4</span></span> | <span data-ttu-id="34989-163">PropertyB</span><span class="sxs-lookup"><span data-stu-id="34989-163">PropertyB</span></span> |
| <span data-ttu-id="34989-164">Property5</span><span class="sxs-lookup"><span data-stu-id="34989-164">Property5</span></span> | <span data-ttu-id="34989-165">PropertyA</span><span class="sxs-lookup"><span data-stu-id="34989-165">PropertyA</span></span> |
| <span data-ttu-id="34989-166">PropertyA</span><span class="sxs-lookup"><span data-stu-id="34989-166">PropertyA</span></span> | <span data-ttu-id="34989-167">可能</span><span class="sxs-lookup"><span data-stu-id="34989-167">Maybe</span></span>     |



 

<span data-ttu-id="34989-168">[選項按鈕資料表](radiobutton-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="34989-168">[RadioButton Table](radiobutton-table.md) (partial)</span></span>



| <span data-ttu-id="34989-169">屬性</span><span class="sxs-lookup"><span data-stu-id="34989-169">Property</span></span>  | <span data-ttu-id="34989-170">單</span><span class="sxs-lookup"><span data-stu-id="34989-170">Order</span></span> | <span data-ttu-id="34989-171">值</span><span class="sxs-lookup"><span data-stu-id="34989-171">Value</span></span> |
|-----------|-------|-------|
| <span data-ttu-id="34989-172">Property1</span><span class="sxs-lookup"><span data-stu-id="34989-172">Property1</span></span> | <span data-ttu-id="34989-173">1</span><span class="sxs-lookup"><span data-stu-id="34989-173">1</span></span>     | <span data-ttu-id="34989-174">是</span><span class="sxs-lookup"><span data-stu-id="34989-174">Yes</span></span>   |
| <span data-ttu-id="34989-175">Property1</span><span class="sxs-lookup"><span data-stu-id="34989-175">Property1</span></span> | <span data-ttu-id="34989-176">2</span><span class="sxs-lookup"><span data-stu-id="34989-176">2</span></span>     | <span data-ttu-id="34989-177">Now</span><span class="sxs-lookup"><span data-stu-id="34989-177">Now</span></span>   |
| <span data-ttu-id="34989-178">Property2</span><span class="sxs-lookup"><span data-stu-id="34989-178">Property2</span></span> | <span data-ttu-id="34989-179">1</span><span class="sxs-lookup"><span data-stu-id="34989-179">1</span></span>     | <span data-ttu-id="34989-180">是</span><span class="sxs-lookup"><span data-stu-id="34989-180">Yes</span></span>   |
| <span data-ttu-id="34989-181">Property2</span><span class="sxs-lookup"><span data-stu-id="34989-181">Property2</span></span> | <span data-ttu-id="34989-182">2</span><span class="sxs-lookup"><span data-stu-id="34989-182">2</span></span>     | <span data-ttu-id="34989-183">否</span><span class="sxs-lookup"><span data-stu-id="34989-183">No</span></span>    |
| <span data-ttu-id="34989-184">Property3</span><span class="sxs-lookup"><span data-stu-id="34989-184">Property3</span></span> | <span data-ttu-id="34989-185">1</span><span class="sxs-lookup"><span data-stu-id="34989-185">1</span></span>     | <span data-ttu-id="34989-186">是</span><span class="sxs-lookup"><span data-stu-id="34989-186">Yes</span></span>   |
| <span data-ttu-id="34989-187">Property3</span><span class="sxs-lookup"><span data-stu-id="34989-187">Property3</span></span> | <span data-ttu-id="34989-188">2</span><span class="sxs-lookup"><span data-stu-id="34989-188">2</span></span>     | <span data-ttu-id="34989-189">否</span><span class="sxs-lookup"><span data-stu-id="34989-189">No</span></span>    |
| <span data-ttu-id="34989-190">Property4</span><span class="sxs-lookup"><span data-stu-id="34989-190">Property4</span></span> | <span data-ttu-id="34989-191">1</span><span class="sxs-lookup"><span data-stu-id="34989-191">1</span></span>     | <span data-ttu-id="34989-192">是</span><span class="sxs-lookup"><span data-stu-id="34989-192">Yes</span></span>   |
| <span data-ttu-id="34989-193">Property4</span><span class="sxs-lookup"><span data-stu-id="34989-193">Property4</span></span> | <span data-ttu-id="34989-194">2</span><span class="sxs-lookup"><span data-stu-id="34989-194">2</span></span>     | <span data-ttu-id="34989-195">否</span><span class="sxs-lookup"><span data-stu-id="34989-195">No</span></span>    |
| <span data-ttu-id="34989-196">PropertyA</span><span class="sxs-lookup"><span data-stu-id="34989-196">PropertyA</span></span> | <span data-ttu-id="34989-197">1</span><span class="sxs-lookup"><span data-stu-id="34989-197">1</span></span>     | <span data-ttu-id="34989-198">是</span><span class="sxs-lookup"><span data-stu-id="34989-198">Yes</span></span>   |
| <span data-ttu-id="34989-199">PropertyA</span><span class="sxs-lookup"><span data-stu-id="34989-199">PropertyA</span></span> | <span data-ttu-id="34989-200">2</span><span class="sxs-lookup"><span data-stu-id="34989-200">2</span></span>     | <span data-ttu-id="34989-201">否</span><span class="sxs-lookup"><span data-stu-id="34989-201">No</span></span>    |
| <span data-ttu-id="34989-202">PropertyB</span><span class="sxs-lookup"><span data-stu-id="34989-202">PropertyB</span></span> | <span data-ttu-id="34989-203">1</span><span class="sxs-lookup"><span data-stu-id="34989-203">1</span></span>     | <span data-ttu-id="34989-204">是</span><span class="sxs-lookup"><span data-stu-id="34989-204">Yes</span></span>   |
| <span data-ttu-id="34989-205">PropertyB</span><span class="sxs-lookup"><span data-stu-id="34989-205">PropertyB</span></span> | <span data-ttu-id="34989-206">2</span><span class="sxs-lookup"><span data-stu-id="34989-206">2</span></span>     | <span data-ttu-id="34989-207">否</span><span class="sxs-lookup"><span data-stu-id="34989-207">No</span></span>    |



 

<span data-ttu-id="34989-208">若要修正此 ICE 回報的錯誤，請檢查下列各項：</span><span class="sxs-lookup"><span data-stu-id="34989-208">To fix the errors reported by this ICE, check the following:</span></span>

-   <span data-ttu-id="34989-209">沒有間接屬性集的每個選項按鈕控制項專案都有屬性欄中列出的屬性：</span><span class="sxs-lookup"><span data-stu-id="34989-209">That every RadioButton control entry without the indirect attribute set has a property listed in the Property column:</span></span>
-   <span data-ttu-id="34989-210">每個這類屬性在選項按鈕資料表中至少有一個對應的專案。</span><span class="sxs-lookup"><span data-stu-id="34989-210">That every such property has at least one corresponding entry in the RadioButton table.</span></span>
-   <span data-ttu-id="34989-211">每個此類屬性都定義于屬性資料表中，其值為選項按鈕資料表中的其中一個選項。</span><span class="sxs-lookup"><span data-stu-id="34989-211">That every such property is defined in the Property table, with a value that is one of the choices from the RadioButton table.</span></span>
-   <span data-ttu-id="34989-212">在屬性工作表中，會定義在選項按鈕控制項的屬性資料行中所參考的每個屬性（attribute）。</span><span class="sxs-lookup"><span data-stu-id="34989-212">That every property referenced in the Property column of a RadioButton control with the indirect attribute set is defined in the Property table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34989-213">相關主題</span><span class="sxs-lookup"><span data-stu-id="34989-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34989-214">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="34989-214">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



