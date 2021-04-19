---
title: AxWindowsMediaPlayer 物件的 KeyDown 事件
description: 按下按鍵時，就會發生 KeyDown 事件。 |AxWindowsMediaPlayer 物件的 KeyDown 事件
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- AxWindowsMediaPlayer 物件的 KeyDown 事件 Windows Media Player
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc89814063e1a43badd22e658b5f19ece7abb074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984821"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="6de3d-105">AxWindowsMediaPlayer 物件的 KeyDown 事件</span><span class="sxs-lookup"><span data-stu-id="6de3d-105">KeyDown Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="6de3d-106">按下按鍵時，就會發生 KeyDown 事件。</span><span class="sxs-lookup"><span data-stu-id="6de3d-106">The KeyDown event occurs when a key is pressed.</span></span>

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a><span data-ttu-id="6de3d-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="6de3d-107">Event Data</span></span>

<span data-ttu-id="6de3d-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ KeyDownEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="6de3d-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEventHandler**.</span></span> <span data-ttu-id="6de3d-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ KeyDownEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="6de3d-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="6de3d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6de3d-110">Property</span></span>    | <span data-ttu-id="6de3d-111">描述</span><span class="sxs-lookup"><span data-stu-id="6de3d-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de3d-112">nKeyCode</span><span class="sxs-lookup"><span data-stu-id="6de3d-112">nKeyCode</span></span>    | <span data-ttu-id="6de3d-113">Int16Specifies 已按下的實體索引鍵。</span><span class="sxs-lookup"><span data-stu-id="6de3d-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="6de3d-114">如需可能的值，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="6de3d-114">For possible values, see Remarks.</span></span><br/>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6de3d-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="6de3d-115">nShiftState</span></span> | <span data-ttu-id="6de3d-116">Int16A 位，具有與 SHIFT 鍵對應的最不重要位 (位 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) 。</span><span class="sxs-lookup"><span data-stu-id="6de3d-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="6de3d-117">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="6de3d-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="6de3d-118">Shift 引數表示這些索引鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="6de3d-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="6de3d-119">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="6de3d-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6de3d-120">備註</span><span class="sxs-lookup"><span data-stu-id="6de3d-120">Remarks</span></span>

<span data-ttu-id="6de3d-121">**NKeyCode** 屬性會指定實體索引鍵。</span><span class="sxs-lookup"><span data-stu-id="6de3d-121">The **nKeyCode** property specifies a physical key.</span></span> <span data-ttu-id="6de3d-122">下表顯示標準鍵盤上主要索引鍵的可能值。</span><span class="sxs-lookup"><span data-stu-id="6de3d-122">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="6de3d-123">主要索引鍵的值。</span><span class="sxs-lookup"><span data-stu-id="6de3d-123">Values for the main keys.</span></span>



