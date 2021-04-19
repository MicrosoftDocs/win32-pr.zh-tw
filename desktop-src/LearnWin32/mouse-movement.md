---
title: 滑鼠移動
description: 滑鼠移動
ms.assetid: 54366E9B-470A-4155-8A5F-425BAC8AC1A5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14176310882651cdeb2939d0db55368ff133ea11
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "106998557"
---
# <a name="mouse-movement"></a><span data-ttu-id="3824f-103">滑鼠移動</span><span class="sxs-lookup"><span data-stu-id="3824f-103">Mouse Movement</span></span>

<span data-ttu-id="3824f-104">當移動滑鼠時，Windows 會張貼 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息。</span><span class="sxs-lookup"><span data-stu-id="3824f-104">When the mouse moves, Windows posts a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="3824f-105">根據預設， **WM \_ MOUSEMOVE** 會移至包含資料指標的視窗。</span><span class="sxs-lookup"><span data-stu-id="3824f-105">By default, **WM\_MOUSEMOVE** goes to the window that contains the cursor.</span></span> <span data-ttu-id="3824f-106">您可以藉由 *捕捉* 滑鼠（如下一節所述）來覆寫此行為。</span><span class="sxs-lookup"><span data-stu-id="3824f-106">You can override this behavior by *capturing* the mouse, which is described in the next section.</span></span>

