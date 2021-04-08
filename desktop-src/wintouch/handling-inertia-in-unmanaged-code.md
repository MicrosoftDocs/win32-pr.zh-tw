---
title: 處理非受控碼中的慣性
description: 本節說明如何使用 IInertiaProcessor 介面處理非受控碼中的慣性。
ms.assetid: 3261b461-add2-4e92-9a51-b2d46630fb4f
keywords:
- Windows Touch，慣性
- Windows Touch，操作處理器
- 慣性，非受控碼
- 慣性、IInertiaProcessor 介面
- 慣性、操作處理器
- 操作處理器，慣性
- IInertiaProcessor 介面，非受控碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de56d06547f426de252a89ef5172df3fe4ca439
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020931"
---
# <a name="handling-inertia-in-unmanaged-code"></a>處理非受控碼中的慣性

本節說明如何使用 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) 介面處理非受控碼中的慣性。

## <a name="overview"></a>概觀

若要在非受控碼中使用慣性，您必須針對操作處理器和慣性處理器來執行事件接收器。 首先，將操作支援新增至您的應用程式，如將 [操作支援加入至非受控碼](adding-manipulation-support-in-unmanaged-code.md)一節中所述。 請注意，操作支援要求您使用觸控訊息而非手勢訊息，將事件資料送入操作處理器。 操作完成後，您也必須針對 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) 介面所產生的事件，執行第二個事件接收，或需要修改您現有的事件接收，以容納 **IInertiaProcessor** 和 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 介面所產生的事件。 基於此範例的目的，從針對將操作支援新增至非受控碼的區段建立的事件接收，以及新增第二個可搭配慣性處理器（而不是操作處理器）的函式，都比較容易。 如此一來，事件接收的實作為操作處理器或慣性處理器的功能。 除了新增第二個函式，事件接收器還會有一個變數，指出它是否會根據慣性輸入執行作業，而不是操作輸入。

### <a name="add-inertia-support-to-a-manipulation-processor-event-sink"></a>將慣性支援新增至操作處理器事件接收器

下列程式碼顯示新的事件接收函式、 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) 介面的新成員變數，以及指出接收器是否針對慣性推斷的旗標。


```C++
    CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd);
    CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd);
```




```C++
    IInertiaProcessor*      m_pInert;
    BOOL fExtrapolating; 
```



當您的類別標頭具有新的函式，以及指出您是否推斷的旗標之後，您可以執行事件接收，以針對 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 事件和 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) 事件具有個別的處理區塊。 接受 **IManipulationProcessor** 和 **IInertiaProcessor** 的函式應該將 **fExtrapolating** 旗標設為 False，這表示這是 **IManipulationProcessor** 事件處理常式。 下列程式碼顯示如何執行使用 **IManipulationProcessor** 之事件接收器的函式。


```C++
CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=FALSE;

    m_pManip = pManip;
    
    m_pInert = pInert;
    
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pManip->QueryInterface(
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
```



下列程式碼顯示如何執行使用 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) 之事件接收器的函式。 這個函式會將 **fExtrapolating** 旗標設為 true，表示事件接收器類別的這個實例將會執行外推，並且會執行先前由操作處理器事件執行的任何移動作業。


```C++
CManipulationEventSink::CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    m_pInert = pInert;
    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=TRUE;

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pInert->QueryInterface(
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
```



> [!Note]  
> 系統會將來自操作處理器事件接收的事件接收類別實作為慣性處理器的事件接收器重複使用。

 

現在，當您將這個類別 **CManipulationEventSink** 時，可以將它視為操作處理器的事件接收器，或是作為慣性處理器的事件接收器。 當它被視為慣性處理器事件接收器時，會將 **fExtrapolating** 旗標設為 true，表示應該推斷操作事件。

> [!Note]  
> [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)和 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)介面都會引發 [**system.windows.uielement.manipulationstarted>**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted) 。

 