| <span data-ttu-id="6de3d-124">Key</span><span class="sxs-lookup"><span data-stu-id="6de3d-124">Key</span></span>                     | <span data-ttu-id="6de3d-125">值</span><span class="sxs-lookup"><span data-stu-id="6de3d-125">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="6de3d-126">A-Z</span><span class="sxs-lookup"><span data-stu-id="6de3d-126">A-Z</span></span>                     | <span data-ttu-id="6de3d-127">65-90</span><span class="sxs-lookup"><span data-stu-id="6de3d-127">65-90</span></span>   |
| <span data-ttu-id="6de3d-128">0-9</span><span class="sxs-lookup"><span data-stu-id="6de3d-128">0-9</span></span>                     | <span data-ttu-id="6de3d-129">48-56</span><span class="sxs-lookup"><span data-stu-id="6de3d-129">48-56</span></span>   |
| <span data-ttu-id="6de3d-130">F1-F12</span><span class="sxs-lookup"><span data-stu-id="6de3d-130">F1-F12</span></span>                  | <span data-ttu-id="6de3d-131">112-123</span><span class="sxs-lookup"><span data-stu-id="6de3d-131">112-123</span></span> |
| <span data-ttu-id="6de3d-132">ESC</span><span class="sxs-lookup"><span data-stu-id="6de3d-132">ESC</span></span>                     | <span data-ttu-id="6de3d-133">27</span><span class="sxs-lookup"><span data-stu-id="6de3d-133">27</span></span>      |
| <span data-ttu-id="6de3d-134">TAB</span><span class="sxs-lookup"><span data-stu-id="6de3d-134">TAB</span></span>                     | <span data-ttu-id="6de3d-135">9</span><span class="sxs-lookup"><span data-stu-id="6de3d-135">9</span></span>       |
| <span data-ttu-id="6de3d-136">CAPS LOCK</span><span class="sxs-lookup"><span data-stu-id="6de3d-136">CAPS LOCK</span></span>               | <span data-ttu-id="6de3d-137">20</span><span class="sxs-lookup"><span data-stu-id="6de3d-137">20</span></span>      |
| <span data-ttu-id="6de3d-138">向左或向右移動 () </span><span class="sxs-lookup"><span data-stu-id="6de3d-138">SHIFT (left or right)</span></span>   | <span data-ttu-id="6de3d-139">16</span><span class="sxs-lookup"><span data-stu-id="6de3d-139">16</span></span>      |
| <span data-ttu-id="6de3d-140">CTRL (左或右) </span><span class="sxs-lookup"><span data-stu-id="6de3d-140">CTRL (left or right)</span></span>    | <span data-ttu-id="6de3d-141">17</span><span class="sxs-lookup"><span data-stu-id="6de3d-141">17</span></span>      |
| <span data-ttu-id="6de3d-142">ALT (左或右) </span><span class="sxs-lookup"><span data-stu-id="6de3d-142">ALT (left or right)</span></span>     | <span data-ttu-id="6de3d-143">18</span><span class="sxs-lookup"><span data-stu-id="6de3d-143">18</span></span>      |
| <span data-ttu-id="6de3d-144">SPACE</span><span class="sxs-lookup"><span data-stu-id="6de3d-144">SPACE</span></span>                   | <span data-ttu-id="6de3d-145">32</span><span class="sxs-lookup"><span data-stu-id="6de3d-145">32</span></span>      |
| <span data-ttu-id="6de3d-146">退格鍵</span><span class="sxs-lookup"><span data-stu-id="6de3d-146">BACKSPACE</span></span>               | <span data-ttu-id="6de3d-147">8</span><span class="sxs-lookup"><span data-stu-id="6de3d-147">8</span></span>       |
| <span data-ttu-id="6de3d-148">ENTER</span><span class="sxs-lookup"><span data-stu-id="6de3d-148">ENTER</span></span>                   | <span data-ttu-id="6de3d-149">13</span><span class="sxs-lookup"><span data-stu-id="6de3d-149">13</span></span>      |
| <span data-ttu-id="6de3d-150">Windows 標誌鍵，左方</span><span class="sxs-lookup"><span data-stu-id="6de3d-150">Windows logo key, left</span></span>  | <span data-ttu-id="6de3d-151">91</span><span class="sxs-lookup"><span data-stu-id="6de3d-151">91</span></span>      |
| <span data-ttu-id="6de3d-152">Windows 標誌鍵，right</span><span class="sxs-lookup"><span data-stu-id="6de3d-152">Windows logo key, right</span></span> | <span data-ttu-id="6de3d-153">92</span><span class="sxs-lookup"><span data-stu-id="6de3d-153">92</span></span>      |
| <span data-ttu-id="6de3d-154">應用程式金鑰</span><span class="sxs-lookup"><span data-stu-id="6de3d-154">Application key</span></span>         | <span data-ttu-id="6de3d-155">93</span><span class="sxs-lookup"><span data-stu-id="6de3d-155">93</span></span>      |



 

<span data-ttu-id="6de3d-156">數位板索引鍵的值。</span><span class="sxs-lookup"><span data-stu-id="6de3d-156">Values for the number pad keys.</span></span>



| <span data-ttu-id="6de3d-157">Key</span><span class="sxs-lookup"><span data-stu-id="6de3d-157">Key</span></span>               | <span data-ttu-id="6de3d-158">值</span><span class="sxs-lookup"><span data-stu-id="6de3d-158">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="6de3d-159">0-9</span><span class="sxs-lookup"><span data-stu-id="6de3d-159">0-9</span></span>               | <span data-ttu-id="6de3d-160">96-105</span><span class="sxs-lookup"><span data-stu-id="6de3d-160">96-105</span></span> |
| <span data-ttu-id="6de3d-161">NUM LOCK</span><span class="sxs-lookup"><span data-stu-id="6de3d-161">NUM LOCK</span></span>          | <span data-ttu-id="6de3d-162">144</span><span class="sxs-lookup"><span data-stu-id="6de3d-162">144</span></span>    |
| <span data-ttu-id="6de3d-163">除以 (/) </span><span class="sxs-lookup"><span data-stu-id="6de3d-163">DIVIDE (/)</span></span>        | <span data-ttu-id="6de3d-164">111</span><span class="sxs-lookup"><span data-stu-id="6de3d-164">111</span></span>    |
| <span data-ttu-id="6de3d-165">將 (乘以 \*) </span><span class="sxs-lookup"><span data-stu-id="6de3d-165">MULTIPLY (\*)</span></span>     | <span data-ttu-id="6de3d-166">106</span><span class="sxs-lookup"><span data-stu-id="6de3d-166">106</span></span>    |
| <span data-ttu-id="6de3d-167">減去 (-) </span><span class="sxs-lookup"><span data-stu-id="6de3d-167">SUBTRACT (-)</span></span>      | <span data-ttu-id="6de3d-168">109</span><span class="sxs-lookup"><span data-stu-id="6de3d-168">109</span></span>    |
| <span data-ttu-id="6de3d-169">新增 (+) </span><span class="sxs-lookup"><span data-stu-id="6de3d-169">ADD (+)</span></span>           | <span data-ttu-id="6de3d-170">107</span><span class="sxs-lookup"><span data-stu-id="6de3d-170">107</span></span>    |
| <span data-ttu-id="6de3d-171"> (輸入) 的分隔符號</span><span class="sxs-lookup"><span data-stu-id="6de3d-171">SEPARATOR (Enter)</span></span> | <span data-ttu-id="6de3d-172">108</span><span class="sxs-lookup"><span data-stu-id="6de3d-172">108</span></span>    |
| <span data-ttu-id="6de3d-173">DECIMAL (。 ) </span><span class="sxs-lookup"><span data-stu-id="6de3d-173">DECIMAL (.)</span></span>       | <span data-ttu-id="6de3d-174">110</span><span class="sxs-lookup"><span data-stu-id="6de3d-174">110</span></span>    |



 

