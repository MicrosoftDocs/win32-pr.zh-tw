---
description: 此程式示範如何建立只使用 c + + 來捕捉 InkCollector 事件的應用程式。 此程式會共同建立 InkCollector 物件，以啟用視窗的筆墨。 每當收到筆劃事件時，它就會顯示訊息方塊。
ms.assetid: 91450559-ae47-457a-a709-b4e4e78bde22
title: C + + 事件接收器範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b24cb718eb0d16830c285691ac5cfedf66d572f447870dc0219beb14c04548a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111128"
---
# <a name="c-event-sinks-sample"></a>C + + 事件接收器範例

此程式示範如何建立只使用 c + + 來捕捉 InkCollector 事件的應用程式。 此程式會共同建立 [**InkCollector**](inkcollector-class.md) 物件，以啟用視窗的筆墨。 每當收到 [**筆劃**](inkcollector-stroke.md) 事件時，它就會顯示訊息方塊。

## <a name="defining-a-wrapper-for-ink-collector-events"></a>定義筆跡收集器事件的包裝函式

類別會處理將筆墨收集器 `InkCollectorEvents` 事件從筆墨收集器傳遞給這個類別的使用者。 `AdviseInkCollector`方法會設定 [**InkCollector**](inkcollector-class.md)物件與這個類別之間的連接。 `Invoke`方法會將 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)事件通知轉換為虛擬函式的呼叫，此函式的使用者可以覆寫此類別的使用者來處理特定事件。

> [!Note]  
> 您必須覆寫虛擬函式，事件處理常式才能取得該事件。 針對所有的預設事件，您必須呼叫筆墨收集器的 [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) 方法，以保證取得事件。 其次，這個物件封送處理本身的自由執行緒，讓所有已執行的事件處理常式也都必須是無限制執行緒。 特別重要的是使用 Windows api，這可能會導致切換至另一個執行緒，因為事件處理常式不保證會在與筆墨收集器連接的視窗相同的執行緒上執行。

 


```C++
// Invoke translates from IDispatch to an event callout
//  that can be overriden by a subclass of this class.
STDMETHOD(Invoke)(
   DISPID dispidMember, 
    REFIID riid,
    LCID lcid, 
    WORD /*wFlags*/, 
    DISPPARAMS* pdispparams, 
    VARIANT* pvarResult,
    EXCEPINFO* /*pexcepinfo*/, 
    UINT* /*puArgErr*/)
{
    switch(dispidMember)
    {
        case DISPID_ICEStroke:
            Stroke(
                (IInkCursor*) pdispparams->rgvarg[2].pdispVal,
                (IInkStrokeDisp*) pdispparams->rgvarg[1].pdispVal,
                (VARIANT_BOOL *)pdispparams->rgvarg[0].pboolVal);
            break;
        ...
    }
    return S_OK;
}

virtual void Stroke(
    IInkCursor* Cursor,
    IInkStrokeDisp* Stroke,
    VARIANT_BOOL *Cancel)
{
    // This is a place holder designed to be overridden by
    //  user of this class.
    return;
}
...
```



`Init`方法會呼叫[CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)來設定自由執行緒封送處理器。


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



`AdviseInkCollector`方法會設定 [**InkCollector**](inkcollector-class.md)物件與這個類別之間的連接。 它會先抓取筆墨收集器的連接點。 然後，它會抓取的指標， `IInkCollectorEvents` 讓它可以建立控制項的諮詢連接。


```C++
// Set up connection between sink and InkCollector
HRESULT AdviseInkCollector(
    IInkCollector *pIInkCollector)
{
    // Get the connection point container
    IConnectionPointContainer *pIConnectionPointContainer;
    HRESULT hr = pIInkCollector->QueryInterface(IID_IConnectionPointContainer, (void **) &pIConnectionPointContainer);
        
    if (FAILED(hr))
        ...
    
    // Find the connection point for Ink Collector events
    hr = pIConnectionPointContainer->FindConnectionPoint(__uuidof(_IInkCollectorEvents), &m_pIConnectionPoint);
        
    if (SUCCEEDED(hr))
    {
        // Hook up sink to connection point
        hr = m_pIConnectionPoint->Advise(this, &m_dwCookie);
    }
    
    if (FAILED(hr))
        ...
    
    // Don't need the connection point container any more.
    pIConnectionPointContainer->Release();
    return hr;
}
```



