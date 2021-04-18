---
title: '動畫 (DirectComposition) '
description: 本主題討論 Microsoft DirectComposition 動畫的基本概念。
ms.assetid: 65DA3971-97C0-4B59-BC67-287AAEAAE340
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7462a10fd83b45c1b90450fdde806ef306a2f6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106965461"
---
# <a name="animation-directcomposition"></a><span data-ttu-id="91770-103">動畫 (DirectComposition) </span><span class="sxs-lookup"><span data-stu-id="91770-103">Animation (DirectComposition)</span></span>

> [!NOTE]
> <span data-ttu-id="91770-104">針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。</span><span class="sxs-lookup"><span data-stu-id="91770-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="91770-105">如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。</span><span class="sxs-lookup"><span data-stu-id="91770-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="91770-106">本主題討論 Microsoft DirectComposition 動畫的基本概念。</span><span class="sxs-lookup"><span data-stu-id="91770-106">This topic discusses the basics of Microsoft DirectComposition animation.</span></span> <span data-ttu-id="91770-107">它包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="91770-107">It contains the following topics:</span></span>

-   [<span data-ttu-id="91770-108">什麼是動畫？</span><span class="sxs-lookup"><span data-stu-id="91770-108">What is an animation?</span></span>](#what-is-an-animation)
-   [<span data-ttu-id="91770-109">可以動畫顯示的屬性</span><span class="sxs-lookup"><span data-stu-id="91770-109">Properties that can be animated</span></span>](#properties-that-can-be-animated)
-   [<span data-ttu-id="91770-110">動畫函數</span><span class="sxs-lookup"><span data-stu-id="91770-110">Animation functions</span></span>](#animation-functions)
-   [<span data-ttu-id="91770-111">動畫區段</span><span class="sxs-lookup"><span data-stu-id="91770-111">Animation segments</span></span>](#animation-segments)
    -   [<span data-ttu-id="91770-112">三次區段</span><span class="sxs-lookup"><span data-stu-id="91770-112">Cubic segment</span></span>](#cubic-segment)
    -   [<span data-ttu-id="91770-113">正弦曲線區段</span><span class="sxs-lookup"><span data-stu-id="91770-113">Sinusoidal segment</span></span>](#sinusoidal-segment)
    -   [<span data-ttu-id="91770-114">重複區段</span><span class="sxs-lookup"><span data-stu-id="91770-114">Repeat segment</span></span>](#repeat-segment)
    -   [<span data-ttu-id="91770-115">結束區段</span><span class="sxs-lookup"><span data-stu-id="91770-115">End segment</span></span>](#end-segment)
-   [<span data-ttu-id="91770-116">與 Windows 動畫管理員的相容性</span><span class="sxs-lookup"><span data-stu-id="91770-116">Compatibility with Windows Animation Manager</span></span>](#compatibility-with-windows-animation-manager)
-   [<span data-ttu-id="91770-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="91770-117">Related topics</span></span>](#related-topics)

## <a name="what-is-an-animation"></a><span data-ttu-id="91770-118">什麼是動畫？</span><span class="sxs-lookup"><span data-stu-id="91770-118">What is an animation?</span></span>

<span data-ttu-id="91770-119">*動畫* 是在每次變更之後，于一段時間內快速進行視覺效果的累加式變更時，所建立的光學假像。</span><span class="sxs-lookup"><span data-stu-id="91770-119">*Animation* is an optical illusion created by quickly making incremental changes to a visual over a period of time while redrawing the visual after each change is made.</span></span> <span data-ttu-id="91770-120">由於重新繪製的速度很快，因此大腦會將累加的變更視為單一變更場景，就像在影片或實況活動影片中一樣。</span><span class="sxs-lookup"><span data-stu-id="91770-120">Because the redraws occur quickly, the brain perceives the incremental changes as a single changing scene, just as in a movie or video of live action.</span></span>

<span data-ttu-id="91770-121">下表說明一些使用動畫的典型方式。</span><span class="sxs-lookup"><span data-stu-id="91770-121">The following table describes some of the typical ways of using animation.</span></span>

| <span data-ttu-id="91770-122">動畫</span><span class="sxs-lookup"><span data-stu-id="91770-122">Animation</span></span>                 | <span data-ttu-id="91770-123">Description</span><span class="sxs-lookup"><span data-stu-id="91770-123">Description</span></span>                                                                                                                                                                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91770-124">捲動</span><span class="sxs-lookup"><span data-stu-id="91770-124">Scrolling</span></span>                 | <span data-ttu-id="91770-125">使用動畫將功能（例如物理模擬動力）新增至滾動清單控制項。</span><span class="sxs-lookup"><span data-stu-id="91770-125">Use animation to add features like physics-emulating momentum to a scrolling list control.</span></span>                                                                                                                                                           |
| <span data-ttu-id="91770-126">場景轉換</span><span class="sxs-lookup"><span data-stu-id="91770-126">Scene transitions</span></span>         | <span data-ttu-id="91770-127">使用動畫來建立導覽場景轉換，以提供工作流程中工作之間的持續性。</span><span class="sxs-lookup"><span data-stu-id="91770-127">Use animation to create navigational scene transitions that provide continuity between tasks in a workflow.</span></span> <span data-ttu-id="91770-128">導覽場景轉換會提供內容，顯示使用者的位置、位置，以及接下來需要前往的位置。</span><span class="sxs-lookup"><span data-stu-id="91770-128">Navigational scene transitions provide context that shows the user where they have been, where they are, and where they need to go next.</span></span> |
| <span data-ttu-id="91770-129">跨視窗互動</span><span class="sxs-lookup"><span data-stu-id="91770-129">Cross-window interactions</span></span> | <span data-ttu-id="91770-130">將不同應用程式的 UI 專案以動畫顯示，讓他們能夠理解它們之間的無縫持續性，以協助使用者完成工作，包括從某個應用程式切換到另一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="91770-130">Animate UI elements of different applications in a way that gives the perception of seamless continuity between them to help the user complete tasks that involve switching from one application to another.</span></span>                                         |



 

## <a name="properties-that-can-be-animated"></a><span data-ttu-id="91770-131">可以動畫顯示的屬性</span><span class="sxs-lookup"><span data-stu-id="91770-131">Properties that can be animated</span></span>

<span data-ttu-id="91770-132">在 DirectComposition 中，您會將動畫套用至定義視覺效果之物件的個別屬性，以建立視覺效果的動畫。</span><span class="sxs-lookup"><span data-stu-id="91770-132">In DirectComposition, you animate a visual by applying animation to individual properties of the objects that define the visual.</span></span> <span data-ttu-id="91770-133">例如，如果您想要在螢幕上水準移動視覺效果，則會將動畫套用至視覺效果的 OffsetX 屬性。</span><span class="sxs-lookup"><span data-stu-id="91770-133">For example, if you want to move a visual horizontally across the screen, you would apply animation to the OffsetX property of the visual.</span></span> <span data-ttu-id="91770-134">同樣地，如果您想要對視覺效果進行簡單的動畫2D 旋轉，則會將動畫套用至2D 轉換物件的 Angle 屬性，然後將2D 轉換物件套用至視覺效果的轉換屬性。</span><span class="sxs-lookup"><span data-stu-id="91770-134">Similarly, if you wanted to do a simple animated 2D rotation of a visual, you would apply animation to the Angle property of a 2D transform object, and then apply the 2D transform object to the Transform property of the visual.</span></span>

<span data-ttu-id="91770-135">DirectComposition 可讓您將動畫套用至任何接受純量值的物件屬性。</span><span class="sxs-lookup"><span data-stu-id="91770-135">DirectComposition enables you to apply animation to any object property that takes a scalar value.</span></span> <span data-ttu-id="91770-136">您可以同時將動畫套用至多個屬性和多個物件。</span><span class="sxs-lookup"><span data-stu-id="91770-136">You can apply simultaneous animations to multiple properties and multiple objects.</span></span>

<span data-ttu-id="91770-137">DirectComposition 會在個別的執行緒上執行動畫。</span><span class="sxs-lookup"><span data-stu-id="91770-137">DirectComposition runs animations on a separate thread.</span></span> <span data-ttu-id="91770-138">您可以啟動一組動畫或一組動畫，然後對應用程式執行緒執行其他工作，甚至讓執行緒進入睡眠狀態，而組合引擎會以適當的畫面播放速率執行動畫。</span><span class="sxs-lookup"><span data-stu-id="91770-138">You can start an animation or set of animations and then do other work on your application threads, or even put threads to sleep, while the composition engine runs the animations at the appropriate frame rate.</span></span>

## <a name="animation-functions"></a><span data-ttu-id="91770-139">動畫函數</span><span class="sxs-lookup"><span data-stu-id="91770-139">Animation functions</span></span>

<span data-ttu-id="91770-140">DirectComposition 會根據您定義的動畫函式，將物件屬性動畫。</span><span class="sxs-lookup"><span data-stu-id="91770-140">DirectComposition animates an object property based on an animation function that you define.</span></span> <span data-ttu-id="91770-141">*動畫* 函式是一種結構，可指定物件屬性值在一段時間內的變更方式。</span><span class="sxs-lookup"><span data-stu-id="91770-141">An *animation function* is a construct that specifies how the value of an object property changes over a period of time.</span></span> <span data-ttu-id="91770-142">例如，您可以定義一個動畫函式，在4秒的過程中，將屬性的值從1變更為360。</span><span class="sxs-lookup"><span data-stu-id="91770-142">For example, you could define an animation function that changes the value of a property from 1 to 360 over the course of 4 seconds.</span></span> <span data-ttu-id="91770-143">然後，如果您將動畫函式套用至2D 旋轉轉換物件的 Angle 屬性，然後將轉換物件套用至視覺效果的轉換屬性，則動畫函式會在4秒的過程中，以完整的圓形旋轉視覺效果。</span><span class="sxs-lookup"><span data-stu-id="91770-143">Then, if you apply the animation function to the Angle property of a 2D rotate transform object, and then apply the transform object to the Transform property of a visual, the animation function would rotate the visual in a full circle over the course of 4 seconds.</span></span>

<span data-ttu-id="91770-144">動畫函式是由呼叫 [**IDCompositionDevice：： CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation)方法所建立的 *動畫物件* 來表示。</span><span class="sxs-lookup"><span data-stu-id="91770-144">An animation function is represented by an *animation object* created by a call to the [**IDCompositionDevice::CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) method.</span></span> <span data-ttu-id="91770-145">您可以使用動畫物件之 [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) 介面的方法，將 *動畫區段*（一次一個）附加至定義動畫函數的陣列，以建立動畫函式。</span><span class="sxs-lookup"><span data-stu-id="91770-145">You create an animation function by using the methods of an animation object's [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) interface to append *animation segments*, one at a time, to the array that defines the animation function.</span></span> <span data-ttu-id="91770-146">附加區段時，您會指定以零為基底的位移，此位移會標示區段的開始時間，相對於動畫函式的開頭。</span><span class="sxs-lookup"><span data-stu-id="91770-146">When appending a segment, you specify a zero-based offset that marks the begin time of the segment, relative to the beginning of the animation function.</span></span> <span data-ttu-id="91770-147">動畫區段必須以開始時間的遞增順序附加。</span><span class="sxs-lookup"><span data-stu-id="91770-147">Animation segments must be appended in increasing order of begin times.</span></span> <span data-ttu-id="91770-148">嘗試附加開始時間早于或等於前一個區段的動畫區段將會失敗。</span><span class="sxs-lookup"><span data-stu-id="91770-148">Attempting to append an animation segment whose begin time is before or equal to a preceding segment will fail.</span></span> <span data-ttu-id="91770-149">動畫函式可以有指定的結束時間，表示函式應該結束的時間。</span><span class="sxs-lookup"><span data-stu-id="91770-149">An animation function can have a specified end time, indicating when the function should conclude.</span></span>

<span data-ttu-id="91770-150">除非另有指定，否則當桌面視窗管理員 (DWM) 接收命令以執行動畫時，就會啟動動畫函式。</span><span class="sxs-lookup"><span data-stu-id="91770-150">Unless otherwise specified, an animation function starts when the Desktop Window Manager (DWM) receives the command to execute the animation.</span></span> <span data-ttu-id="91770-151">每個區段都會執行，直到達到下一個區段的開始時間為止。</span><span class="sxs-lookup"><span data-stu-id="91770-151">Each segment runs until the begin time of the next segment is reached.</span></span> <span data-ttu-id="91770-152">在區段之間的動畫屬性值中發生的任何不連續變更，都會視為離散變更。</span><span class="sxs-lookup"><span data-stu-id="91770-152">Any discontinuous changes that occur in the animated property value between segments are considered to be discrete changes.</span></span>

<span data-ttu-id="91770-153">您可以將動畫函式套用至屬性，方法是將屬性值設定為代表動畫函式的動畫物件的 [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) 指標。</span><span class="sxs-lookup"><span data-stu-id="91770-153">You apply an animation function to a property by setting the property value to the [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) pointer of the animation object that represents the animation function.</span></span> <span data-ttu-id="91770-154">相同的動畫物件可以套用至相同物件的多個屬性，也可以套用至相同裝置所建立之其他物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="91770-154">The same animation object can be applied to multiple properties of the same object, as well as to the properties of other objects created by the same device.</span></span>

## <a name="animation-segments"></a><span data-ttu-id="91770-155">動畫區段</span><span class="sxs-lookup"><span data-stu-id="91770-155">Animation segments</span></span>

<span data-ttu-id="91770-156">動畫區段是動畫函數的基本計時定義;它們是建立更複雜和更高層級動畫函式的基本類型。</span><span class="sxs-lookup"><span data-stu-id="91770-156">Animation segments are the fundamental timing definitions of an animation function; they are the primitives from which more complex and higher level animation functions are built.</span></span> <span data-ttu-id="91770-157">動畫區段是由一系列的參數所構成，這些參數描述函式和區段開始的時間（相對於動畫函式的開頭）。</span><span class="sxs-lookup"><span data-stu-id="91770-157">An animation segment is constructed from a series of parameters that describe the function and the time when the segment begins, relative to the beginning of the animation function.</span></span> <span data-ttu-id="91770-158">針對每個區段，時間 (*t*) 沿著水準軸進行，並從 *t* = 0 開始。</span><span class="sxs-lookup"><span data-stu-id="91770-158">For every segment, time (*t*) progresses along the horizontal axis and begins at *t* = 0.</span></span>

### <a name="cubic-segment"></a><span data-ttu-id="91770-159">三次區段</span><span class="sxs-lookup"><span data-stu-id="91770-159">Cubic segment</span></span>

<span data-ttu-id="91770-160">三次區段的時間是由三個多項式所定義。</span><span class="sxs-lookup"><span data-stu-id="91770-160">The timing of a cubic segment is defined by a cubic polynomial.</span></span> <span data-ttu-id="91770-161">針對指定的時間輸入 (*t*) ，輸出值會由下列方程式提供：</span><span class="sxs-lookup"><span data-stu-id="91770-161">For a given time input (*t*), the output value is given by the following equation:</span></span>

<span data-ttu-id="91770-162">*x* (*t*) = *at*³ + *bt*² + *ct*  +  *d*</span><span class="sxs-lookup"><span data-stu-id="91770-162">*x*(*t*) = *at*³ + *bt*² + *ct* + *d*</span></span>

<span data-ttu-id="91770-163">下圖顯示包含兩個三個三個區段的動畫函數。</span><span class="sxs-lookup"><span data-stu-id="91770-163">The following diagram shows an animation function that contains of two cubic segments.</span></span> <span data-ttu-id="91770-164">第一個區段會將值從0轉換為16秒，而第二個區段則會在接下來4秒將值從16變更為0。</span><span class="sxs-lookup"><span data-stu-id="91770-164">The first segment transitions a value from 0 to 16 over 4 seconds, and the second changes the value linearly from 16 to 0 over the next 4 seconds.</span></span> <span data-ttu-id="91770-165">第一個轉換會沿著這個三個多項式發生：</span><span class="sxs-lookup"><span data-stu-id="91770-165">The first transition occurs along this cubic polynomial:</span></span>

<span data-ttu-id="91770-166">*x* (*t*) = *t*³-6 *t*² + 12 *t*</span><span class="sxs-lookup"><span data-stu-id="91770-166">*x*(*t*) = *t*³ - 6 *t*² + 12 *t*</span></span>

<span data-ttu-id="91770-167">第二個轉換會在此執行：</span><span class="sxs-lookup"><span data-stu-id="91770-167">and the second transition occurs along this one:</span></span>

<span data-ttu-id="91770-168">*x* (*t*) =-4 *t* + 16</span><span class="sxs-lookup"><span data-stu-id="91770-168">*x*(*t*) = - 4 *t* + 16</span></span>

![有兩個三個三個區段的動畫函式圖表](images/cubicsegment.png)

<span data-ttu-id="91770-170">您可以使用 [**IDCompositionAnimation：： AddCubic**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addcubic) 方法，將三個區段加入至動畫函數。</span><span class="sxs-lookup"><span data-stu-id="91770-170">You add a cubic segment to an animation function by using the [**IDCompositionAnimation::AddCubic**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addcubic) method.</span></span>

### <a name="sinusoidal-segment"></a><span data-ttu-id="91770-171">正弦曲線區段</span><span class="sxs-lookup"><span data-stu-id="91770-171">Sinusoidal segment</span></span>

<span data-ttu-id="91770-172">正弦曲線區段的時間是由下列方程式所定義：</span><span class="sxs-lookup"><span data-stu-id="91770-172">The timing of a sinusoidal segment is defined by the following equation:</span></span>

<span data-ttu-id="91770-173">*x* (*t*) =*偏差*  +  *幅度* \* sin (*t* \* *頻率* \* 2 \* PI +*階段* \* PI/180.0) </span><span class="sxs-lookup"><span data-stu-id="91770-173">*x*(*t*) = *Bias* + *Amplitude* \* sin(*t*\**Frequency*\*2\*PI + *Phase*\*PI/180.0)</span></span>

<span data-ttu-id="91770-174">您可以使用 [**IDCompositionAnimation：： AddSinusoidal**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addsinusoidal) 方法，將正弦曲線區段新增至動畫函數。</span><span class="sxs-lookup"><span data-stu-id="91770-174">You add a sinusoidal segment to an animation function by using the [**IDCompositionAnimation::AddSinusoidal**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addsinusoidal) method.</span></span>

### <a name="repeat-segment"></a><span data-ttu-id="91770-175">重複區段</span><span class="sxs-lookup"><span data-stu-id="91770-175">Repeat segment</span></span>

<span data-ttu-id="91770-176">重複區段會重複動畫函式的先前指定部分。</span><span class="sxs-lookup"><span data-stu-id="91770-176">A repeat segment repeats a specified preceding portion of an animation function.</span></span> <span data-ttu-id="91770-177">重複區段會導致動畫函式的指定部分無限期地迴圈，直到遇到下一個區段或到達動畫的指定結束為止。</span><span class="sxs-lookup"><span data-stu-id="91770-177">A repeat segment causes the specified portion of the animation function to loop indefinitely until the next segment is encountered or the specified end of the animation is reached.</span></span> <span data-ttu-id="91770-178">動畫先前的部分是由其他區段組成，包括其他重複區段。</span><span class="sxs-lookup"><span data-stu-id="91770-178">The preceding portion of an animation is made of other segments, including other repeat segments.</span></span> <span data-ttu-id="91770-179">重複區段無法用作動畫函式中的第一個區段。</span><span class="sxs-lookup"><span data-stu-id="91770-179">A repeat segment cannot be used as the first segment in an animation function.</span></span>

<span data-ttu-id="91770-180">下圖顯示的動畫函式包含四個三秒期間的三個三區段，後面接著重複的區段，持續12秒。</span><span class="sxs-lookup"><span data-stu-id="91770-180">The following diagram shows an animation function that consists two cubic segments of 4 seconds duration each, followed by a repeat segment that lasts 12 seconds.</span></span> <span data-ttu-id="91770-181">重複區段會在動畫中開始8秒，並重複兩次動畫的前6秒，直到到達結束區段20秒為止。</span><span class="sxs-lookup"><span data-stu-id="91770-181">The repeat segment begins 8 seconds into the animation and repeats the previous 6 seconds of the animation two times until the end segment is reached at 20 seconds.</span></span>

![包含兩個三個三個區段和一個重複區段的動畫函式圖表](images/repeatsegment.png)

<span data-ttu-id="91770-183">若要將重複區段加入至動畫函式，請使用 [**IDCompositionAnimation：： AddRepeat**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addrepeat) 方法。</span><span class="sxs-lookup"><span data-stu-id="91770-183">To add a repeat segment to an animation function, use the [**IDCompositionAnimation::AddRepeat**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addrepeat) method.</span></span>

### <a name="end-segment"></a><span data-ttu-id="91770-184">結束區段</span><span class="sxs-lookup"><span data-stu-id="91770-184">End segment</span></span>

<span data-ttu-id="91770-185">從區段中建立動畫函式之後，您可以附加結束區段，讓動畫函式在特定時間結束。</span><span class="sxs-lookup"><span data-stu-id="91770-185">After constructing an animation function from segments, you can append an end segment to cause the animation function to end at a particular time.</span></span> <span data-ttu-id="91770-186">如果您未附加結束區段，則動畫函式的最後一個區段會無限期執行。</span><span class="sxs-lookup"><span data-stu-id="91770-186">If you do not append an end segment, the final segment of the animation function runs indefinitely.</span></span>

<span data-ttu-id="91770-187">您可以藉由呼叫 [**IDCompositionAnimation：： end**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end) 方法，指定從動畫函式的開頭算起的位移（表示函式的結束點），以附加結束區段。</span><span class="sxs-lookup"><span data-stu-id="91770-187">You append an end segment by calling the [**IDCompositionAnimation::End**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end) method, specifying an offset from the beginning of the animation function which indicates the function's end point.</span></span> <span data-ttu-id="91770-188">位移必須大於前一個區段的開始位移。</span><span class="sxs-lookup"><span data-stu-id="91770-188">The offset must be greater than the beginning offset of the preceding segment.</span></span> <span data-ttu-id="91770-189">此外，結束區段無法當做動畫函式中的第一個基本函數使用。</span><span class="sxs-lookup"><span data-stu-id="91770-189">Also, an end segment cannot be used as the first primitive in an animation function.</span></span>

<span data-ttu-id="91770-190">當您呼叫 [**End**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end)時，也會針對要製作動畫的屬性指定最後一個值。</span><span class="sxs-lookup"><span data-stu-id="91770-190">When you call [**End**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end), you also specify a final value for the property being animated.</span></span> <span data-ttu-id="91770-191">當到達動畫函式的結束點時，屬性會設定為指定的最後一個值。</span><span class="sxs-lookup"><span data-stu-id="91770-191">The property is set to the specified final value at the moment when the end point of the animation function is reached.</span></span>

<span data-ttu-id="91770-192">附加結束區段之後，您就無法將任何其他區段附加至動畫函數。</span><span class="sxs-lookup"><span data-stu-id="91770-192">After appending an end segment, you cannot append any other segments to the animation function.</span></span> <span data-ttu-id="91770-193">也就是說，除了 [**IDCompositionAnimation：： Reset**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-reset)之外，在動畫物件上的所有方法呼叫都會失敗。</span><span class="sxs-lookup"><span data-stu-id="91770-193">That is, all method calls on the animation object fail except [**IDCompositionAnimation::Reset**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-reset).</span></span> <span data-ttu-id="91770-194">呼叫 **Reset** 會傳回動畫物件以清除狀態，其中動畫函式不包含任何區段，此時您可以再次加入區段。</span><span class="sxs-lookup"><span data-stu-id="91770-194">Calling **Reset** returns the animation object to clean state in which the animation function contains no segments, at which point you can once again add segments.</span></span>

## <a name="compatibility-with-windows-animation-manager"></a><span data-ttu-id="91770-195">與 Windows 動畫管理員的相容性</span><span class="sxs-lookup"><span data-stu-id="91770-195">Compatibility with Windows Animation Manager</span></span>

<span data-ttu-id="91770-196">Windows 動畫管理員 (Windows 動畫) 以與 DirectComposition API 相容的格式輸出動畫基本專案。</span><span class="sxs-lookup"><span data-stu-id="91770-196">Windows Animation Manager (Windows Animation) outputs animation primitives in a format that is compatible with the DirectComposition API.</span></span> <span data-ttu-id="91770-197">這表示 DirectComposition 可以根據 Windows 動畫建立的動畫基本專案來建立動畫。</span><span class="sxs-lookup"><span data-stu-id="91770-197">This means that DirectComposition can create animations based on animation primitives created by Windows Animation.</span></span>

<span data-ttu-id="91770-198">如需詳細資訊，請參閱 [Windows 動畫管理員](/windows/desktop/UIAnimation/-main-portal)、 [**IUIAnimationVariable2：： GetCurve**](/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve) 方法，以及 [使用 Windows 動畫管理員 v2 管理 DirectComposition 動畫](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)。</span><span class="sxs-lookup"><span data-stu-id="91770-198">For more information, see [Windows Animation Manager](/windows/desktop/UIAnimation/-main-portal), the [**IUIAnimationVariable2::GetCurve**](/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve) method, and [Managing DirectComposition Animation with Windows Animation Manager v2](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager).</span></span>

## <a name="related-topics"></a><span data-ttu-id="91770-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="91770-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91770-200">DirectComposition 概念</span><span class="sxs-lookup"><span data-stu-id="91770-200">DirectComposition Concepts</span></span>](directcomposition-concepts.md)
</dt> </dl>

 

 
