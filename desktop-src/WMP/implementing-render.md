---
title: 執行轉譯
description: 執行轉譯
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- 視覺效果，計時事件
- 自訂視覺效果，計時事件
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- 視覺效果，RenderWindow 函式
- 自訂視覺效果，RenderWindow 函式
- 轉譯函數，參數
- RenderWindow 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023047"
---
# <a name="implementing-render"></a><span data-ttu-id="56b51-111">執行轉譯</span><span class="sxs-lookup"><span data-stu-id="56b51-111">Implementing Render</span></span>

<span data-ttu-id="56b51-112">要考慮視覺化程式設計，最簡單的方式就是建立計時事件的處理常式。</span><span class="sxs-lookup"><span data-stu-id="56b51-112">The easiest way to think of visualization programming is that you are creating a handler for a timed event.</span></span> <span data-ttu-id="56b51-113">在特定間隔中，Windows Media Player 會取得所播放音訊資料的快照集，並將快照集資料提供給目前載入的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="56b51-113">At specific intervals, Windows Media Player takes a snapshot of the audio data it is playing, and provides the snapshot data to the currently loaded visualization.</span></span> <span data-ttu-id="56b51-114">這類似于事件驅動程式設計，而且是 Microsoft Windows 的程式設計模型的一部分。</span><span class="sxs-lookup"><span data-stu-id="56b51-114">This is similar to event-driven programming and is part of the programming model of Microsoft Windows.</span></span> <span data-ttu-id="56b51-115">您會撰寫程式碼，並等候特定事件呼叫它。</span><span class="sxs-lookup"><span data-stu-id="56b51-115">You write code and wait for it to be called by a particular event.</span></span>

<span data-ttu-id="56b51-116">如果您的程式碼是 [IWMPEffects：： Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) 函式的執行，以便在無視窗模式中轉譯，則會收到下列參數：</span><span class="sxs-lookup"><span data-stu-id="56b51-116">If your code is an implementation of the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function for rendering in windowless mode, it receives the following parameters:</span></span>

<span data-ttu-id="56b51-117">*TimedLevel*</span><span class="sxs-lookup"><span data-stu-id="56b51-117">*TimedLevel*</span></span>

<span data-ttu-id="56b51-118">這是定義您的程式碼將分析之音訊資料的結構。</span><span class="sxs-lookup"><span data-stu-id="56b51-118">This is a structure that defines the audio data your code will be analyzing.</span></span> <span data-ttu-id="56b51-119">此結構是由兩個數組所組成。</span><span class="sxs-lookup"><span data-stu-id="56b51-119">The structure is composed of two arrays.</span></span> <span data-ttu-id="56b51-120">第一個陣列是以頻率資訊為基礎，其中包含將音訊頻譜的快照分割成1024部分。</span><span class="sxs-lookup"><span data-stu-id="56b51-120">The first array is based on frequency information and contains a snapshot of the audio spectrum divided into 1024 portions.</span></span> <span data-ttu-id="56b51-121">陣列中的每個資料格都包含0到255的值。</span><span class="sxs-lookup"><span data-stu-id="56b51-121">Each cell of the array contains a value from 0 to 255.</span></span> <span data-ttu-id="56b51-122">第一個儲存格從 20 Hz 和最後一個 22050 Hz 開始。</span><span class="sxs-lookup"><span data-stu-id="56b51-122">The first cell starts at 20 Hz and the last at 22050 Hz.</span></span> <span data-ttu-id="56b51-123">陣列以二維表示身歷聲音訊。</span><span class="sxs-lookup"><span data-stu-id="56b51-123">The array is two dimensional to represent stereo audio.</span></span> <span data-ttu-id="56b51-124">第二個數組是以波形資訊為基礎，而且對應到音訊電源，也就是最強的波浪值，值愈大。</span><span class="sxs-lookup"><span data-stu-id="56b51-124">The second array is based on waveform information and corresponds to audio power, where the stronger the wave is, the larger the value.</span></span> <span data-ttu-id="56b51-125">波形陣列是以極短時間間隔拍攝之音訊電力最後1024磁區的細微快照。</span><span class="sxs-lookup"><span data-stu-id="56b51-125">The waveform array is a granular snapshot of the last 1024 slices of audio power taken at very small time intervals.</span></span> <span data-ttu-id="56b51-126">這個陣列也是兩個代表身歷聲音訊的維度。</span><span class="sxs-lookup"><span data-stu-id="56b51-126">This array also is two dimensional to represent stereo audio.</span></span>

<span data-ttu-id="56b51-127">*HDC*</span><span class="sxs-lookup"><span data-stu-id="56b51-127">*HDC*</span></span>

<span data-ttu-id="56b51-128">這是 Microsoft Windows 的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="56b51-128">This is a Microsoft Windows handle to a device context.</span></span> <span data-ttu-id="56b51-129">這會提供一種方式來識別 Windows 的繪圖介面。</span><span class="sxs-lookup"><span data-stu-id="56b51-129">This gives a way to identify the drawing surface to Windows.</span></span> <span data-ttu-id="56b51-130">您不需要加以建立，只需要將它用於特定的繪圖函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="56b51-130">You do not need to create it, you just need to use it for specific drawing function calls.</span></span>

<span data-ttu-id="56b51-131">*矩形*</span><span class="sxs-lookup"><span data-stu-id="56b51-131">*RECT*</span></span>

