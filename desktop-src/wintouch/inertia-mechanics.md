---
title: 慣性機制
description: 慣性機制
ms.assetid: 188b6936-b36e-4e57-9118-8b61ed134c17
keywords:
- Windows Touch，慣性
- Windows Touch，平滑動畫
- Windows Touch，彈性邊界
- 慣性，機制
- 慣性，計算基本概念
- 慣性，物理總覽
- 慣性，平滑動畫
- 慣性、彈性邊界
- 平滑動畫
- 彈性邊界
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be79b27900c6921c972710e7e922ab42b834afc1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300360"
---
# <a name="inertia-mechanics"></a><span data-ttu-id="91a2f-113">慣性機制</span><span class="sxs-lookup"><span data-stu-id="91a2f-113">Inertia Mechanics</span></span>

<span data-ttu-id="91a2f-114">慣性可用來執行計算，以製作物件移動的動畫，並在併入 Windows Touch 的應用程式中啟用一般可用性支援。</span><span class="sxs-lookup"><span data-stu-id="91a2f-114">Inertia is used to perform calculations for animating object movement and to enable support for generic usability in applications incorporating Windows Touch.</span></span> <span data-ttu-id="91a2f-115">本節將說明慣性啟用的下列功能。</span><span class="sxs-lookup"><span data-stu-id="91a2f-115">This section illustrates the following features that are enabled by inertia.</span></span>

-   <span data-ttu-id="91a2f-116">慣性物理的簡短總覽。</span><span class="sxs-lookup"><span data-stu-id="91a2f-116">A brief overview of inertia physics.</span></span>
-   <span data-ttu-id="91a2f-117">使用速度與減速屬性來平滑物件動畫。</span><span class="sxs-lookup"><span data-stu-id="91a2f-117">Smooth object animation using the velocity and deceleration properties.</span></span>
-   <span data-ttu-id="91a2f-118">使用置換屬性平滑物件動畫。</span><span class="sxs-lookup"><span data-stu-id="91a2f-118">Smooth object animation using a displacement property.</span></span>
-   <span data-ttu-id="91a2f-119">使用彈性範圍從螢幕邊緣跳動。</span><span class="sxs-lookup"><span data-stu-id="91a2f-119">Bouncing from the screen edges using elastic bounds.</span></span>

## <a name="inertia-physics-overview"></a><span data-ttu-id="91a2f-120">慣性物理總覽</span><span class="sxs-lookup"><span data-stu-id="91a2f-120">Inertia Physics Overview</span></span>

<span data-ttu-id="91a2f-121">慣性處理器會使用簡單的物理模型，其中包含位置、減速值和初始速度。</span><span class="sxs-lookup"><span data-stu-id="91a2f-121">The inertia processor uses a simple physics model that incorporates a position, a deceleration value, and an initial velocity.</span></span> <span data-ttu-id="91a2f-122">時間是用來做為模型的動態輸入，以判斷正在取代之物件的目前位置。</span><span class="sxs-lookup"><span data-stu-id="91a2f-122">Time is used as the dynamic input to the model to determine the current position of an object being displaced.</span></span> <span data-ttu-id="91a2f-123">下圖和公式概述用來計算物件位置的物理模型。</span><span class="sxs-lookup"><span data-stu-id="91a2f-123">The following graph and formula outline the physics model used for calculating object positions.</span></span>

![圖例顯示用來計算物件位置的圖形和公式](images/velocity.png)

