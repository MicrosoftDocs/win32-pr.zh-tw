---
title: 'Windows Touch (的 c + + 範例) '
description: Windows Touch 的便箋範例示範如何使用 Windows Touch 的訊息，將觸控點的追蹤繪製至視窗。
ms.assetid: 6c4b4595-1e95-499c-b045-b5ae01aa5a6e
keywords:
- Windows Touch，程式碼範例
- Windows Touch，範例程式碼
- Windows Touch，範例簿範例
- 便箋範例
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: afdd39e886d97671942b4ff67a74c0da75924fbb
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024294"
---
# <a name="windows-touch-scratchpad-sample-c"></a><span data-ttu-id="5d0d9-107">Windows Touch (的 c + + 範例) </span><span class="sxs-lookup"><span data-stu-id="5d0d9-107">Windows Touch Scratchpad Sample (C++)</span></span>

<span data-ttu-id="5d0d9-108">[Windows Touch 的便箋範例示範](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md)如何使用 Windows Touch 的訊息，將觸控點的追蹤繪製至視窗。</span><span class="sxs-lookup"><span data-stu-id="5d0d9-108">The [Windows Touch Scratchpad sample](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="5d0d9-109">主要手指的追蹤（先放在數位板上）會以黑色繪製。</span><span class="sxs-lookup"><span data-stu-id="5d0d9-109">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="5d0d9-110">次要手指會以六種其他色彩繪製：紅色、綠色、藍色、青色、洋紅和黃色。</span><span class="sxs-lookup"><span data-stu-id="5d0d9-110">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta, and yellow.</span></span> <span data-ttu-id="5d0d9-111">下圖顯示應用程式在執行時的外觀。</span><span class="sxs-lookup"><span data-stu-id="5d0d9-111">The following image shows how the application could look while running.</span></span>

![螢幕擷取畫面，顯示 windows 觸控式的便箋，螢幕上有紅色和黑色波浪線](images/mtscratchpadwmtouch.png)

<span data-ttu-id="5d0d9-113">針對此應用程式，此視窗會註冊為觸控視窗、觸控訊息會被解釋為將觸控點新增至筆劃物件，並將筆墨筆劃轉譯至 **WM_PAINT** 訊息處理常式中的螢幕。</span><span class="sxs-lookup"><span data-stu-id="5d0d9-113">For this application, the window is registered as a touch window, touch messages are interpreted to add touch points to stroke objects, and ink strokes are rendered to the screen in the **WM_PAINT** message handler.</span></span>

<span data-ttu-id="5d0d9-114">下列程式碼顯示如何將視窗註冊為觸控視窗。</span><span class="sxs-lookup"><span data-stu-id="5d0d9-114">The following code shows how the window is registered as a touch window.</span></span>

```C++
    // Register application window for receiving multitouch input. Use default settings.
    if(!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multitouch input", L"Error", MB_OK);
        return FALSE;
    }
```

<span data-ttu-id="5d0d9-115">下列程式碼示範如何使用觸控訊息將觸控點新增至筆跡筆觸。</span><span class="sxs-lookup"><span data-stu-id="5d0d9-115">The following code shows how touch messages are used to add touch points to ink strokes.</span></span>

```C++
        // WM_TOUCH message handlers
        case WM_TOUCH:
            {
                // WM_TOUCH message can contain several messages from different contacts
                // packed together.
                // Message parameters need to be decoded:
                unsigned int numInputs = (unsigned int) wParam; // Number of actual per-contact messages
                TOUCHINPUT* ti = new TOUCHINPUT[numInputs]; // Allocate the storage for the parameters of the per-contact messages
                if(ti == NULL)
                {
                    break;
                }
                // Unpack message parameters into the array of TOUCHINPUT structures, each
                // representing a message for one single contact.
                if(GetTouchInputInfo((HTOUCHINPUT)lParam, numInputs, ti, sizeof(TOUCHINPUT)))
                {
                    // For each contact, dispatch the message to the appropriate message
                    // handler.
                    for(unsigned int i=0; i<numInputs; ++i)
                    {
                        if(ti[i].dwFlags & TOUCHEVENTF_DOWN)
                        {
                            OnTouchDownHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_MOVE)
                        {
                            OnTouchMoveHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_UP)
                        {
                            OnTouchUpHandler(hWnd, ti[i]);
                        }
                    }
                }
                CloseTouchInputHandle((HTOUCHINPUT)lParam);
                delete [] ti;
            }
            break;
```

<span data-ttu-id="5d0d9-116">下列程式碼顯示如何在 **WM_PAINT** 訊息處理常式中，將筆墨筆觸繪製到螢幕。</span><span class="sxs-lookup"><span data-stu-id="5d0d9-116">The following code shows how the ink strokes are drawn to the screen in the **WM_PAINT** message handler.</span></span>

```C++
        case WM_PAINT:
            hdc = BeginPaint(hWnd, &ps);
            // Full redraw: draw complete collection of finished strokes and
            // also all the strokes that are currently in drawing.
            g_StrkColFinished.Draw(hdc);
            g_StrkColDrawing.Draw(hdc);
            EndPaint(hWnd, &ps);
            break;
```

<span data-ttu-id="5d0d9-117">下列程式碼顯示筆觸物件如何將筆劃轉譯至螢幕。</span><span class="sxs-lookup"><span data-stu-id="5d0d9-117">The following code shows how the stroke object renders strokes to the screen.</span></span>

```C++
void CStroke::Draw(HDC hDC) const
{
    if(m_nCount < 2)
    {
        return;
    }

    HPEN hPen = CreatePen(PS_SOLID, 3, m_clr);
    HGDIOBJ hOldPen = SelectObject(hDC, hPen);
    Polyline(hDC, m_arrData, m_nCount);
    SelectObject(hDC, hOldPen);
    DeleteObject(hPen);
}
```

## <a name="related-topics"></a><span data-ttu-id="5d0d9-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d0d9-118">Related topics</span></span>

<span data-ttu-id="5d0d9-119">[Windows Touch 的 (的範例 c # ) ](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md)、 [多點觸控式的應用程式 (WM_TOUCH/c # ) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS)、 [多點觸控式的便箋應用程式 (WM_TOUCH/c + +) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp)、 [Windows Touch 範例](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="5d0d9-119">[Windows Touch Scratchpad Sample (C#)](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md), [Multi-touch Scratchpad Application (WM_TOUCH/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [Multi-touch Scratchpad Application (WM_TOUCH/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
