---
description: 此程式示範如何建立只使用 c + + 來捕捉 InkCollector 事件的應用程式。 此程式會共同建立 InkCollector 物件，以啟用視窗的筆墨。 每當收到筆劃事件時，它就會顯示訊息方塊。
ms.assetid: 91450559-ae47-457a-a709-b4e4e78bde22
title: C + + 事件接收器範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e950254293b676088d8b281624c089b098e5dca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967066"
---
# <a name="c-event-sinks-sample"></a><span data-ttu-id="f9d5b-105">C + + 事件接收器範例</span><span class="sxs-lookup"><span data-stu-id="f9d5b-105">C++ Event Sinks Sample</span></span>

<span data-ttu-id="f9d5b-106">此程式示範如何建立只使用 c + + 來捕捉 InkCollector 事件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-106">This program demonstrates how you can build an application that captures InkCollector events using only C++.</span></span> <span data-ttu-id="f9d5b-107">此程式會共同建立 [**InkCollector**](inkcollector-class.md) 物件，以啟用視窗的筆墨。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-107">This program co-creates an [**InkCollector**](inkcollector-class.md) object to ink -enable the window.</span></span> <span data-ttu-id="f9d5b-108">每當收到 [**筆劃**](inkcollector-stroke.md) 事件時，它就會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-108">It displays a message box whenever a [**Stroke**](inkcollector-stroke.md) event is received.</span></span>

## <a name="defining-a-wrapper-for-ink-collector-events"></a><span data-ttu-id="f9d5b-109">定義筆跡收集器事件的包裝函式</span><span class="sxs-lookup"><span data-stu-id="f9d5b-109">Defining a Wrapper for Ink Collector Events</span></span>

<span data-ttu-id="f9d5b-110">類別會處理將筆墨收集器 `InkCollectorEvents` 事件從筆墨收集器傳遞給這個類別的使用者。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-110">The `InkCollectorEvents` Class handles passing ink collector events from the ink collector to the user of this class.</span></span> <span data-ttu-id="f9d5b-111">`AdviseInkCollector`方法會設定 [**InkCollector**](inkcollector-class.md)物件與這個類別之間的連接。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-111">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="f9d5b-112">`Invoke`方法會將 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)事件通知轉換為虛擬函式的呼叫，此函式的使用者可以覆寫此類別的使用者來處理特定事件。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-112">The `Invoke` method converts the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) event notification into a call to a virtual function that the user of this class can override to process a particular event.</span></span>

> [!Note]  
> <span data-ttu-id="f9d5b-113">您必須覆寫虛擬函式，事件處理常式才能取得該事件。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-113">You must do more than override the virtual function for an event handler to get that event.</span></span> <span data-ttu-id="f9d5b-114">針對所有的預設事件，您必須呼叫筆墨收集器的 [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) 方法，以保證取得事件。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-114">For all but default events, you have to call the ink collector's [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) method to guarantee getting an event.</span></span> <span data-ttu-id="f9d5b-115">其次，這個物件封送處理本身的自由執行緒，讓所有已執行的事件處理常式也都必須是無限制執行緒。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-115">Secondly, this object marshals itself free threaded so all implemented event handlers need to be free threaded as well.</span></span> <span data-ttu-id="f9d5b-116">特別重要的是，使用 Windows Api 可能會導致切換至另一個執行緒，因為事件處理常式不保證會在與筆墨收集器連接之視窗的相同執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-116">Of particular importance is using Windows APIs, which may cause a switch to another thread as the event handler is not guaranteed to be running on the same thread as the window connected with the ink collector.</span></span>

 


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



<span data-ttu-id="f9d5b-117">`Init`方法會呼叫[CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)來設定自由執行緒封送處理器。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-117">The `Init` method calls [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) to set up a free threaded marshaler.</span></span>


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



<span data-ttu-id="f9d5b-118">`AdviseInkCollector`方法會設定 [**InkCollector**](inkcollector-class.md)物件與這個類別之間的連接。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-118">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="f9d5b-119">它會先抓取筆墨收集器的連接點。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-119">It first retrieves a connection point to the ink collector.</span></span> <span data-ttu-id="f9d5b-120">然後，它會抓取的指標， `IInkCollectorEvents` 讓它可以建立控制項的諮詢連接。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-120">Then it retrieves a pointer to the `IInkCollectorEvents` so that it may establish an advisory connection to the control.</span></span>


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



