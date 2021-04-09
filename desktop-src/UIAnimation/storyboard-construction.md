---
title: 分鏡腳本總覽
description: 本總覽著重于如何在 Windows 動畫中使用轉換和分鏡腳本。
ms.assetid: d37718ac-0256-4a24-a26c-d29173593be0
keywords:
- Windows 動畫視窗動畫、分鏡腳本總覽
- 分鏡腳本視窗動畫，說明
- 轉換 Windows 動畫，說明
- 轉換 Windows 動畫，自訂
- interpolators Windows 動畫，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d8e0af3937cd31ccdc43216a9d3426bad0e7b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682558"
---
# <a name="storyboard-overview"></a><span data-ttu-id="e839b-108">分鏡腳本總覽</span><span class="sxs-lookup"><span data-stu-id="e839b-108">Storyboard Overview</span></span>

<span data-ttu-id="e839b-109">本總覽著重于如何在 Windows 動畫中使用轉換和分鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="e839b-109">This overview focuses on how transitions and storyboards are used in Windows Animation.</span></span> <span data-ttu-id="e839b-110">如需 Windows 動畫元件的總覽，請參閱 [Windows 動畫總覽](scenic-animation-api-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="e839b-110">For an overview of the components of Windows Animation, see [Windows Animation Overview](scenic-animation-api-overview.md).</span></span>

<span data-ttu-id="e839b-111">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="e839b-111">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="e839b-112">轉換</span><span class="sxs-lookup"><span data-stu-id="e839b-112">Transitions</span></span>](#custom-transitions)
    -   [<span data-ttu-id="e839b-113">轉換程式庫</span><span class="sxs-lookup"><span data-stu-id="e839b-113">Transition Library</span></span>](#transition-library)
    -   [<span data-ttu-id="e839b-114">自訂轉換</span><span class="sxs-lookup"><span data-stu-id="e839b-114">Custom Transitions</span></span>](#custom-transitions)
-   [<span data-ttu-id="e839b-115">Storyboard</span><span class="sxs-lookup"><span data-stu-id="e839b-115">Storyboards</span></span>](#storyboards)
    -   [<span data-ttu-id="e839b-116">建立簡單的分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="e839b-116">Building a Simple Storyboard</span></span>](#building-a-simple-storyboard)
    -   [<span data-ttu-id="e839b-117">使用 Context-Sensitive 持續時間</span><span class="sxs-lookup"><span data-stu-id="e839b-117">Using a Context-Sensitive Duration</span></span>](#using-a-context-sensitive-duration)
    -   [<span data-ttu-id="e839b-118">建立更複雜的分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="e839b-118">Building a More Complex Storyboard</span></span>](#building-a-more-complex-storyboard)
    -   [<span data-ttu-id="e839b-119">使用主要畫面格</span><span class="sxs-lookup"><span data-stu-id="e839b-119">Using Keyframes</span></span>](#using-keyframes)
    -   [<span data-ttu-id="e839b-120">保留變數</span><span class="sxs-lookup"><span data-stu-id="e839b-120">Holding Variables</span></span>](#holding-variables)
    -   [<span data-ttu-id="e839b-121">排程分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="e839b-121">Scheduling a Storyboard</span></span>](#scheduling-a-storyboard)
-   [<span data-ttu-id="e839b-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="e839b-122">Related topics</span></span>](#related-topics)

## <a name="transitions"></a><span data-ttu-id="e839b-123">轉換</span><span class="sxs-lookup"><span data-stu-id="e839b-123">Transitions</span></span>

<span data-ttu-id="e839b-124">轉換會定義單一動畫變數在特定時間間隔內的變更方式。</span><span class="sxs-lookup"><span data-stu-id="e839b-124">A transition defines how a single animation variable changes over a particular time interval.</span></span> <span data-ttu-id="e839b-125">Windows 動畫包含一般轉換的程式庫，可供開發人員套用至一或多個動畫變數。</span><span class="sxs-lookup"><span data-stu-id="e839b-125">Windows Animation includes a library of common transitions that developers can apply to one or more animation variables.</span></span> <span data-ttu-id="e839b-126">不同類型的轉換具有不同的參數集，這些參數可能會在轉換完成時包括變數的值、轉換的持續時間，或是基礎數學函數的唯一數量（例如加速或震盪的範圍）。</span><span class="sxs-lookup"><span data-stu-id="e839b-126">Different kinds of transitions have different sets of parameters, which may include the value of the variable when the transition completes, the duration of the transition, or quantities unique to the underlying mathematical function, such as acceleration or range of oscillation.</span></span>

<span data-ttu-id="e839b-127">所有轉換都會共用兩個隱含參數：數學函式的初始值和初始速度 (斜率) 。</span><span class="sxs-lookup"><span data-stu-id="e839b-127">All transitions share two implicit parameters: the initial value and initial velocity (slope) of the mathematical function.</span></span> <span data-ttu-id="e839b-128">這些可以由應用程式明確指定，但通常會在轉換開始時，由動畫管理員設定為動畫變數的值和速度。</span><span class="sxs-lookup"><span data-stu-id="e839b-128">These may be specified explicitly by the application, but are typically set by the animation manager to the value and velocity of the animation variable when the transition begins.</span></span>

-   [<span data-ttu-id="e839b-129">轉換程式庫</span><span class="sxs-lookup"><span data-stu-id="e839b-129">Transition Library</span></span>](#transition-library)
-   [<span data-ttu-id="e839b-130">自訂轉換</span><span class="sxs-lookup"><span data-stu-id="e839b-130">Custom Transitions</span></span>](#custom-transitions)

### <a name="transition-library"></a><span data-ttu-id="e839b-131">轉換程式庫</span><span class="sxs-lookup"><span data-stu-id="e839b-131">Transition Library</span></span>

<span data-ttu-id="e839b-132">轉換程式庫目前提供下列轉換。</span><span class="sxs-lookup"><span data-stu-id="e839b-132">The following transitions are currently provided by the transition library.</span></span> <span data-ttu-id="e839b-133">如果應用程式需要無法使用轉換程式庫指定的效果，開發人員可以藉由為應用程式執行自訂插即用，或使用協力廠商的轉換程式庫，來建立其他類型的轉換。</span><span class="sxs-lookup"><span data-stu-id="e839b-133">If an application requires an effect that cannot be specified by using the transition library, developers can create other kinds of transitions by implementing a custom interpolator for the application, or using a transition library from a third party.</span></span>



| <span data-ttu-id="e839b-134">轉換名稱</span><span class="sxs-lookup"><span data-stu-id="e839b-134">Transition Name</span></span>                        | <span data-ttu-id="e839b-135">Description</span><span class="sxs-lookup"><span data-stu-id="e839b-135">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e839b-136">加速-減速</span><span class="sxs-lookup"><span data-stu-id="e839b-136">accelerate-decelerate</span></span><br/>       | <span data-ttu-id="e839b-137">動畫變數會加速，並在指定的期間內減緩。</span><span class="sxs-lookup"><span data-stu-id="e839b-137">The animation variable speeds up and then slows down over a given duration.</span></span><br/>                                                                                                               |
| <span data-ttu-id="e839b-138">常數</span><span class="sxs-lookup"><span data-stu-id="e839b-138">constant</span></span><br/>                    | <span data-ttu-id="e839b-139">動畫變數會在整個轉換期間維持其初始值。</span><span class="sxs-lookup"><span data-stu-id="e839b-139">The animation variable remains at its initial value throughout the transition.</span></span><br/>                                                                                                            |
| <span data-ttu-id="e839b-140">三次方</span><span class="sxs-lookup"><span data-stu-id="e839b-140">cubic</span></span><br/>                       | <span data-ttu-id="e839b-141">動畫變數在指定的持續期間內，會以指定的最終速度，從其初始值變更為指定的最後一個值。</span><span class="sxs-lookup"><span data-stu-id="e839b-141">The animation variable changes from its initial value to a specified final value, with a specified final velocity, over a given duration.</span></span><br/>                                                 |
| <span data-ttu-id="e839b-142">離散</span><span class="sxs-lookup"><span data-stu-id="e839b-142">discrete</span></span><br/>                    | <span data-ttu-id="e839b-143">動畫變數在指定的延遲時間仍維持其初始值，然後立即切換到指定的最終值，並針對指定的保留時間維持在該值的值。</span><span class="sxs-lookup"><span data-stu-id="e839b-143">The animation variable remains at its initial value for a specified delay time, then switches instantaneously to a specified final value and remains at that value for a given hold time.</span></span><br/> |
| <span data-ttu-id="e839b-144">暫態</span><span class="sxs-lookup"><span data-stu-id="e839b-144">instantaneous</span></span><br/>               | <span data-ttu-id="e839b-145">動畫變數會立即從其目前的值變更為指定的最後一個值。</span><span class="sxs-lookup"><span data-stu-id="e839b-145">The animation variable changes instantly from its current value to a specified final value.</span></span><br/>                                                                                               |
| <span data-ttu-id="e839b-146">linear</span><span class="sxs-lookup"><span data-stu-id="e839b-146">linear</span></span><br/>                      | <span data-ttu-id="e839b-147">動畫變數會在指定的持續期間，以線性方式從其初始值轉換為指定的最終值。</span><span class="sxs-lookup"><span data-stu-id="e839b-147">The animation variable transitions linearly from its initial value to a specified final value over a given duration.</span></span><br/>                                                                      |
| <span data-ttu-id="e839b-148">線性的速度</span><span class="sxs-lookup"><span data-stu-id="e839b-148">linear from speed</span></span><br/>           | <span data-ttu-id="e839b-149">動畫變數會從其初始值以線性方式轉換為指定的最終值（具有指定的速度）。</span><span class="sxs-lookup"><span data-stu-id="e839b-149">The animation variable transitions linearly from its initial value to a specified final value with a specified speed.</span></span><br/>                                                                     |
| <span data-ttu-id="e839b-150">從加速拋物線</span><span class="sxs-lookup"><span data-stu-id="e839b-150">parabolic from acceleration</span></span><br/> | <span data-ttu-id="e839b-151">動畫變數會從其初始值轉換為指定的最後一個值，並使用指定的加速來變更其速度。</span><span class="sxs-lookup"><span data-stu-id="e839b-151">The animation variable transitions from its initial value to a specified final value, with a specified final velocity, changing its velocity with a specified acceleration.</span></span><br/>               |
| <span data-ttu-id="e839b-152">逆轉</span><span class="sxs-lookup"><span data-stu-id="e839b-152">reversal</span></span><br/>                    | <span data-ttu-id="e839b-153">變數會在指定的期間內變更方向。</span><span class="sxs-lookup"><span data-stu-id="e839b-153">The variable changes direction over a given duration.</span></span> <span data-ttu-id="e839b-154">最後一個值將會與初始值相同，最後的速度將會是初始速度的負數值。</span><span class="sxs-lookup"><span data-stu-id="e839b-154">The final value will be the same as the initial value and the final velocity will be the negative of the initial velocity.</span></span><br/>          |
| <span data-ttu-id="e839b-155">從範圍正弦曲線</span><span class="sxs-lookup"><span data-stu-id="e839b-155">sinusoidal from range</span></span><br/>       | <span data-ttu-id="e839b-156">在指定的期間內，oscillates 指定的值範圍內的變數（具有指定的震盪期間）。</span><span class="sxs-lookup"><span data-stu-id="e839b-156">The variable oscillates within a given range of values, with a specified period of oscillation, for a given duration.</span></span><br/>                                                                     |
| <span data-ttu-id="e839b-157">從速度正弦曲線</span><span class="sxs-lookup"><span data-stu-id="e839b-157">sinusoidal from velocity</span></span><br/>    | <span data-ttu-id="e839b-158">在指定的期間內，變數 oscillates 具有指定的震盪期間。</span><span class="sxs-lookup"><span data-stu-id="e839b-158">The variable oscillates with a specified period of oscillation, for a given duration.</span></span> <span data-ttu-id="e839b-159">震盪的波幅取決於變數的初始速度。</span><span class="sxs-lookup"><span data-stu-id="e839b-159">The amplitude of oscillation is determined by the variable's initial velocity.</span></span><br/>                      |
| <span data-ttu-id="e839b-160">順利停止</span><span class="sxs-lookup"><span data-stu-id="e839b-160">smooth stop</span></span><br/>                 | <span data-ttu-id="e839b-161">動畫變數在時間的最長持續時間內，會在指定的最終值上變成平滑停止。</span><span class="sxs-lookup"><span data-stu-id="e839b-161">The animation variable comes to a smooth stop at a specified final value, within a maximum duration of time.</span></span><br/>                                                                              |



 

<span data-ttu-id="e839b-162">下表包含每個轉換的圖例。</span><span class="sxs-lookup"><span data-stu-id="e839b-162">The following table contains illustrations for each of these transitions.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![瞬間轉換的圖例](images/instantaneoustransition.png)  ![常數轉換的圖例](images/constanttransition.png)  ![線性轉換的圖例](images/lineartransition.png)  ![從速度 lineat 轉換的圖例](images/lineartransitionfromspeed.png)  ![離散轉換的圖例](images/discretetransition.png) |
| ![從加速拋物線轉換的圖例](images/parabolictransitionfromacceleration.png)  ![三次轉換的圖例](images/cubictransition.png)  ![平滑停止轉換的圖例](images/smoothstoptransition.png)                                                                                                                                       |
| ![反轉轉換的圖例](images/reversaltransition.png)  ![從速度正弦曲線轉換的圖例](images/sinusolidaltransitionfromvelocity.png)  ![從範圍正弦曲線轉換的圖例](images/sinusolidaltransitionfromrange.png)                                                                                                                  |
| ![accellerate 和減速轉換的圖例](images/acceleratedeceleratetransition.png)                                                                                                                                                                                                                                                                                               |



 

### <a name="custom-transitions"></a><span data-ttu-id="e839b-175">自訂轉換</span><span class="sxs-lookup"><span data-stu-id="e839b-175">Custom Transitions</span></span>

<span data-ttu-id="e839b-176">*插* 即用會定義數學函式，以決定動畫變數在從其初始值移至最後一個值時，如何隨著時間變更。</span><span class="sxs-lookup"><span data-stu-id="e839b-176">An *interpolator* defines the mathematical function that determines how an animation variable changes over time as it progresses from its initial value to a final value.</span></span> <span data-ttu-id="e839b-177">轉換程式庫中的每個轉換都有一個相關聯的插隨插即用，該物件是由系統所提供並會執行插即插</span><span class="sxs-lookup"><span data-stu-id="e839b-177">Each transition in the transition library has an associated interpolator object that is provided by the system and implements the interpolator function.</span></span> <span data-ttu-id="e839b-178">如果應用程式需要無法使用轉換程式庫指定的效果，則可以藉由針對每個新轉換來執行插即用物件，來執行一或多個自訂轉換。</span><span class="sxs-lookup"><span data-stu-id="e839b-178">If an application requires an effect that cannot be specified using the transition library, it can implement one or more custom transitions by implementing an interpolator object for each new transition.</span></span> <span data-ttu-id="e839b-179">插即用物件不能直接用於應用程式，而必須改為包裝在相關聯的轉換中。</span><span class="sxs-lookup"><span data-stu-id="e839b-179">Interpolator objects cannot be used directly by applications and must instead be wrapped in an associated transition.</span></span> <span data-ttu-id="e839b-180">*轉換 factory* 用來從插即用物件產生轉換。</span><span class="sxs-lookup"><span data-stu-id="e839b-180">A *transition factory* is used to generate transitions from an interpolator object.</span></span> <span data-ttu-id="e839b-181">如需詳細資訊，請參閱 [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) 和 [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory) 。</span><span class="sxs-lookup"><span data-stu-id="e839b-181">See [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) and [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory) for more details.</span></span>

<span data-ttu-id="e839b-182">請注意，大部分的應用程式都有使用轉換程式庫所需的所有轉換，因此不需要執行插即用。</span><span class="sxs-lookup"><span data-stu-id="e839b-182">Note that most applications will have all of the transitions they need by using the transition library, and therefore would not need to implement an interpolator.</span></span>

## <a name="storyboards"></a><span data-ttu-id="e839b-183">Storyboard</span><span class="sxs-lookup"><span data-stu-id="e839b-183">Storyboards</span></span>

<span data-ttu-id="e839b-184">分鏡腳本是一組隨時間套用至一或多個動畫變數的轉換集合。</span><span class="sxs-lookup"><span data-stu-id="e839b-184">A storyboard is a collection of transitions applied to one or more animation variables over time.</span></span> <span data-ttu-id="e839b-185">分鏡腳本中的轉換保證會彼此保持同步，而且分鏡腳本已排程或取消為一個單位。</span><span class="sxs-lookup"><span data-stu-id="e839b-185">The transitions in a storyboard are guaranteed to remain synchronized relative to one another, and the storyboard is scheduled or canceled as a unit.</span></span> <span data-ttu-id="e839b-186">建立所需的轉換之後，應用程式會使用動畫管理員來建立分鏡腳本、將轉換新增至腳本、適當地設定分鏡腳本，並將它排程為盡可能播放。</span><span class="sxs-lookup"><span data-stu-id="e839b-186">After creating the desired transitions, an application creates a storyboard using the animation manager, adds the transitions to the storyboard, configures the storyboard appropriately, and schedules it to play as soon as possible.</span></span> <span data-ttu-id="e839b-187">動畫管理員會決定分鏡腳本的實際開始時間，因為可能會有與其他分鏡腳本的競爭，且目前會以動畫顯示相同的變數。</span><span class="sxs-lookup"><span data-stu-id="e839b-187">The animation manager determines the storyboard's actual start time, because there may be contention with other storyboards currently animating the same variables.</span></span>

<span data-ttu-id="e839b-188">分鏡腳本的整體持續時間取決於分鏡腳本內轉換的持續時間。</span><span class="sxs-lookup"><span data-stu-id="e839b-188">The overall duration of a storyboard depends on the durations of the transitions within the storyboard.</span></span> <span data-ttu-id="e839b-189">轉換的持續時間不需要固定;轉換開始時，可以由動畫變數的值和速度來決定。</span><span class="sxs-lookup"><span data-stu-id="e839b-189">The duration of a transition need not be fixed; it can be determined by the value and velocity of the animated variables when the transition begins.</span></span> <span data-ttu-id="e839b-190">因此，分鏡腳本的持續時間也可能取決於其動畫的變數狀態。</span><span class="sxs-lookup"><span data-stu-id="e839b-190">So, the duration of a storyboard can also depend on the state of the variables it animates.</span></span>

<span data-ttu-id="e839b-191">下列範例假設已建立動畫管理員、轉換程式庫和計時器。</span><span class="sxs-lookup"><span data-stu-id="e839b-191">The following examples assume that an animation manager, transition library, and timer have been created.</span></span> <span data-ttu-id="e839b-192">如需詳細資訊，請參閱 [建立主要動畫物件](adding-animation-to-an-application.md)。</span><span class="sxs-lookup"><span data-stu-id="e839b-192">For more information, see [Create the Main Animation Objects](adding-animation-to-an-application.md).</span></span> <span data-ttu-id="e839b-193">範例也假設應用程式已使用 [**IUIAnimationManager：： CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) 方法建立三個動畫變數 (X、Y 和 Z) ，而五個轉換 (T1、T2、T3、T4 和 T5) 使用 [**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary) 介面的其中一個方法。</span><span class="sxs-lookup"><span data-stu-id="e839b-193">The examples also assume that the application has created three animation variables (X, Y and Z) by using the [**IUIAnimationManager::CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) method, and five transitions (T1, T2, T3, T4, and T5) by using the one of the methods of the [**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary) interface.</span></span>

-   [<span data-ttu-id="e839b-194">建立簡單的分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="e839b-194">Building a Simple Storyboard</span></span>](#building-a-simple-storyboard)
-   [<span data-ttu-id="e839b-195">使用 Context-Sensitive 持續時間</span><span class="sxs-lookup"><span data-stu-id="e839b-195">Using a Context-Sensitive Duration</span></span>](#using-a-context-sensitive-duration)
-   [<span data-ttu-id="e839b-196">建立更複雜的分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="e839b-196">Building a More Complex Storyboard</span></span>](#building-a-more-complex-storyboard)
-   [<span data-ttu-id="e839b-197">使用主要畫面格</span><span class="sxs-lookup"><span data-stu-id="e839b-197">Using Keyframes</span></span>](#using-keyframes)
-   [<span data-ttu-id="e839b-198">保留變數</span><span class="sxs-lookup"><span data-stu-id="e839b-198">Holding Variables</span></span>](#holding-variables)
-   [<span data-ttu-id="e839b-199">排程分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="e839b-199">Scheduling a Storyboard</span></span>](#scheduling-a-storyboard)

### <a name="building-a-simple-storyboard"></a><span data-ttu-id="e839b-200">建立簡單的分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="e839b-200">Building a Simple Storyboard</span></span>

<span data-ttu-id="e839b-201">若要建立簡單的分鏡腳本，請使用 [**IUIAnimationManager：： CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) 方法來建立新的分鏡腳本、 [**IUIAnimationTransitionLibrary：： CreateLinearTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransition) 方法來建立線性轉換、T1 和 [**IUIAnimationStoryboard：： AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) 方法，以將 T1 轉換套用至變數 X，並將產生的轉換加入至腳本。</span><span class="sxs-lookup"><span data-stu-id="e839b-201">To build a simple storyboard, use the [**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) method to create a new storyboard, the [**IUIAnimationTransitionLibrary::CreateLinearTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransition) method to create a linear transition, T1, and the [**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) method to apply the T1 transition to the variable X and add the resulting transition to the storyboard.</span></span>

<span data-ttu-id="e839b-202">此程式會產生簡單的分鏡腳本，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="e839b-202">This process yields a simple storyboard, as shown in the following figure.</span></span> <span data-ttu-id="e839b-203">分鏡腳本包含一個轉換 T1，讓變數 X 的值在固定的時間內以線性方式變更。</span><span class="sxs-lookup"><span data-stu-id="e839b-203">The storyboard contains one transition, T1, such that the value of variable X changes linearly over a fixed duration of time.</span></span>

![顯示簡單分鏡腳本有固定持續時間的圖例](images/simplestoryboardfixedduration.png)

<span data-ttu-id="e839b-205">請注意，在這種簡單的案例中，替代選項是使用 [**IUIAnimationManager：： ScheduleTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-scheduletransition) 方法。</span><span class="sxs-lookup"><span data-stu-id="e839b-205">Note that for such a simple scenario, an alternative option is to use the [**IUIAnimationManager::ScheduleTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-scheduletransition) method.</span></span>

### <a name="using-a-context-sensitive-duration"></a><span data-ttu-id="e839b-206">使用 Context-Sensitive 持續時間</span><span class="sxs-lookup"><span data-stu-id="e839b-206">Using a Context-Sensitive Duration</span></span>

<span data-ttu-id="e839b-207">雖然某些轉換有固定的持續時間，但其他的持續時間取決於轉換開始時的動畫變數初始值或速度。</span><span class="sxs-lookup"><span data-stu-id="e839b-207">While some transitions have a fixed duration, the duration of others depends on the initial value or velocity of the animated variable when the transition begins.</span></span> <span data-ttu-id="e839b-208">例如， [**IUIAnimationTransitionLibrary：： CreateLinearTransitionFromSpeed**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransitionfromspeed) 方法會建立一個持續期間的轉換，與動畫變數的初始值和指定的最後一個值之間的差異成正比。</span><span class="sxs-lookup"><span data-stu-id="e839b-208">For example, the [**IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransitionfromspeed) method creates a transition with a duration that is proportional to the difference between the initial value of the animation variable and the specified final value.</span></span> <span data-ttu-id="e839b-209">在此圖中，和其餘的圖例（具有任意持續時間的轉換）會顯示一個問號 (？ ) ，而且實際的持續時間會在腳本播放時決定。</span><span class="sxs-lookup"><span data-stu-id="e839b-209">In this illustration, and the remaining illustrations, such transitions with arbitrary durations are shown with a question mark (?), and their actual durations are determined when the storyboard plays.</span></span>

![圖例顯示具有未知持續時間的簡單分鏡腳本](images/simplestoryboardunknownduration.png)

### <a name="building-a-more-complex-storyboard"></a><span data-ttu-id="e839b-211">建立更複雜的分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="e839b-211">Building a More Complex Storyboard</span></span>

<span data-ttu-id="e839b-212">建立分鏡腳本並加入單一轉換 T1 之後，您可以再次呼叫 [**IUIAnimationStoryboard：： AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) 方法，但使用 T2 而不是 T1，來附加 X 變數的第二個轉換。</span><span class="sxs-lookup"><span data-stu-id="e839b-212">After creating a storyboard and adding a single transition, T1, you can append a second transition for the X variable by calling the [**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) method again, but with T2 instead of T1.</span></span>

<span data-ttu-id="e839b-213">假設 T2 轉換具有內容相關的持續時間，則腳本現在會包含影響變數 X 之任意持續時間的兩個反向轉換。</span><span class="sxs-lookup"><span data-stu-id="e839b-213">Assuming that the T2 transition has a duration that is context-sensitive, the storyboard now contains two back-to-back transitions of arbitrary duration affecting the variable X.</span></span>

![顯示分鏡腳本的圖例，其中包含兩個在相同變數上的轉換](images/appendingwithaddtransition.png)

<span data-ttu-id="e839b-215">使用變數 Y 和轉換 T3 再次呼叫 [**AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) ，會在腳本的開頭新增第三個轉換。</span><span class="sxs-lookup"><span data-stu-id="e839b-215">Calling [**AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) again with variable Y and transition T3 adds a third transition at the start of the storyboard.</span></span> <span data-ttu-id="e839b-216">根據在腳本播放時的 X 和 Y 值，T3 可能會在 T1 之後結束，甚至在 T2 之後結束。</span><span class="sxs-lookup"><span data-stu-id="e839b-216">Depending on the values of X and Y when the storyboard plays, T3 may end after T1 or even after T2.</span></span>

![顯示分鏡腳本包含跨多個變數之轉換的圖例](images/multivariablestoryboard.png)

### <a name="using-keyframes"></a><span data-ttu-id="e839b-218">使用主要畫面格</span><span class="sxs-lookup"><span data-stu-id="e839b-218">Using Keyframes</span></span>

<span data-ttu-id="e839b-219">若要在腳本開頭的位移加入轉換，您必須先新增主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="e839b-219">To add a transition at an offset from the start of the storyboard, you must first add a keyframe.</span></span> <span data-ttu-id="e839b-220">主要畫面格代表時刻的時間，而且本身不會影響分鏡腳本的行為。</span><span class="sxs-lookup"><span data-stu-id="e839b-220">Keyframes represent instants in time and by themselves have no effect on the behavior of the storyboard.</span></span> <span data-ttu-id="e839b-221">每個分鏡腳本都有一個隱含的主要畫面格，代表腳本的開頭、Ui 動畫主要畫面格 [**\_ \_ \_ \_ 開始**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85)); 您可以透過呼叫 [**IUIAnimationStoryboard：： AddKeyframeAtOffset**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset) 方法與 UI 動畫主要畫面格 **\_ \_ \_ \_ 開始**，從一開始的位移加入新的主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="e839b-221">Every storyboard has an implicit keyframe representing the start of the storyboard, [**UI\_ANIMATION\_KEYFRAME\_STORYBOARD\_START**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85)); you can add new keyframes at offsets from the start by calling the [**IUIAnimationStoryboard::AddKeyframeAtOffset**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset) method with **UI\_ANIMATION\_KEYFRAME\_STORYBOARD\_START**.</span></span>

<span data-ttu-id="e839b-222">您新增主要畫面格的位移一律相對於另一個主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="e839b-222">The offset at which you add a keyframe is always relative to another keyframe.</span></span> <span data-ttu-id="e839b-223">下圖顯示加入 keyframe1 和轉換 T4 的結果，此結果會套用至變數 Z、與 keyframe1 對齊，並以固定期間建立。</span><span class="sxs-lookup"><span data-stu-id="e839b-223">The following diagram shows the result of adding keyframe1 and transition T4, which is applied to variable Z, aligned with keyframe1, and created with a fixed duration.</span></span> <span data-ttu-id="e839b-224">當然，因為其他轉換的持續時間尚未得知，所以 T4 可能不是最後一個轉換完成。</span><span class="sxs-lookup"><span data-stu-id="e839b-224">Of course, because the durations of the other transitions are not yet known, T4 might not be the last transition to finish.</span></span>

![圖例顯示在主要畫面格對齊的轉換](images/addtransitionatkeyframe.png)

<span data-ttu-id="e839b-226">您也可以使用 [**IUIAnimationStoryboard：： AddKeyframeAfterTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition) 方法，將主要畫面格放在轉換的結尾。</span><span class="sxs-lookup"><span data-stu-id="e839b-226">Keyframes can also be placed at the ends of transitions, using the [**IUIAnimationStoryboard::AddKeyframeAfterTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition) method.</span></span> <span data-ttu-id="e839b-227">下圖顯示在 T2 之後新增 keyframe2 的結果，以及 T2 之後的 keyframe3。</span><span class="sxs-lookup"><span data-stu-id="e839b-227">The following diagram shows the result of adding keyframe2 after T1 and keyframe3 after T2.</span></span>

![此圖顯示各種轉換之後的主要畫面格加法](images/addkeyframeaftertransition.png)

<span data-ttu-id="e839b-229">由於在分鏡腳本播放之前，T1 和 T2 的持續時間是未知的，因此在那之前，keyframe2 和 keyframe3 的位移也不會決定。</span><span class="sxs-lookup"><span data-stu-id="e839b-229">Because the durations of T1 and T2 are not known until the storyboard plays, the offsets of keyframe2 and keyframe3 also are not determined until then.</span></span> <span data-ttu-id="e839b-230">因此，keyframe2 甚至 keyframe3 可能會在 keyframe1 之前發生。</span><span class="sxs-lookup"><span data-stu-id="e839b-230">Consequently, keyframe2 and even keyframe3 can occur earlier than keyframe1.</span></span>

<span data-ttu-id="e839b-231">轉換的開始和結束都可以使用 [**IUIAnimationStoryboard：： AddTransitionBetweenKeyframes**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes) 方法來與主要畫面格對齊。</span><span class="sxs-lookup"><span data-stu-id="e839b-231">Both the start and end of a transition can be aligned with keyframes by using the [**IUIAnimationStoryboard::AddTransitionBetweenKeyframes**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes) method.</span></span> <span data-ttu-id="e839b-232">下圖顯示在變數 Y 上新增第五個轉換（T5）在 keyframe2 和 keyframe3 之間的結果。</span><span class="sxs-lookup"><span data-stu-id="e839b-232">The following diagram shows the result of adding a fifth transition, T5, on variable Y, between keyframe2 and keyframe3.</span></span> <span data-ttu-id="e839b-233">這會改變 T5 的持續時間，取決於 keyframe2 和 keyframe3 的相對位移，使其更長或更短。</span><span class="sxs-lookup"><span data-stu-id="e839b-233">This alters the duration of T5, making it longer or shorter depending on the relative offsets of keyframe2 and keyframe3.</span></span>

![顯示在主要畫面格之間轉換 additon 的圖例](images/addtransitionbetweenkeyframes.png)

### <a name="holding-variables"></a><span data-ttu-id="e839b-235">保留變數</span><span class="sxs-lookup"><span data-stu-id="e839b-235">Holding Variables</span></span>

<span data-ttu-id="e839b-236">如果 T4 在 T2 和 T5 之後結束，腳本會停止將變數 X 和 Y 建立動畫，讓其他分鏡腳本能以動畫顯示。</span><span class="sxs-lookup"><span data-stu-id="e839b-236">If T4 does end after T2 and T5, the storyboard stops animating variables X and Y, making them available for other storyboards to animate.</span></span> <span data-ttu-id="e839b-237">不過，應用程式可以呼叫 [**IUIAnimationStoryboard：： HoldVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-holdvariable) 方法，要求腳本在腳本完成之前，保留其最終值的部分或所有變數。</span><span class="sxs-lookup"><span data-stu-id="e839b-237">However, the application can call the [**IUIAnimationStoryboard::HoldVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-holdvariable) method to request that the storyboard hold some or all of the variables it animates at their final values until the storyboard has completed.</span></span> <span data-ttu-id="e839b-238">下圖顯示 T4 最後完成時，保留 X 和 Z 的結果。</span><span class="sxs-lookup"><span data-stu-id="e839b-238">The following diagram shows the result of holding X and Z when T4 finishes last.</span></span> <span data-ttu-id="e839b-239">請注意，分鏡腳本會在腳本完成之前，保留其最終值的 X。</span><span class="sxs-lookup"><span data-stu-id="e839b-239">Notice that the storyboard holds X at its final value until the storyboard has completed.</span></span> <span data-ttu-id="e839b-240">此保留對 Z 沒有任何作用，因為在 T4 完成時，腳本會結束。</span><span class="sxs-lookup"><span data-stu-id="e839b-240">The hold has no effect on Z because the storyboard ends when T4 finishes.</span></span>

![圖例顯示在完成腳本完成之前將變數保留在最後的值](images/holdvariable.png)

<span data-ttu-id="e839b-242">雖然此腳本未持有 Y，但在 T5 完成之後，其值不會變更，除非有另一個分鏡腳本的動畫。</span><span class="sxs-lookup"><span data-stu-id="e839b-242">Even though Y is not held by this storyboard, its value does not change after T5 completes unless another storyboard animates it.</span></span> <span data-ttu-id="e839b-243">因為沒有保留 Y，所以任何其他分鏡腳本（不論優先權為何）都可以在 T5 完成之後建立 Y 的動畫。</span><span class="sxs-lookup"><span data-stu-id="e839b-243">Because Y is not held, any other storyboard, regardless of priority, can animate Y after T5 has finished.</span></span> <span data-ttu-id="e839b-244">相反地，因為會保留 X，所以較低優先順序的分鏡腳本無法在此腳本完成之前建立 X 的動畫。</span><span class="sxs-lookup"><span data-stu-id="e839b-244">In contrast, because X is held, a lower-priority storyboard cannot animate X until this storyboard is finished.</span></span>

<span data-ttu-id="e839b-245">當分鏡腳本開始播放時，所有這些圖例都會假設變數有任意一組目前的值。</span><span class="sxs-lookup"><span data-stu-id="e839b-245">All of these illustrations have assumed an arbitrary set of current values for the variables when the storyboard starts playing.</span></span> <span data-ttu-id="e839b-246">如果遇到其他值，內容相關轉換的持續時間可能會不同，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="e839b-246">If other values are encountered, the durations of the context-sensitive transitions are likely to be different, as shown in the following illustration.</span></span>

![圖例顯示變更上圖所使用之初始條件的結果](images/holdvariablez.png)

<span data-ttu-id="e839b-248">在此案例中，T5 會在 T3 完成之前開始，T3 則會被修剪。</span><span class="sxs-lookup"><span data-stu-id="e839b-248">In this scenario, T5 begins before T3 has finished, and T3 is therefore trimmed.</span></span> <span data-ttu-id="e839b-249">因為 T4 的完成時間早于 T2 和 T5，所以 Z 的值會保留到腳本的結尾。</span><span class="sxs-lookup"><span data-stu-id="e839b-249">Because T4 finishes earlier than T2 and T5, the value of Z is held until the end of the storyboard.</span></span> <span data-ttu-id="e839b-250">一般來說，當腳本開始播放時，變數的值和速度可能會影響主要畫面格的順序以及分鏡腳本的整體長度和圖形。</span><span class="sxs-lookup"><span data-stu-id="e839b-250">In general, the values and velocities of variables when a storyboard starts playing can affect keyframe ordering and the overall length and shape of the storyboard.</span></span>

### <a name="scheduling-a-storyboard"></a><span data-ttu-id="e839b-251">排程分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="e839b-251">Scheduling a Storyboard</span></span>

<span data-ttu-id="e839b-252">排程分鏡腳本時，其開始時間是由其外框和目前在排程中的分鏡腳本大綱所決定。</span><span class="sxs-lookup"><span data-stu-id="e839b-252">When scheduling a storyboard, its start time is determined by its outline and the outlines of the storyboards that are currently in the schedule.</span></span> <span data-ttu-id="e839b-253">具體而言，當分鏡腳本繪製每個個別變數的第一個和最後一點時，會決定兩個分鏡腳本是否會發生衝突，但內轉換的內部詳細資料並不重要。</span><span class="sxs-lookup"><span data-stu-id="e839b-253">Specifically, the first and last moments when the storyboard animates each individual variable determine whether and when two storyboards collide, but the internal details of the transitions within are not important.</span></span>

<span data-ttu-id="e839b-254">下圖顯示分鏡腳本的大綱，其中有五個轉換以動畫顯示三個變數。</span><span class="sxs-lookup"><span data-stu-id="e839b-254">The following illustration shows the outline of a storyboard with five transitions animating three variables.</span></span>

![顯示分鏡腳本的圖，其中有五個轉換動畫三個變數](images/storyboardwithoutline.png)

<span data-ttu-id="e839b-256">Windows 動畫平臺的基石是支援在需要時，讓一個動畫先完成，再開始進行。</span><span class="sxs-lookup"><span data-stu-id="e839b-256">A cornerstone of the Windows Animation platform is its support for letting one animation complete before another begins, when necessary.</span></span> <span data-ttu-id="e839b-257">雖然這可排除許多邏輯問題，但它也會在 UI 中引進任意延遲。</span><span class="sxs-lookup"><span data-stu-id="e839b-257">While this eliminates many logical problems, it also introduces arbitrary latency in the UI.</span></span> <span data-ttu-id="e839b-258">若要解決此情況，應用程式可以使用 [**IUIAnimationStoryboard：： SetLongestAcceptableDelay**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay)方法指定可接受的分鏡腳本 *最長延遲* 時間，而動畫管理員會使用此資訊，在經過指定的延遲期間之前，排程腳本。</span><span class="sxs-lookup"><span data-stu-id="e839b-258">To address this, applications can specify the *longest acceptable delay* for a storyboard to start, using the [**IUIAnimationStoryboard::SetLongestAcceptableDelay**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay) method, and the animation manager uses this information to schedule the storyboard before the specified latency period elapses.</span></span> <span data-ttu-id="e839b-259">當您排定分鏡腳本時，動畫管理員會決定是否必須先取消、修剪、結束和/或壓縮其他的分鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="e839b-259">When a storyboard is scheduled, the animation manager determines if other storyboards must first be canceled, trimmed, concluded, and/or compressed.</span></span>

<span data-ttu-id="e839b-260">應用程式可以註冊一個處理常式，當腳本的狀態變更時，就會呼叫此處理程式。</span><span class="sxs-lookup"><span data-stu-id="e839b-260">An application can register a handler that will be called when a storyboard's status changes.</span></span> <span data-ttu-id="e839b-261">這可讓應用程式在分鏡腳本開始播放、執行完成、完全從排程中移除，或防止因較高優先順序的腳本中斷而無法完成時回應。</span><span class="sxs-lookup"><span data-stu-id="e839b-261">This enables the application to respond when the storyboard starts playing, runs to completion, is removed entirely from the schedule, or is prevented from completing due to interruption by a higher-priority storyboard.</span></span> <span data-ttu-id="e839b-262">若要識別傳遞給分鏡腳本事件處理常式 (或優先順序比較) 的分鏡腳本，應用程式可以使用 [**IUIAnimationStoryboard：： SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-settag) 方法，將標記套用至分鏡腳本，類似于可用來識別變數的範例。</span><span class="sxs-lookup"><span data-stu-id="e839b-262">To identify the storyboards passed to storyboard event handlers (or priority comparisons), an application can use the [**IUIAnimationStoryboard::SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-settag) method to apply tags to storyboards, similar to those that can be used to identify variables.</span></span> <span data-ttu-id="e839b-263">如同使用分鏡腳本重複使用，開發人員在使用標記來識別分鏡腳本時必須特別小心，並確定當使用者動作導致許多分鏡腳本排入佇列時，不會發生多義性。</span><span class="sxs-lookup"><span data-stu-id="e839b-263">As with storyboard re-use, developers must exercise caution when using tags to identify storyboards, and be sure that ambiguities do not arise when user actions result in many storyboards being queued.</span></span>

<span data-ttu-id="e839b-264">下列範例會示範兩種嘗試排程在本主題先前章節中所建立之分鏡腳本的變化。</span><span class="sxs-lookup"><span data-stu-id="e839b-264">The following examples show two variations of an attempt to schedule the storyboard built in the earlier sections of this topic.</span></span>

<span data-ttu-id="e839b-265">在此案例中，已排程6個分鏡腳本（A 到 F），以建立變數 W、X、Y 和 Z 的動畫，但只有 A 和 B 已開始播放。</span><span class="sxs-lookup"><span data-stu-id="e839b-265">In this scenario, six storyboards, A through F, have already been scheduled to animate variables W, X, Y and Z, but only A and B have started playing.</span></span> <span data-ttu-id="e839b-266">標示為 G 的新分鏡腳本，可接受的最長延遲設定為下圖所示的持續時間。</span><span class="sxs-lookup"><span data-stu-id="e839b-266">The new storyboard, labeled G, has its longest acceptable delay set to the duration shown in the following illustration.</span></span>

![顯示將新的腳本新增至現有排程的圖例](images/existingschedule1withlines.png)

<span data-ttu-id="e839b-268">應用程式已註冊優先順序比較，包括下列邏輯：</span><span class="sxs-lookup"><span data-stu-id="e839b-268">The application has registered priority comparisons that include the following logic:</span></span>

-   <span data-ttu-id="e839b-269">G 只能取消 C 和 E，而且只可以防止失敗。</span><span class="sxs-lookup"><span data-stu-id="e839b-269">G can cancel only C and E, and only to prevent failure.</span></span>
-   <span data-ttu-id="e839b-270">G 只能修剪 A、C、E 和 F，而只會避免失敗。</span><span class="sxs-lookup"><span data-stu-id="e839b-270">G can trim only A, C, E and F, and only to prevent failure.</span></span>
-   <span data-ttu-id="e839b-271">任何分鏡腳本都可以壓縮任何其他分鏡腳本 (壓縮一律是為了避免) 失敗。</span><span class="sxs-lookup"><span data-stu-id="e839b-271">Any storyboard can compress any other storyboard (compression is always done only to prevent failure).</span></span>

> [!Note]  
> <span data-ttu-id="e839b-272">「僅為了防止失敗」的辨識符號表示 \_ 只有當 *priorityEffect* 參數是 **UI \_ 動畫 \_ 優先權 \_ 效果 \_ 失敗** 時，註冊的優先順序比較才會傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="e839b-272">The qualifier "only to prevent failure" means that the registered priority comparisons return S\_OK only when the *priorityEffect* parameter is **UI\_ANIMATION\_PRIORITY\_EFFECT\_FAILURE**.</span></span> <span data-ttu-id="e839b-273">如需詳細資料，請參閱 [**IUIAnimationPriorityComparison：： HasPriority**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationprioritycomparison-haspriority) 方法。</span><span class="sxs-lookup"><span data-stu-id="e839b-273">See the [**IUIAnimationPriorityComparison::HasPriority**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationprioritycomparison-haspriority) method for details.</span></span>

 

<span data-ttu-id="e839b-274">若要在經過最長可接受的延遲之前開始，動畫管理員必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e839b-274">To start G before the longest acceptable delay has elapsed, the animation manager must do the following:</span></span>

-   <span data-ttu-id="e839b-275">修剪 F</span><span class="sxs-lookup"><span data-stu-id="e839b-275">Trim F</span></span>
-   <span data-ttu-id="e839b-276">取消 E</span><span class="sxs-lookup"><span data-stu-id="e839b-276">Cancel E</span></span>

<span data-ttu-id="e839b-277">當 E 取消時，會發現 D 和 F，並還原為其原始大綱：</span><span class="sxs-lookup"><span data-stu-id="e839b-277">When E is canceled, D and F are uncovered and revert to their original outlines:</span></span>

![顯示原始大綱的圖例](images/existingschedule1bwithlines.png)

<span data-ttu-id="e839b-279">動畫管理員不需要先取消或修剪 C，就能在其可接受的延遲時間最長之前進行排程，因此 C 和 G 的會議會決定 G 的開始時間。</span><span class="sxs-lookup"><span data-stu-id="e839b-279">The animation manager does not need to cancel or trim C to schedule before its longest acceptable delay has elapsed, so the meeting of C and G determines when G starts.</span></span>

![圖例顯示已修剪 f 以允許 c 和 g 符合](images/schedule1withgwithlines.png)

<span data-ttu-id="e839b-281">成功排程 G 之後，可以判斷其轉換的持續時間，並因此其外框的其餘部分是已知的。</span><span class="sxs-lookup"><span data-stu-id="e839b-281">After G has been successfully scheduled, the durations of its transitions can be determined, and the remainder of its outline is therefore known.</span></span> <span data-ttu-id="e839b-282">但是，如果後續已從排程中移除另一個腳本，則大綱可能會變更。</span><span class="sxs-lookup"><span data-stu-id="e839b-282">However, the outline can change if another storyboard is subsequently removed from the schedule.</span></span>

<span data-ttu-id="e839b-283">作為第二個範例，請考慮上述案例，但以較短的最長可接受延遲指定給 G。</span><span class="sxs-lookup"><span data-stu-id="e839b-283">As a second example, consider a scenario like that above, but with a shorter longest acceptable delay specified for G.</span></span>

![顯示上一個案例的圖例，以較短的最長可接受延遲為 g](images/existingschedule2withlines.png)

<span data-ttu-id="e839b-285">在此情況下，會採取下列動作：</span><span class="sxs-lookup"><span data-stu-id="e839b-285">In this case, the following actions are taken:</span></span>

-   <span data-ttu-id="e839b-286">修剪 F</span><span class="sxs-lookup"><span data-stu-id="e839b-286">Trim F</span></span>
-   <span data-ttu-id="e839b-287">取消 E</span><span class="sxs-lookup"><span data-stu-id="e839b-287">Cancel E</span></span>
-   <span data-ttu-id="e839b-288">取消 C</span><span class="sxs-lookup"><span data-stu-id="e839b-288">Cancel C</span></span>

<span data-ttu-id="e839b-289">此外，動畫管理員必須以顯示的數量來壓縮 D，讓 G 在可接受的最長延遲時間後啟動，而不會在稍後進行。</span><span class="sxs-lookup"><span data-stu-id="e839b-289">Also, the animation manager must compress D by the amount shown to enable G to start after its longest acceptable delay, and no later.</span></span>

![圖例顯示 d 必須壓縮以讓 g 以最長可接受的延遲啟動](images/trimmedandcancelledwithlines.png)

<span data-ttu-id="e839b-291">為了保留其相對時間，A、B 和 F 也會進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="e839b-291">To preserve their relative timing, A, B, and F are compressed as well.</span></span>

![顯示 a、b、d 和 f 壓縮的圖例](images/schedule2withgwithlines.png)

<span data-ttu-id="e839b-293">不過，不相關變數 (的分鏡腳本不會顯示) 不會被壓縮。</span><span class="sxs-lookup"><span data-stu-id="e839b-293">However, storyboards on unrelated variables (not shown) would not be compressed.</span></span>

<span data-ttu-id="e839b-294">同樣地，G 的大綱現在是已知的，與第一個案例中的結果不同，因為當 G 開始時，變數會有不同的值。</span><span class="sxs-lookup"><span data-stu-id="e839b-294">Once again, the outline of G is now known and is different from the result in the first scenario because the variables have different values when G begins.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e839b-295">相關主題</span><span class="sxs-lookup"><span data-stu-id="e839b-295">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e839b-296">**IUIAnimationManager**</span><span class="sxs-lookup"><span data-stu-id="e839b-296">**IUIAnimationManager**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[<span data-ttu-id="e839b-297">**IUIAnimationPriorityComparison**</span><span class="sxs-lookup"><span data-stu-id="e839b-297">**IUIAnimationPriorityComparison**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)
</dt> <dt>

[<span data-ttu-id="e839b-298">**IUIAnimationStoryboard**</span><span class="sxs-lookup"><span data-stu-id="e839b-298">**IUIAnimationStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)
</dt> <dt>

[<span data-ttu-id="e839b-299">**IUIAnimationTransitionLibrary**</span><span class="sxs-lookup"><span data-stu-id="e839b-299">**IUIAnimationTransitionLibrary**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> </dl>

 

