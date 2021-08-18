---
title: 在非受控碼中新增操作支援
description: 本節說明如何藉由執行 IManipulationEvents 介面的事件接收，來將操作支援新增至非受控程式碼 \_ 。
ms.assetid: 7d8c6230-eaca-43c7-ad2f-651851b69d7f
keywords:
- Windows觸控、操作
- Windows觸控、_IManipulationEvents 介面
- WindowsTouch、IManipulationProcessor 介面
- 操作，在非受控碼中新增支援
- 操作，非受控碼支援
- 操作，支援非受控碼
- 操作，_IManipulationEvents 介面
- 操作，IManipulationProcessor 介面
- _IManipulationEvents 介面，在非受控碼中操作支援
- IManipulationProcessor 介面，在非受控碼中操作支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ff526c128b6da83fae3a74b88cd3bb21bc3a81c507c0a76a7c70dbddc5f76d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709998"
---
# <a name="adding-manipulation-support-in-unmanaged-code"></a>在非受控碼中新增操作支援

本節說明如何藉由執行 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)介面的事件接收，來將操作支援新增至非受控程式碼。

下圖概述操作架構。

![顯示傳遞給物件操作處理器的 windows 觸控訊息的圖例，該物件會使用 imanipulationevents 介面來處理事件。 \-](images/manipulation-arch.png)

從 [**WM \_ 觸控**](wm-touchdown.md) 訊息接收的觸控資料會連同觸控訊息中的連絡人識別碼一起傳遞給 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 。 根據訊息序列， **IManipulationProcessor** 介面將會計算要執行的轉換類型，以及與此轉換相關聯的值。 然後， **IManipulationProcessor** 會產生由事件接收器處理的 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) 。 然後，事件接收器可以使用這些值，在要轉換的物件上執行自訂作業。

若要將操作支援新增至您的應用程式，您必須遵循下列步驟：

1.  執行 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)介面的事件接收。
2.  建立 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 介面的實例。
3.  建立事件接收器的實例，並設定觸控事件。
4.  將觸控事件資料傳送給操作處理器。

本節說明將操作支援新增至應用程式時必須遵循的步驟。 系統會在每個步驟提供程式碼，讓您開始使用。

> [!Note]  
> 您無法同時使用操作和筆勢，因為筆勢和觸控訊息是互斥的。

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a>執行 IManipualtionEvents 介面的事件接收 \_

建立事件接收器的實例之前，您必須先建立一個類別來執行事件的 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)介面。 這是您的事件接收器。 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)介面所產生的事件是由事件接收器處理。 下列程式碼顯示繼承 **\_ IManipulationEvents** 介面之類別的範例標頭。

```C++
// Manipulation Header Files
#include <comdef.h>
#include <manipulations.h>
#include <ocidl.h>

class CManipulationEventSink : _IManipulationEvents
{
public:
    CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd);

    int GetStartedEventCount();
    int GetDeltaEventCount();
    int GetCompletedEventCount();
    double CManipulationEventSink::GetX();
    double CManipulationEventSink::GetY();        

    ~CManipulationEventSink();

    //////////////////////////////
    // IManipulationEvents methods
    //////////////////////////////
    virtual HRESULT STDMETHODCALLTYPE ManipulationStarted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationDelta( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y,
        /* [in] */ FLOAT translationDeltaX,
        /* [in] */ FLOAT translationDeltaY,
        /* [in] */ FLOAT scaleDelta,
        /* [in] */ FLOAT expansionDelta,
        /* [in] */ FLOAT rotationDelta,
        /* [in] */ FLOAT cumulativeTranslationX,
        /* [in] */ FLOAT cumulativeTranslationY,
        /* [in] */ FLOAT cumulativeScale,
        /* [in] */ FLOAT cumulativeExpansion,
        /* [in] */ FLOAT cumulativeRotation);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationCompleted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y,
        /* [in] */ FLOAT cumulativeTranslationX,
        /* [in] */ FLOAT cumulativeTranslationY,
        /* [in] */ FLOAT cumulativeScale,
        /* [in] */ FLOAT cumulativeExpansion,
        /* [in] */ FLOAT cumulativeRotation);

    ////////////////////////////////////////////////////////////
    // IUnknown methods
    ////////////////////////////////////////////////////////////
    STDMETHOD_(ULONG, AddRef)(void);
    STDMETHOD_(ULONG, Release)(void);
    STDMETHOD(QueryInterface)(REFIID riid, LPVOID *ppvObj);

private:
    double m_fX;
    double m_fY;

    int m_cRefCount;
    int m_cStartedEventCount;
    int m_cDeltaEventCount;
    int m_cCompletedEventCount;

    IManipulationProcessor* m_pManip;

    IConnectionPointContainer* m_pConPointContainer;
    IConnectionPoint* m_pConnPoint;
    
    HWND m_hWnd;
};     
```

