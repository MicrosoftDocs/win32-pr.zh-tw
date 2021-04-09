---
title: 'Windows Touch 手勢範例 (MTGestures) '
description: 本節說明 Windows Touch 手勢範例。
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
keywords:
- Windows Touch，程式碼範例
- Windows Touch，範例程式碼
- Windows Touch，手勢
- Windows Touch、手勢範例
- 手勢範例
- 手勢，範例程式碼
- 手勢，程式碼範例
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 0e01d97e844af37caeb5c33f3cb780601da4629d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681395"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a><span data-ttu-id="e5f94-110">Windows Touch 手勢範例 (MTGestures) </span><span class="sxs-lookup"><span data-stu-id="e5f94-110">Windows Touch Gesture Sample (MTGestures)</span></span>

<span data-ttu-id="e5f94-111">本節說明 Windows Touch 手勢範例。</span><span class="sxs-lookup"><span data-stu-id="e5f94-111">This section describes the Windows Touch Gesture sample.</span></span>

<span data-ttu-id="e5f94-112">Windows Touch 手勢範例示範如何使用筆勢訊息來轉譯、旋轉和調整由圖形裝置介面 (GDI) 轉譯的方塊，方法是處理 [**WM_GESTURE**](wm-gesture.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="e5f94-112">The Windows Touch Gesture sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="e5f94-113">下列螢幕擷取畫面顯示範例在執行時的外觀。</span><span class="sxs-lookup"><span data-stu-id="e5f94-113">The following screen shot shows how the sample looks when it is running.</span></span>

![螢幕擷取畫面，顯示正在執行的 windows 觸控手勢範例，並在螢幕上使用旋轉的黑色空心矩形](images/mtgestures.png)

<span data-ttu-id="e5f94-115">在此範例中，會將手勢訊息傳遞至手勢引擎，然後呼叫繪圖物件上的方法，以轉譯、旋轉和縮放具有處理這些命令之方法的物件。</span><span class="sxs-lookup"><span data-stu-id="e5f94-115">For this sample, gesture messages are passed to a gesture engine, which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="e5f94-116">若要協助示範範例的運作方式，請考慮使用兩個點一下命令來啟用或停用轉譯方塊中的對角線線的步驟。</span><span class="sxs-lookup"><span data-stu-id="e5f94-116">To help show how the sample works, consider the steps for using the two-finger tap command to enable or disable diagonal lines in the rendered box.</span></span> <span data-ttu-id="e5f94-117">使用者執行雙向點一下手勢，以產生程式所處理的訊息。</span><span class="sxs-lookup"><span data-stu-id="e5f94-117">A user performs the two-finger tap gesture, which generates a message that is handled by the program.</span></span> <span data-ttu-id="e5f94-118">當處理訊息時，它會切換布林值，以便在繪圖物件上轉譯對角線，然後物件將會轉譯對角線線。</span><span class="sxs-lookup"><span data-stu-id="e5f94-118">When the message is handled, it will toggle a Boolean for rendering diagonals on the drawing object, and the object will then render the diagonal lines.</span></span>

<span data-ttu-id="e5f94-119">下列程式碼示範如何從 WndProc 方法將手勢訊息傳遞至手勢引擎。</span><span class="sxs-lookup"><span data-stu-id="e5f94-119">The following code shows how gesture messages are passed to the gesture engine from the WndProc method.</span></span>

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

<span data-ttu-id="e5f94-120">下列程式碼顯示手勢引擎如何處理雙向的點一下命令。</span><span class="sxs-lookup"><span data-stu-id="e5f94-120">The following code shows how the gesture engine handles the two-finger tap command.</span></span>

```C++
// Two-finger tap command
void CMyGestureEngine::ProcessTwoFingerTap(void)
{
    if(_pcRect)
    {
        _pcRect->ToggleDrawDiagonals();
    }
}
```

<span data-ttu-id="e5f94-121">下列程式碼顯示繪圖物件如何切換對角線。</span><span class="sxs-lookup"><span data-stu-id="e5f94-121">The following code shows how the drawing object toggles its diagonals.</span></span>

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

<span data-ttu-id="e5f94-122">下列程式碼顯示物件如何在其 draw 方法中轉譯對角線線。</span><span class="sxs-lookup"><span data-stu-id="e5f94-122">The following code shows how the object renders diagonal lines in its draw method.</span></span>

```C++
    if(_bDrawDiagonals)
    {
        // draw diagonals
        MoveToEx(hdc,ptRect[0].x,ptRect[0].y,NULL);
        LineTo(hdc,ptRect[2].x,ptRect[2].y);
        MoveToEx(hdc,ptRect[1].x,ptRect[1].y,NULL);
        LineTo(hdc,ptRect[3].x,ptRect[3].y);
    }
```

## <a name="related-topics"></a><span data-ttu-id="e5f94-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5f94-123">Related topics</span></span>

<span data-ttu-id="e5f94-124">[多點觸控手勢應用程式 (c # ) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS)、 [多點觸控手勢應用程式 (c + +) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp)、 [Windows Touch 範例](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="e5f94-124">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
