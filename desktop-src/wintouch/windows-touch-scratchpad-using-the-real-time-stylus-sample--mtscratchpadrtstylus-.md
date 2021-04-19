---
title: '使用即時手寫筆範例 (c + + 的 Windows Touch 便箋) '
description: Windows Touch 的便箋範例 (MTScratchpadRTStylus) 會示範如何使用 Windows Touch 訊息來繪製觸控點至視窗的追蹤。
ms.assetid: c72ddc71-48b7-4c26-af2b-10919038eaf8
keywords:
- Windows Touch，程式碼範例
- Windows Touch，範例程式碼
- Windows Touch，範例簿範例
- 便箋範例
- Windows Touch，即時手寫筆 (RTS) 物件
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 94d425bcb39dd35d3bd71636fb19b6b408af9477
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106969689"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="a2c1f-108">使用即時手寫筆範例 (c + + 的 Windows Touch 便箋) </span><span class="sxs-lookup"><span data-stu-id="a2c1f-108">Windows Touch Scratchpad using the Real-time Stylus Sample (C++)</span></span>

<span data-ttu-id="a2c1f-109">Windows Touch 的便箋範例 ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) 會示範如何使用 Windows Touch 訊息來繪製觸控點至視窗的追蹤。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="a2c1f-110">主要手指的追蹤（先放在數位板上）會以黑色繪製。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="a2c1f-111">次要手指會以六種其他色彩繪製：紅色、綠色、藍色、青色、洋紅和黃色。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta, and yellow.</span></span> <span data-ttu-id="a2c1f-112">下列螢幕擷取畫面顯示應用程式在執行時的外觀。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-112">The following screen shot shows how the application could look while running.</span></span>

![螢幕擷取畫面，其中顯示使用即時手寫筆的 windows touch 攝影範例，並在畫面上顯示綠色、紅色、三個黑色和藍線](images/mtscratchpadrtstylus.png)

<span data-ttu-id="a2c1f-114">在此範例中，會建立即時手寫筆 (RTS) 物件，並啟用多個連絡人點的支援。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-114">For this sample, the Real-time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="a2c1f-115">DynamicRenderer 外掛程式會新增至 RTS 以呈現內容。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="a2c1f-116">外掛程式（ **CSyncEventHandlerRTS**）的執行是追蹤手指的數目，以及變更動態轉譯器繪製的色彩。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-116">A plug-in, **CSyncEventHandlerRTS**, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="a2c1f-117">使用 RTS 外掛程式堆疊中的這兩個外掛程式時，Windows Touch 的便箋會將主要連絡人轉譯為黑色，而其餘的連絡人會以各種不同的色彩呈現。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="a2c1f-118">下列程式碼顯示如何建立 RTS 物件，並支援多個接觸點。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-118">The following code shows how the RTS object is created with support for multiple contact points.</span></span>

```C++
IRealTimeStylus* CreateRealTimeStylus(HWND hWnd)
{
    // Check input argument
    if (hWnd == NULL)
    {
        ASSERT(hWnd && L"CreateRealTimeStylus: invalid argument hWnd");
        return NULL;
    }

    // Create RTS object
    IRealTimeStylus* pRealTimeStylus = NULL;
    HRESULT hr = CoCreateInstance(CLSID_RealTimeStylus, NULL, CLSCTX_ALL, IID_PPV_ARGS(&pRealTimeStylus));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to CoCreateInstance of RealTimeStylus");
        return NULL;
    }

    // Attach RTS object to a window
    hr = pRealTimeStylus->put_HWND((HANDLE_PTR)hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to set window handle");
        pRealTimeStylus->Release();
        return NULL;
    }

    // Register RTS object for receiving multi-touch input.
    IRealTimeStylus3* pRealTimeStylus3 = NULL;
    hr = pRealTimeStylus->QueryInterface(&pRealTimeStylus3);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: cannot access IRealTimeStylus3");
        pRealTimeStylus->Release();
        return NULL;
    }
    hr = pRealTimeStylus3->put_MultiTouchEnabled(TRUE);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to enable multi-touch");
        pRealTimeStylus->Release();
        pRealTimeStylus3->Release();
        return NULL;
    }
    pRealTimeStylus3->Release();

    return pRealTimeStylus;
}
```

<span data-ttu-id="a2c1f-119">下列程式碼顯示如何建立動態轉譯器外掛程式，並將其新增至 RTS。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-119">The following code shows how the dynamic renderer plug-in is created and added to the RTS.</span></span>

