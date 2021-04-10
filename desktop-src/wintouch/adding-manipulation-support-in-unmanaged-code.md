---
title: 在非受控碼中新增操作支援
description: 本節說明如何藉由執行 IManipulationEvents 介面的事件接收，來將操作支援新增至非受控程式碼 \_ 。
ms.assetid: 7d8c6230-eaca-43c7-ad2f-651851b69d7f
keywords:
- Windows Touch，操作
- Windows Touch，_IManipulationEvents 介面
- Windows Touch，IManipulationProcessor 介面
- 操作，在非受控碼中新增支援
- 操作，非受控碼支援
- 操作，支援非受控碼
- 操作，_IManipulationEvents 介面
- 操作，IManipulationProcessor 介面
- _IManipulationEvents 介面，在非受控碼中操作支援
- IManipulationProcessor 介面，在非受控碼中操作支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2e000b6d3518c4e90eb5ae03b581e81037edf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093028"
---
# <a name="adding-manipulation-support-in-unmanaged-code"></a><span data-ttu-id="7e50b-113">在非受控碼中新增操作支援</span><span class="sxs-lookup"><span data-stu-id="7e50b-113">Adding Manipulation Support in Unmanaged Code</span></span>

<span data-ttu-id="7e50b-114">本節說明如何藉由執行 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)介面的事件接收，來將操作支援新增至非受控程式碼。</span><span class="sxs-lookup"><span data-stu-id="7e50b-114">This section explains how to add manipulation support to unmanaged code by implementing an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>

<span data-ttu-id="7e50b-115">下圖概述操作架構。</span><span class="sxs-lookup"><span data-stu-id="7e50b-115">The following image outlines the manipulation architecture.</span></span>

![顯示傳遞給物件操作處理器的 windows 觸控訊息的圖例，該物件會使用 imanipulationevents 介面來處理事件。 \-](images/manipulation-arch.png)

<span data-ttu-id="7e50b-117">從 [**WM \_ 觸控**](wm-touchdown.md) 訊息接收的觸控資料會連同觸控訊息中的連絡人識別碼一起傳遞給 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 。</span><span class="sxs-lookup"><span data-stu-id="7e50b-117">Touch data that is received from [**WM\_TOUCH**](wm-touchdown.md) messages is passed to the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) together with the contact ID from the touch message.</span></span> <span data-ttu-id="7e50b-118">根據訊息序列， **IManipulationProcessor** 介面將會計算要執行的轉換類型，以及與此轉換相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="7e50b-118">Based on the message sequence, the **IManipulationProcessor** interface will calculate what kind of transformation is being performed and what the values associated with this transformation are.</span></span> <span data-ttu-id="7e50b-119">然後， **IManipulationProcessor** 會產生由事件接收器處理的 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) 。</span><span class="sxs-lookup"><span data-stu-id="7e50b-119">The **IManipulationProcessor** will then generate [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) which are handled by an event sink.</span></span> <span data-ttu-id="7e50b-120">然後，事件接收器可以使用這些值，在要轉換的物件上執行自訂作業。</span><span class="sxs-lookup"><span data-stu-id="7e50b-120">The event sink can then use these values to perform custom operations on the object being transformed.</span></span>

<span data-ttu-id="7e50b-121">若要將操作支援新增至您的應用程式，您必須遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="7e50b-121">To add manipulation support to your application, you must follow these steps:</span></span>

1.  <span data-ttu-id="7e50b-122">執行 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)介面的事件接收。</span><span class="sxs-lookup"><span data-stu-id="7e50b-122">Implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>
2.  <span data-ttu-id="7e50b-123">建立 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="7e50b-123">Create an instance of an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>
3.  <span data-ttu-id="7e50b-124">建立事件接收器的實例，並設定觸控事件。</span><span class="sxs-lookup"><span data-stu-id="7e50b-124">Create an instance of your event sink and set up touch events.</span></span>
4.  <span data-ttu-id="7e50b-125">將觸控事件資料傳送給操作處理器。</span><span class="sxs-lookup"><span data-stu-id="7e50b-125">Send touch event data to the manipulation processor.</span></span>

<span data-ttu-id="7e50b-126">本節說明將操作支援新增至應用程式時必須遵循的步驟。</span><span class="sxs-lookup"><span data-stu-id="7e50b-126">This section explains the steps that you must follow to add manipulation support to your application.</span></span> <span data-ttu-id="7e50b-127">系統會在每個步驟提供程式碼，讓您開始使用。</span><span class="sxs-lookup"><span data-stu-id="7e50b-127">Code is provided at each step to get you started.</span></span>

> [!Note]  
> <span data-ttu-id="7e50b-128">您無法同時使用操作和筆勢，因為筆勢和觸控訊息是互斥的。</span><span class="sxs-lookup"><span data-stu-id="7e50b-128">You cannot use manipulations and gestures at the same time because gesture and touch messages are mutually exclusive.</span></span>

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a><span data-ttu-id="7e50b-129">執行 IManipualtionEvents 介面的事件接收 \_</span><span class="sxs-lookup"><span data-stu-id="7e50b-129">Implement an Event Sink for \_IManipualtionEvents Interface</span></span>

