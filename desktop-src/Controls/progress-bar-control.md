---
title: 關於進度列控制項
description: 進度列是一種視窗，可讓應用程式用來指出冗長作業的進度。 它是由在作業進行時動畫的矩形所組成。
ms.assetid: 1db7a5c9-71cd-4ebc-86b8-8159f30348fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00c80b1f9e97cec1657fe979a19437f607251b8
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683145"
---
# <a name="about-progress-bar-controls"></a><span data-ttu-id="5e11c-104">關於進度列控制項</span><span class="sxs-lookup"><span data-stu-id="5e11c-104">About Progress Bar Controls</span></span>

<span data-ttu-id="5e11c-105">進度列是一種視窗，可讓應用程式用來指出冗長作業的進度。</span><span class="sxs-lookup"><span data-stu-id="5e11c-105">A progress bar is a window that an application can use to indicate the progress of a lengthy operation.</span></span>

<span data-ttu-id="5e11c-106">它是由在作業進行時動畫的矩形所組成。</span><span class="sxs-lookup"><span data-stu-id="5e11c-106">It consists of a rectangle that is animated as an operation progresses.</span></span>

<span data-ttu-id="5e11c-107">下圖顯示不使用視覺化樣式的進度列。</span><span class="sxs-lookup"><span data-stu-id="5e11c-107">The following illustration shows a progress bar that does not use visual styles.</span></span>

![進度列的螢幕擷取畫面，可線上條中新增矩形以表示進度](images/pb-oldstyle.png)

