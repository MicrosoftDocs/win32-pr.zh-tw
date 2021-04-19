---
title: Player. KeyDown 事件
description: 按下按鍵時，就會發生 KeyDown 事件。 |Player. KeyDown 事件
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- KeyDown 事件 Windows Media Player
- KeyDown 事件 Windows Media Player、Player 類別
- Player 類別 Windows Media Player，KeyDown 事件
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226430421977a58eca02b7a42cf0349f2a5ff520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991177"
---
# <a name="playerkeydown-event"></a><span data-ttu-id="0afe1-107">Player. KeyDown 事件</span><span class="sxs-lookup"><span data-stu-id="0afe1-107">Player.KeyDown event</span></span>

<span data-ttu-id="0afe1-108">按下按鍵時，就會發生 **KeyDown** 事件。</span><span class="sxs-lookup"><span data-stu-id="0afe1-108">The **KeyDown** event occurs when a key is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0afe1-109">語法</span><span class="sxs-lookup"><span data-stu-id="0afe1-109">Syntax</span></span>


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="0afe1-110">參數</span><span class="sxs-lookup"><span data-stu-id="0afe1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0afe1-111">*nKeyCode*</span><span class="sxs-lookup"><span data-stu-id="0afe1-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="0afe1-112"> (**int**) 指定按下哪個實體索引鍵的 **數目**。</span><span class="sxs-lookup"><span data-stu-id="0afe1-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="0afe1-113">如需了解可能的值，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="0afe1-113">For possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="0afe1-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="0afe1-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="0afe1-115">**Number** (**int**) 指定具有最少有效位數的位位（對應至 SHIFT 鍵 (BIT 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) ）。</span><span class="sxs-lookup"><span data-stu-id="0afe1-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="0afe1-116">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="0afe1-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="0afe1-117">Shift 引數表示這些索引鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="0afe1-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="0afe1-118">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="0afe1-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0afe1-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="0afe1-119">Return value</span></span>

<span data-ttu-id="0afe1-120">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0afe1-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0afe1-121">備註</span><span class="sxs-lookup"><span data-stu-id="0afe1-121">Remarks</span></span>

<span data-ttu-id="0afe1-122">*NKeyCode* 引數會指定實體索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0afe1-122">The *nKeyCode* argument specifies a physical key.</span></span> <span data-ttu-id="0afe1-123">下表顯示標準鍵盤上主要索引鍵的可能值。</span><span class="sxs-lookup"><span data-stu-id="0afe1-123">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="0afe1-124">主要索引鍵的值。</span><span class="sxs-lookup"><span data-stu-id="0afe1-124">Values for the main keys.</span></span>