在指定標頭的情況下，您必須建立事件介面的執行，讓您的類別執行您想要操作處理器執行的動作。 下列程式碼是一種範本，可針對 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)介面執行事件接收的最小功能。

```C++
#include "stdafx.h"
#include "cmanipulationeventsink.h"

CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    m_pManip = manip;
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = manip->QueryInterface(
      IID_IConnectionPointContainer, 
          (LPVOID*) &spConnectionContainer
        );
    //hr = manip->QueryInterface(&spConnectionContainer);
    if (spConnectionContainer == NULL){
        // something went wrong, try to gracefully quit
        
    }

    //Get a connection point.
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnPoint);
    if (m_pConnPoint == NULL){
        // something went wrong, try to gracefully quit
    }

    DWORD dwCookie;

    //Advise.
    hr = m_pConnPoint->Advise(this, &dwCookie);
}

int CManipulationEventSink::GetStartedEventCount()
{
    return m_cStartedEventCount;
}

int CManipulationEventSink::GetDeltaEventCount()
{
    return m_cDeltaEventCount;
}

int CManipulationEventSink::GetCompletedEventCount()
{
    return m_cCompletedEventCount;
}

double CManipulationEventSink::GetX()
{
    return m_fX;
}

double CManipulationEventSink::GetY()
{
    return m_fY;
}

CManipulationEventSink::~CManipulationEventSink()
{
    //Cleanup.
}

///////////////////////////////////
//Implement IManipulationEvents
///////////////////////////////////

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;
    
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT translationDeltaX,
    /* [in] */ FLOAT translationDeltaY,
    /* [in] */ FLOAT scaleDelta,
    /* [in] */ FLOAT expansionDelta,
    /* [in] */ FLOAT rotationDelta,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cDeltaEventCount ++;
    
    RECT rect;
        
    GetWindowRect(m_hWnd, &rect);
    
    int oldWidth =  rect.right-rect.left;
    int oldHeight = rect.bottom-rect.top;            

    // scale and translate the window size / position    
    MoveWindow(m_hWnd,                                                     // the window to move
               static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
               static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
               static_cast<int>(oldWidth * scaleDelta),                    // width
               static_cast<int>(oldHeight * scaleDelta),                   // height
               TRUE);                                                      // redraw
                     
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cCompletedEventCount ++;

    m_fX = x;
    m_fY = y;

    // place your code handler here to do any operations based on the manipulation   

    return S_OK;
}


/////////////////////////////////
//Implement IUnknown
/////////////////////////////////

ULONG CManipulationEventSink::AddRef(void) 
{
    return ++m_cRefCount;
}

ULONG CManipulationEventSink::Release(void)
{ 
    m_cRefCount --;

    if(0 == m_cRefCount) {
        delete this;
        return 0;
    }

    return m_cRefCount;
}

HRESULT CManipulationEventSink::QueryInterface(REFIID riid, LPVOID *ppvObj) 
{
    if (IID__IManipulationEvents == riid) {
        *ppvObj = (_IManipulationEvents *)(this); AddRef(); return S_OK;
    } else if (IID_IUnknown == riid) {
        *ppvObj = (IUnknown *)(this); AddRef(); return S_OK;
    } else {
        return E_NOINTERFACE;
    }
}         
```