<span data-ttu-id="91a2f-125">在用來計算目前位置 (x) 的公式中，初始速度 (v) 會乘以經過的時間 () ，並減少 (d) 次時間平方的最小速度。</span><span class="sxs-lookup"><span data-stu-id="91a2f-125">In the formula used for calculating the current position (x), the initial velocity (v) is multiplied by the time elapsed (t) and is reduced by the deceleration factor (d) times time squared.</span></span> <span data-ttu-id="91a2f-126">這會導致物件的速度變得更順暢。</span><span class="sxs-lookup"><span data-stu-id="91a2f-126">This results in smooth object deceleration.</span></span> <span data-ttu-id="91a2f-127">在上圖中，最左邊的第一個 () 的曲線部分，因為目前的速度是初始速度，所以物件很快就會移動。</span><span class="sxs-lookup"><span data-stu-id="91a2f-127">In the previous illustration at the initial (leftmost) part of the curve, the object is moving quickly because its current velocity is the initial velocity.</span></span> <span data-ttu-id="91a2f-128">在最後的 (最右邊) 部分的曲線，物件已完全停止，因為它的速度是0。</span><span class="sxs-lookup"><span data-stu-id="91a2f-128">At the final (rightmost) part of the curve, the object has completely stopped because its velocity is 0.</span></span> <span data-ttu-id="91a2f-129">X 速度、y 速度和旋轉速度的物件速度計算，全都使用此公式來進行計算。</span><span class="sxs-lookup"><span data-stu-id="91a2f-129">Object velocity calculations for x-velocity, y-velocity, and rotational velocity all use this formula for calculations.</span></span>

<span data-ttu-id="91a2f-130">慣性處理器所使用的所有距離都是相對的。</span><span class="sxs-lookup"><span data-stu-id="91a2f-130">All distance used for the inertia processor is relative.</span></span> <span data-ttu-id="91a2f-131">如果您想要使用螢幕座標，請將螢幕座標傳遞給操作 (或慣性) 處理器;如果您想要使用絕對座標，請將這些座標傳遞到您所使用的處理器。</span><span class="sxs-lookup"><span data-stu-id="91a2f-131">If you want to use screen coordinates, you pass screen coordinates to the manipulation (or inertia) processor; if you want to use absolute coordinates, you pass those into the processor you are using.</span></span> <span data-ttu-id="91a2f-132">無論您使用的值為何，操作處理器都會使用毫秒的時鐘刻度來處理時間。</span><span class="sxs-lookup"><span data-stu-id="91a2f-132">Regardless of the values that you are using, the manipulation processor will use millisecond clock ticks for processing the time.</span></span> <span data-ttu-id="91a2f-133">您可以使用 [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) 方法，或透過呼叫來使用預設的時間 [**戳，將**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)這些值直接傳遞至慣性處理器。</span><span class="sxs-lookup"><span data-stu-id="91a2f-133">These values can either be passed directly to the inertia processor using the [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) method or by using the default timestamp through calls to [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process).</span></span>

## <a name="smooth-object-animation-using-the-velocity-and-deceleration-properties"></a><span data-ttu-id="91a2f-134">使用速度與減速屬性平滑物件動畫</span><span class="sxs-lookup"><span data-stu-id="91a2f-134">Smooth Object Animation using the Velocity and Deceleration Properties</span></span>

<span data-ttu-id="91a2f-135">您可以藉由設定慣性處理器介面中的速度和減速值，然後呼叫 [**進程**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)，來啟用平滑動畫。</span><span class="sxs-lookup"><span data-stu-id="91a2f-135">You can enable smooth animation by directly interacting with the physics model by setting the velocity and deceleration values in the inertia processor interface and then calling [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process).</span></span> <span data-ttu-id="91a2f-136">呼叫 **進程** 將會觸發物件操作，而該操作接著應該會造成 UI 更新。</span><span class="sxs-lookup"><span data-stu-id="91a2f-136">Calling **Process** will trigger object manipulations which in turn should cause UI updates.</span></span> <span data-ttu-id="91a2f-137">傳遞至慣性處理器的物件速度值通常會在完成時從操作處理器取得。</span><span class="sxs-lookup"><span data-stu-id="91a2f-137">Object velocity values passed to the inertia processor are typically taken from the manipulation processor upon completion.</span></span> <span data-ttu-id="91a2f-138">您的減速值會取決於您想要讓物件成為動畫的時間長度，以及您用來計算的單位。</span><span class="sxs-lookup"><span data-stu-id="91a2f-138">Your deceleration value will be dependent on how long you want your object to be animated for and the units that you are using for your calculations.</span></span> <span data-ttu-id="91a2f-139">因為這些值是相依的，有時您必須從 maniplation 處理器調整輸入速度，並使用任意值來因應速度。</span><span class="sxs-lookup"><span data-stu-id="91a2f-139">Because the values are dependent, sometimes you must scale the input velocity from the maniplation processor and use arbitrary values for deceleration.</span></span> <span data-ttu-id="91a2f-140">下列值一般適用于您要將 centipixel 值從 [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) 結構的 x 和 y 屬性傳遞至操作處理器的各種案例。</span><span class="sxs-lookup"><span data-stu-id="91a2f-140">The following values are typical for various scenarios where you are passing centipixel values from the x and y properties of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure to the manipulation processor.</span></span>



