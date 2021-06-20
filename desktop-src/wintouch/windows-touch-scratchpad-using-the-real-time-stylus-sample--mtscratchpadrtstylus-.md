---
title: '使用即時手寫筆範例 (c + + 的 Windows Touch 便箋) '
description: 複習 Windows Touch 的 (MTScratchpadRTStylus) 範例，其中會示範如何使用 Windows Touch 的訊息，將觸控點的追蹤繪製至視窗。
ms.assetid: c72ddc71-48b7-4c26-af2b-10919038eaf8
keywords:
- Windows Touch，程式碼範例
- Windows Touch，範例程式碼
- Windows Touch，範例簿範例
- 便箋範例
- Windows Touch，即時手寫筆 (RTS) 物件
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 42e32e66942f3dcfad11b8b777e846e0cee6c0b3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406291"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>使用即時手寫筆範例 (c + + 的 Windows Touch 便箋) 

Windows Touch 的便箋範例 ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) 會示範如何使用 Windows Touch 訊息來繪製觸控點至視窗的追蹤。 主要手指的追蹤（先放在數位板上）會以黑色繪製。 次要手指會以六種其他色彩繪製：紅色、綠色、藍色、青色、洋紅和黃色。 下列螢幕擷取畫面顯示應用程式在執行時的外觀。

![螢幕擷取畫面，其中顯示使用即時手寫筆的 windows touch 攝影範例，並在畫面上顯示綠色、紅色、三個黑色和藍線](images/mtscratchpadrtstylus.png)

在此範例中，會建立即時手寫筆 (RTS) 物件，並啟用多個連絡人點的支援。 DynamicRenderer 外掛程式會新增至 RTS 以呈現內容。 外掛程式（ **CSyncEventHandlerRTS**）的執行是追蹤手指的數目，以及變更動態轉譯器繪製的色彩。 使用 RTS 外掛程式堆疊中的這兩個外掛程式時，Windows Touch 的便箋會將主要連絡人轉譯為黑色，而其餘的連絡人會以各種不同的色彩呈現。

下列程式碼顯示如何建立 RTS 物件，並支援多個接觸點。

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

下列程式碼顯示如何建立動態轉譯器外掛程式，並將其新增至 RTS。

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

下列程式碼會在 **CSyncEventHandlerRTS**（自訂的 RTS 外掛程式）中變更 **StylusDown** 事件處理常式的手寫筆筆觸色彩。

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

當 *m_nContacts* 值遞增時，它將會變更動態轉譯器中所設定的色彩。 非主要連絡人的筆觸將會以不同的色彩來繪製。

## <a name="related-topics"></a>相關主題

[多點觸控式的程式簿應用程式 (rts/c # ) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)、多點觸控式的 [程式 (RTS/c + +) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)、 [Windows Touch 範例](windows-touch-samples.md)