<span data-ttu-id="f9d5b-121">`UnadviseInkCollector`方法會釋放物件對控制項的連接。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-121">The `UnadviseInkCollector` method releases the connections the object has to the control.</span></span>


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a><span data-ttu-id="f9d5b-122">定義筆墨收集器事件處理常式</span><span class="sxs-lookup"><span data-stu-id="f9d5b-122">Defining an Ink Collector Events Handler</span></span>

<span data-ttu-id="f9d5b-123">CMyInkEvents 類別會覆寫 InkCollectorEvents 類別之 [**Stroke**](inkcollector-stroke.md) 事件處理常式的預設行為。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-123">The CMyInkEvents Class overrides the default behavior of the [**Stroke**](inkcollector-stroke.md) event handler of the InkCollectorEvents Class.</span></span> <span data-ttu-id="f9d5b-124">當 [**InkCollector**](inkcollector-class.md) 收到 **筆劃** 事件時，筆觸方法會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-124">The Stroke method displays a message box when the [**InkCollector**](inkcollector-class.md) receives a **Stroke** event.</span></span>


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



## <a name="defining-an-ink-collector-wrapper"></a><span data-ttu-id="f9d5b-125">定義筆墨收集器包裝函式</span><span class="sxs-lookup"><span data-stu-id="f9d5b-125">Defining an Ink Collector Wrapper</span></span>

<span data-ttu-id="f9d5b-126">CMyInkCollector 類別的 Init 方法會宣告並初始化 CMyInkEvents 物件。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-126">The CMyInkCollector Class's Init method declares and initializes a CMyInkEvents object.</span></span> <span data-ttu-id="f9d5b-127">然後，它會建立 [**InkCollector**](inkcollector-class.md) 物件，並將筆墨收集器和事件處理常式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-127">It then creates an [**InkCollector**](inkcollector-class.md) object and associates the ink collector and the event handler.</span></span> <span data-ttu-id="f9d5b-128">最後， **InkCollector** 會附加至視窗並啟用。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-128">Finally, the **InkCollector** is attached to the window and enabled.</span></span>


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



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a><span data-ttu-id="f9d5b-129">存取 Tablet PC 介面和包裝函式類別</span><span class="sxs-lookup"><span data-stu-id="f9d5b-129">Accessing the Tablet PC Interfaces and the Wrapper Classes</span></span>

<span data-ttu-id="f9d5b-130">首先，請加入 Tablet PC 自動化介面的標頭。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-130">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="f9d5b-131">這些會隨 Microsoft <entity type="reg"/> Windows <entity type="reg"/> XP Tablet PC Edition 開發工具組1.7 一起安裝。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-131">These are installed with the Microsoft<entity type="reg"/> Windows<entity type="reg"/> XP Tablet PC Edition Development Kit 1.7.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="f9d5b-132">然後，加入包裝函式類別的標頭，並定義 [**InkCollector**](inkcollector-class.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-132">Then, include the headers for the wrapper classes and [**InkCollector**](inkcollector-class.md) event handler was defined.</span></span>


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a><span data-ttu-id="f9d5b-133">呼叫包裝函式類別</span><span class="sxs-lookup"><span data-stu-id="f9d5b-133">Calling the Wrapper Classes</span></span>

<span data-ttu-id="f9d5b-134">建立視窗時，視窗程式會建立筆墨收集器包裝函式，並將包裝函式初始化。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-134">When the window is created, the Window procedure creates an ink collector wrapper and initializes the wrapper.</span></span> <span data-ttu-id="f9d5b-135">當視窗損毀時，視窗程式會刪除筆墨收集器包裝函式。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-135">When the window is destroyed, the Window procedure deletes the ink collector wrapper.</span></span> <span data-ttu-id="f9d5b-136">筆墨收集器包裝函式會處理其相關事件處理常式的建立和刪除。</span><span class="sxs-lookup"><span data-stu-id="f9d5b-136">The ink collector wrapper handles the creation and deletion of its associated event handler.</span></span>


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



 

 
