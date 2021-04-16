---
title: 舊版支援移動捲軸
description: 本節說明如何在以 Windows 為基礎的應用程式中使用捲軸來移動流覽。
ms.assetid: a8906b48-b804-4f3a-bb9b-dc94b632e2f7
keywords:
- Windows Touch，舊版支援
- 使用捲軸移動流覽
- Windows Touch，使用捲軸移動
- Windows Touch、捲軸
- 捲軸、移動流覽
- 捲軸，舊版支援
- Windows Touch，手勢
- 手勢，使用捲軸移動
- Windows Touch，筆觸
- 筆觸，使用捲軸移動
- 筆觸，停用
- Windows Touch，滑鼠滾輪訊息
- 滑鼠滾輪訊息
- Windows Touch，自訂移動
- 移動流覽、捲軸
- 移動流覽，舊版支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f6b9dd47821205a6aa5b6f07e5053e31597358
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104558925"
---
# <a name="legacy-support-for-panning-with-scroll-bars"></a><span data-ttu-id="d3fd8-119">舊版支援移動捲軸</span><span class="sxs-lookup"><span data-stu-id="d3fd8-119">Legacy Support for Panning with Scroll Bars</span></span>

<span data-ttu-id="d3fd8-120">本節說明如何在以 Windows 為基礎的應用程式中使用捲軸來移動流覽。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-120">This section describes support for panning using scroll bars in Windows-based applications.</span></span>

<span data-ttu-id="d3fd8-121">在 Windows 7 中，移動手勢會產生 WM \_ \* 捲軸訊息，以啟用移動的舊版支援。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-121">In Windows 7, panning gestures generate WM\_\*SCROLL messages to enable legacy support for panning.</span></span> <span data-ttu-id="d3fd8-122">因為您的應用程式可能不支援所有的 WM \_ \* 捲軸訊息，所以移動流覽可能無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-122">Because your applications may not support all of the WM\_\*SCROLL messages, panning may not work correctly.</span></span> <span data-ttu-id="d3fd8-123">本主題說明您必須採取的步驟，以確保應用程式中的舊版移動流覽體驗如使用者預期般運作。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-123">This topic describes the steps you must take to ensure that the legacy panning experience in applications functions as users expect.</span></span>

## <a name="overview"></a><span data-ttu-id="d3fd8-124">概觀</span><span class="sxs-lookup"><span data-stu-id="d3fd8-124">Overview</span></span>

<span data-ttu-id="d3fd8-125">下列各節說明如何啟用舊版的移動體驗：</span><span class="sxs-lookup"><span data-stu-id="d3fd8-125">The following sections explain how to enable the legacy panning experience:</span></span>

-   <span data-ttu-id="d3fd8-126">使用捲軸來建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-126">Create an application with scroll bars.</span></span>
-   <span data-ttu-id="d3fd8-127">停用筆觸。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-127">Disable flicks.</span></span>
-   <span data-ttu-id="d3fd8-128">自訂移動流覽體驗。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-128">Customize the panning experience.</span></span>

## <a name="create-an-application-with-scroll-bars"></a><span data-ttu-id="d3fd8-129">建立具有捲軸的應用程式</span><span class="sxs-lookup"><span data-stu-id="d3fd8-129">Create an Application with Scroll Bars</span></span>

<span data-ttu-id="d3fd8-130">使用 Microsoft Visual Studio wizard 啟動新的 Win32 專案。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-130">Start a new Win32 project using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="d3fd8-131">請確定應用程式類型已設為 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-131">Make sure the application type is set to the Windows application.</span></span> <span data-ttu-id="d3fd8-132">您不需要啟用 Active Template Library (ATL) 的支援。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-132">You don't need to enable support for the Active Template Library (ATL).</span></span> <span data-ttu-id="d3fd8-133">下圖顯示您的專案在啟動後的樣子。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-133">The following image shows what your project will look like after you have started it.</span></span>

![顯示沒有捲軸之視窗的螢幕擷取畫面](images/gpd-1.png)

<span data-ttu-id="d3fd8-135">接下來，啟用影像上的捲軸。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-135">Next, enable scroll bars on the image.</span></span> <span data-ttu-id="d3fd8-136">變更 **InitInstance** 中的視窗建立程式碼，讓 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 函式呼叫建立具有捲軸的視窗。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-136">Change the window creation code in **InitInstance** so that the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function call creates a window with scroll bars.</span></span> <span data-ttu-id="d3fd8-137">下列程式碼示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-137">The following code shows how to do this.</span></span>


```C++
   hWnd = CreateWindow(
      szWindowClass, 
      szTitle, 
      WS_OVERLAPPEDWINDOW | WS_VSCROLL,  // style
      200,                               // x
      200,                               // y
      550,                               // width
      300,                               // height
      NULL,
      NULL,
      hInstance,
      NULL
    );  
```



<span data-ttu-id="d3fd8-138">變更視窗建立程式碼之後，您的應用程式將會有捲軸。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-138">After you have changed the window creation code, your application will have a scroll bar.</span></span> <span data-ttu-id="d3fd8-139">下圖顯示應用程式目前的外觀。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-139">The following image shows how the application might look at this point.</span></span>