<span data-ttu-id="6de3d-175">導覽鍵的值。</span><span class="sxs-lookup"><span data-stu-id="6de3d-175">Values for the navigation keys.</span></span>



| <span data-ttu-id="6de3d-176">Key</span><span class="sxs-lookup"><span data-stu-id="6de3d-176">Key</span></span>         | <span data-ttu-id="6de3d-177">值</span><span class="sxs-lookup"><span data-stu-id="6de3d-177">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="6de3d-178">Insert</span><span class="sxs-lookup"><span data-stu-id="6de3d-178">INSERT</span></span>      | <span data-ttu-id="6de3d-179">45</span><span class="sxs-lookup"><span data-stu-id="6de3d-179">45</span></span>    |
| <span data-ttu-id="6de3d-180">刪除</span><span class="sxs-lookup"><span data-stu-id="6de3d-180">DELETE</span></span>      | <span data-ttu-id="6de3d-181">46</span><span class="sxs-lookup"><span data-stu-id="6de3d-181">46</span></span>    |
| <span data-ttu-id="6de3d-182">HOME</span><span class="sxs-lookup"><span data-stu-id="6de3d-182">HOME</span></span>        | <span data-ttu-id="6de3d-183">36</span><span class="sxs-lookup"><span data-stu-id="6de3d-183">36</span></span>    |
| <span data-ttu-id="6de3d-184">END</span><span class="sxs-lookup"><span data-stu-id="6de3d-184">END</span></span>         | <span data-ttu-id="6de3d-185">35</span><span class="sxs-lookup"><span data-stu-id="6de3d-185">35</span></span>    |
| <span data-ttu-id="6de3d-186">PAGE UP</span><span class="sxs-lookup"><span data-stu-id="6de3d-186">PAGE UP</span></span>     | <span data-ttu-id="6de3d-187">33</span><span class="sxs-lookup"><span data-stu-id="6de3d-187">33</span></span>    |
| <span data-ttu-id="6de3d-188">PAGE DOWN</span><span class="sxs-lookup"><span data-stu-id="6de3d-188">PAGE DOWN</span></span>   | <span data-ttu-id="6de3d-189">34</span><span class="sxs-lookup"><span data-stu-id="6de3d-189">34</span></span>    |
| <span data-ttu-id="6de3d-190">向上鍵</span><span class="sxs-lookup"><span data-stu-id="6de3d-190">UP ARROW</span></span>    | <span data-ttu-id="6de3d-191">38</span><span class="sxs-lookup"><span data-stu-id="6de3d-191">38</span></span>    |
| <span data-ttu-id="6de3d-192">DOWN ARROW</span><span class="sxs-lookup"><span data-stu-id="6de3d-192">DOWN ARROW</span></span>  | <span data-ttu-id="6de3d-193">40</span><span class="sxs-lookup"><span data-stu-id="6de3d-193">40</span></span>    |
| <span data-ttu-id="6de3d-194">向左鍵</span><span class="sxs-lookup"><span data-stu-id="6de3d-194">LEFT ARROW</span></span>  | <span data-ttu-id="6de3d-195">37</span><span class="sxs-lookup"><span data-stu-id="6de3d-195">37</span></span>    |
| <span data-ttu-id="6de3d-196">向右鍵</span><span class="sxs-lookup"><span data-stu-id="6de3d-196">RIGHT ARROW</span></span> | <span data-ttu-id="6de3d-197">39</span><span class="sxs-lookup"><span data-stu-id="6de3d-197">39</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="6de3d-198">規格需求</span><span class="sxs-lookup"><span data-stu-id="6de3d-198">Requirements</span></span>



| <span data-ttu-id="6de3d-199">需求</span><span class="sxs-lookup"><span data-stu-id="6de3d-199">Requirement</span></span> | <span data-ttu-id="6de3d-200">值</span><span class="sxs-lookup"><span data-stu-id="6de3d-200">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de3d-201">版本</span><span class="sxs-lookup"><span data-stu-id="6de3d-201">Version</span></span><br/>   | <span data-ttu-id="6de3d-202">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="6de3d-202">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="6de3d-203">命名空間</span><span class="sxs-lookup"><span data-stu-id="6de3d-203">Namespace</span></span><br/> | <span data-ttu-id="6de3d-204">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="6de3d-204">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="6de3d-205">組件</span><span class="sxs-lookup"><span data-stu-id="6de3d-205">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6de3d-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="6de3d-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de3d-207">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6de3d-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de3d-208">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6de3d-208">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





