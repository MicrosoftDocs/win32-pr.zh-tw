---
title: 使用 Direct2D 繪製
description: 建立圖形資源之後，您就可以開始繪製。
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f8f3cf82d3ce6f485a7c54700c32c9eb65d054
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463036"
---
# <a name="drawing-with-direct2d"></a><span data-ttu-id="148c1-103">使用 Direct2D 繪製</span><span class="sxs-lookup"><span data-stu-id="148c1-103">Drawing with Direct2D</span></span>

<span data-ttu-id="148c1-104">建立圖形資源之後，您就可以開始繪製。</span><span class="sxs-lookup"><span data-stu-id="148c1-104">After you create your graphics resources, you are ready to draw.</span></span>

## <a name="drawing-an-ellipse"></a><span data-ttu-id="148c1-105">繪製橢圓形</span><span class="sxs-lookup"><span data-stu-id="148c1-105">Drawing an Ellipse</span></span>

<span data-ttu-id="148c1-106">[Circle](your-first-direct2d-program.md)程式會執行非常簡單的繪圖邏輯：</span><span class="sxs-lookup"><span data-stu-id="148c1-106">The [Circle](your-first-direct2d-program.md) program performs very simple drawing logic:</span></span>

1.  <span data-ttu-id="148c1-107">以純色填滿背景。</span><span class="sxs-lookup"><span data-stu-id="148c1-107">Fill the background with a solid color.</span></span>
2.  <span data-ttu-id="148c1-108">繪製實心的圓形。</span><span class="sxs-lookup"><span data-stu-id="148c1-108">Draw a filled circle.</span></span>

![圓形程式的螢幕擷取畫面。](images/graphics08.png)

