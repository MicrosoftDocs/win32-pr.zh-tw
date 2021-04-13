---
title: 'Windows Touch 操作範例 (MTManipulation) '
description: 本節說明 Windows Touch 操作範例。
ms.assetid: 59b9279c-ffa3-42c3-a01f-3ea7aca8f235
keywords:
- Windows Touch，程式碼範例
- Windows Touch，範例程式碼
- Windows Touch，操作
- Windows Touch，操作範例
- 操作，範例程式碼
- 操作，程式碼範例
- 操作範例
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: b93ac4d7cd6724d5475c919c74b90eaf106d2803
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374419"
---
# <a name="windows-touch-manipulation-sample-mtmanipulation"></a>Windows Touch 操作範例 (MTManipulation) 

本節說明 Windows Touch 操作範例。

Windows Touch 操作範例示範如何使用 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 介面轉譯、旋轉和縮放物件，以及如何執行 [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) 事件接收器。 下列螢幕擷取畫面顯示範例在執行時的外觀。

![顯示 windows 觸控操作範例的螢幕擷取畫面，其中有一個旋轉藍色的白色矩形，其藍色線條從相反的邊角繪製](images/mtmanipulation.png)

在此範例中，會建立可透過程式設計方式轉譯、旋轉或縮放的 **CDrawingObject** 類別。 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)介面具現化。 會建立操作事件接收器，以在其函式上接受 **CDrawingObject** 類別和 **IManipulationProcessor** 介面的指標。 IManipulationProcessor 的連接點會在操作事件接收器的執行中建立，因此，由 **IManipulationProcessor** 引發的事件會由事件接收器接收。 觸控資料會送至 **IManipulationProcessor** 介面，然後介面會引發 [**_IManipulationEvent**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) 事件。 **CManipulationEventSink** 類別中的事件處理常式將會藉由呼叫 **CDrawingObject** 指標上的存取子，來更新 **CDrawingObject** 的方向。

下列程式碼顯示如何設定視窗以進行觸控，以及如何將 **CDrawingObject** 和 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 具現化並傳遞至 **CManipulationEventSink** 的函式。

```C++
CDrawingObject g_cRect; // CDrawingObject class holds information about the rectangle
                        // and it is responsible for painting the rectangle.

(...)

BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
(...)
    // Register application window for receiving multi-touch input. Use default settings.
    if (!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multi-touch input", L"Error", MB_OK);
        return FALSE;
    }
    ASSERT(IsTouchWindow(hWnd, NULL));

    // Instantiate the ManipulationProcessor object
    HRESULT hr = CoCreateInstance(__uuidof(ManipulationProcessor), NULL, CLSCTX_ALL, IID_PPV_ARGS(&g_pIManipProc));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"InitInstance: failed to instantiate the ManipulationProcessor object");
        return FALSE;
    }

    // Instantiate the event sink with the manipulation processor and pointer to the rectangle object
    g_pManipulationEventSink = new CManipulationEventSink(&g_cRect);
    if (g_pManipulationEventSink == NULL)
    {
        ASSERT(g_pManipulationEventSink && L"InitInstance: failed to instantiate the CManipulationEventSink class");
        g_pIManipProc->Release();
        g_pIManipProc = NULL;
        return FALSE;
    }

    // Establish the link between ManipulationEventSink and ManipulationProcessor
    if (!g_pManipulationEventSink->Connect(g_pIManipProc))
    {
        ASSERT(FALSE && L"InitInstance: failed to connect ManipulationEventSink and ManipulationProcessor");
        g_pIManipProc->Release();
        g_pIManipProc = NULL;
        g_pManipulationEventSink->Release();
        g_pManipulationEventSink = NULL;
        return FALSE;
    }
```

下列程式碼顯示操作事件接收器 **CManipulationEventSink** 的函式。

```C++
CManipulationEventSink::CManipulationEventSink(CDrawingObject* pcDrawingObject)
:   m_cRefCount(1),
    m_pConnection(NULL),
    m_dwCookie(0),
    m_pcDrawingObject(pcDrawingObject)
{
    ASSERT((pcDrawingObject != NULL) && L"CManipulationEventSink constructor: incorrect argument");
}
```

下列程式碼顯示事件接收器如何連接至操作處理器。

```C++
bool CManipulationEventSink::Connect(IManipulationProcessor* pManipulationProcessor)
{
    // Check input arguments
    if (pManipulationProcessor == NULL)
    {
        ASSERT((pManipulationProcessor != NULL) && L"CManipulationEventSink::Create : incorrect arguments");
        return false;
    }

    // Check object state
    if ((m_dwCookie != 0) || (m_pConnection != NULL))
    {
        ASSERT((m_dwCookie == 0) && (m_pConnection == NULL) && L"CManipulationEventSink::Connect : connection already established");
        return false;
    }

    // Get the container with the connection points.
    IConnectionPointContainer* pConnectionContainer = NULL;
    HRESULT hr = pManipulationProcessor->QueryInterface(&pConnectionContainer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CManipulationEventSink::Connect : failed to get the container with the connection points");
        return false;
    }

    // Get a connection point.
    hr = pConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnection);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CManipulationEventSink::Connect : failed to get a connection point");
        pConnectionContainer->Release();
        return false;
    }

    // Release the connection container.
    pConnectionContainer->Release();

    // Advise. Establishes an advisory connection between the connection point and the
    // caller's sink object.
    hr = m_pConnection->Advise(this, &m_dwCookie);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CManipulationEventSink::Connect : failed to Advise");
        m_pConnection->Release();
        m_pConnection = NULL;
        return false;
    }

    return true;
}
```