請特別注意類別中的 [**system.windows.uielement.manipulationstarted>**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted)、 [**system.windows.uielement.manipulationdelta>**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)和 [**system.windows.uielement.manipulationcompleted>**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) 方法的執行方式。 這些是介面中最有可能的方法，將會要求您根據事件中傳遞的操作資訊來執行作業。 另請注意，函式中的第二個參數是事件操作中所使用的物件。 在用來產生範例的程式碼中，會將應用程式的 hWnd 傳送至函式，使其可以重新置放和調整大小。

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a>建立 IManipulationProcessor 介面的實例

在您將使用操作的程式碼中，您必須建立 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 介面的實例。 首先，您必須加入操作類別的支援。 下列程式碼示範如何在您的類別中執行這項作業。

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

當您有操作處理器的變數，而且已包含操作的標頭之後，您必須建立 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 介面的實例。 這是 COM 物件。 因此，您必須呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)，然後為 **IManipulationProcessor** 的參考建立實例。 下列程式碼會示範如何建立這個介面的實例。

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a>建立事件接收器的實例，並設定觸控事件

在您的程式碼中包含事件接收器類別的定義，然後加入操作事件接收器類別的變數。 下列程式碼範例包含類別實作為的標頭，並設定用來儲存事件接收器的全域變數。

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

當您擁有變數並已包含新事件接收器類別的定義之後，就可以使用您在上一個步驟中設定的操作處理器來建立類別。 下列程式碼顯示如何從 **OnInitDialog** 建立此類別的實例。

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> 您建立事件接收器實例的方式，取決於您使用運算元據進行的工作。 在大多數情況下，您將會建立一個操作處理器事件接收，其與此範例的函式不同。

### <a name="send-touch-event-data-to-the-manipulation-processor"></a>傳送觸控事件資料至操作處理器

既然您已設定操作處理器和事件接收器，您必須將觸控資料摘要到操作處理器，以觸發操作事件。

> [!Note]  
> 這是[與 Windows Touch 訊息開始使用](getting-started-with-multi-touch-messages.md)中所討論的相同程式。

首先，您將建立一些程式碼來解碼 [**WM \_ 觸控**](wm-touchdown.md) 訊息，並將它們傳送至 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 介面以引發事件。 下列程式碼顯示從 **WndProc** 方法呼叫的範例執行，並傳回訊息的 **LRESULT** 。

```C++
LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam )
{
  UINT cInputs = LOWORD(wParam);
  PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
  
  BOOL bHandled = FALSE;
  
  if (NULL != pInputs) {
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
      cInputs,
      pInputs,
      sizeof(TOUCHINPUT))) {      
      for (UINT i=0; i<cInputs; i++){
        if (pInputs[i].dwFlags & TOUCHEVENTF_DOWN){
            g_pIManipProc->ProcessDown(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_UP){
            g_pIManipProc->ProcessUp(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_MOVE){
            g_pIManipProc->ProcessMove(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
      }      
    } else {
      // GetLastError() and error handling
    }
    delete [] pInputs;
  } else {
    // error handling, presumably out of memory
  }
  if (bHandled){
    // if you don't want to pass to DefWindowProc, close the touch input handle
    if (!CloseTouchInputHandle((HTOUCHINPUT)lParam)) {
        // error handling
    }
    return 0;
  }else{
    return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
  }
}
```

現在您已有可解碼 [**wm \_ 觸控**](wm-touchdown.md)訊息的公用程式方法，您必須從 **WndProc** 方法將 **wm \_ 觸控** 訊息傳遞至公用程式函式。 下列程式碼顯示如何執行這項作業。

```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_TOUCH:
        return OnTouch(hWnd, wParam, lParam);
    case WM_PAINT:
        hdc = BeginPaint(hWnd, &ps);
        // TODO: Add any drawing code here...
        EndPaint(hWnd, &ps);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```

您已在事件接收器中執行的自訂方法現在應該可以運作。 在此範例中，觸及視窗將會移動它。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[操作](getting-started-with-manipulations.md)
</dt> </dl>


 