<span data-ttu-id="148c1-110">由於轉譯目標是視窗 (而不是點陣圖或其他螢幕外表面) ，因此繪圖是為了回應 [**WM \_ 繪製**](/windows/desktop/gdi/wm-paint) 訊息而完成。</span><span class="sxs-lookup"><span data-stu-id="148c1-110">Because the render target is a window (as opposed to a bitmap or other offscreen surface), drawing is done in response to [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) messages.</span></span> <span data-ttu-id="148c1-111">下列程式碼顯示圓形程式的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="148c1-111">The following code shows the window procedure for the Circle program.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_PAINT:
            OnPaint();
            return 0;

         // Other messages not shown...
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```

<span data-ttu-id="148c1-112">以下是繪製圓形的程式碼。</span><span class="sxs-lookup"><span data-stu-id="148c1-112">Here is the code that draws the circle.</span></span>

```C++
void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="148c1-113">[**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget)介面用於所有繪製作業。</span><span class="sxs-lookup"><span data-stu-id="148c1-113">The [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface is used for all drawing operations.</span></span> <span data-ttu-id="148c1-114">程式的 `OnPaint` 方法會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="148c1-114">The program's `OnPaint` method does the following:</span></span>

1.  <span data-ttu-id="148c1-115">[**ID2D1RenderTarget：： BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)方法表示繪圖的起點。</span><span class="sxs-lookup"><span data-stu-id="148c1-115">The [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method signals the start of drawing.</span></span>
2.  <span data-ttu-id="148c1-116">[**ID2D1RenderTarget：： Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)方法會以純色填滿整個呈現目標。</span><span class="sxs-lookup"><span data-stu-id="148c1-116">The [**ID2D1RenderTarget::Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) method fills the entire render target with a solid color.</span></span> <span data-ttu-id="148c1-117">色彩會以 [**D2D1 \_ 色 \_ F**](/windows/desktop/Direct2D/d2d1-color-f) 結構的形式提供。</span><span class="sxs-lookup"><span data-stu-id="148c1-117">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) structure.</span></span> <span data-ttu-id="148c1-118">您可以使用 [**D2D1：： ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) 類別來初始化結構。</span><span class="sxs-lookup"><span data-stu-id="148c1-118">You can use the [**D2D1::ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) class to initialize the structure.</span></span> <span data-ttu-id="148c1-119">如需詳細資訊，請參閱 [在 Direct2D 中使用色彩](using-color-in-direct2d.md)。</span><span class="sxs-lookup"><span data-stu-id="148c1-119">For more information, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>
3.  <span data-ttu-id="148c1-120">[**ID2D1RenderTarget：： FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))方法會繪製填滿的橢圓形，並使用指定的筆刷來填滿。</span><span class="sxs-lookup"><span data-stu-id="148c1-120">The [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws a filled ellipse, using the specified brush for the fill.</span></span> <span data-ttu-id="148c1-121">橢圓形是由中心點以及 x 和 y 半徑來指定。</span><span class="sxs-lookup"><span data-stu-id="148c1-121">An ellipse is specified by a center point and the x- and y-radii.</span></span> <span data-ttu-id="148c1-122">如果 x 和 y 半徑相同，則結果為圓形。</span><span class="sxs-lookup"><span data-stu-id="148c1-122">If the x- and y-radii are the same, the result is a circle.</span></span>
4.  <span data-ttu-id="148c1-123">[**ID2D1RenderTarget：： EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)方法會針對此框架完成繪圖的信號。</span><span class="sxs-lookup"><span data-stu-id="148c1-123">The [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method signals the completion of drawing for this frame.</span></span> <span data-ttu-id="148c1-124">所有繪圖作業都必須放在對 [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 和 **EndDraw** 的呼叫之間。</span><span class="sxs-lookup"><span data-stu-id="148c1-124">All drawing operations must be placed between calls to [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw**.</span></span>

<span data-ttu-id="148c1-125">[**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)、 [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)和 [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))方法都有 **void** 傳回型別。</span><span class="sxs-lookup"><span data-stu-id="148c1-125">The [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear), and [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) methods all have a **void** return type.</span></span> <span data-ttu-id="148c1-126">如果在這些方法的任何一執行期間發生錯誤，則會透過 [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法的傳回值發出錯誤。</span><span class="sxs-lookup"><span data-stu-id="148c1-126">If an error occurs during the execution of any of these methods, the error is signaled through the return value of the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="148c1-127">`CreateGraphicsResources`方法會顯示在[建立 Direct2D 資源](render-targets--devices--and-resources.md)的主題中。</span><span class="sxs-lookup"><span data-stu-id="148c1-127">The `CreateGraphicsResources` method is shown in the topic [Creating Direct2D Resources](render-targets--devices--and-resources.md).</span></span> <span data-ttu-id="148c1-128">這個方法會建立呈現目標和純色筆刷。</span><span class="sxs-lookup"><span data-stu-id="148c1-128">This method creates the render target and the solid-color brush.</span></span>

<span data-ttu-id="148c1-129">裝置可能會緩衝繪製命令並順延強制，直到呼叫 [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 為止。</span><span class="sxs-lookup"><span data-stu-id="148c1-129">The device might buffer the drawing commands and defer executing them until [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) is called.</span></span> <span data-ttu-id="148c1-130">您可以藉由呼叫 [**ID2D1RenderTarget：： Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush)來強制裝置執行任何暫止的繪圖命令。</span><span class="sxs-lookup"><span data-stu-id="148c1-130">You can force the device to execute any pending drawing commands by calling [**ID2D1RenderTarget::Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span> <span data-ttu-id="148c1-131">不過，清除可能會降低效能。</span><span class="sxs-lookup"><span data-stu-id="148c1-131">Flushing can reduce performance, however.</span></span>

## <a name="handling-device-loss"></a><span data-ttu-id="148c1-132">處理裝置遺失</span><span class="sxs-lookup"><span data-stu-id="148c1-132">Handling Device Loss</span></span>

<span data-ttu-id="148c1-133">當程式正在執行時，您所使用的圖形裝置可能會變成無法使用。</span><span class="sxs-lookup"><span data-stu-id="148c1-133">While your program is running, the graphics device that you are using might become unavailable.</span></span> <span data-ttu-id="148c1-134">例如，如果顯示解析度變更，或使用者移除顯示器介面卡，則裝置可能會遺失。</span><span class="sxs-lookup"><span data-stu-id="148c1-134">For example, the device can be lost if the display resolution changes, or if the user removes the display adapter.</span></span> <span data-ttu-id="148c1-135">如果裝置遺失，轉譯目標也會變成無效，以及與裝置相關聯之任何裝置相依的資源。</span><span class="sxs-lookup"><span data-stu-id="148c1-135">If the device is lost, the render target also becomes invalid, along with any device-dependent resources that were associated with the device.</span></span> <span data-ttu-id="148c1-136">Direct2D 藉由從 [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)方法傳回錯誤碼 **D2DERR 重新建立 \_ \_ 目標**，來為遺失的裝置發出信號。</span><span class="sxs-lookup"><span data-stu-id="148c1-136">Direct2D signals a lost device by returning the error code **D2DERR\_RECREATE\_TARGET** from the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="148c1-137">如果您收到此錯誤碼，則必須重新建立轉譯目標和所有裝置相依的資源。</span><span class="sxs-lookup"><span data-stu-id="148c1-137">If you receive this error code, you must re-create the render target and all device-dependent resources.</span></span>

<span data-ttu-id="148c1-138">若要捨棄資源，只要釋放該資源的介面即可。</span><span class="sxs-lookup"><span data-stu-id="148c1-138">To discard a resource, simply release the interface for that resource.</span></span>


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



<span data-ttu-id="148c1-139">建立資源可能是昂貴的作業，因此請勿重新建立每個 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息的資源。</span><span class="sxs-lookup"><span data-stu-id="148c1-139">Creating a resource can be an expensive operation, so do not recreate your resources for every [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="148c1-140">建立資源一次，並快取資源指標，直到資源因為裝置遺失而變成無效，或直到您不再需要該資源為止。</span><span class="sxs-lookup"><span data-stu-id="148c1-140">Create a resource once, and cache the resource pointer until the resource becomes invalid due to device loss, or until you no longer need that resource.</span></span>

## <a name="the-direct2d-render-loop"></a><span data-ttu-id="148c1-141">Direct2D 轉譯迴圈</span><span class="sxs-lookup"><span data-stu-id="148c1-141">The Direct2D Render Loop</span></span>

<span data-ttu-id="148c1-142">無論您的繪圖為何，您的程式都應該執行如下所示的迴圈。</span><span class="sxs-lookup"><span data-stu-id="148c1-142">Regardless of what you draw, your program should perform a loop similar to following.</span></span>

1.  <span data-ttu-id="148c1-143">建立與裝置無關的資源。</span><span class="sxs-lookup"><span data-stu-id="148c1-143">Create device-independent resources.</span></span>
2.  <span data-ttu-id="148c1-144">呈現場景。</span><span class="sxs-lookup"><span data-stu-id="148c1-144">Render the scene.</span></span>
    1.  <span data-ttu-id="148c1-145">檢查有效的轉譯目標是否存在。</span><span class="sxs-lookup"><span data-stu-id="148c1-145">Check if a valid render target exists.</span></span> <span data-ttu-id="148c1-146">如果沒有，請建立轉譯目標和裝置相依的資源。</span><span class="sxs-lookup"><span data-stu-id="148c1-146">If not, create the render target and the device-dependent resources.</span></span>
    2.  <span data-ttu-id="148c1-147">呼叫 [**ID2D1RenderTarget：： BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)。</span><span class="sxs-lookup"><span data-stu-id="148c1-147">Call [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span></span>
    3.  <span data-ttu-id="148c1-148">發出繪製命令。</span><span class="sxs-lookup"><span data-stu-id="148c1-148">Issue drawing commands.</span></span>
    4.  <span data-ttu-id="148c1-149">呼叫 [**ID2D1RenderTarget：： EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)。</span><span class="sxs-lookup"><span data-stu-id="148c1-149">Call [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>
    5.  <span data-ttu-id="148c1-150">如果 [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 傳回 **D2DERR \_ 重新建立 \_ 目標**，請捨棄轉譯目標和裝置相依的資源。</span><span class="sxs-lookup"><span data-stu-id="148c1-150">If [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) returns **D2DERR\_RECREATE\_TARGET**, discard the render target and device-dependent resources.</span></span>
3.  <span data-ttu-id="148c1-151">每當您需要更新或重繪場景時，重複步驟2。</span><span class="sxs-lookup"><span data-stu-id="148c1-151">Repeat step 2 whenever you need to update or redraw the scene.</span></span>

<span data-ttu-id="148c1-152">如果呈現目標為視窗，則每當視窗收到 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息時，就會發生步驟2。</span><span class="sxs-lookup"><span data-stu-id="148c1-152">If the render target is a window, step 2 occurs whenever the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="148c1-153">此處所顯示的迴圈會捨棄裝置相依的資源，並在下一個迴圈開始時重新建立， (步驟 2a) 來處理裝置遺失。</span><span class="sxs-lookup"><span data-stu-id="148c1-153">The loop shown here handles device loss by discarding the device-dependent resources and re-creating them at the start of the next loop (step 2a).</span></span>

## <a name="next"></a><span data-ttu-id="148c1-154">下一個</span><span class="sxs-lookup"><span data-stu-id="148c1-154">Next</span></span>

[<span data-ttu-id="148c1-155">DPI 和 Device-Independent 圖元</span><span class="sxs-lookup"><span data-stu-id="148c1-155">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)

 

 