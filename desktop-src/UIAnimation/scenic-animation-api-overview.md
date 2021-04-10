---
title: Windows 動畫總覽
description: 本總覽提供 Windows 動畫管理員的簡介，並著重于重要元件和概念。
ms.assetid: de1380c9-6801-4178-9281-a23af7d71d77
keywords:
- Windows 動畫視窗動畫、總覽
- 動畫管理員物件視窗動畫，說明
- 動畫變數 Windows 動畫，說明
- 動畫計時器物件視窗動畫，說明
- 計時系統視窗動畫
- 上下文相關持續時間 Windows 動畫
- 符合 Windows 動畫的速度
- 爭用管理視窗動畫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a60b02b29d8d434cc93420f36c3cdca4428f94c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023575"
---
# <a name="windows-animation-overview"></a><span data-ttu-id="86d88-111">Windows 動畫總覽</span><span class="sxs-lookup"><span data-stu-id="86d88-111">Windows Animation Overview</span></span>

<span data-ttu-id="86d88-112">本總覽提供 Windows 動畫管理員的簡介，並著重于重要元件和概念。</span><span class="sxs-lookup"><span data-stu-id="86d88-112">This overview provides an introduction to the Windows Animation Manager and focuses on key components and concepts.</span></span> <span data-ttu-id="86d88-113">如需分鏡腳本和轉換的詳細資訊，請參閱分鏡腳本 [總覽](storyboard-construction.md)。</span><span class="sxs-lookup"><span data-stu-id="86d88-113">For more information on storyboards and transitions, see [Storyboard Overview](storyboard-construction.md).</span></span>