![顯示具有垂直捲動條但沒有文字之視窗的螢幕擷取畫面](images/gpd-2.png)

<span data-ttu-id="d3fd8-141">在您變更視窗建立程式碼之後，請在應用程式中加入捲軸物件，並在其中加入一些要滾動的文字。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-141">After you have changed the window creation code, add a scroll bar object to your application and some text to scroll.</span></span> <span data-ttu-id="d3fd8-142">將下列程式碼放在 **WndProc** 方法的頂端。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-142">Place the following code into the top of the **WndProc** method.</span></span>


```C++
    TEXTMETRIC tm;     
    SCROLLINFO si; 
     
    // These variables are required to display text. 
    static int xClient;     // width of client area 
    static int yClient;     // height of client area 
    static int xClientMax;  // maximum width of client area 
     
    static int xChar;       // horizontal scrolling unit 
    static int yChar;       // vertical scrolling unit 
    static int xUpper;      // average width of uppercase letters 
     
    static int xPos;        // current horizontal scrolling position 
    static int yPos;        // current vertical scrolling position 
     
    int i;                  // loop counter 
    int x, y;               // horizontal and vertical coordinates
     
    int FirstLine;          // first line in the invalidated area 
    int LastLine;           // last line in the invalidated area 
    HRESULT hr;
    int abcLength = 0;  // length of an abc[] item

    int lines = 0;

    // Create an array of lines to display. 
    static const int LINES=28;
    static LPCWSTR abc[] = { 
       L"anteater",  L"bear",      L"cougar", 
       L"dingo",     L"elephant",  L"falcon", 
       L"gazelle",   L"hyena",     L"iguana", 
       L"jackal",    L"kangaroo",  L"llama", 
       L"moose",     L"newt",      L"octopus", 
       L"penguin",   L"quail",     L"rat", 
       L"squid",     L"tortoise",  L"urus", 
       L"vole",      L"walrus",    L"xylophone", 
       L"yak",       L"zebra",
       L"This line contains words, but no character. Go figure.",
       L""
     };        
```



<span data-ttu-id="d3fd8-143">接下來，請執行應用程式邏輯來設定文字度量的文字計算。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-143">Next, implement the application logic for configuring the text calculations for text metrics.</span></span> <span data-ttu-id="d3fd8-144">下列程式碼應取代 **WndProc** 函式中的現有 **WM \_ 建立** 案例。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-144">The following code should replace the existing **WM\_CREATE** case in the **WndProc** function.</span></span>


```C++
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hWnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hWnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0;
```



<span data-ttu-id="d3fd8-145">接下來，在調整視窗大小時，執行重新計算文字區塊的應用程式邏輯。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-145">Next, implement the application logic for recalculation of the text block when the window is resized.</span></span> <span data-ttu-id="d3fd8-146">下列程式碼應該放入 **WndProc** 中的訊息參數。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-146">The following code should be placed into the message switch in **WndProc**.</span></span>


```C++
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hWnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hWnd, SB_HORZ, &si, TRUE);            
        return 0;
```



<span data-ttu-id="d3fd8-147">接下來，執行垂直捲動條訊息的應用程式邏輯。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-147">Next, implement the application logic for vertical scroll messages.</span></span> <span data-ttu-id="d3fd8-148">下列程式碼應該放入 **WndProc** 中的訊息參數。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-148">The following code should be placed into the message switch in **WndProc**.</span></span>


```C++
        case WM_VSCROLL:
         // Get all the vertical scroll bar information
         si.cbSize = sizeof (si);
         si.fMask  = SIF_ALL;
         GetScrollInfo (hWnd, SB_VERT, &si);
         // Save the position for comparison later on
         yPos = si.nPos;
         switch (LOWORD (wParam))
         {
         // user clicked the HOME keyboard key
         case SB_TOP:
             si.nPos = si.nMin;
             break;
              
         // user clicked the END keyboard key
         case SB_BOTTOM:
             si.nPos = si.nMax;
             break;
              
         // user clicked the top arrow
         case SB_LINEUP:
             si.nPos -= 1;
             break;
              
         // user clicked the bottom arrow
         case SB_LINEDOWN:
             si.nPos += 1;
             break;
              
         // user clicked the scroll bar shaft above the scroll box
         case SB_PAGEUP:
             si.nPos -= si.nPage;
             break;
              
         // user clicked the scroll bar shaft below the scroll box
         case SB_PAGEDOWN:
             si.nPos += si.nPage;
             break;
              
         // user dragged the scroll box
         case SB_THUMBTRACK:
             si.nPos = si.nTrackPos;
             break;

         // user positioned the scroll box
         // This message is the one used by Windows Touch
         case SB_THUMBPOSITION:
             si.nPos = HIWORD(wParam);
             break;
                            
         default:
              break; 
         }
         // Set the position and then retrieve it.  Due to adjustments
         //   by Windows it may not be the same as the value set.
         si.fMask = SIF_POS;
         SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
         GetScrollInfo (hWnd, SB_VERT, &si);
         // If the position has changed, scroll window and update it
         if (si.nPos != yPos)
         {                    
          ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
          UpdateWindow (hWnd);
         }
         break;
```