`UnadviseInkCollector`方法會釋放物件對控制項的連接。


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a>定義筆墨收集器事件處理常式

CMyInkEvents 類別會覆寫 InkCollectorEvents 類別之 [**Stroke**](inkcollector-stroke.md) 事件處理常式的預設行為。 當 [**InkCollector**](inkcollector-class.md) 收到 **筆劃** 事件時，筆觸方法會顯示訊息方塊。


```C++
class CMyInkEvents : public InkCollectorEvents
{
public:

    // Event: Stroke
    virtual void Stroke(
        IInkCursor* Cursor,
        IInkStrokeDisp* Stroke,
        VARIANT_BOOL *Cancel)
    {
        // Demonstrate that the event notification was received.
        MessageBox(m_hWnd, "Stroke Event", "Event Received", MB_OK);
    }
    
    CMyInkEvents()
    {
        m_hWnd = NULL;
    }
    
    HRESULT Init(
        HWND hWnd)
    {
        m_hWnd = hWnd;
        return InkCollectorEvents::Init();
    }    
    
    HWND m_hWnd;
};
```



## <a name="defining-an-ink-collector-wrapper"></a>定義筆墨收集器包裝函式

CMyInkCollector 類別的 Init 方法會宣告並初始化 CMyInkEvents 物件。 然後，它會建立 [**InkCollector**](inkcollector-class.md) 物件，並將筆墨收集器和事件處理常式產生關聯。 最後， **InkCollector** 會附加至視窗並啟用。


```C++
// Handle all initializaton
HRESULT Init(
HWND hWnd)
{
    // Initialize event sink. This consists of setting
    //  up the free threaded marshaler.
    HRESULT hr = m_InkEvents.Init(hWnd);

    if (FAILED(hr))
        ...

    // Create the ink collector
    hr = CoCreateInstance(CLSID_InkCollector, NULL, CLSCTX_ALL, IID_IInkCollector, (void **) &m_pInkCollector);

    if (FAILED(hr))
        ...

    // Set up connection between Ink Collector and our event sink
    hr = m_InkEvents.AdviseInkCollector(m_pInkCollector);

    if (FAILED(hr))
        ...

    // Attach Ink Collector to window
    hr = m_pInkCollector->put_hWnd((long) hWnd);

    if (FAILED(hr))
        ...

    // Allow Ink Collector to receive input.
    return m_pInkCollector->put_Enabled(VARIANT_TRUE);
}
```



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a>存取 Tablet PC 介面和包裝函式類別

首先，請加入 Tablet PC 自動化介面的標頭。 這些都隨 Microsoft <entity type="reg"/> Windows <entity type="reg"/> XP Tablet PC Edition 開發工具組1.7 一起安裝。


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



然後，加入包裝函式類別的標頭，並定義 [**InkCollector**](inkcollector-class.md) 事件處理常式。


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a>呼叫包裝函式類別

建立視窗時，視窗程式會建立筆墨收集器包裝函式，並將包裝函式初始化。 當視窗損毀時，視窗程式會刪除筆墨收集器包裝函式。 筆墨收集器包裝函式會處理其相關事件處理常式的建立和刪除。


```C++
case WM_CREATE:

    // Allocate and initialize memory for object
    pmic = new CMyInkCollector();

    if (pmic != NULL)
    {
        // Real initialization. This consists of creating
        //  an ink collector object and attaching it to
        //  the current window. 
        if (SUCCEEDED(pmic->Init(hWnd)))
        {
            return 0;
        }
        
        // Failure free resources.
        delete pmic;
        pmic = NULL;
    }
    
    return -1;
...
case WM_DESTROY:
    // The destructor for the object handles releasing the
    //  InkCollector and disconnecting the InkCollector
    //  from the object's event sink. 
    delete pmic;
    pmic = NULL;
    PostQuitMessage(0);
    break;
```



 

 