<span data-ttu-id="5e11c-109">下圖顯示使用視覺化樣式的進度列。</span><span class="sxs-lookup"><span data-stu-id="5e11c-109">The following illustration shows a progress bar using visual styles.</span></span> <span data-ttu-id="5e11c-110">控制項的外觀會依作業系統和選取的主題而有所不同。</span><span class="sxs-lookup"><span data-stu-id="5e11c-110">The appearance of the control will vary depending on the operating system and the selected theme.</span></span> <span data-ttu-id="5e11c-111">如需詳細資訊，請參閱 [視覺化樣式](themes-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="5e11c-111">For more information, see [Visual Styles](themes-overview.md).</span></span>

![進度列的螢幕擷取畫面，可延長動畫的綠色矩形以表示進度](images/pb-newstyle.png)

<span data-ttu-id="5e11c-113">下列標題底下包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5e11c-113">More information is contained under the following headings.</span></span>

-   [<span data-ttu-id="5e11c-114">使用進度列</span><span class="sxs-lookup"><span data-stu-id="5e11c-114">Using Progress Bars</span></span>](#using-progress-bars)
    -   [<span data-ttu-id="5e11c-115">範圍和目前的位置</span><span class="sxs-lookup"><span data-stu-id="5e11c-115">Range and Current Position</span></span>](#range-and-current-position)
    -   [<span data-ttu-id="5e11c-116">預設進度列訊息處理</span><span class="sxs-lookup"><span data-stu-id="5e11c-116">Default Progress Bar Message Processing</span></span>](#default-progress-bar-message-processing)
    -   [<span data-ttu-id="5e11c-117">天棚樣式</span><span class="sxs-lookup"><span data-stu-id="5e11c-117">Marquee Style</span></span>](#marquee-style)

## <a name="using-progress-bars"></a><span data-ttu-id="5e11c-118">使用進度列</span><span class="sxs-lookup"><span data-stu-id="5e11c-118">Using Progress Bars</span></span>

<span data-ttu-id="5e11c-119">您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立進度列，並指定 [**進度 \_ 類別**](common-control-window-classes.md) 視窗類別。</span><span class="sxs-lookup"><span data-stu-id="5e11c-119">You can create a progress bar by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**PROGRESS\_CLASS**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="5e11c-120">載入通用控制項 DLL 時，會註冊此視窗類別。</span><span class="sxs-lookup"><span data-stu-id="5e11c-120">This window class is registered when the common controls DLL is loaded.</span></span> <span data-ttu-id="5e11c-121">如需詳細資訊，請參閱 [關於通用控制項](common-controls-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="5e11c-121">For more information, see [About Common Controls](common-controls-intro.md).</span></span>

<span data-ttu-id="5e11c-122">您也可以在 Microsoft Visual Studio 的 [工具箱] 中取得控制項，在其中呼叫進度控制項。</span><span class="sxs-lookup"><span data-stu-id="5e11c-122">The control is also available in the Microsoft Visual Studio Toolbox, where it is called Progress Control.</span></span>

### <a name="range-and-current-position"></a><span data-ttu-id="5e11c-123">範圍和目前的位置</span><span class="sxs-lookup"><span data-stu-id="5e11c-123">Range and Current Position</span></span>

<span data-ttu-id="5e11c-124">進度列的 *範圍* 代表整個作業的持續時間，而 *目前的位置* 則代表應用程式完成作業所完成的進度。</span><span class="sxs-lookup"><span data-stu-id="5e11c-124">A progress bar's *range* represents the entire duration of the operation, and the *current position* represents the progress that the application has made toward completing the operation.</span></span> <span data-ttu-id="5e11c-125">視窗程式會使用範圍和目前的位置，來決定要以醒目提示色彩填滿的進度列百分比。</span><span class="sxs-lookup"><span data-stu-id="5e11c-125">The window procedure uses the range and the current position to determine the percentage of the progress bar to fill with the highlight color.</span></span>

<span data-ttu-id="5e11c-126">如果您未設定範圍值，系統會將最小值設定為0，並將最大值設定為100。</span><span class="sxs-lookup"><span data-stu-id="5e11c-126">If you do not set the range values, the system sets the minimum value to 0 and the maximum value to 100.</span></span> <span data-ttu-id="5e11c-127">您可以使用 [**PBM \_ SETRANGE**](pbm-setrange.md) 訊息，將範圍調整為方便的整數。</span><span class="sxs-lookup"><span data-stu-id="5e11c-127">You can adjust the range to convenient integers by using the [**PBM\_SETRANGE**](pbm-setrange.md) message.</span></span>

<span data-ttu-id="5e11c-128">進度列提供數個可供您用來設定目前位置的訊息。</span><span class="sxs-lookup"><span data-stu-id="5e11c-128">A progress bar provides several messages that you can use to set the current position.</span></span> <span data-ttu-id="5e11c-129">[**PBM \_ SETPOS**](pbm-setpos.md)訊息會將位置設定為指定的值。</span><span class="sxs-lookup"><span data-stu-id="5e11c-129">The [**PBM\_SETPOS**](pbm-setpos.md) message sets the position to a given value.</span></span> <span data-ttu-id="5e11c-130">[**PBM \_ DELTAPOS**](pbm-deltapos.md)訊息會將指定的值加入至目前的位置，以將位置往前移。</span><span class="sxs-lookup"><span data-stu-id="5e11c-130">The [**PBM\_DELTAPOS**](pbm-deltapos.md) message advances the position by adding a specified value to the current position.</span></span>

<span data-ttu-id="5e11c-131">[**PBM \_ SETSTEP**](pbm-setstep.md)訊息可讓您指定進度列的步驟增量。</span><span class="sxs-lookup"><span data-stu-id="5e11c-131">The [**PBM\_SETSTEP**](pbm-setstep.md) message allows you to specify a step increment for a progress bar.</span></span> <span data-ttu-id="5e11c-132">之後，每當您將 [**PBM \_ STEPIT**](pbm-stepit.md) 訊息傳送到進度列時，目前的位置就會以指定的增量前進。</span><span class="sxs-lookup"><span data-stu-id="5e11c-132">Subsequently, whenever you send the [**PBM\_STEPIT**](pbm-stepit.md) message to the progress bar, the current position advances by the specified increment.</span></span> <span data-ttu-id="5e11c-133">依預設，步驟遞增會設定為10。</span><span class="sxs-lookup"><span data-stu-id="5e11c-133">By default, the step increment is set to 10.</span></span>

### <a name="default-progress-bar-message-processing"></a><span data-ttu-id="5e11c-134">預設進度列訊息處理</span><span class="sxs-lookup"><span data-stu-id="5e11c-134">Default Progress Bar Message Processing</span></span>

<span data-ttu-id="5e11c-135">本節說明由 [**進度 \_ 類別**](common-control-window-classes.md) 類別的視窗程式所處理的訊息。</span><span class="sxs-lookup"><span data-stu-id="5e11c-135">This section describes the messages handled by the window procedure for the [**PROGRESS\_CLASS**](common-control-window-classes.md) class.</span></span>



| <span data-ttu-id="5e11c-136">訊息</span><span class="sxs-lookup"><span data-stu-id="5e11c-136">Message</span></span>            | <span data-ttu-id="5e11c-137">處理已執行</span><span class="sxs-lookup"><span data-stu-id="5e11c-137">Processing performed</span></span>                                                                                                                                                               |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e11c-138">**WM \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="5e11c-138">**WM\_CREATE**</span></span>     | <span data-ttu-id="5e11c-139">配置並初始化初始結構。</span><span class="sxs-lookup"><span data-stu-id="5e11c-139">Allocates and initializes an initial structure.</span></span>                                                                                                                                    |
| <span data-ttu-id="5e11c-140">**WM 損 \_ 毀**</span><span class="sxs-lookup"><span data-stu-id="5e11c-140">**WM\_DESTROY**</span></span>    | <span data-ttu-id="5e11c-141">釋出與進度列相關聯的所有資源。</span><span class="sxs-lookup"><span data-stu-id="5e11c-141">Frees all resources associated with the progress bar.</span></span>                                                                                                                              |
| <span data-ttu-id="5e11c-142">**WM \_ ERASEBKGND**</span><span class="sxs-lookup"><span data-stu-id="5e11c-142">**WM\_ERASEBKGND**</span></span> | <span data-ttu-id="5e11c-143">繪製進度列的背景和框線。</span><span class="sxs-lookup"><span data-stu-id="5e11c-143">Draws the background and borders of the progress bar.</span></span>                                                                                                                              |
| <span data-ttu-id="5e11c-144">**WM \_ GETFONT**</span><span class="sxs-lookup"><span data-stu-id="5e11c-144">**WM\_GETFONT**</span></span>    | <span data-ttu-id="5e11c-145">傳回目前字型的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5e11c-145">Returns the handle to the current font.</span></span> <span data-ttu-id="5e11c-146">進度列目前不會繪製文字，因此傳送此訊息不會影響控制項。</span><span class="sxs-lookup"><span data-stu-id="5e11c-146">The progress bar does not currently draw text, so sending this message has no effect on the control.</span></span>                                       |
| <span data-ttu-id="5e11c-147">**WM \_ 油漆**</span><span class="sxs-lookup"><span data-stu-id="5e11c-147">**WM\_PAINT**</span></span>      | <span data-ttu-id="5e11c-148">繪製進度列。</span><span class="sxs-lookup"><span data-stu-id="5e11c-148">Draws the progress bar.</span></span> <span data-ttu-id="5e11c-149">如果 *wParam* 參數不是 **Null**，則控制項會假設值為 HDC，並且使用該裝置內容繪製。</span><span class="sxs-lookup"><span data-stu-id="5e11c-149">If the *wParam* parameter is non-**NULL**, the control assumes that the value is an HDC and paints using that device context.</span></span>                              |
| <span data-ttu-id="5e11c-150">**WM \_ SETFONT**</span><span class="sxs-lookup"><span data-stu-id="5e11c-150">**WM\_SETFONT**</span></span>    | <span data-ttu-id="5e11c-151">將控制碼儲存至新的字型，並將控制碼傳回至先前的字型。</span><span class="sxs-lookup"><span data-stu-id="5e11c-151">Saves the handle to the new font and returns the handle to the previous font.</span></span> <span data-ttu-id="5e11c-152">進度列目前不會繪製文字，因此傳送此訊息不會影響控制項。</span><span class="sxs-lookup"><span data-stu-id="5e11c-152">The progress bar does not currently draw text, so sending this message has no effect on the control.</span></span> |



 

### <a name="marquee-style"></a><span data-ttu-id="5e11c-153">天棚樣式</span><span class="sxs-lookup"><span data-stu-id="5e11c-153">Marquee Style</span></span>

<span data-ttu-id="5e11c-154">藉由建立具有 [**PBS \_ 字幕**](progress-bar-control-styles.md) 樣式的進度列控制項，您可以用顯示活動的方式建立動畫，但不會指出工作的完成比例。</span><span class="sxs-lookup"><span data-stu-id="5e11c-154">By creating the progress bar control with the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style, you can animate it in a way that shows activity but does not indicate what proportion of the task is complete.</span></span> <span data-ttu-id="5e11c-155">進度列反白顯示的部分會隨著橫條的長度重複移動。</span><span class="sxs-lookup"><span data-stu-id="5e11c-155">The highlighted part of the progress bar moves repeatedly along the length of the bar.</span></span> <span data-ttu-id="5e11c-156">您可以藉由傳送 [**PBM \_ SETMARQUEE**](pbm-setmarquee.md) 訊息來開始和停止動畫，以及控制其速度。</span><span class="sxs-lookup"><span data-stu-id="5e11c-156">You can start and stop the animation, and control its speed, by sending the [**PBM\_SETMARQUEE**](pbm-setmarquee.md) message.</span></span> <span data-ttu-id="5e11c-157">天棚進度列沒有範圍或位置。</span><span class="sxs-lookup"><span data-stu-id="5e11c-157">Marquee progress bars do not have a range or position.</span></span>

<span data-ttu-id="5e11c-158">下圖顯示捲軸模式的進度列。</span><span class="sxs-lookup"><span data-stu-id="5e11c-158">The following illustration shows a progress bar in marquee mode.</span></span> <span data-ttu-id="5e11c-159">反白顯示的部分會在橫條之間移動。</span><span class="sxs-lookup"><span data-stu-id="5e11c-159">The highlighted part moves across the bar.</span></span>

![進度列的螢幕擷取畫面，在灰色矩形上移動綠色醒目提示以表示進度](images/pb-marquee.png)

 

 