<span data-ttu-id="d3fd8-149">接下來，更新程式碼以重新繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-149">Next, update the code to redraw the window.</span></span> <span data-ttu-id="d3fd8-150">下列程式碼應取代 **WndProc** 中的預設 **WM \_ 油漆** 案例。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-150">The following code should replace the default **WM\_PAINT** case in **WndProc**.</span></span>


```C++
    case WM_PAINT:
         // Prepare the window for painting
         hdc = BeginPaint (hWnd, &ps);
         // Get vertical scroll bar position
         si.cbSize = sizeof (si);
         si.fMask  = SIF_POS;
         GetScrollInfo (hWnd, SB_VERT, &si);
         yPos = si.nPos;
         // Get horizontal scroll bar position
         GetScrollInfo (hWnd, SB_HORZ, &si);
         xPos = si.nPos;
         // Find painting limits
         FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
         LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
         
         
         for (i = FirstLine; i <= LastLine; i++)         
         {
              x = xChar * (1 - xPos);
              y = yChar * (i - yPos);
              
              // Note that "55" in the following depends on the 
              // maximum size of an abc[] item.
              //
              abcLength = wcslen(abc[i]);
              hr = S_OK;
              if ((FAILED(hr)))
              {
                 MessageBox(hWnd, L"err", L"err", NULL);
              }else{
                  TextOut(hdc, x, y, abc[i], abcLength);
              }
              
         }
         // Indicate that painting is finished
         EndPaint (hWnd, &ps);
         return 0;
```



<span data-ttu-id="d3fd8-151">現在當您建立並執行您的應用程式時，它應該會有使用中的文字和垂直捲動條。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-151">Now when you build and run your application, it should have the boilerplate text and a vertical scroll bar.</span></span> <span data-ttu-id="d3fd8-152">下圖顯示您的應用程式可能外觀。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-152">The following image shows how your application might look.</span></span>

![顯示具有垂直捲動條和文字之視窗的螢幕擷取畫面](images/gpd-3.png)

## <a name="disable-flicks"></a><span data-ttu-id="d3fd8-154">停用筆觸</span><span class="sxs-lookup"><span data-stu-id="d3fd8-154">Disable Flicks</span></span>

<span data-ttu-id="d3fd8-155">若要改善您應用程式中的移動流覽體驗，您應該關閉筆觸。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-155">To improve the panning experience in your application, you should turn off flicks.</span></span> <span data-ttu-id="d3fd8-156">若要這樣做，請在 *hWnd* 值初始化時，設定視窗屬性。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-156">To do this, set window properties on the *hWnd* value when it is initialized.</span></span> <span data-ttu-id="d3fd8-157">用於筆觸的值會儲存在 tpcshrd 標頭中，也必須包含在內。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-157">The values used for flicks are stored in the tpcshrd.h header, which also must be included.</span></span> <span data-ttu-id="d3fd8-158">在您建立 *hWnd* 之後，下列程式碼應該放在 include 指示詞和 **InitInstance** 函式中。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-158">The following code should be placed in your include directives and in the **InitInstance** function after you have created your *hWnd*.</span></span>

> [!Note]  
> <span data-ttu-id="d3fd8-159">這適用于需要立即針對觸控或觸控事件進行回應的應用程式，而不是測試時間或距離閾值。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-159">This is useful for applications that require immediate feedback on a touch or pen down event instead of testing for a time or distance threshold.</span></span>

 


```C++
#include <tpcshrd.h>
```




```C++
[...]
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow){
[...]
  
```




```C++
   const DWORD_PTR dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
   
   SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
```



## <a name="customize-the-panning-experience"></a><span data-ttu-id="d3fd8-160">自訂移動流覽體驗</span><span class="sxs-lookup"><span data-stu-id="d3fd8-160">Customize the Panning Experience</span></span>

<span data-ttu-id="d3fd8-161">根據預設，您可能會想要使用 Windows 7 提供的不同移動流覽體驗。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-161">You might want a different panning experience than Windows 7 offers by default.</span></span> <span data-ttu-id="d3fd8-162">若要改善移動流覽體驗，您必須加入 [**WM \_ 手勢**](wm-gesture.md) 訊息的處理常式。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-162">To improve the panning experience, you must add the handler for the [**WM\_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="d3fd8-163">如需詳細資訊，請參閱 [改善 Single-Finger 移動體驗](improving-the-single-finger-panning-experience.md)。</span><span class="sxs-lookup"><span data-stu-id="d3fd8-163">For more information, see [Improving the Single-Finger Panning Experience](improving-the-single-finger-panning-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3fd8-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="d3fd8-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3fd8-165">Windows Touch 手勢</span><span class="sxs-lookup"><span data-stu-id="d3fd8-165">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

 