---
title: 改善 Single-Finger 的移動體驗
description: 如果您建立以 Windows Touch 為目標的應用程式，它會自動提供基本的移動流覽支援。 不過，您可以使用 WM \_ 手勢訊息來為單一手指移動提供增強的支援。
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Windows Touch 的單指移動
- Windows Touch，移動流覽
- Windows Touch、捲軸
- Windows Touch，筆觸
- Windows Touch，軌跡平移訊息
- Windows Touch，界限意見反應
- 單一手指移動
- 單向移動
- 移動流覽、界限意見反應
- 捲軸、單鍵移動
- 筆觸，單一手指移動
- 捲軸，停用
- 筆觸，停用
- 手勢，軌跡平移訊息
- 移動流覽、軌跡平移訊息
- 界限意見反應，單一手指移動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9081903600918485f1e3241a02c01b5438c1aae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682537"
---
# <a name="improving-the-single-finger-panning-experience"></a><span data-ttu-id="5b7ae-120">改善 Single-Finger 的移動體驗</span><span class="sxs-lookup"><span data-stu-id="5b7ae-120">Improving the Single-Finger Panning Experience</span></span>

<span data-ttu-id="5b7ae-121">如果您建立以 Windows Touch 為目標的應用程式，它會自動提供基本的移動流覽支援。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-121">If you build an application that targets Windows Touch, it automatically provides basic panning support.</span></span> <span data-ttu-id="5b7ae-122">不過，您可以使用 [**WM \_ 手勢**](wm-gesture.md) 訊息來為單一手指移動提供增強的支援。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-122">However, you can use the [**WM\_GESTURE**](wm-gesture.md) message to provide enhanced support for single-finger panning.</span></span>

## <a name="overview"></a><span data-ttu-id="5b7ae-123">概觀</span><span class="sxs-lookup"><span data-stu-id="5b7ae-123">Overview</span></span>

<span data-ttu-id="5b7ae-124">若要改善單指的移動體驗，請使用下列步驟，如本主題的後續章節所述：</span><span class="sxs-lookup"><span data-stu-id="5b7ae-124">To improve the single-finger panning experience, use these steps, as explained in subsequent sections of this topic:</span></span>

-   <span data-ttu-id="5b7ae-125">建立具有捲軸的應用程式，並停用筆觸。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-125">Create an application with scroll bars and with flicks disabled.</span></span>
-   <span data-ttu-id="5b7ae-126">新增對軌跡平移訊息的支援。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-126">Add support for gesture pan messages.</span></span>
-   <span data-ttu-id="5b7ae-127">啟用彈跳。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-127">Enable bounce.</span></span>

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a><span data-ttu-id="5b7ae-128">建立具有捲軸的應用程式並停用筆觸</span><span class="sxs-lookup"><span data-stu-id="5b7ae-128">Create an Application with Scroll Bars and with Flicks Disabled</span></span>

<span data-ttu-id="5b7ae-129">開始之前，您必須建立具有捲軸的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-129">Before you begin, you must create an application with scroll bars.</span></span> <span data-ttu-id="5b7ae-130">[使用捲軸來移動流覽的舊版支援](legacy-support-for-panning-with-scrollbars.md)會說明此流程。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-130">The section [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) explains this process.</span></span> <span data-ttu-id="5b7ae-131">如果您想要從範例內容開始，請移至該區段，並建立具有捲軸的應用程式，然後停用筆觸。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-131">If you want to start with the example content, go to that section and create an application with scroll bars and then disable flicks.</span></span> <span data-ttu-id="5b7ae-132">如果您已經有具有正常運作捲軸的應用程式，請停用筆觸，如該章節所述。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-132">If you already have an application with functioning scroll bars, disable flicks as described in that section.</span></span>

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a><span data-ttu-id="5b7ae-133">新增軌跡平移訊息的自訂移動流覽支援</span><span class="sxs-lookup"><span data-stu-id="5b7ae-133">Add Custom Panning Support for Gesture Pan Messages</span></span>

<span data-ttu-id="5b7ae-134">若要支援軌跡平移訊息，您必須在 **WndProc** 方法中處理這些訊息。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-134">To support gesture pan messages, you must handle them in the **WndProc** method.</span></span> <span data-ttu-id="5b7ae-135">手勢訊息是用來判斷移動流覽訊息的水準和垂直差異。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-135">The gesture messages are used to determine horizontal and vertical deltas for pan messages.</span></span> <span data-ttu-id="5b7ae-136">差異是用來更新捲軸物件，此物件會更新使用者介面。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-136">The deltas are used to update the scroll bar object, which updates the user interface.</span></span>

<span data-ttu-id="5b7ae-137">首先，更新 targetver.h .h 檔案中的 Windows 版本設定，以啟用 Windows Touch。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-137">First, update the Windows version settings in the targetver.h file to enable Windows Touch.</span></span> <span data-ttu-id="5b7ae-138">下列程式碼顯示各種 Windows 版本設定，這些設定應該取代 targetver.h 中的設定。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-138">The following code shows the various Windows version settings that should replace those in targetver.h.</span></span>


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



<span data-ttu-id="5b7ae-139">接下來，將 UXTheme 檔案新增至您的專案，並將 UXTheme 程式庫新增至專案的其他相依性。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-139">Next, add the UXTheme.h file to your project and add the uxtheme.lib library to the additional dependencies of your project.</span></span>


```C++
#include <uxtheme.h>
```



<span data-ttu-id="5b7ae-140">接下來，將下列變數新增至 **WndProc** 函式的頂端。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-140">Next, add the following variables to the top of the **WndProc** function.</span></span> <span data-ttu-id="5b7ae-141">這些將用於移動用的計算。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-141">These will be used in calculations for panning.</span></span>


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