<span data-ttu-id="56b51-132">這是定義繪圖介面大小的 Microsoft Windows 矩形。</span><span class="sxs-lookup"><span data-stu-id="56b51-132">This is a Microsoft Windows rectangle that defines the size of a drawing surface.</span></span> <span data-ttu-id="56b51-133">這是具有四個屬性的簡單矩形： **left**、 **right**、 **top** 和 **底端**。</span><span class="sxs-lookup"><span data-stu-id="56b51-133">This is a simple rectangle with four properties: **left**, **right**, **top**, and **bottom**.</span></span> <span data-ttu-id="56b51-134">實際的值是由 Windows Media Player 提供，因此您可以決定使用者或外觀開發人員如何調整您將繪製的視窗大小。</span><span class="sxs-lookup"><span data-stu-id="56b51-134">The actual values are supplied by Windows Media Player so that you can determine how the user or skin developer has sized the window you will draw on.</span></span> <span data-ttu-id="56b51-135">它也會決定要呈現其效果的 HDC 上的位置。</span><span class="sxs-lookup"><span data-stu-id="56b51-135">It also determines the position on the HDC that the effect is supposed to render on.</span></span>

<span data-ttu-id="56b51-136">如果您的程式碼是 **IWMPEffects2：： RenderWindowed** 函式的執行，以便在視窗中轉譯，則會收到下列參數：</span><span class="sxs-lookup"><span data-stu-id="56b51-136">If your code is an implementation of the **IWMPEffects2::RenderWindowed** function for rendering in a window, it receives the following parameters:</span></span>

<span data-ttu-id="56b51-137">*TimedLevel*</span><span class="sxs-lookup"><span data-stu-id="56b51-137">*TimedLevel*</span></span>

<span data-ttu-id="56b51-138">這是 **轉譯函數所接收的相同** 資訊。</span><span class="sxs-lookup"><span data-stu-id="56b51-138">This is the same information that the **Render** function receives.</span></span>

<span data-ttu-id="56b51-139">*fRequiredRender*</span><span class="sxs-lookup"><span data-stu-id="56b51-139">*fRequiredRender*</span></span>

<span data-ttu-id="56b51-140">*FRequiredRender* 參數會通知您，您的視覺效果必須自行重新繪製，例如，當另一個視窗拖曳至另一個視窗時。</span><span class="sxs-lookup"><span data-stu-id="56b51-140">The *fRequiredRender* parameter informs you that your visualization must repaint itself—for example, when another window is dragged over it.</span></span> <span data-ttu-id="56b51-141">當此值為 false 時，如果目前的媒體專案已停止或暫停，您可以放心地跳過轉譯程式碼。</span><span class="sxs-lookup"><span data-stu-id="56b51-141">When this value is false, you can safely skip over the rendering code if the current media item is stopped or paused.</span></span> <span data-ttu-id="56b51-142">這可讓您避免不必要地耗用 CPU 迴圈。</span><span class="sxs-lookup"><span data-stu-id="56b51-142">This lets you avoid consuming CPU cycles unnecessarily.</span></span>

<span data-ttu-id="56b51-143">外掛程式 Wizard 所產生的範例外掛程式不會提供 **RenderWindowed** 的自訂執行。</span><span class="sxs-lookup"><span data-stu-id="56b51-143">The sample plug-in generated by the Plug-in Wizard does not provide a custom implementation for **RenderWindowed**.</span></span> <span data-ttu-id="56b51-144">相反地，範例外掛程式程式碼會從 [IWMPEffects2：： Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)中 Windows Media Player 所提供的父視窗抓取裝置內容，然後以 RECT 結構的形式抓取父視窗的維度，然後呼叫 **，以使用** 來自 **RENDERWINDOWED** 的裝置內容、RECT 和計時層級指標進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="56b51-144">Instead, the sample plug-in code retrieves the device context from the parent window provided by Windows Media Player in [IWMPEffects2::Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), then retrieves the dimensions of the parent window as a RECT structure, and then calls through to **Render** using the device context, the RECT, and the timed level pointer from **RenderWindowed**.</span></span>

<span data-ttu-id="56b51-145">下列各節提供 **有關執行轉譯** 的詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="56b51-145">The following sections provide more information about implementing **Render**:</span></span>

-   [<span data-ttu-id="56b51-146">使用計時層級</span><span class="sxs-lookup"><span data-stu-id="56b51-146">Using Timed Levels</span></span>](using-timed-levels.md)
-   [<span data-ttu-id="56b51-147">使用裝置內容</span><span class="sxs-lookup"><span data-stu-id="56b51-147">Using Device Contexts</span></span>](using-device-contexts.md)
-   [<span data-ttu-id="56b51-148">使用矩形</span><span class="sxs-lookup"><span data-stu-id="56b51-148">Using Rectangles</span></span>](using-rectangles.md)
-   [<span data-ttu-id="56b51-149">範例轉譯程式碼</span><span class="sxs-lookup"><span data-stu-id="56b51-149">Sample Render Code</span></span>](sample-render-code.md)

## <a name="related-topics"></a><span data-ttu-id="56b51-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="56b51-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56b51-151">**執行您的程式碼**</span><span class="sxs-lookup"><span data-stu-id="56b51-151">**Implementing Your Code**</span></span>](implementing-your-code.md)
</dt> </dl>

 

 