```C++
IDynamicRenderer* CreateDynamicRenderer(IRealTimeStylus* pRealTimeStylus)
{
    // Check input argument
    if (pRealTimeStylus == NULL)
    {
        ASSERT(pRealTimeStylus && L"CreateDynamicRenderer: invalid argument RealTimeStylus");
        return NULL;
    }

    // Get window handle from RTS object
    HWND hWnd = NULL;
    HRESULT hr = pRealTimeStylus->get_HWND((HANDLE_PTR*)&hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to get window handle");
        return NULL;
    }

    // Create DynamicRenderer object
    IDynamicRenderer* pDynamicRenderer = NULL;
    hr = CoCreateInstance(CLSID_DynamicRenderer, NULL, CLSCTX_ALL, IID_PPV_ARGS(&pDynamicRenderer));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to CoCreateInstance of DynamicRenderer");
        return NULL;
    }

    // Add DynamicRenderer to the RTS object as a synchronous plugin
    IStylusSyncPlugin* pSyncDynamicRenderer = NULL;
    hr = pDynamicRenderer->QueryInterface(&pSyncDynamicRenderer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to access IStylusSyncPlugin of DynamicRenderer");
        pDynamicRenderer->Release();
        return NULL;
    }

    hr = pRealTimeStylus->AddStylusSyncPlugin(
        0,                      // insert plugin at position 0 in the sync plugin list
        pSyncDynamicRenderer);  // plugin to be inserted - DynamicRenderer
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to add DynamicRenderer to the RealTimeStylus plugins");
        pDynamicRenderer->Release();
        pSyncDynamicRenderer->Release();
        return NULL;
    }

    // Attach DynamicRenderer to the same window RTS object is attached to
    hr = pDynamicRenderer->put_HWND((HANDLE_PTR)hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to set window handle");
        pDynamicRenderer->Release();
        pSyncDynamicRenderer->Release();
        return NULL;
    }

    pSyncDynamicRenderer->Release();

    return pDynamicRenderer;
}
```

<span data-ttu-id="a2c1f-120">下列程式碼會在 **CSyncEventHandlerRTS**（自訂的 RTS 外掛程式）中變更 **StylusDown** 事件處理常式的手寫筆筆觸色彩。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-120">The following code changes the stylus stroke color for the **StylusDown** event handler in the **CSyncEventHandlerRTS**, a custom RTS plug-in.</span></span>

```C++
HRESULT CSyncEventHandlerRTS::StylusDown(
    IRealTimeStylus* /* piRtsSrc */,
    const StylusInfo* /* pStylusInfo */,
    ULONG /* cPropCountPerPkt */,
    LONG* /* pPacket */,
    LONG** /* ppInOutPkt */)
{
    // Get DrawingAttributes of DynamicRenderer
    IInkDrawingAttributes* pDrawingAttributesDynamicRenderer;
    HRESULT hr = g_pDynamicRenderer->get_DrawingAttributes(&pDrawingAttributesDynamicRenderer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CSyncEventHandlerRTS::StylusDown: failed to get RTS's drawing attributes");
        return hr;
    }

    // Set new stroke color to the DrawingAttributes of the DynamicRenderer
    // If there are no fingers down, this is a primary contact
    hr = pDrawingAttributesDynamicRenderer->put_Color(GetTouchColor(m_nContacts == 0));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CSyncEventHandlerRTS::StylusDown: failed to set color");
        pDrawingAttributesDynamicRenderer->Release();
        return hr;
    }

    pDrawingAttributesDynamicRenderer->Release();

    ++m_nContacts;  // Increment finger-down counter

    return S_OK;
}
```

<span data-ttu-id="a2c1f-121">當 *m_nContacts* 值遞增時，它將會變更動態轉譯器中所設定的色彩。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-121">When the *m_nContacts* value is incremented, it will change the color set in the dynamic renderer.</span></span> <span data-ttu-id="a2c1f-122">非主要連絡人的筆觸將會以不同的色彩來繪製。</span><span class="sxs-lookup"><span data-stu-id="a2c1f-122">Strokes that are not the primary contact will be drawn with different colors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2c1f-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="a2c1f-123">Related topics</span></span>

<span data-ttu-id="a2c1f-124">[多點觸控式的程式簿應用程式 (rts/c # ) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)、多點觸控式的 [程式 (RTS/c + +) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)、 [Windows Touch 範例](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="a2c1f-124">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