| <span data-ttu-id="91a2f-141">狀況</span><span class="sxs-lookup"><span data-stu-id="91a2f-141">Scenario</span></span>    | <span data-ttu-id="91a2f-142">屬性 Set</span><span class="sxs-lookup"><span data-stu-id="91a2f-142">Property Set</span></span>                                                                       | <span data-ttu-id="91a2f-143">減速值</span><span class="sxs-lookup"><span data-stu-id="91a2f-143">Deceleration Value</span></span> | <span data-ttu-id="91a2f-144">典型的速度輸入調整</span><span class="sxs-lookup"><span data-stu-id="91a2f-144">Typical Velocity Input Scaling</span></span>                                  | <span data-ttu-id="91a2f-145">備註</span><span class="sxs-lookup"><span data-stu-id="91a2f-145">Notes</span></span>                                                                                 |
|-------------|------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91a2f-146">翻譯</span><span class="sxs-lookup"><span data-stu-id="91a2f-146">Translation</span></span> | [<span data-ttu-id="91a2f-147">**DesiredDeceleration**</span><span class="sxs-lookup"><span data-stu-id="91a2f-147">**DesiredDeceleration**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | <span data-ttu-id="91a2f-148">0.003 f</span><span class="sxs-lookup"><span data-stu-id="91a2f-148">0.003f</span></span>             | <span data-ttu-id="91a2f-149">無。</span><span class="sxs-lookup"><span data-stu-id="91a2f-149">None.</span></span>                                                           | <span data-ttu-id="91a2f-150">使用此值將會導致使用觸控輸入時的較長距離動畫。</span><span class="sxs-lookup"><span data-stu-id="91a2f-150">Using this value will result in longer distance animations when using touch input.</span></span>    |
| <span data-ttu-id="91a2f-151">翻譯</span><span class="sxs-lookup"><span data-stu-id="91a2f-151">Translation</span></span> | [<span data-ttu-id="91a2f-152">**DesiredDeceleration**</span><span class="sxs-lookup"><span data-stu-id="91a2f-152">**DesiredDeceleration**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | <span data-ttu-id="91a2f-153">0.001 f</span><span class="sxs-lookup"><span data-stu-id="91a2f-153">0.001f</span></span>             | <span data-ttu-id="91a2f-154">1/20 個觸控輸入的初始速度，無滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="91a2f-154">1/20th initial velocity for touch inputs, none for mouse inputs</span></span> | <span data-ttu-id="91a2f-155">使用這個值時，會在第二個指定的一般速度輸入周圍建立動畫。</span><span class="sxs-lookup"><span data-stu-id="91a2f-155">Using this value will animate for around a second given typical velocity inputs.</span></span>      |
| <span data-ttu-id="91a2f-156">翻譯</span><span class="sxs-lookup"><span data-stu-id="91a2f-156">Translation</span></span> | [<span data-ttu-id="91a2f-157">**DesiredDeceleration**</span><span class="sxs-lookup"><span data-stu-id="91a2f-157">**DesiredDeceleration**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | <span data-ttu-id="91a2f-158">0.5 f</span><span class="sxs-lookup"><span data-stu-id="91a2f-158">0.5f</span></span>               | <span data-ttu-id="91a2f-159">無</span><span class="sxs-lookup"><span data-stu-id="91a2f-159">None</span></span>                                                            | <span data-ttu-id="91a2f-160">使用這個值可讓您在大型的 Windows Touch 顯示器上自然覺得動畫。</span><span class="sxs-lookup"><span data-stu-id="91a2f-160">Using this value gives a natural feel to animation on large Windows Touch displays.</span></span>   |
| <span data-ttu-id="91a2f-161">旋轉</span><span class="sxs-lookup"><span data-stu-id="91a2f-161">Rotation</span></span>    | [<span data-ttu-id="91a2f-162">**DesiredAngularDeceleration**</span><span class="sxs-lookup"><span data-stu-id="91a2f-162">**DesiredAngularDeceleration**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | <span data-ttu-id="91a2f-163">0.000015 f</span><span class="sxs-lookup"><span data-stu-id="91a2f-163">0.000015f</span></span>          | <span data-ttu-id="91a2f-164">弧度已轉換為度。</span><span class="sxs-lookup"><span data-stu-id="91a2f-164">Radians converted to degrees.</span></span>                                   | <span data-ttu-id="91a2f-165">使用此值會在使用觸控輸入時產生較長的旋轉動畫。</span><span class="sxs-lookup"><span data-stu-id="91a2f-165">Using this value results in longer rotational animations when using touch input.</span></span>      |
| <span data-ttu-id="91a2f-166">旋轉</span><span class="sxs-lookup"><span data-stu-id="91a2f-166">Rotation</span></span>    | [<span data-ttu-id="91a2f-167">**DesiredAngularDeceleration**</span><span class="sxs-lookup"><span data-stu-id="91a2f-167">**DesiredAngularDeceleration**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | <span data-ttu-id="91a2f-168">0.00001 f</span><span class="sxs-lookup"><span data-stu-id="91a2f-168">0.00001f</span></span>           | <span data-ttu-id="91a2f-169">1/40th 觸控輸入的旋轉差異，無滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="91a2f-169">1/40th rotation delta for touch inputs, none for mouse inputs</span></span>   | <span data-ttu-id="91a2f-170">這個值是以弧度為單位，因此您必須使用極小的減速和速度值。</span><span class="sxs-lookup"><span data-stu-id="91a2f-170">This value is in radians so you must use very small deceleration and velocity values.</span></span> |
| <span data-ttu-id="91a2f-171">旋轉</span><span class="sxs-lookup"><span data-stu-id="91a2f-171">Rotation</span></span>    | [<span data-ttu-id="91a2f-172">**DesiredAngularDeceleration**</span><span class="sxs-lookup"><span data-stu-id="91a2f-172">**DesiredAngularDeceleration**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | <span data-ttu-id="91a2f-173">0.000005 f</span><span class="sxs-lookup"><span data-stu-id="91a2f-173">0.000005f</span></span>          | <span data-ttu-id="91a2f-174">無</span><span class="sxs-lookup"><span data-stu-id="91a2f-174">None</span></span>                                                            | <span data-ttu-id="91a2f-175">此值對於大型的 Windows Touch 顯示有自然的感覺。</span><span class="sxs-lookup"><span data-stu-id="91a2f-175">This value has a natural feel on large Windows Touch displays.</span></span>                        |



 

## <a name="smooth-object-animation-using-the-desired-displacement-property"></a><span data-ttu-id="91a2f-176">使用所需的置換屬性來平滑物件動畫</span><span class="sxs-lookup"><span data-stu-id="91a2f-176">Smooth Object Animation using the Desired Displacement Property</span></span>

<span data-ttu-id="91a2f-177">在某些情況下，您不會想要使用使用者的輸入來取代物件，但您仍然想要物件在螢幕上流暢地產生動畫。</span><span class="sxs-lookup"><span data-stu-id="91a2f-177">In some cases, you don't want to use the user's input for object displacement, but you still want an object to smoothly animate across the screen.</span></span> <span data-ttu-id="91a2f-178">在這種情況下，您可以使用慣性處理器中的置換屬性，讓處理器計算在畫面上移動物件的初始速度。</span><span class="sxs-lookup"><span data-stu-id="91a2f-178">In this case, you can use displacement properties in the inertia processor to have the processor calculate the initial velocity for moving an object across the screen.</span></span>

## <a name="controlling-object-position-using-elastic-bounds"></a><span data-ttu-id="91a2f-179">使用彈性界限控制物件位置</span><span class="sxs-lookup"><span data-stu-id="91a2f-179">Controlling Object Position Using Elastic Bounds</span></span>

<span data-ttu-id="91a2f-180">當您的物件是在螢幕上移動之後，您通常會想要在它離開使用者的觀點之前先將它停止。</span><span class="sxs-lookup"><span data-stu-id="91a2f-180">After you have an object that is moving across the screen, you will typically want for it to stop before it goes outside of the user's viewpoint.</span></span> <span data-ttu-id="91a2f-181">慣性處理器會透過界限和彈性邊界屬性來啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="91a2f-181">The inertia processor enables this functionality through the boundary and elastic margin properties.</span></span> <span data-ttu-id="91a2f-182">下圖說明一般應用程式中的各種界限和邊界屬性。</span><span class="sxs-lookup"><span data-stu-id="91a2f-182">The following image illustrates the various boundary and margin properties in a typical application.</span></span>

![顯示界限和彈性 margin 屬性的螢幕擷取畫面](images/elastic-illustrated.png)

<span data-ttu-id="91a2f-184">您可以為您的應用程式設定左、上、右、下限和彈性邊界，而慣性處理器將會處理在界限內保持 UI 元素的位置。</span><span class="sxs-lookup"><span data-stu-id="91a2f-184">You set the left, upper, right, and lower boundaries and elastic margins for your application, and the inertia processor will handle keeping UI elements within the bounds.</span></span> <span data-ttu-id="91a2f-185">當物件達到彈性邊界時，它會變慢，直到到達界限為止。</span><span class="sxs-lookup"><span data-stu-id="91a2f-185">When an object reaches an elastic margin, it will slow down until it reaches the boundary.</span></span> <span data-ttu-id="91a2f-186">它永遠不會在慣性期間保留該邊界，但仍會移動到物件的垂直慣性元件減速至0為止。</span><span class="sxs-lookup"><span data-stu-id="91a2f-186">It will never leave that margin again during inertia, but will still move until the object's perpendicular inertia component decelerates to 0.</span></span> <span data-ttu-id="91a2f-187">在圖例中，會將圓形朝左邊的彈性界限進行取代。</span><span class="sxs-lookup"><span data-stu-id="91a2f-187">In the illustration, a circle is displaced toward the left elastic boundary.</span></span> <span data-ttu-id="91a2f-188">實心箭號會顯示操作的方向;實心圓圈是物件的初始位置;實心箭號是在圓形達到彈性邊界之前所做的變更;虛線箭號會顯示慣性處理器在達到邊界之後操作圓形的位置;而且虛線圓形會顯示物件停止的位置。</span><span class="sxs-lookup"><span data-stu-id="91a2f-188">The solid arrow shows the direction of the manipulation; the solid circle is the initial position of the object; the solid arrow is the changes made before the circle hits the elastic margin; the dashed arrow shows where the inertia processor manipulates the circle after it hits the margin; and the dashed circles show where the object stops.</span></span>

> [!Note]  
> <span data-ttu-id="91a2f-189">設定邊界屬性會向外移動界限。</span><span class="sxs-lookup"><span data-stu-id="91a2f-189">Setting the margin properties will move the bounds outward.</span></span> <span data-ttu-id="91a2f-190">例如，如果您的頂端界限設定為50，然後將最高彈性的邊界設定為10，則您的最上層界限將會有效地變成40。</span><span class="sxs-lookup"><span data-stu-id="91a2f-190">For example, if your top boundary is set to 50 and then you set the top elastic margin to 10, your top boundary will effectively become 40.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="91a2f-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="91a2f-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91a2f-192">處理非受控碼中的慣性</span><span class="sxs-lookup"><span data-stu-id="91a2f-192">Handling Inertia in Unmanaged Code</span></span>](handling-inertia-in-unmanaged-code.md)
</dt> <dt>

[<span data-ttu-id="91a2f-193">慣性</span><span class="sxs-lookup"><span data-stu-id="91a2f-193">Inertia</span></span>](getting-started-with-inertia.md)
</dt> <dt>

[<span data-ttu-id="91a2f-194">操作</span><span class="sxs-lookup"><span data-stu-id="91a2f-194">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