<span data-ttu-id="7e50b-130">建立事件接收器的實例之前，您必須先建立一個類別來執行事件的 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)介面。</span><span class="sxs-lookup"><span data-stu-id="7e50b-130">Before you can create an instance of your event sink, you must create a class that implements the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface for eventing.</span></span> <span data-ttu-id="7e50b-131">這是您的事件接收器。</span><span class="sxs-lookup"><span data-stu-id="7e50b-131">This is your event sink.</span></span> <span data-ttu-id="7e50b-132">[**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)介面所產生的事件是由事件接收器處理。</span><span class="sxs-lookup"><span data-stu-id="7e50b-132">Events generated by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface are handled by your event sink.</span></span> <span data-ttu-id="7e50b-133">下列程式碼顯示繼承 **\_ IManipulationEvents** 介面之類別的範例標頭。</span><span class="sxs-lookup"><span data-stu-id="7e50b-133">The following code shows an example header for a class that inherits the **\_IManipulationEvents** interface.</span></span>

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

<span data-ttu-id="7e50b-134">在指定標頭的情況下，您必須建立事件介面的執行，讓您的類別執行您想要操作處理器執行的動作。</span><span class="sxs-lookup"><span data-stu-id="7e50b-134">Given the header, you must create an implementation of the events interface so that your class performs the actions that you want the manipulation processor to perform.</span></span> <span data-ttu-id="7e50b-135">下列程式碼是一種範本，可針對 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)介面執行事件接收的最小功能。</span><span class="sxs-lookup"><span data-stu-id="7e50b-135">The following code is a template that implements the minimum functionality of an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>

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

<span data-ttu-id="7e50b-136">請特別注意類別中的 [**system.windows.uielement.manipulationstarted>**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted)、 [**system.windows.uielement.manipulationdelta>**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)和 [**system.windows.uielement.manipulationcompleted>**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) 方法的執行方式。</span><span class="sxs-lookup"><span data-stu-id="7e50b-136">Pay extra attention to implementations of [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta), and [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) methods in the class.</span></span> <span data-ttu-id="7e50b-137">這些是介面中最有可能的方法，將會要求您根據事件中傳遞的操作資訊來執行作業。</span><span class="sxs-lookup"><span data-stu-id="7e50b-137">These are the most likely methods in the interface that will require you to perform operations based on the manipulation information that is passed around in the event.</span></span> <span data-ttu-id="7e50b-138">另請注意，函式中的第二個參數是事件操作中所使用的物件。</span><span class="sxs-lookup"><span data-stu-id="7e50b-138">Note also that the second parameter in the constructor is the object that is used in the event manipulations.</span></span> <span data-ttu-id="7e50b-139">在用來產生範例的程式碼中，會將應用程式的 hWnd 傳送至函式，使其可以重新置放和調整大小。</span><span class="sxs-lookup"><span data-stu-id="7e50b-139">In the code used for producing the sample, the hWnd for the application is sent to the constructor so that it can be repositioned and resized.</span></span>

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a><span data-ttu-id="7e50b-140">建立 IManipulationProcessor 介面的實例</span><span class="sxs-lookup"><span data-stu-id="7e50b-140">Create an instance of an IManipulationProcessor Interface</span></span>

<span data-ttu-id="7e50b-141">在您將使用操作的程式碼中，您必須建立 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="7e50b-141">In the code where you will use manipulations, you must create an instance of an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span> <span data-ttu-id="7e50b-142">首先，您必須加入操作類別的支援。</span><span class="sxs-lookup"><span data-stu-id="7e50b-142">First you must add support for the manipulations class.</span></span> <span data-ttu-id="7e50b-143">下列程式碼示範如何在您的類別中執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="7e50b-143">The following code shows how you can do this in your class.</span></span>

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

<span data-ttu-id="7e50b-144">當您有操作處理器的變數，而且已包含操作的標頭之後，您必須建立 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="7e50b-144">After you have your variable for the manipulation processor and you have included the headers for manipulations, you have to create an instance of the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span> <span data-ttu-id="7e50b-145">這是 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="7e50b-145">This is a COM object.</span></span> <span data-ttu-id="7e50b-146">因此，您必須呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)，然後為 **IManipulationProcessor** 的參考建立實例。</span><span class="sxs-lookup"><span data-stu-id="7e50b-146">Therefore, you must call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), and then create an instance of your reference to the **IManipulationProcessor**.</span></span> <span data-ttu-id="7e50b-147">下列程式碼會示範如何建立這個介面的實例。</span><span class="sxs-lookup"><span data-stu-id="7e50b-147">The following code shows how you can create an instance of this interface.</span></span>

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a><span data-ttu-id="7e50b-148">建立事件接收器的實例，並設定觸控事件</span><span class="sxs-lookup"><span data-stu-id="7e50b-148">Create an instance of your Event Sink and set up Touch Events</span></span>