| <span data-ttu-id="0afe1-125">Key</span><span class="sxs-lookup"><span data-stu-id="0afe1-125">Key</span></span>                     | <span data-ttu-id="0afe1-126">值</span><span class="sxs-lookup"><span data-stu-id="0afe1-126">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="0afe1-127">A-Z</span><span class="sxs-lookup"><span data-stu-id="0afe1-127">A-Z</span></span>                     | <span data-ttu-id="0afe1-128">65-90</span><span class="sxs-lookup"><span data-stu-id="0afe1-128">65-90</span></span>   |
| <span data-ttu-id="0afe1-129">0-9</span><span class="sxs-lookup"><span data-stu-id="0afe1-129">0-9</span></span>                     | <span data-ttu-id="0afe1-130">48-56</span><span class="sxs-lookup"><span data-stu-id="0afe1-130">48-56</span></span>   |
| <span data-ttu-id="0afe1-131">F1-F12</span><span class="sxs-lookup"><span data-stu-id="0afe1-131">F1-F12</span></span>                  | <span data-ttu-id="0afe1-132">112-123</span><span class="sxs-lookup"><span data-stu-id="0afe1-132">112-123</span></span> |
| <span data-ttu-id="0afe1-133">ESC</span><span class="sxs-lookup"><span data-stu-id="0afe1-133">ESC</span></span>                     | <span data-ttu-id="0afe1-134">27</span><span class="sxs-lookup"><span data-stu-id="0afe1-134">27</span></span>      |
| <span data-ttu-id="0afe1-135">TAB</span><span class="sxs-lookup"><span data-stu-id="0afe1-135">TAB</span></span>                     | <span data-ttu-id="0afe1-136">9</span><span class="sxs-lookup"><span data-stu-id="0afe1-136">9</span></span>       |
| <span data-ttu-id="0afe1-137">CAPS LOCK</span><span class="sxs-lookup"><span data-stu-id="0afe1-137">CAPS LOCK</span></span>               | <span data-ttu-id="0afe1-138">20</span><span class="sxs-lookup"><span data-stu-id="0afe1-138">20</span></span>      |
| <span data-ttu-id="0afe1-139">向左或向右移動 () </span><span class="sxs-lookup"><span data-stu-id="0afe1-139">SHIFT (left or right)</span></span>   | <span data-ttu-id="0afe1-140">16</span><span class="sxs-lookup"><span data-stu-id="0afe1-140">16</span></span>      |
| <span data-ttu-id="0afe1-141">CTRL (左或右) </span><span class="sxs-lookup"><span data-stu-id="0afe1-141">CTRL (left or right)</span></span>    | <span data-ttu-id="0afe1-142">17</span><span class="sxs-lookup"><span data-stu-id="0afe1-142">17</span></span>      |
| <span data-ttu-id="0afe1-143">ALT (左或右) </span><span class="sxs-lookup"><span data-stu-id="0afe1-143">ALT (left or right)</span></span>     | <span data-ttu-id="0afe1-144">18</span><span class="sxs-lookup"><span data-stu-id="0afe1-144">18</span></span>      |
| <span data-ttu-id="0afe1-145">SPACE</span><span class="sxs-lookup"><span data-stu-id="0afe1-145">SPACE</span></span>                   | <span data-ttu-id="0afe1-146">32</span><span class="sxs-lookup"><span data-stu-id="0afe1-146">32</span></span>      |
| <span data-ttu-id="0afe1-147">退格鍵</span><span class="sxs-lookup"><span data-stu-id="0afe1-147">BACKSPACE</span></span>               | <span data-ttu-id="0afe1-148">8</span><span class="sxs-lookup"><span data-stu-id="0afe1-148">8</span></span>       |
| <span data-ttu-id="0afe1-149">ENTER</span><span class="sxs-lookup"><span data-stu-id="0afe1-149">ENTER</span></span>                   | <span data-ttu-id="0afe1-150">13</span><span class="sxs-lookup"><span data-stu-id="0afe1-150">13</span></span>      |
| <span data-ttu-id="0afe1-151">Windows 標誌鍵，左方</span><span class="sxs-lookup"><span data-stu-id="0afe1-151">Windows logo key, left</span></span>  | <span data-ttu-id="0afe1-152">91</span><span class="sxs-lookup"><span data-stu-id="0afe1-152">91</span></span>      |
| <span data-ttu-id="0afe1-153">Windows 標誌鍵，right</span><span class="sxs-lookup"><span data-stu-id="0afe1-153">Windows logo key, right</span></span> | <span data-ttu-id="0afe1-154">92</span><span class="sxs-lookup"><span data-stu-id="0afe1-154">92</span></span>      |
| <span data-ttu-id="0afe1-155">應用程式金鑰</span><span class="sxs-lookup"><span data-stu-id="0afe1-155">Application key</span></span>         | <span data-ttu-id="0afe1-156">93</span><span class="sxs-lookup"><span data-stu-id="0afe1-156">93</span></span>      |



 

<span data-ttu-id="0afe1-157">數位板索引鍵的值。</span><span class="sxs-lookup"><span data-stu-id="0afe1-157">Values for the number pad keys.</span></span>



| <span data-ttu-id="0afe1-158">Key</span><span class="sxs-lookup"><span data-stu-id="0afe1-158">Key</span></span>               | <span data-ttu-id="0afe1-159">值</span><span class="sxs-lookup"><span data-stu-id="0afe1-159">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="0afe1-160">0-9</span><span class="sxs-lookup"><span data-stu-id="0afe1-160">0-9</span></span>               | <span data-ttu-id="0afe1-161">96-105</span><span class="sxs-lookup"><span data-stu-id="0afe1-161">96-105</span></span> |
| <span data-ttu-id="0afe1-162">NUM LOCK</span><span class="sxs-lookup"><span data-stu-id="0afe1-162">NUM LOCK</span></span>          | <span data-ttu-id="0afe1-163">144</span><span class="sxs-lookup"><span data-stu-id="0afe1-163">144</span></span>    |
| <span data-ttu-id="0afe1-164">除以 (/) </span><span class="sxs-lookup"><span data-stu-id="0afe1-164">DIVIDE (/)</span></span>        | <span data-ttu-id="0afe1-165">111</span><span class="sxs-lookup"><span data-stu-id="0afe1-165">111</span></span>    |
| <span data-ttu-id="0afe1-166">將 (乘以 \*) </span><span class="sxs-lookup"><span data-stu-id="0afe1-166">MULTIPLY (\*)</span></span>     | <span data-ttu-id="0afe1-167">106</span><span class="sxs-lookup"><span data-stu-id="0afe1-167">106</span></span>    |
| <span data-ttu-id="0afe1-168">減去 (-) </span><span class="sxs-lookup"><span data-stu-id="0afe1-168">SUBTRACT (-)</span></span>      | <span data-ttu-id="0afe1-169">109</span><span class="sxs-lookup"><span data-stu-id="0afe1-169">109</span></span>    |
| <span data-ttu-id="0afe1-170">新增 (+) </span><span class="sxs-lookup"><span data-stu-id="0afe1-170">ADD (+)</span></span>           | <span data-ttu-id="0afe1-171">107</span><span class="sxs-lookup"><span data-stu-id="0afe1-171">107</span></span>    |
| <span data-ttu-id="0afe1-172"> (輸入) 的分隔符號</span><span class="sxs-lookup"><span data-stu-id="0afe1-172">SEPARATOR (Enter)</span></span> | <span data-ttu-id="0afe1-173">108</span><span class="sxs-lookup"><span data-stu-id="0afe1-173">108</span></span>    |
| <span data-ttu-id="0afe1-174">DECIMAL (。 ) </span><span class="sxs-lookup"><span data-stu-id="0afe1-174">DECIMAL (.)</span></span>       | <span data-ttu-id="0afe1-175">110</span><span class="sxs-lookup"><span data-stu-id="0afe1-175">110</span></span>    |



 