下列程式碼顯示如何將觸控資料傳遞給操作事件接收器。

```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
(...)

    switch (message)
    {
 (...)
    // WM_TOUCH message handlers
    case WM_TOUCH:
        {
            // WM_TOUCH message can contain several messages from different contacts
            // packed together.
            // Message parameters need to be decoded:
            UINT  cInputs  = (int) wParam;      // Number of actual per-contact messages
            TOUCHINPUT* pInputs = new TOUCHINPUT[cInputs]; // Allocate the storage for the parameters of the per-contact messages
            if (pInputs == NULL)
            {
                break;
            }
            // Unpack message parameters into the array of TOUCHINPUT structures, each
            // representing a message for one single contact.
            if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT)))
            {
                // For each contact, dispatch the message to the appropriate message
                // handler.
                for (unsigned int i = 0; i < cInputs; i++)
                {
                    if (pInputs[i].dwFlags & TOUCHEVENTF_DOWN)
                    {
                        g_pIManipProc->ProcessDown(pInputs[i].dwID, (FLOAT)pInputs[i].x, (FLOAT)pInputs[i].y);
                    }
                    else if (pInputs[i].dwFlags & TOUCHEVENTF_MOVE)
                    {
                        g_pIManipProc->ProcessMove(pInputs[i].dwID, (FLOAT)pInputs[i].x, (FLOAT)pInputs[i].y);
                    }
                    else if (pInputs[i].dwFlags & TOUCHEVENTF_UP)
                    {
                        g_pIManipProc->ProcessUp(pInputs[i].dwID, (FLOAT)pInputs[i].x, (FLOAT)pInputs[i].y);
                    }
                }
            }
            else
            {
                // error handling, presumably out of memory
                ASSERT(FALSE && L"Error: failed to execute GetTouchInputInfo");
                delete [] pInputs;
                break;
            }
            if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
            {
                // error handling, presumably out of memory
                ASSERT(FALSE && L"Error: failed to execute CloseTouchInputHandle");
                delete [] pInputs;
                break;
            }
            delete [] pInputs;

            // Force redraw of the rectangle
            InvalidateRect(hWnd, NULL, TRUE);
        }
        break;
```

下列程式碼顯示事件處理常式如何更新物件方向和操作差異事件的大小。

```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta(
    /* [in] */ FLOAT /* x */,
    /* [in] */ FLOAT /* y */,
    /* [in] */ FLOAT translationDeltaX,
    /* [in] */ FLOAT translationDeltaY,
    /* [in] */ FLOAT scaleDelta,
    /* [in] */ FLOAT /* expansionDelta */,
    /* [in] */ FLOAT rotationDelta,
    /* [in] */ FLOAT /* cumulativeTranslationX */,
    /* [in] */ FLOAT /* cumulativeTranslationY */,
    /* [in] */ FLOAT /* cumulativeScale */,
    /* [in] */ FLOAT /* cumulativeExpansion */,
    /* [in] */ FLOAT /* cumulativeRotation */)
{
    m_pcDrawingObject->ApplyManipulationDelta(translationDeltaX,translationDeltaY,scaleDelta,rotationDelta);

    return S_OK;
}
```

下列程式碼是在 **CDrawingObject** 類別中執行 **ApplyManipulationDelta** 的程式碼。

```C++
// This function is responsible for manipulation of the rectangle.
// It is called from CManipulationEventSink class.
// in:
//      translationDeltaX - shift of the x-coordinate (1/100 of pixel units)
//      translationDeltaY - shift of the y-coordinate (1/100 of pixel units)
//             scaleDelta - scale factor (zoom in/out)
//          rotationDelta - rotation angle in radians
void CDrawingObject::ApplyManipulationDelta(
    const FLOAT translationDeltaX,
    const FLOAT translationDeltaY,
    const FLOAT scaleDelta,
    const FLOAT rotationDelta
)
{
    _ptCenter.x += (LONG) (translationDeltaX / 100.0);
    _ptCenter.y += (LONG) (translationDeltaY / 100.0);

    _dScalingFactor *= scaleDelta;

    _dRotationAngle -= rotationDelta; // we are substracting because Y-axis is down
}
```

在 **CDrawingObject** 的中心點、縮放比例和旋轉角度更新之後，物件將會自行轉換。

## <a name="related-topics"></a>相關主題

[多點觸控操作應用程式](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp)、 [操作和慣性範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp)、 [Windows Touch 範例](windows-touch-samples.md)