<span data-ttu-id="7e50b-149">在您的程式碼中包含事件接收器類別的定義，然後加入操作事件接收器類別的變數。</span><span class="sxs-lookup"><span data-stu-id="7e50b-149">Include the definition for your event sink class to your code and then add a variable for the manipulation event sink class.</span></span> <span data-ttu-id="7e50b-150">下列程式碼範例包含類別實作為的標頭，並設定用來儲存事件接收器的全域變數。</span><span class="sxs-lookup"><span data-stu-id="7e50b-150">The following code example includes the header for the class implementation and sets up a global variable to store the event sink.</span></span>

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

<span data-ttu-id="7e50b-151">當您擁有變數並已包含新事件接收器類別的定義之後，就可以使用您在上一個步驟中設定的操作處理器來建立類別。</span><span class="sxs-lookup"><span data-stu-id="7e50b-151">After you have the variable and have included your definition for the new event sink class, you can construct the class by using the manipulation processor that you have set up in the previous step.</span></span> <span data-ttu-id="7e50b-152">下列程式碼顯示如何從 **OnInitDialog** 建立此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="7e50b-152">The following code shows how an instance of this class would be created from **OnInitDialog**.</span></span>

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> <span data-ttu-id="7e50b-153">您建立事件接收器實例的方式，取決於您使用運算元據進行的工作。</span><span class="sxs-lookup"><span data-stu-id="7e50b-153">The way that you create an instance of your event sink depends on what you are doing with the manipulation data.</span></span> <span data-ttu-id="7e50b-154">在大多數情況下，您將會建立一個操作處理器事件接收，其與此範例的函式不同。</span><span class="sxs-lookup"><span data-stu-id="7e50b-154">In most cases, you will create a manipulation processor event sink that does not have the same constructor as this example.</span></span>

### <a name="send-touch-event-data-to-the-manipulation-processor"></a><span data-ttu-id="7e50b-155">傳送觸控事件資料至操作處理器</span><span class="sxs-lookup"><span data-stu-id="7e50b-155">Send Touch Event Data to the Manipulation Processor</span></span>

<span data-ttu-id="7e50b-156">既然您已設定操作處理器和事件接收器，您必須將觸控資料摘要到操作處理器，以觸發操作事件。</span><span class="sxs-lookup"><span data-stu-id="7e50b-156">Now that you have your manipulation processor and event sink set up, you must feed touch data to the manipulation processor to trigger manipulation events.</span></span>

> [!Note]  
> <span data-ttu-id="7e50b-157">這是 [與 Windows Touch 訊息開始使用](getting-started-with-multi-touch-messages.md)中所討論的相同程式。</span><span class="sxs-lookup"><span data-stu-id="7e50b-157">This is the same procedure as discussed in [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md).</span></span>

<span data-ttu-id="7e50b-158">首先，您將建立一些程式碼來解碼 [**WM \_ 觸控**](wm-touchdown.md) 訊息，並將它們傳送至 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 介面以引發事件。</span><span class="sxs-lookup"><span data-stu-id="7e50b-158">First, you will create some code to decode the [**WM\_TOUCH**](wm-touchdown.md) messages and send them to the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface to raise events.</span></span> <span data-ttu-id="7e50b-159">下列程式碼顯示從 **WndProc** 方法呼叫的範例執行，並傳回訊息的 **LRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="7e50b-159">The following code shows an example implementation that is called from the **WndProc** method and return an **LRESULT** for messaging.</span></span>

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

<span data-ttu-id="7e50b-160">現在您已有可解碼 [**wm \_ 觸控**](wm-touchdown.md)訊息的公用程式方法，您必須從 **WndProc** 方法將 **wm \_ 觸控** 訊息傳遞至公用程式函式。</span><span class="sxs-lookup"><span data-stu-id="7e50b-160">Now that you have a utility method for decoding the [**WM\_TOUCH**](wm-touchdown.md) message, you must pass the **WM\_TOUCH** messages to the utility function from your **WndProc** method.</span></span> <span data-ttu-id="7e50b-161">下列程式碼顯示如何執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="7e50b-161">The following code shows how you can do this.</span></span>

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

<span data-ttu-id="7e50b-162">您已在事件接收器中執行的自訂方法現在應該可以運作。</span><span class="sxs-lookup"><span data-stu-id="7e50b-162">The custom methods that you have implemented in your event sink should now work.</span></span> <span data-ttu-id="7e50b-163">在此範例中，觸及視窗將會移動它。</span><span class="sxs-lookup"><span data-stu-id="7e50b-163">In this example, touching the window will move it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e50b-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e50b-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e50b-165">操作</span><span class="sxs-lookup"><span data-stu-id="7e50b-165">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>


 