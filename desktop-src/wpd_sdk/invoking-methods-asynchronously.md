---
description: 以非同步方式叫用服務方法
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: 以非同步方式叫用服務方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef4f0eb2e75b977b53300bed6eab4c909fa7796
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423848"
---
# <a name="invoking-service-methods-asynchronously"></a><span data-ttu-id="e073b-103">以非同步方式叫用服務方法</span><span class="sxs-lookup"><span data-stu-id="e073b-103">Invoking Service Methods Asynchronously</span></span>

<span data-ttu-id="e073b-104">WpdServiceApiSample 應用程式包含的程式碼會示範應用程式如何以非同步方式叫用服務方法。</span><span class="sxs-lookup"><span data-stu-id="e073b-104">The WpdServiceApiSample application includes code that demonstrates how an application can invoke the service methods asynchronously.</span></span> <span data-ttu-id="e073b-105">此範例會使用下列介面。</span><span class="sxs-lookup"><span data-stu-id="e073b-105">This sample uses the following interfaces.</span></span>



| <span data-ttu-id="e073b-106">介面</span><span class="sxs-lookup"><span data-stu-id="e073b-106">Interface</span></span>    | <span data-ttu-id="e073b-107">描述</span><span class="sxs-lookup"><span data-stu-id="e073b-107">Description</span></span>          |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e073b-108">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="e073b-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | <span data-ttu-id="e073b-109">用來取出 **IPortableDeviceServiceMethods** 介面，以便在指定的服務上叫用方法。</span><span class="sxs-lookup"><span data-stu-id="e073b-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="e073b-110">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="e073b-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | <span data-ttu-id="e073b-111">用來叫用服務方法。</span><span class="sxs-lookup"><span data-stu-id="e073b-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="e073b-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e073b-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                                  | <span data-ttu-id="e073b-113">用來保存外寄方法參數和傳入方法的結果。</span><span class="sxs-lookup"><span data-stu-id="e073b-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="e073b-114">如果方法不需要任何參數或傳回任何結果，這可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="e073b-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |
| [<span data-ttu-id="e073b-115">**IPortableDeviceServiceMethodCallback**</span><span class="sxs-lookup"><span data-stu-id="e073b-115">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | <span data-ttu-id="e073b-116">當方法完成時，由應用程式所執行以接收方法的結果。</span><span class="sxs-lookup"><span data-stu-id="e073b-116">Implemented by the application to receive the method results when a method has completed.</span></span>                                                                               |



 

<span data-ttu-id="e073b-117">當使用者在命令列選擇選項 "10" 時，應用程式會叫用在 ServiceMethods .cpp 模組中找到的 **InvokeMethodsAsync** 方法。</span><span class="sxs-lookup"><span data-stu-id="e073b-117">When the user chooses option "10" at the command line, the application invokes the **InvokeMethodsAsync** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="e073b-118">請注意，在叫用方法之前，範例應用程式會在連線的裝置上開啟連絡人服務。</span><span class="sxs-lookup"><span data-stu-id="e073b-118">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="e073b-119">服務方法會封裝每個服務定義和實行的功能。</span><span class="sxs-lookup"><span data-stu-id="e073b-119">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="e073b-120">它們對每種服務類型都是唯一的，並以 GUID 表示。</span><span class="sxs-lookup"><span data-stu-id="e073b-120">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="e073b-121">例如，連絡人服務會定義 **BeginSync** 方法，讓應用程式呼叫以準備裝置來同步處理連絡人物件，並使用 **EndSync** 方法來通知裝置同步處理已完成。</span><span class="sxs-lookup"><span data-stu-id="e073b-121">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="e073b-122">應用程式會藉由呼叫 [**IPortableDeviceServiceMethods：： Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)來執行可攜式裝置服務方法。</span><span class="sxs-lookup"><span data-stu-id="e073b-122">Applications execute a portable device service method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="e073b-123">服務方法不應與 WPD 命令混淆。</span><span class="sxs-lookup"><span data-stu-id="e073b-123">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="e073b-124">WPD 命令是標準 WPD 設備磁碟機介面 (DDI) 的一部分，而且是 WPD 應用程式與驅動程式之間的通訊機制。</span><span class="sxs-lookup"><span data-stu-id="e073b-124">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="e073b-125">命令是預先定義的，依類別目錄分組 (例如， **WPD \_ CATEGORY \_ COMMON**) ，並且以 **PROPERTYKEY** 結構表示。</span><span class="sxs-lookup"><span data-stu-id="e073b-125">Commands are predefined, grouped by categories (for example, **WPD\_CATEGORY\_COMMON**), and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="e073b-126">應用程式會藉由呼叫 [**IPortableDeviceService：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)，將命令傳送至設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="e073b-126">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="e073b-127">如需詳細資訊，請參閱命令主題。</span><span class="sxs-lookup"><span data-stu-id="e073b-127">For more information, see the Commands topic.</span></span>

<span data-ttu-id="e073b-128">**InvokeMethodsAsync** 方法會叫用 [**IPortableDeviceService：：方法**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities)來取出 [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)介面。</span><span class="sxs-lookup"><span data-stu-id="e073b-128">The **InvokeMethodsAsync** method invokes [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="e073b-129">使用這個介面時，它會叫用 **InvokeMethodAsync** helper 函數兩次;針對 **BeginSync** 方法，一次用於 **EndSync** 方法。</span><span class="sxs-lookup"><span data-stu-id="e073b-129">Using this interface, it invokes the **InvokeMethodAsync** helper function twice; once for the **BeginSync** method and once for the **EndSync** method.</span></span> <span data-ttu-id="e073b-130">在此範例中， **InvokeMethodAsync** 會在呼叫 [**IPortableDeviceServiceMethodCallback：： OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) 時無限期等候全域事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="e073b-130">In this example, , **InvokeMethodAsync** waits indefinitely for a global event to be signaled when [**IPortableDeviceServiceMethodCallback::OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) is called.</span></span>

<span data-ttu-id="e073b-131">下列程式碼會使用 **InvokeMethodsAsync** 方法。</span><span class="sxs-lookup"><span data-stu-id="e073b-131">The following code uses the **InvokeMethodsAsync** method.</span></span>


```C++
// Invoke methods on the Contacts Service asynchornously.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethodsAsync(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke the BeginSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_BeginSync);

        // This method does not take any parameters, so we pass in NULL
        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_BeginSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_EndSync);

        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_EndSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
    }
}
```



<span data-ttu-id="e073b-132">**InvokeMethodAsync** helper 函式會針對它所叫用的每個方法，執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e073b-132">The **InvokeMethodAsync** helper function does the following for each method that it invokes:</span></span>

-   <span data-ttu-id="e073b-133">建立監視的全域事件控制碼，以判斷方法是否完成。</span><span class="sxs-lookup"><span data-stu-id="e073b-133">Creates a global event handle that it monitors to determine method completion.</span></span>
-   <span data-ttu-id="e073b-134">建立 **CMethodCallback** 物件，該物件會提供做為 [**IPortableDeviceServiceMethods： InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync)的引數。</span><span class="sxs-lookup"><span data-stu-id="e073b-134">Creates a **CMethodCallback** object that is supplied as an argument to [**IPortableDeviceServiceMethods:InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span></span>
-   <span data-ttu-id="e073b-135">呼叫 **IPortableDeviceServiceMethods：： InvokeAsync** 方法以叫用指定的方法。</span><span class="sxs-lookup"><span data-stu-id="e073b-135">Calls the **IPortableDeviceServiceMethods::InvokeAsync** method to invoke the given method.</span></span>
-   <span data-ttu-id="e073b-136">監視全域事件控制碼是否完成。</span><span class="sxs-lookup"><span data-stu-id="e073b-136">Monitors the global event handle for completion.</span></span>
-   <span data-ttu-id="e073b-137">執行清除。</span><span class="sxs-lookup"><span data-stu-id="e073b-137">Performs cleanup.</span></span>

<span data-ttu-id="e073b-138">**CMethodCallback** 類別會示範應用程式如何執行 [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)。</span><span class="sxs-lookup"><span data-stu-id="e073b-138">The **CMethodCallback** class demonstrates how an application can implement [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span></span> <span data-ttu-id="e073b-139">此類別中的 **OnComplete** 執行會通知事件，告知應用程式服務方法已完成。</span><span class="sxs-lookup"><span data-stu-id="e073b-139">The implementation of **OnComplete** in this class signals an event to notify the application that the service method has completed.</span></span> <span data-ttu-id="e073b-140">除了 **OnComplete** 方法之外，此類別還會執行 **AddRef**、 **QueryInterface** 和 **Release**，用來維護物件的參考計數和它所執行的介面。</span><span class="sxs-lookup"><span data-stu-id="e073b-140">In addition to the **OnComplete** method, this class implements **AddRef**, **QueryInterface**, and **Release**, which are used to maintain the object's reference count and the interfaces that it implements.</span></span>


```C++
class CMethodCallback : public IPortableDeviceServiceMethodCallback
{
public:
   CMethodCallback () : m_cRef(1)
   {
   }

   ~CMethodCallback ()
   {
   }

public:
    // IPortableDeviceServiceMethodCallback::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE OnComplete(
        HRESULT                 hrStatus,
        IPortableDeviceValues*  /*pResults*/) // We are ignoring results as our methods will not return any results
    {
        printf("** Method completed, status HRESULT = 0x%lx **\n", hrStatus);

        if (g_hMethodCompleteEvent != NULL)
        {
            SetEvent(g_hMethodCompleteEvent);
        }          
        return S_OK;
    }

    // IUnknown::AddRef
    virtual ULONG STDMETHODCALLTYPE AddRef(void)
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    // IUnknown::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceServiceMethodCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            *ppvObj = NULL;
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    // IUnknown::Release
    virtual ULONG STDMETHODCALLTYPE Release(void)
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

private:
    DWORD   m_cRef;
};
```



## <a name="related-topics"></a><span data-ttu-id="e073b-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="e073b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e073b-142">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="e073b-142">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="e073b-143">**IPortableDeviceServiceMethodCallback**</span><span class="sxs-lookup"><span data-stu-id="e073b-143">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[<span data-ttu-id="e073b-144">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="e073b-144">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="e073b-145">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="e073b-145">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