<span data-ttu-id="3824f-107">[**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)訊息包含的參數與滑鼠點擊的訊息相同。</span><span class="sxs-lookup"><span data-stu-id="3824f-107">The [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message contains the same parameters as the messages for mouse clicks.</span></span> <span data-ttu-id="3824f-108">*LParam* 的最低16位包含 x 座標，後面的16個位包含 y 座標。</span><span class="sxs-lookup"><span data-stu-id="3824f-108">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="3824f-109">使用 [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 並 [**取得 \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏，將座標從 *LPARAM* 解壓縮。</span><span class="sxs-lookup"><span data-stu-id="3824f-109">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span> <span data-ttu-id="3824f-110">*WParam* 參數包含位 **or** of 旗標，表示另一個滑鼠按鍵的狀態以及 SHIFT 和 CTRL 鍵。</span><span class="sxs-lookup"><span data-stu-id="3824f-110">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span> <span data-ttu-id="3824f-111">下列程式碼會從 *lParam* 取得滑鼠座標。</span><span class="sxs-lookup"><span data-stu-id="3824f-111">The following code gets the mouse coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="3824f-112">請記住，這些座標是以圖元為單位，而不是與裝置無關的圖元 (Dip) 。</span><span class="sxs-lookup"><span data-stu-id="3824f-112">Remember that these coordinates are in pixels, not device-independent pixels (DIPs).</span></span> <span data-ttu-id="3824f-113">稍後在本主題中，我們將探討在兩個單元之間轉換的程式碼。</span><span class="sxs-lookup"><span data-stu-id="3824f-113">Later in this topic, we will look at code that converts between the two units.</span></span>

<span data-ttu-id="3824f-114">如果資料指標的位置與視窗相對，則視窗也可以收到 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息。</span><span class="sxs-lookup"><span data-stu-id="3824f-114">A window can also receive a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message if the position of the cursor changes relative to the window.</span></span> <span data-ttu-id="3824f-115">例如，如果游標位於視窗上，而使用者隱藏了視窗，即使滑鼠未移動，視窗仍會收到 **WM 的 \_ MOUSEMOVE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="3824f-115">For example, if the cursor is positioned over a window, and the user hides the window, the window receives **WM\_MOUSEMOVE** messages even if the mouse did not move.</span></span> <span data-ttu-id="3824f-116">這種行為的結果之一，是在 **WM \_ MOUSEMOVE** 訊息之間的滑鼠座標可能不會變更。</span><span class="sxs-lookup"><span data-stu-id="3824f-116">One consequence of this behavior is that the mouse coordinates might not change between **WM\_MOUSEMOVE** messages.</span></span>

## <a name="capturing-mouse-movement-outside-the-window"></a><span data-ttu-id="3824f-117">在視窗外捕捉滑鼠移動</span><span class="sxs-lookup"><span data-stu-id="3824f-117">Capturing Mouse Movement Outside the Window</span></span>

<span data-ttu-id="3824f-118">根據預設，如果滑鼠移動超過工作區邊緣，則視窗會停止接收 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息。</span><span class="sxs-lookup"><span data-stu-id="3824f-118">By default, a window stops receiving [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages if the mouse moves past the edge of the client area.</span></span> <span data-ttu-id="3824f-119">但是針對某些作業，您可能需要在這個點之後追蹤滑鼠位置。</span><span class="sxs-lookup"><span data-stu-id="3824f-119">But for some operations, you might need to track the mouse position beyond this point.</span></span> <span data-ttu-id="3824f-120">例如，繪圖程式可能會讓使用者將選取矩形拖曳到視窗邊緣以外的範圍，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="3824f-120">For example, a drawing program might enable the user to drag the selection rectangle beyond the edge of the window, as shown in the following diagram.</span></span>

![滑鼠捕捉的圖例。](images/input01.png)

<span data-ttu-id="3824f-122">若要在視窗邊緣之後接收滑鼠移動訊息，請呼叫 [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) 函數。</span><span class="sxs-lookup"><span data-stu-id="3824f-122">To receive mouse-move messages past the edge of the window, call the [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) function.</span></span> <span data-ttu-id="3824f-123">呼叫此函式之後，只要使用者至少按住一個滑鼠按鍵，就會繼續收到 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息，即使滑鼠移至視窗外也一樣。</span><span class="sxs-lookup"><span data-stu-id="3824f-123">After this function is called, the window will continue to receive [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages for as long as the user holds at least one mouse button down, even if the mouse moves outside the window.</span></span> <span data-ttu-id="3824f-124">[捕獲] 視窗必須是前景視窗，而且一次只能有一個視窗是 [捕獲] 視窗。</span><span class="sxs-lookup"><span data-stu-id="3824f-124">The capture window must be the foreground window, and only one window can be the capture window at a time.</span></span> <span data-ttu-id="3824f-125">若要釋放滑鼠捕捉，請呼叫 [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) 函式。</span><span class="sxs-lookup"><span data-stu-id="3824f-125">To release mouse capture, call the [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) function.</span></span>

<span data-ttu-id="3824f-126">您通常會以下列方式使用 [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) 和 [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) 。</span><span class="sxs-lookup"><span data-stu-id="3824f-126">You would typically use [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) and [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) in the following way.</span></span>

1.  <span data-ttu-id="3824f-127">當使用者按下滑鼠左鍵時，請呼叫 [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) 來開始捕獲滑鼠。</span><span class="sxs-lookup"><span data-stu-id="3824f-127">When the user presses the left mouse button, call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to start capturing the mouse.</span></span>
2.  <span data-ttu-id="3824f-128">回應滑鼠移動的訊息。</span><span class="sxs-lookup"><span data-stu-id="3824f-128">Respond to mouse-move messages.</span></span>
3.  <span data-ttu-id="3824f-129">當使用者放開滑鼠左鍵時，請呼叫 [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture)。</span><span class="sxs-lookup"><span data-stu-id="3824f-129">When the user releases the left mouse button, call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).</span></span>

## <a name="example-drawing-circles"></a><span data-ttu-id="3824f-130">範例：繪製圓形</span><span class="sxs-lookup"><span data-stu-id="3824f-130">Example: Drawing Circles</span></span>

<span data-ttu-id="3824f-131">讓我們藉由讓使用者使用滑鼠繪製圓形，來擴充 [模組 3](module-3---windows-graphics.md) 的圓形程式。</span><span class="sxs-lookup"><span data-stu-id="3824f-131">Let's extend the Circle program from [Module 3](module-3---windows-graphics.md) by enabling the user to draw a circle with the mouse.</span></span> <span data-ttu-id="3824f-132">從 [Direct2D 圓形範例](direct2d-circle-sample.md) 程式開始。</span><span class="sxs-lookup"><span data-stu-id="3824f-132">Start with the [Direct2D Circle Sample](direct2d-circle-sample.md) program.</span></span> <span data-ttu-id="3824f-133">我們將修改此範例中的程式碼，以新增簡單的繪圖。</span><span class="sxs-lookup"><span data-stu-id="3824f-133">We will modify the code in this sample to add simple drawing.</span></span> <span data-ttu-id="3824f-134">首先，將新的成員變數新增至 `MainWindow` 類別。</span><span class="sxs-lookup"><span data-stu-id="3824f-134">First, add a new member variable to the `MainWindow` class.</span></span>


```C++
    D2D1_POINT_2F           ptMouse;
```



<span data-ttu-id="3824f-135">當使用者拖曳滑鼠時，這個變數會儲存滑鼠下移的位置。</span><span class="sxs-lookup"><span data-stu-id="3824f-135">This variable stores the mouse-down position while the user is dragging the mouse.</span></span> <span data-ttu-id="3824f-136">在此函式中 `MainWindow` ，初始化 *省略號* 和 *ptMouse* 變數。</span><span class="sxs-lookup"><span data-stu-id="3824f-136">In the `MainWindow` constructor, initialize the *ellipse* and *ptMouse* variables.</span></span>


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



<span data-ttu-id="3824f-137">移除方法的主體 `MainWindow::CalculateLayout` ; 此範例不需要它。</span><span class="sxs-lookup"><span data-stu-id="3824f-137">Remove the body of the `MainWindow::CalculateLayout` method; it's not required for this example.</span></span>


```C++
    void    CalculateLayout() { }
```



<span data-ttu-id="3824f-138">接下來，宣告左邊按鈕的訊息處理常式、向上左鍵和滑鼠移動訊息。</span><span class="sxs-lookup"><span data-stu-id="3824f-138">Next, declare message handlers for the left-button down, left-button up, and mouse-move messages.</span></span>


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



<span data-ttu-id="3824f-139">滑鼠座標是以實體圖元為單位，但 Direct2D 預期與裝置無關的圖元 (Dip) 。</span><span class="sxs-lookup"><span data-stu-id="3824f-139">Mouse coordinates are given in physical pixels, but Direct2D expects device-independent pixels (DIPs).</span></span> <span data-ttu-id="3824f-140">若要正確處理高 DPI 設定，您必須將圖元座標轉譯為 Dip。</span><span class="sxs-lookup"><span data-stu-id="3824f-140">To handle high-DPI settings correctly, you must translate the pixel coordinates into DIPs.</span></span> <span data-ttu-id="3824f-141">如需 DPI 的詳細討論，請參閱 [DPI 和 Device-Independent 圖元](dpi-and-device-independent-pixels.md)。</span><span class="sxs-lookup"><span data-stu-id="3824f-141">For more discussion about DPI, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span> <span data-ttu-id="3824f-142">下列程式碼顯示可將圖元轉換成 Dip 的 helper 類別。</span><span class="sxs-lookup"><span data-stu-id="3824f-142">The following code shows a helper class that converts pixels into DIPs.</span></span>


```C++
class DPIScale
{
    static float scaleX;
    static float scaleY;

public:
    static void Initialize(ID2D1Factory *pFactory)
    {
        FLOAT dpiX, dpiY;
        pFactory->GetDesktopDpi(&dpiX, &dpiY);
        scaleX = dpiX/96.0f;
        scaleY = dpiY/96.0f;
    }

    template <typename T>
    static D2D1_POINT_2F PixelsToDips(T x, T y)
    {
        return D2D1::Point2F(static_cast<float>(x) / scaleX, static_cast<float>(y) / scaleY);
    }
};

float DPIScale::scaleX = 1.0f;
float DPIScale::scaleY = 1.0f;
```



<span data-ttu-id="3824f-143">`DPIScale::Initialize`在您建立 Direct2D factory 物件之後，于 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)處理常式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="3824f-143">Call `DPIScale::Initialize` in your [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) handler, after you create the Direct2D factory object.</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        DPIScale::Initialize(pFactory);
        return 0;
```



<span data-ttu-id="3824f-144">若要從滑鼠訊息的 Dip 中取得滑鼠座標，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="3824f-144">To get the mouse coordinates in DIPs from the mouse messages, do the following:</span></span>

1.  <span data-ttu-id="3824f-145">使用 [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 並 [**取得 \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏來取得圖元座標。</span><span class="sxs-lookup"><span data-stu-id="3824f-145">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to get the pixel coordinates.</span></span> <span data-ttu-id="3824f-146">這些巨集定義于 WindowsX 中，因此請記得將該標頭包含在您的專案中。</span><span class="sxs-lookup"><span data-stu-id="3824f-146">These macros are defined in WindowsX.h, so remember to include that header in your project.</span></span>
2.  <span data-ttu-id="3824f-147">呼叫 `DPIScale::PixelsToDipsX` 並 `DPIScale::PixelsToDipsY` 將圖元轉換為 dip。</span><span class="sxs-lookup"><span data-stu-id="3824f-147">Call `DPIScale::PixelsToDipsX` and `DPIScale::PixelsToDipsY` to convert pixels to DIPs.</span></span>

<span data-ttu-id="3824f-148">現在將訊息處理常式新增至您的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="3824f-148">Now add the message handlers to your window procedure.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        OnLButtonDown(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;

    case WM_LBUTTONUP: 
        OnLButtonUp();
        return 0;

    case WM_MOUSEMOVE: 
        OnMouseMove(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;
```



<span data-ttu-id="3824f-149">最後，執行訊息處理常式本身。</span><span class="sxs-lookup"><span data-stu-id="3824f-149">Finally, implement the message handlers themselves.</span></span>

### <a name="left-button-down"></a><span data-ttu-id="3824f-150">向下鍵向下按鈕</span><span class="sxs-lookup"><span data-stu-id="3824f-150">Left Button Down</span></span>

<span data-ttu-id="3824f-151">針對左側按鈕的訊息，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="3824f-151">For the left-button down message, do the following:</span></span>

1.  <span data-ttu-id="3824f-152">呼叫 [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) 以開始捕獲滑鼠。</span><span class="sxs-lookup"><span data-stu-id="3824f-152">Call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to begin capturing the mouse.</span></span>
2.  <span data-ttu-id="3824f-153">將滑鼠按一下的位置儲存在 *ptMouse* 變數中。</span><span class="sxs-lookup"><span data-stu-id="3824f-153">Store the position of the mouse click in the *ptMouse* variable.</span></span> <span data-ttu-id="3824f-154">這個位置會定義橢圓形周框方塊的左上角。</span><span class="sxs-lookup"><span data-stu-id="3824f-154">This position defines the upper left corner of the bounding box for the ellipse.</span></span>
3.  <span data-ttu-id="3824f-155">重設橢圓形結構。</span><span class="sxs-lookup"><span data-stu-id="3824f-155">Reset the ellipse structure.</span></span>
4.  <span data-ttu-id="3824f-156">呼叫 [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)。</span><span class="sxs-lookup"><span data-stu-id="3824f-156">Call [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="3824f-157">此函數會強制重新繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="3824f-157">This function forces the window to be repainted.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a><span data-ttu-id="3824f-158">滑鼠移動</span><span class="sxs-lookup"><span data-stu-id="3824f-158">Mouse Move</span></span>

<span data-ttu-id="3824f-159">針對滑鼠移動訊息，檢查滑鼠左鍵是否已關閉。</span><span class="sxs-lookup"><span data-stu-id="3824f-159">For the mouse-move message, check whether the left mouse button is down.</span></span> <span data-ttu-id="3824f-160">如果是，請重新計算省略號，然後重新繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="3824f-160">If it is, recalculate the ellipse and repaint the window.</span></span> <span data-ttu-id="3824f-161">在 Direct2D 中，會以中心點和 x 和 y 半徑來定義橢圓形。</span><span class="sxs-lookup"><span data-stu-id="3824f-161">In Direct2D, an ellipse is defined by the center point and x- and y-radii.</span></span> <span data-ttu-id="3824f-162">我們想要繪製一個橢圓形，使其符合滑鼠下點所定義的周框方塊 (*ptMouse*) 和目前的游標位置 (*x*， *y*) ，因此需要一點算術才能找出橢圓形的寬度、高度和位置。</span><span class="sxs-lookup"><span data-stu-id="3824f-162">We want to draw an ellipse that fits the bounding box defined by the mouse-down point (*ptMouse*) and the current cursor position (*x*, *y*), so a bit of arithmetic is needed to find the width, height, and position of the ellipse.</span></span>

<span data-ttu-id="3824f-163">下列程式碼會重新計算省略號，然後呼叫 [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) 來重新繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="3824f-163">The following code recalculates the ellipse and then calls [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) to repaint the window.</span></span>

![顯示有 x 和 y 半徑之橢圓形的圖表。](images/input02.png)


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    if (flags & MK_LBUTTON) 
    { 
        const D2D1_POINT_2F dips = DPIScale::PixelsToDips(pixelX, pixelY);

        const float width = (dips.x - ptMouse.x) / 2;
        const float height = (dips.y - ptMouse.y) / 2;
        const float x1 = ptMouse.x + width;
        const float y1 = ptMouse.y + height;

        ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);

        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



### <a name="left-button-up"></a><span data-ttu-id="3824f-165">左方按鈕向上鍵</span><span class="sxs-lookup"><span data-stu-id="3824f-165">Left Button Up</span></span>

<span data-ttu-id="3824f-166">針對左側按鈕的訊息，只要呼叫 [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) 來釋放滑鼠捕捉。</span><span class="sxs-lookup"><span data-stu-id="3824f-166">For the left-button-up message, simply call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) to release the mouse capture.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a><span data-ttu-id="3824f-167">下一個</span><span class="sxs-lookup"><span data-stu-id="3824f-167">Next</span></span>

[<span data-ttu-id="3824f-168">其他滑鼠操作</span><span class="sxs-lookup"><span data-stu-id="3824f-168">Other Mouse Operations</span></span>](other-mouse-operations.md)

 

 