<span data-ttu-id="0afe1-176">導覽鍵的值。</span><span class="sxs-lookup"><span data-stu-id="0afe1-176">Values for the navigation keys.</span></span>



| <span data-ttu-id="0afe1-177">Key</span><span class="sxs-lookup"><span data-stu-id="0afe1-177">Key</span></span>         | <span data-ttu-id="0afe1-178">值</span><span class="sxs-lookup"><span data-stu-id="0afe1-178">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="0afe1-179">Insert</span><span class="sxs-lookup"><span data-stu-id="0afe1-179">INSERT</span></span>      | <span data-ttu-id="0afe1-180">45</span><span class="sxs-lookup"><span data-stu-id="0afe1-180">45</span></span>    |
| <span data-ttu-id="0afe1-181">刪除</span><span class="sxs-lookup"><span data-stu-id="0afe1-181">DELETE</span></span>      | <span data-ttu-id="0afe1-182">46</span><span class="sxs-lookup"><span data-stu-id="0afe1-182">46</span></span>    |
| <span data-ttu-id="0afe1-183">HOME</span><span class="sxs-lookup"><span data-stu-id="0afe1-183">HOME</span></span>        | <span data-ttu-id="0afe1-184">36</span><span class="sxs-lookup"><span data-stu-id="0afe1-184">36</span></span>    |
| <span data-ttu-id="0afe1-185">END</span><span class="sxs-lookup"><span data-stu-id="0afe1-185">END</span></span>         | <span data-ttu-id="0afe1-186">35</span><span class="sxs-lookup"><span data-stu-id="0afe1-186">35</span></span>    |
| <span data-ttu-id="0afe1-187">PAGE UP</span><span class="sxs-lookup"><span data-stu-id="0afe1-187">PAGE UP</span></span>     | <span data-ttu-id="0afe1-188">33</span><span class="sxs-lookup"><span data-stu-id="0afe1-188">33</span></span>    |
| <span data-ttu-id="0afe1-189">PAGE DOWN</span><span class="sxs-lookup"><span data-stu-id="0afe1-189">PAGE DOWN</span></span>   | <span data-ttu-id="0afe1-190">34</span><span class="sxs-lookup"><span data-stu-id="0afe1-190">34</span></span>    |
| <span data-ttu-id="0afe1-191">向上鍵</span><span class="sxs-lookup"><span data-stu-id="0afe1-191">UP ARROW</span></span>    | <span data-ttu-id="0afe1-192">38</span><span class="sxs-lookup"><span data-stu-id="0afe1-192">38</span></span>    |
| <span data-ttu-id="0afe1-193">DOWN ARROW</span><span class="sxs-lookup"><span data-stu-id="0afe1-193">DOWN ARROW</span></span>  | <span data-ttu-id="0afe1-194">40</span><span class="sxs-lookup"><span data-stu-id="0afe1-194">40</span></span>    |
| <span data-ttu-id="0afe1-195">向左鍵</span><span class="sxs-lookup"><span data-stu-id="0afe1-195">LEFT ARROW</span></span>  | <span data-ttu-id="0afe1-196">37</span><span class="sxs-lookup"><span data-stu-id="0afe1-196">37</span></span>    |
| <span data-ttu-id="0afe1-197">向右鍵</span><span class="sxs-lookup"><span data-stu-id="0afe1-197">RIGHT ARROW</span></span> | <span data-ttu-id="0afe1-198">39</span><span class="sxs-lookup"><span data-stu-id="0afe1-198">39</span></span>    |



 

<span data-ttu-id="0afe1-199">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="0afe1-199">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="0afe1-200">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="0afe1-200">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="0afe1-201">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0afe1-201">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0afe1-202">規格需求</span><span class="sxs-lookup"><span data-stu-id="0afe1-202">Requirements</span></span>



| <span data-ttu-id="0afe1-203">需求</span><span class="sxs-lookup"><span data-stu-id="0afe1-203">Requirement</span></span> | <span data-ttu-id="0afe1-204">值</span><span class="sxs-lookup"><span data-stu-id="0afe1-204">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0afe1-205">版本</span><span class="sxs-lookup"><span data-stu-id="0afe1-205">Version</span></span><br/> | <span data-ttu-id="0afe1-206">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="0afe1-206">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="0afe1-207">DLL</span><span class="sxs-lookup"><span data-stu-id="0afe1-207">DLL</span></span><br/>     | <dl> <span data-ttu-id="0afe1-208"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0afe1-208"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0afe1-209">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0afe1-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0afe1-210">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="0afe1-210">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