<span data-ttu-id="86d88-114">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="86d88-114">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="86d88-115">基本概念</span><span class="sxs-lookup"><span data-stu-id="86d88-115">Basic Concepts</span></span>](#basic-concepts)
-   [<span data-ttu-id="86d88-116">Windows 動畫的元件</span><span class="sxs-lookup"><span data-stu-id="86d88-116">Components of Windows Animation</span></span>](#components-of-windows-animation)
-   [<span data-ttu-id="86d88-117">Windows 動畫 API</span><span class="sxs-lookup"><span data-stu-id="86d88-117">The Windows Animation API</span></span>](#the-windows-animation-api)
-   [<span data-ttu-id="86d88-118">組態</span><span class="sxs-lookup"><span data-stu-id="86d88-118">Configurations</span></span>](#configurations)
    -   [<span data-ttu-id="86d88-119">應用程式驅動的動畫</span><span class="sxs-lookup"><span data-stu-id="86d88-119">Application-Driven Animation</span></span>](#application-driven-animation)
    -   [<span data-ttu-id="86d88-120">計時器驅動動畫</span><span class="sxs-lookup"><span data-stu-id="86d88-120">Timer-Driven Animation</span></span>](#timer-driven-animation)
-   [<span data-ttu-id="86d88-121">Advanced 功能</span><span class="sxs-lookup"><span data-stu-id="86d88-121">Advanced Features</span></span>](#advanced-features)
    -   [<span data-ttu-id="86d88-122">爭用管理</span><span class="sxs-lookup"><span data-stu-id="86d88-122">Contention Management</span></span>](#contention-management)
-   [<span data-ttu-id="86d88-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="86d88-123">Related topics</span></span>](#related-topics)

## <a name="basic-concepts"></a><span data-ttu-id="86d88-124">基本概念</span><span class="sxs-lookup"><span data-stu-id="86d88-124">Basic Concepts</span></span>

<span data-ttu-id="86d88-125">*動畫* 是連續的靜止影像順序，會在播放時產生移動的假像。</span><span class="sxs-lookup"><span data-stu-id="86d88-125">*Animation* is a sequence of successive still images that produces an illusion of movement when played back.</span></span> <span data-ttu-id="86d88-126">在其使用者介面中使用互動式動畫可提供應用程式獨特的特性，以及改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="86d88-126">Using interactive animation in its user interface can give an application a unique personality as well as improve the user experience.</span></span> <span data-ttu-id="86d88-127">動畫可協助您在使用者介面中傳達主要狀態變更，並協助管理使用者介面的複雜度。</span><span class="sxs-lookup"><span data-stu-id="86d88-127">Animation can help to communicate major state changes in the user interface and help to manage the complexity of the user interface.</span></span> <span data-ttu-id="86d88-128">動畫也可以新增到使用者對應用程式品質的認知。</span><span class="sxs-lookup"><span data-stu-id="86d88-128">Animation can also add to the user's perception of the quality of an application.</span></span>

<span data-ttu-id="86d88-129">例如，工作列中使用 Windows 動畫來協助您管理和存取檔案和程式，以及放大鏡來放大螢幕的不同部分，讓使用者更容易看見。</span><span class="sxs-lookup"><span data-stu-id="86d88-129">As examples, Windows Animation is used in the taskbar to help you manage and access files and programs, and Magnifier to enlarge different parts of the screen to make them easier for users to see.</span></span>

<span data-ttu-id="86d88-130">動畫的基礎單位是要進行動畫的視覺元素特性，以及該特性如何隨著時間而變更的描述。</span><span class="sxs-lookup"><span data-stu-id="86d88-130">The fundamental units of an animation are the characteristic of a visual element to be animated and the description of how that characteristic changes over time.</span></span> <span data-ttu-id="86d88-131">應用程式可以建立各種特性的動畫，例如位置、色彩、大小、旋轉、對比和不透明度。</span><span class="sxs-lookup"><span data-stu-id="86d88-131">An application can animate a wide variety of characteristics such as position, color, size, rotation, contrast, and opacity.</span></span>

<span data-ttu-id="86d88-132">在 Windows 動畫中， *動畫變數* 表示要進行動畫的特性。</span><span class="sxs-lookup"><span data-stu-id="86d88-132">In Windows Animation, an *animation variable* represents the characteristic to be animated.</span></span> <span data-ttu-id="86d88-133">*轉換* 會描述動畫變數的值如何隨著動畫而變更。</span><span class="sxs-lookup"><span data-stu-id="86d88-133">A *transition* describes how the value of that animation variable changes as animation occurs.</span></span> <span data-ttu-id="86d88-134">例如，視覺元素可能會有指定其不透明度的動畫變數，而使用者動作可能會產生將該不透明度從50值轉換為100的轉換，表示從半透明到完全不透明的動畫。</span><span class="sxs-lookup"><span data-stu-id="86d88-134">For example, a visual element might have an animation variable that specifies its opacity, and a user action might generate a transition that takes that opacity from a value of 50 to 100, representing an animation from semi-transparent to fully opaque.</span></span>

<span data-ttu-id="86d88-135">分鏡 *腳本是一組在一* 段時間內套用至一或多個動畫變數的轉換。</span><span class="sxs-lookup"><span data-stu-id="86d88-135">A *storyboard* is a set of transitions applied to one or more animation variables over time.</span></span> <span data-ttu-id="86d88-136">應用程式會藉由建立和播放腳本，然後繪製離散框架的順序來顯示動畫，因為動畫變數的值會隨著時間而變更。</span><span class="sxs-lookup"><span data-stu-id="86d88-136">An application displays animations by constructing and playing storyboards and then drawing sequences of discrete frames as the values of animation variables change over time.</span></span>

## <a name="components-of-windows-animation"></a><span data-ttu-id="86d88-137">Windows 動畫的元件</span><span class="sxs-lookup"><span data-stu-id="86d88-137">Components of Windows Animation</span></span>

<span data-ttu-id="86d88-138">Windows 動畫包含下列元件：</span><span class="sxs-lookup"><span data-stu-id="86d88-138">Windows Animation consists of the following components:</span></span>

<dl> <dt>

<span data-ttu-id="86d88-139"><span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>動畫管理員</span><span class="sxs-lookup"><span data-stu-id="86d88-139"><span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>animation manager</span></span>
</dt> <dd>

<span data-ttu-id="86d88-140">應用程式會使用動畫管理員物件來建立動畫變數和分鏡腳本、排程和控制動畫，以及在應用程式繪製每個畫面格之前更新狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="86d88-140">Applications use an animation manager object to create animation variables and storyboards, schedule and control animations, and update state information before the application draws each frame.</span></span> <span data-ttu-id="86d88-141">單一動畫管理員物件通常會管理整個應用程式的所有動畫，因此可對所有已排程的分鏡腳本進行全域控制。</span><span class="sxs-lookup"><span data-stu-id="86d88-141">A single animation manager object typically manages all animations across an application and therefore has global control over all scheduled storyboards.</span></span>

</dd> <dt>

<span data-ttu-id="86d88-142"><span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>動畫變數</span><span class="sxs-lookup"><span data-stu-id="86d88-142"><span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>animation variables</span></span>
</dt> <dd>

<span data-ttu-id="86d88-143">在開始任何動畫之前，應用程式必須建立動畫變數物件。</span><span class="sxs-lookup"><span data-stu-id="86d88-143">Before starting any animations, an application needs to create animation variable objects.</span></span> <span data-ttu-id="86d88-144">動畫變數表示要進行動畫的視覺元素的其中一個層面。</span><span class="sxs-lookup"><span data-stu-id="86d88-144">An animation variable represents one aspect of a visual element to be animated.</span></span> <span data-ttu-id="86d88-145">變數是純量浮點值，雖然值可以四捨五入為整數值。</span><span class="sxs-lookup"><span data-stu-id="86d88-145">The variable is a scalar floating-point value, although the value can be rounded to an integer value.</span></span>

<span data-ttu-id="86d88-146">動畫變數的存留期通常與用來建立動畫的視覺元素相同。</span><span class="sxs-lookup"><span data-stu-id="86d88-146">An animation variable typically has the same lifetime as the visual element it is to animate.</span></span> <span data-ttu-id="86d88-147">建立變數時，會指定動畫變數的初始值。</span><span class="sxs-lookup"><span data-stu-id="86d88-147">The initial value of an animation variable is specified when the variable is created.</span></span> <span data-ttu-id="86d88-148">之後，無法直接變更其值;您必須透過動畫管理員來更新它。</span><span class="sxs-lookup"><span data-stu-id="86d88-148">Thereafter, its value cannot be changed directly; it must be updated through the animation manager.</span></span>

<span data-ttu-id="86d88-149">動畫變數可以透過 *標記* 來識別，也就是將整數識別碼與 COM 物件的指標配對。</span><span class="sxs-lookup"><span data-stu-id="86d88-149">An animation variable can be identified by a *tag*, which is a pairing of an integer identifier with a pointer to a COM object.</span></span> <span data-ttu-id="86d88-150">標記不需要是唯一的，除非應用程式使用它來搜尋變數。</span><span class="sxs-lookup"><span data-stu-id="86d88-150">A tag need not be unique, unless the application uses it to search for a variable.</span></span> <span data-ttu-id="86d88-151">根據預設，動畫變數沒有標記，而任何讀取其標記的嘗試都將會失敗，直到已設定一個標記為止。</span><span class="sxs-lookup"><span data-stu-id="86d88-151">By default, an animation variable does not have a tag, and any attempts to read its tag will fail until one has been set.</span></span>

</dd> <dt>

<span data-ttu-id="86d88-152"><span id="timing_system"></span><span id="TIMING_SYSTEM"></span>計時系統</span><span class="sxs-lookup"><span data-stu-id="86d88-152"><span id="timing_system"></span><span id="TIMING_SYSTEM"></span>timing system</span></span>
</dt> <dd>

<span data-ttu-id="86d88-153">Windows 動畫包含時間系統，可協助確保動畫是以平滑且一致的畫面播放速率轉譯，同時也可減少系統資源忙碌時的系統資源使用方式。</span><span class="sxs-lookup"><span data-stu-id="86d88-153">Windows Animation includes a timing system that helps to ensure that animations are rendered at a frame rate that is smooth and consistent, while also reducing the use of system resources for rendering when the system is busy.</span></span> <span data-ttu-id="86d88-154">*計時器* 會自動指出一小段時間（稱為 *滴答*），以協助管理動畫呈現。</span><span class="sxs-lookup"><span data-stu-id="86d88-154">A *timer* helps to manage animation rendering by automatically indicating the passage of a small unit of time, called a *tick*.</span></span> <span data-ttu-id="86d88-155">計時系統會監視整體系統轉譯 *效能，並* 以動態方式增加或減少刻度的頻率來調整動畫。</span><span class="sxs-lookup"><span data-stu-id="86d88-155">The timing system monitors overall system rendering performance and *throttles* animations by dynamically increasing or decreasing the frequency of ticks.</span></span> <span data-ttu-id="86d88-156">應用程式可讓計時器驅動動畫管理員，並且可以註冊處理常式，以便在管理員更新每個刻度之前和之後收到通知。</span><span class="sxs-lookup"><span data-stu-id="86d88-156">Applications can let a timer drive the animation manager and can register a handler to be notified before and after the manager is updated for each tick.</span></span> <span data-ttu-id="86d88-157">應用程式可以為計時器指定可接受的最小動畫畫面播放速率，並且在動畫的實際畫面播放速率低於此速率時收到通知。</span><span class="sxs-lookup"><span data-stu-id="86d88-157">Applications can specify the minimum acceptable animation frame rate for a timer and be notified if an animation's actual frame rate falls below this rate.</span></span>

<span data-ttu-id="86d88-158">若要節省系統資源，您可以設定計時器，在沒有任何動畫發生時將其停用。</span><span class="sxs-lookup"><span data-stu-id="86d88-158">To conserve system resources, a timer can be configured to disable itself when no animation is taking place.</span></span>

</dd> </dl>

## <a name="the-windows-animation-api"></a><span data-ttu-id="86d88-159">Windows 動畫 API</span><span class="sxs-lookup"><span data-stu-id="86d88-159">The Windows Animation API</span></span>

<span data-ttu-id="86d88-160">Windows 動畫 API 是單一執行緒的 COM 型 API，可為開發人員提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="86d88-160">The Windows Animation API is a single-threaded COM-based API that provides the following features for developers:</span></span>

-   <span data-ttu-id="86d88-161">動畫管理員物件 [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))，用於建立動畫物件和控制動畫</span><span class="sxs-lookup"><span data-stu-id="86d88-161">An animation manager object, [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)), for creating animation objects and controlling animations</span></span>
-   <span data-ttu-id="86d88-162">動畫變數和分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="86d88-162">Animation variables and storyboards</span></span>
-   <span data-ttu-id="86d88-163">立即可用的轉換基礎程式庫 [**UIAnimationTransitionLibrary**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86d88-163">A foundational library, [**UIAnimationTransitionLibrary**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85)), of ready-to-use transitions</span></span>
-   <span data-ttu-id="86d88-164">計時器物件（ [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))），用來判斷目前的時間，以及選擇性地驅動動畫</span><span class="sxs-lookup"><span data-stu-id="86d88-164">A timer object, [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)), for determining the current time and, optionally, for driving animation</span></span>
-   <span data-ttu-id="86d88-165">用於監視動畫狀態和進度的事件攔截</span><span class="sxs-lookup"><span data-stu-id="86d88-165">Event hooks for monitoring the state and progress of animation</span></span>

<span data-ttu-id="86d88-166">如需完整的 API 參考，請參閱 [Windows 動畫參考](windows-animation-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="86d88-166">For the complete API reference, see [Windows Animation Reference](windows-animation-reference.md).</span></span> <span data-ttu-id="86d88-167">如需範例程式碼，請參閱 [Windows 動畫](using-windows-animation.md) 工作和 [windows 動畫範例](windows-animation-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="86d88-167">For example code, see [Windows Animation Tasks](using-windows-animation.md) and [Windows Animation Samples](windows-animation-samples.md).</span></span>

## <a name="configurations"></a><span data-ttu-id="86d88-168">設定</span><span class="sxs-lookup"><span data-stu-id="86d88-168">Configurations</span></span>

<span data-ttu-id="86d88-169">應用程式必須在排程新動畫之前取得目前的時間。</span><span class="sxs-lookup"><span data-stu-id="86d88-169">Applications must get the current time before scheduling a new animation.</span></span> <span data-ttu-id="86d88-170">以下是 Windows 動畫所支援的計時機制：</span><span class="sxs-lookup"><span data-stu-id="86d88-170">The following are the timing mechanisms supported by Windows Animation:</span></span>

-   [<span data-ttu-id="86d88-171">應用程式驅動的動畫</span><span class="sxs-lookup"><span data-stu-id="86d88-171">Application-Driven Animation</span></span>](#application-driven-animation)
-   [<span data-ttu-id="86d88-172">計時器驅動動畫</span><span class="sxs-lookup"><span data-stu-id="86d88-172">Timer-Driven Animation</span></span>](#timer-driven-animation)

### <a name="application-driven-animation"></a><span data-ttu-id="86d88-173">Application-Driven 動畫</span><span class="sxs-lookup"><span data-stu-id="86d88-173">Application-Driven Animation</span></span>

<span data-ttu-id="86d88-174">使用硬體加速圖形 API 的應用程式可以與監視器重新整理頻率進行同步處理，以轉譯平滑動畫。</span><span class="sxs-lookup"><span data-stu-id="86d88-174">Applications using a hardware-accelerated graphics API can synchronize with the monitor refresh rate to render smooth animations.</span></span> <span data-ttu-id="86d88-175">或者，應用程式可以使用自己的計時機制，來判斷何時繪製動畫的每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="86d88-175">Alternately, an application may use a timing mechanism of its own to determine when to draw each frame of an animation.</span></span> <span data-ttu-id="86d88-176">在任一種情況下，應用程式都會告知動畫管理員何時更新其狀態。</span><span class="sxs-lookup"><span data-stu-id="86d88-176">In either case, the application will tell the animation manager when to update its state.</span></span> <span data-ttu-id="86d88-177">動畫計時器仍然可以用來判斷具有高精確度的目前時間，以動畫管理員所需的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="86d88-177">An animation timer can still be used to determine the current time with high precision, in the units required by the animation manager.</span></span>

<span data-ttu-id="86d88-178">下圖顯示當應用程式直接驅動動畫更新時，應用程式與 Windows 動畫元件之間的互動。</span><span class="sxs-lookup"><span data-stu-id="86d88-178">The following diagram shows the interactions between an application and the Windows Animation components when the application is driving animation updates directly.</span></span>

![此圖顯示應用程式直接驅動動畫更新時，應用程式與 windows 動畫元件之間的互動。](images/animationupdates.png)

<span data-ttu-id="86d88-180">在最簡單的設定中，應用程式會在每次螢幕重新整理時重繪所有專案，即使沒有播放動畫也是一樣。</span><span class="sxs-lookup"><span data-stu-id="86d88-180">In the simplest configuration, an application will redraw everything every time the screen is refreshed, even when no animations are playing.</span></span> <span data-ttu-id="86d88-181">為了避免浪費的工作，應用程式可以註冊管理員事件處理常式，以便在有動畫排程時收到通知，並且可以偵測排程是空的，讓它可以停止重繪。</span><span class="sxs-lookup"><span data-stu-id="86d88-181">To avoid wasted work, an application can register a manager event handler to be notified when there are animations scheduled, and can detect when the schedule is empty so that it can stop redrawing.</span></span>

### <a name="timer-driven-animation"></a><span data-ttu-id="86d88-182">Timer-Driven 動畫</span><span class="sxs-lookup"><span data-stu-id="86d88-182">Timer-Driven Animation</span></span>

<span data-ttu-id="86d88-183">應用程式可能會讓動畫計時器告知動畫管理員何時更新其狀態，而且只會在發生每項更新時收到通知，而不是直接更新動畫管理員。</span><span class="sxs-lookup"><span data-stu-id="86d88-183">Rather than updating the animation manager directly, applications may let the animation timer tell the animation manager when to update its state, and simply be notified when each update has taken place.</span></span> <span data-ttu-id="86d88-184">這種方法建議用於舊版圖形 Api。</span><span class="sxs-lookup"><span data-stu-id="86d88-184">This approach is recommended for older graphics APIs.</span></span> <span data-ttu-id="86d88-185">一般而言，如果可以與監視器重新整理頻率進行同步處理，最好是這麼做，並使用應用程式驅動的動畫。</span><span class="sxs-lookup"><span data-stu-id="86d88-185">In general, if it is possible to synchronize with the monitor refresh rate, it is better to do so and use application-driven animation.</span></span>

<span data-ttu-id="86d88-186">下圖顯示當動畫計時器驅動動畫更新時，應用程式與 Windows 動畫元件之間的互動。</span><span class="sxs-lookup"><span data-stu-id="86d88-186">The following diagram shows the interactions between an application and the Windows Animation components when the animation timer is driving animation updates.</span></span>

![此圖顯示當動畫計時器驅動動畫更新時，應用程式與 windows 動畫元件之間的互動。](images/animationtimerupdates.png)

<span data-ttu-id="86d88-188">計時器可以設定為只有在已排程動畫時才執行;這麼做只是在計時器和動畫管理員連接時傳遞特定參數的簡單做法。</span><span class="sxs-lookup"><span data-stu-id="86d88-188">The timer can be configured to run only when the animations are scheduled; doing so is a simple matter of passing a particular parameter when the timer and animation manager are connected.</span></span>

## <a name="advanced-features"></a><span data-ttu-id="86d88-189">進階功能</span><span class="sxs-lookup"><span data-stu-id="86d88-189">Advanced Features</span></span>

<span data-ttu-id="86d88-190">除了支援動畫的基本基礎之外，Windows 動畫還支援數種先進的動畫技術，包括：</span><span class="sxs-lookup"><span data-stu-id="86d88-190">Beyond a basic foundation to support animation, Windows Animation includes support for several advanced animation techniques, including:</span></span>

<dl> <dt>

<span data-ttu-id="86d88-191"><span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*區分內容的持續時間*</span><span class="sxs-lookup"><span data-stu-id="86d88-191"><span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*context-sensitive duration*</span></span>
</dt> <dd>

<span data-ttu-id="86d88-192">轉換的持續時間不需要固定;您可以根據轉換開始時的動畫變數值和速度來決定此值。</span><span class="sxs-lookup"><span data-stu-id="86d88-192">The duration of a transition need not be fixed; it can be determined based on the value and velocity of the animated variable when the transition begins.</span></span>

</dd> <dt>

<span data-ttu-id="86d88-193"><span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*速度相符*</span><span class="sxs-lookup"><span data-stu-id="86d88-193"><span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*velocity matching*</span></span>
</dt> <dd>

<span data-ttu-id="86d88-194">如果移動物件的位置和速度在值之間沒有立即跳躍，移動物件的位置和速度通常會更適合眼睛。</span><span class="sxs-lookup"><span data-stu-id="86d88-194">Movement is generally more pleasing to the eye if a moving object's position and velocity do not jump instantaneously between values.</span></span> <span data-ttu-id="86d88-195">當新的分鏡腳本中斷目前現正播放的腳本時，速度比對可讓新的分鏡腳本在上一次結束的位置順利挑選。</span><span class="sxs-lookup"><span data-stu-id="86d88-195">When a new storyboard interrupts one that is currently playing, velocity matching enables the new storyboard to pick up smoothly where the previous one ended.</span></span>

</dd> <dt>

<span data-ttu-id="86d88-196"><span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*爭用管理*</span><span class="sxs-lookup"><span data-stu-id="86d88-196"><span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*contention management*</span></span>
</dt> <dd>

<span data-ttu-id="86d88-197">如果兩個分鏡腳本需要同時更新相同的動畫變數，則會發生排程衝突。</span><span class="sxs-lookup"><span data-stu-id="86d88-197">If two storyboards need to update the same animation variable simultaneously, a scheduling conflict occurs.</span></span> <span data-ttu-id="86d88-198">Windows 動畫可讓應用程式判斷任何兩個分鏡腳本的相對優先權，而不需要每個分鏡腳本有特定的數值優先順序。</span><span class="sxs-lookup"><span data-stu-id="86d88-198">Rather than requiring a specific numeric priority for each storyboard, Windows Animation enables the application to determine the relative priorities of any two storyboards.</span></span>

</dd> </dl>

### <a name="contention-management"></a><span data-ttu-id="86d88-199">爭用管理</span><span class="sxs-lookup"><span data-stu-id="86d88-199">Contention Management</span></span>

<span data-ttu-id="86d88-200">開發人員可以執行 *優先順序比較* 回呼，以比較已排程之分鏡腳本的優先順序以及已在排程中的分鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="86d88-200">Developers can implement a *priority comparison* callback to compare the priority of the storyboard of being scheduled and the storyboard that is already in the schedule.</span></span> <span data-ttu-id="86d88-201">執行優先順序比較的應用程式可以使用任何慣用的邏輯來判斷分鏡腳本預先 empts 另一個的時間。</span><span class="sxs-lookup"><span data-stu-id="86d88-201">An application implementing a priority comparison can use any preferred logic to determine when a storyboard pre-empts another.</span></span> <span data-ttu-id="86d88-202">為了解決排程衝突，Windows 動畫會以下列順序要求應用程式執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="86d88-202">To resolve the scheduling conflict, Windows Animation asks the application which of these actions may be taken, in the following order:</span></span>

-   <span data-ttu-id="86d88-203">**取消已排程的分鏡腳本。**</span><span class="sxs-lookup"><span data-stu-id="86d88-203">**Cancel the scheduled storyboard.**</span></span> <span data-ttu-id="86d88-204">如果排定的分鏡腳本尚未開始播放，它可能會取消並立即從排程中移除。</span><span class="sxs-lookup"><span data-stu-id="86d88-204">If the scheduled storyboard has not yet started to play, it might be canceled and immediately removed from the schedule.</span></span>
-   <span data-ttu-id="86d88-205">**修剪排程的分鏡腳本。**</span><span class="sxs-lookup"><span data-stu-id="86d88-205">**Trim the scheduled storyboard.**</span></span> <span data-ttu-id="86d88-206">當新的分鏡腳本修剪排程的分鏡腳本時，排程的分鏡腳本會在新的腳本開始建立動畫時立即停止影響變數。</span><span class="sxs-lookup"><span data-stu-id="86d88-206">When a new storyboard trims a scheduled storyboard, the scheduled storyboard ceases to affect the variable as soon as the new storyboard begins to animate it.</span></span> <span data-ttu-id="86d88-207">系統會比對速度，讓新的分鏡腳本能夠順暢地挑選前一個。</span><span class="sxs-lookup"><span data-stu-id="86d88-207">The velocities are matched, enabling the new storyboard to pick up smoothly where the previous one left off.</span></span>
-   <span data-ttu-id="86d88-208">**結束排程的分鏡腳本。**</span><span class="sxs-lookup"><span data-stu-id="86d88-208">**Conclude the scheduled storyboard.**</span></span> <span data-ttu-id="86d88-209">只有當分鏡腳本包含了無限期重複的迴圈時，才會結束。</span><span class="sxs-lookup"><span data-stu-id="86d88-209">A storyboard may be concluded only if it contains a loop that repeats indefinitely.</span></span> <span data-ttu-id="86d88-210">如果腳本在結束時為這類迴圈，則目前的重複項會完成，而腳本的其餘部分則會播放。</span><span class="sxs-lookup"><span data-stu-id="86d88-210">If the storyboard is in such a loop when concluded, the current repetition completes, and the remainder of the storyboard then plays.</span></span> <span data-ttu-id="86d88-211">如果在分鏡腳本結束時，迴圈尚未開始，則會完全略過迴圈。</span><span class="sxs-lookup"><span data-stu-id="86d88-211">If the loop has not yet begun when a storyboard is concluded, the loop is skipped entirely.</span></span>
-   <span data-ttu-id="86d88-212">**壓縮已排程的分鏡腳本。**</span><span class="sxs-lookup"><span data-stu-id="86d88-212">**Compress the scheduled storyboard.**</span></span> <span data-ttu-id="86d88-213">如果無法選擇修剪或取消已排程的分鏡腳本，則可以完成腳本。</span><span class="sxs-lookup"><span data-stu-id="86d88-213">If trimming or canceling the scheduled storyboard is not an option, the storyboard is allowed to complete.</span></span> <span data-ttu-id="86d88-214">Windows 動畫引進了可將排程的分鏡腳本 (的時間以及在) 之前排定的任何分鏡腳本，讓變數更快達到其最終狀態的可能性。</span><span class="sxs-lookup"><span data-stu-id="86d88-214">Windows Animation introduces the possibility of compressing the time available for the scheduled storyboard (and any storyboards scheduled before it), so the variables reach their final state more quickly.</span></span> <span data-ttu-id="86d88-215">套用壓縮時，會暫時加速受影響的分鏡腳本，讓它們的播放速度更快。</span><span class="sxs-lookup"><span data-stu-id="86d88-215">When compression is applied, time is temporarily accelerated for affected storyboards, so they play faster.</span></span>

<span data-ttu-id="86d88-216">如果註冊的優先順序比較物件不允許上述任何動作，則嘗試排程新的分鏡腳本會失敗。</span><span class="sxs-lookup"><span data-stu-id="86d88-216">If none of the above actions is allowed by the registered priority comparison objects, the attempt to schedule the new storyboard fails.</span></span> <span data-ttu-id="86d88-217">根據預設，所有的分鏡腳本都可以修剪、結束或壓縮以防止失敗，但無法取消任何。</span><span class="sxs-lookup"><span data-stu-id="86d88-217">By default, all storyboards can be trimmed, concluded, or compressed to prevent failure, but none can be canceled.</span></span>

<span data-ttu-id="86d88-218">下圖顯示分鏡腳本的生命週期，使用 UI 動畫分鏡腳本 [**\_ \_ \_ 狀態**](/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status) 列舉所定義的狀態。</span><span class="sxs-lookup"><span data-stu-id="86d88-218">The following diagram shows the life cycle of a storyboard, using the states defined by the [**UI\_ANIMATION\_STORYBOARD\_STATUS**](/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status) enumeration.</span></span> <span data-ttu-id="86d88-219">應用程式會使用 Windows 動畫 API 來建立分鏡腳本，並提交以進行排程。</span><span class="sxs-lookup"><span data-stu-id="86d88-219">Applications use the Windows Animation API to build a storyboard and submit it for scheduling.</span></span> <span data-ttu-id="86d88-220">動畫管理員會排定分鏡腳本並管理動畫。</span><span class="sxs-lookup"><span data-stu-id="86d88-220">The animation manager schedules the storyboard and manages the animation.</span></span>

![顯示動畫管理員如何排程腳本和管理動畫的圖表。](images/statediagram.png)

<span data-ttu-id="86d88-222">如需分鏡腳本排程和管理的詳細資訊，請參閱分鏡腳本 [總覽](storyboard-construction.md)。</span><span class="sxs-lookup"><span data-stu-id="86d88-222">For more information on storyboard scheduling and management, see [Storyboard Overview](storyboard-construction.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="86d88-223">相關主題</span><span class="sxs-lookup"><span data-stu-id="86d88-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86d88-224">Windows 動畫參考</span><span class="sxs-lookup"><span data-stu-id="86d88-224">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> <dt>

[<span data-ttu-id="86d88-225">Windows 動畫範例</span><span class="sxs-lookup"><span data-stu-id="86d88-225">Windows Animation Samples</span></span>](windows-animation-samples.md)
</dt> <dt>

[<span data-ttu-id="86d88-226">Windows 動畫工作</span><span class="sxs-lookup"><span data-stu-id="86d88-226">Windows Animation Tasks</span></span>](using-windows-animation.md)
</dt> </dl>

 

 