當操作開始時，會設定 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) 介面屬性。 下列程式碼顯示如何處理已啟動的事件。


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;       

    // set origins in manipulation processor
    m_pInert->put_InitialOriginX(x);
    m_pInert->put_InitialOriginY(y);
    
    RECT screenRect;

    HWND desktop = GetDesktopWindow();
    GetClientRect(desktop, &screenRect);

    // physics settings
    // deceleration is units per square millisecond
    m_pInert->put_DesiredDeceleration(.1f);

    // set the boundaries        
    screenRect.left-= 1024;
    m_pInert->put_BoundaryLeft  ( static_cast<float>(screenRect.left   * 100));
    m_pInert->put_BoundaryTop   ( static_cast<float>(screenRect.top    * 100));
    m_pInert->put_BoundaryRight ( static_cast<float>(screenRect.right  * 100));
    m_pInert->put_BoundaryBottom( static_cast<float>(screenRect.bottom * 100));
    
    
    // Elastic boundaries - I set these to 90% of the screen 
    // so... 5% at left, 95% right, 5% top,  95% bottom
    // Values are whole numbers because units are in centipixels
    m_pInert->put_ElasticMarginLeft  (static_cast<float>(screenRect.left   * 5));
    m_pInert->put_ElasticMarginTop   (static_cast<float>(screenRect.top    * 5));
    m_pInert->put_ElasticMarginRight (static_cast<float>(screenRect.right  * 95));
    m_pInert->put_ElasticMarginBottom(static_cast<float>(screenRect.bottom * 95));
    
    
    return S_OK;
}
```



在此範例中，會使用操作差異來四處移動視窗。 下列程式碼顯示差異事件的處理方式。


```C++
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
    MoveWindow(m_hWnd,                                              // the window to move
        static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
        static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
        static_cast<int>(oldWidth * scaleDelta),                    // width
        static_cast<int>(oldHeight * scaleDelta),                   // height
        TRUE);                                                      // redraw
                     
    return S_OK;
}
```



在此範例中，操作已完成的事件會啟動或停止將在 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)介面上呼叫 [**進程**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)的計時器。 下列程式碼顯示如何處理已完成的操作事件。


```C++
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
    
    if (fExtrapolating){
        //Inertia Complete, stop the timer used for processing      
        KillTimer(m_hWnd,0);        
    }else{ 
        // setup velocities for inertia processor
        float vX = 0.0f;
        float vY = 0.0f;
        float vA = 0.0f;
        m_pManip->GetVelocityX(&vX);
        m_pManip->GetVelocityY(&vY);
        m_pManip->GetAngularVelocity(&vA);

        // complete any previous processing
        m_pInert->Complete();
        
        // Reset sets the  initial timestamp
        m_pInert->Reset();
                
        // 
        m_pInert->put_InitialVelocityX(vX);
        m_pInert->put_InitialVelocityY(vY);        
        
        m_pInert->put_InitialOriginX(x);
        m_pInert->put_InitialOriginY(y);
        
           
        // Start a timer
        SetTimer(m_hWnd,0, 50, 0);        
    }

    return S_OK;
}
```



下列程式碼示範如何在 **WndProc** 中解讀 **WM \_ 計時器** 訊息，以在 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)介面上執行 [**處理**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)呼叫。


```C++
case WM_TIMER:       
  if (g_pIInertProc){
    BOOL b;       
    g_pIInertProc->Process(&b);        
  }
  break;
```



### <a name="coinitialize-the-inertia-processor-and-manipulation-processor-and-initialize-the-event-sinks"></a>CoInitialize 慣性處理器和操作處理器，並初始化事件接收器

當您修改事件接收以同時支援 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 和 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)之後，您就可以初始化事件接收，並將其設定為從您的應用程式執行。 下列程式碼顯示如何配置介面指標。


```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;
IInertiaProcessor*      g_pIInertProc;
```



下列程式碼範例會示範如何具現化您的介面。


```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
   
   hr = CoCreateInstance(CLSID_InertiaProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIInertProc)
   );
```



下列程式碼範例示範如何在指定介面指標的情況下，建立事件接收器，並註冊觸控輸入的視窗。


```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, g_pIInertProc, hWnd);
   g_pManipulationEventSink = new CManipulationEventSink(g_pIInertProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[慣性](getting-started-with-inertia.md)
</dt> </dl>

 

 