<span data-ttu-id="5b7ae-142">接下來，新增 [**WM \_ 手勢**](wm-gesture.md) 訊息的處理常式，以便根據移動流覽手勢以差異更新捲軸。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-142">Next, add the handler for the [**WM\_GESTURE**](wm-gesture.md) message so that the scroll bars are updated with deltas based on panning gestures.</span></span> <span data-ttu-id="5b7ae-143">這可讓您更精細地控制移動。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-143">This gives you a much finer-grained control of panning.</span></span>

<span data-ttu-id="5b7ae-144">下列程式碼會從 *lParam* 取得 [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)結構、儲存結構的最後一個 y 座標，以及決定要更新捲軸物件的位置變更。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-144">The following code gets the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure from the *lParam*, saves the last y-coordinate from the structure, and determines the change in position to update the scroll bar object.</span></span> <span data-ttu-id="5b7ae-145">下列程式碼應該放在您的 **WndProc** switch 語句中。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-145">The following code should be placed in your **WndProc** switch statement.</span></span>


```C++
    case WM_GESTURE:        
        // Get all the vertial scroll bar information
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hWnd, SB_VERT, &si);
        yPos = si.nPos;

        ZeroMemory(&gi, sizeof(GESTUREINFO));
        gi.cbSize = sizeof(GESTUREINFO);
        bResult = GetGestureInfo((HGESTUREINFO)lParam, &gi);

        if (bResult){
            // now interpret the gesture            
            switch (gi.dwID){
                case GID_BEGIN:
                   lastY = gi.ptsLocation.y;
                   CloseGestureInfoHandle((HGESTUREINFO)lParam);
                   break;                     
                // A CUSTOM PAN HANDLER
                // COMMENT THIS CASE OUT TO ENABLE DEFAULT HANDLER BEHAVIOR
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin || si.nPos >= (si.nMax - si.nPage)){                    
                        // we reached the bottom / top, pan
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
                case GID_ZOOM:
                   // Add Zoom handler 
                   return DefWindowProc(hWnd, message, lParam, wParam);
                default:
                   // You have encountered an unknown gesture
                   return DefWindowProc(hWnd, message, lParam, wParam);
             }          
        }else{
            DWORD dwErr = GetLastError();
            if (dwErr > 0){
                // something is wrong 
                // 87 indicates that you are probably using a bad
                // value for the gi.cbSize
            }
        } 
        return DefWindowProc (hWnd, message, wParam, lParam);
```



<span data-ttu-id="5b7ae-146">現在，當您在視窗上執行平移手勢時，您會看到具有慣性的文字捲軸。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-146">Now, when you perform the pan gesture on your window, you will see the text scroll with inertia.</span></span> <span data-ttu-id="5b7ae-147">至此，您可能會想要將文字變更為具有更多行，讓您可以探索移動大型文字區段的位置。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-147">At this point, you might want to change the text to have more lines so that you can explore panning large sections of text.</span></span>

## <a name="boundary-feedback-in-wndproc"></a><span data-ttu-id="5b7ae-148">WndProc 中的界限意見反應</span><span class="sxs-lookup"><span data-stu-id="5b7ae-148">Boundary Feedback in WndProc</span></span>

<span data-ttu-id="5b7ae-149">界限意見反應是在使用者到達 pannable 區域結尾時提供給使用者的一種視覺效果意見反應。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-149">Boundary feedback is a type of visual feedback given to users when they reach the end of a pannable area.</span></span> <span data-ttu-id="5b7ae-150">當到達界限時，應用程式會觸發此程式。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-150">It is triggered by the application when a boundary is reached.</span></span> <span data-ttu-id="5b7ae-151">在先前的 [**wm \_ 手勢**](wm-gesture.md) 訊息範例中， `(si.nPos == si.yPos)` 會使用來自 **wm \_ 手勢** 案例的結束條件來測試您已達到 pannable 區域的結尾。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-151">In the previous example implementation of the [**WM\_GESTURE**](wm-gesture.md) message, the end condition `(si.nPos == si.yPos)` from the **WM\_GESTURE** case is used to test that you have reached the end of a pannable region.</span></span> <span data-ttu-id="5b7ae-152">下列變數用來追蹤值和測試錯誤。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-152">The following variables are used to track values and test errors.</span></span>


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



<span data-ttu-id="5b7ae-153">平移手勢案例會更新以觸發界限意見反應。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-153">The pan gesture case is updated to trigger boundary feedback.</span></span> <span data-ttu-id="5b7ae-154">下列程式碼說明來自 [**WM \_ 手勢**](wm-gesture.md)訊息處理常式的 **GID \_ 平移** 案例。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-154">The following code illustrates the **GID\_PAN** case from the [**WM\_GESTURE**](wm-gesture.md) message handler.</span></span>


```C++
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin){                    
                        // we reached the top, pan upwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }else if (si.nPos >= (si.nMax - si.nPage)){
                        // we reached the bottom, pan downwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
  
```



<span data-ttu-id="5b7ae-155">現在，當使用者移動超過捲軸區域底部時，您的應用程式視窗應該會有界限的意見反應。</span><span class="sxs-lookup"><span data-stu-id="5b7ae-155">Now your application's window should have boundary feedback when a user pans past the bottom of the scroll bar region.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b7ae-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b7ae-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b7ae-157">Windows Touch 手勢</span><span class="sxs-lookup"><span data-stu-id="5b7ae-157">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="5b7ae-158">**BeginPanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="5b7ae-158">**BeginPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[<span data-ttu-id="5b7ae-159">**EndPanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="5b7ae-159">**EndPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[<span data-ttu-id="5b7ae-160">**UpdatePanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="5b7ae-160">**UpdatePanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 