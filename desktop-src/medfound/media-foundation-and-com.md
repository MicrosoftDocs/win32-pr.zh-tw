---
description: Microsoft 媒體基礎使用混合的 COM 結構，但不是以 COM 為基礎的完整 API。
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: 媒體基礎和 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb7d05bac6a3f4deef2c004c6980ef1351c3823
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106975602"
---
# <a name="media-foundation-and-com"></a><span data-ttu-id="ff36b-103">媒體基礎和 COM</span><span class="sxs-lookup"><span data-stu-id="ff36b-103">Media Foundation and COM</span></span>

<span data-ttu-id="ff36b-104">Microsoft 媒體基礎使用混合的 COM 結構，但不是以 COM 為基礎的完整 API。</span><span class="sxs-lookup"><span data-stu-id="ff36b-104">Microsoft Media Foundation uses a mix of COM constructs, but is not a fully COM-based API.</span></span> <span data-ttu-id="ff36b-105">本主題說明 COM 與媒體基礎之間的互動。</span><span class="sxs-lookup"><span data-stu-id="ff36b-105">This topic describes the interaction between COM and Media Foundation.</span></span> <span data-ttu-id="ff36b-106">它也會定義開發媒體基礎外掛程式元件的一些最佳作法。</span><span class="sxs-lookup"><span data-stu-id="ff36b-106">It also defines some best practices for developing Media Foundation plug-in components.</span></span> <span data-ttu-id="ff36b-107">遵循這些做法可協助您避免一些常見但微妙的程式設計錯誤。</span><span class="sxs-lookup"><span data-stu-id="ff36b-107">Following these practices can help you to avoid some common but subtle programming errors.</span></span>

-   [<span data-ttu-id="ff36b-108">應用程式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="ff36b-108">Best Practices for Applications</span></span>](#best-practices-for-applications)
-   [<span data-ttu-id="ff36b-109">媒體基礎元件的最佳作法</span><span class="sxs-lookup"><span data-stu-id="ff36b-109">Best Practices for Media Foundation Components</span></span>](#best-practices-for-media-foundation-components)
-   [<span data-ttu-id="ff36b-110">總結</span><span class="sxs-lookup"><span data-stu-id="ff36b-110">Summary</span></span>](#summary)
-   [<span data-ttu-id="ff36b-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff36b-111">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-applications"></a><span data-ttu-id="ff36b-112">應用程式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="ff36b-112">Best Practices for Applications</span></span>

<span data-ttu-id="ff36b-113">在媒體基礎中， [工作佇列](work-queues.md)會處理非同步處理和回呼。</span><span class="sxs-lookup"><span data-stu-id="ff36b-113">In Media Foundation, asynchronous processing and callbacks are handled by [work queues](work-queues.md).</span></span> <span data-ttu-id="ff36b-114">工作佇列一律會有多執行緒的單元 (MTA) 執行緒，因此，如果應用程式也在 MTA 執行緒上執行，則會有更簡單的執行。</span><span class="sxs-lookup"><span data-stu-id="ff36b-114">Work queues always have multithreaded apartment (MTA) threads, so an application will have a simpler implementation if it runs on an MTA thread as well.</span></span> <span data-ttu-id="ff36b-115">因此，建議使用 **COINIT \_ 多執行緒** 旗標來呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 。</span><span class="sxs-lookup"><span data-stu-id="ff36b-115">Therefore, it is recommended to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="ff36b-116">媒體基礎不會將單一執行緒的單元 (STA) 物件封送處理至工作佇列執行緒。</span><span class="sxs-lookup"><span data-stu-id="ff36b-116">Media Foundation does not marshal single-threaded apartment (STA) objects to work queue threads.</span></span> <span data-ttu-id="ff36b-117">也不會確保不會維護 STA 變異。</span><span class="sxs-lookup"><span data-stu-id="ff36b-117">Nor does it ensure that STA invariants are maintained.</span></span> <span data-ttu-id="ff36b-118">因此，STA 應用程式必須小心不要將 STA 物件或 proxy 傳遞給媒體基礎 Api。</span><span class="sxs-lookup"><span data-stu-id="ff36b-118">Therefore, an STA application must be careful to not pass STA objects or proxies to Media Foundation APIs.</span></span> <span data-ttu-id="ff36b-119">媒體基礎中不支援僅限 STA 的物件。</span><span class="sxs-lookup"><span data-stu-id="ff36b-119">Objects that are STA-only are not supported in Media Foundation.</span></span>

<span data-ttu-id="ff36b-120">如果您有 MTA 或無限制執行緒物件的 STA proxy，則可以使用工作佇列回呼將物件封送處理至 MTA proxy。</span><span class="sxs-lookup"><span data-stu-id="ff36b-120">If you have an STA proxy to an MTA or free-threaded object, the object can be marshaled to an MTA proxy by using a work-queue callback.</span></span> <span data-ttu-id="ff36b-121">[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)函數可以傳回原始指標或 STA proxy，視該 CLSID 的登錄中定義的物件模型而定。</span><span class="sxs-lookup"><span data-stu-id="ff36b-121">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function can return either a raw pointer or an STA proxy, depending on the object model defined in the registry for that CLSID.</span></span> <span data-ttu-id="ff36b-122">如果傳回 STA proxy，您就不能將指標傳遞至媒體基礎 API。</span><span class="sxs-lookup"><span data-stu-id="ff36b-122">If an STA proxy is returned, you must not pass the pointer to a Media Foundation API.</span></span>

<span data-ttu-id="ff36b-123">例如，假設您想要將 **IPropertyStore** 指標傳遞至 [**IMFSourceResolver：： BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) 方法。</span><span class="sxs-lookup"><span data-stu-id="ff36b-123">For example, suppose that you want to pass an **IPropertyStore** pointer to the [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method.</span></span> <span data-ttu-id="ff36b-124">您可以呼叫 **PSCreateMemoryPropertyStore** 來建立 **IPropertyStore** 指標。</span><span class="sxs-lookup"><span data-stu-id="ff36b-124">You might call **PSCreateMemoryPropertyStore** to create the **IPropertyStore** pointer.</span></span> <span data-ttu-id="ff36b-125">如果您是從 STA 呼叫，則必須先封送處理指標，再將它傳遞給 **BeginCreateObjectFromURL**。</span><span class="sxs-lookup"><span data-stu-id="ff36b-125">If you are calling from an STA, you must marshal the pointer before passing it to **BeginCreateObjectFromURL**.</span></span>

<span data-ttu-id="ff36b-126">下列程式碼說明如何將 STA proxy 封送處理至媒體基礎 API。</span><span class="sxs-lookup"><span data-stu-id="ff36b-126">The following code shows how to marshal an STA proxy to a Media Foundation API.</span></span>


```C++
class CCreateSourceMarshalCallback
    : public IMFAsyncCallback
{
public:
    CCreateSourceMarshalCallback(
        LPCWSTR szURL, 
        IMFSourceResolver* pResolver, 
        IPropertyStore* pSourceProps, 
        IMFAsyncCallback* pCompletionCallback, 
        HRESULT& hr
        )
        : m_szURL(szURL), 
          m_pResolver(pResolver), 
          m_pCompletionCallback(pCompletionCallback),
          m_pGIT(NULL),
          m_cRef(1)
    {
        hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable, NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGIT));

        if(SUCCEEDED(hr))
        {
            hr = m_pGIT->RegisterInterfaceInGlobal(
                pSourceProps, IID_IPropertyStore, &m_dwInterfaceCookie);
        }
    }
    ~CCreateSourceMarshalCallback()
    {
        SafeRelease(&m_pResolver);
        SafeRelease(&m_pCompletionCallback);
        SafeRelease(&m_pGIT);
    }


    STDMETHOD_(ULONG, AddRef)()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHOD_(ULONG, Release)()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (0 == cRef)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHOD(QueryInterface)(REFIID riid, LPVOID* ppvObject)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCreateSourceMarshalCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppvObject);

    }

    STDMETHOD(GetParameters)(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHOD(Invoke)(IMFAsyncResult* pResult)
    {
        IPropertyStore *pSourceProps = NULL;

        HRESULT hr = m_pGIT->GetInterfaceFromGlobal(
            m_dwInterfaceCookie, 
            IID_PPV_ARGS(&pSourceProps)
            );

        if(SUCCEEDED(hr))
        {
            hr = m_pResolver->BeginCreateObjectFromURL(
                m_szURL, MF_RESOLUTION_MEDIASOURCE, pSourceProps, NULL, 
                m_pCompletionCallback, NULL);
        }

        SafeRelease(&pSourceProps);
        return hr;
    }

private:
    LPCWSTR m_szURL;
    IMFSourceResolver *m_pResolver;
    IMFAsyncCallback *m_pCompletionCallback;
    IGlobalInterfaceTable *m_pGIT;
    DWORD m_dwInterfaceCookie;
    LONG m_cRef;
};
```



<span data-ttu-id="ff36b-127">如需全域介面表的詳細資訊，請參閱 [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable)。</span><span class="sxs-lookup"><span data-stu-id="ff36b-127">For more information about the global interface table, see [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="ff36b-128">如果您使用媒體基礎同進程，從媒體基礎方法和函式傳回的物件就是物件的直接指標。</span><span class="sxs-lookup"><span data-stu-id="ff36b-128">If you are using Media Foundation in-process, objects returned from Media Foundation methods and functions are direct pointers to the object.</span></span> <span data-ttu-id="ff36b-129">若為跨進程媒體基礎，這些物件可能是 MTA proxy，如果需要，則應該封送處理至 STA 執行緒。</span><span class="sxs-lookup"><span data-stu-id="ff36b-129">For cross-process Media Foundation, these objects may be MTA proxies, and should be marshaled into an STA thread if needed there.</span></span> <span data-ttu-id="ff36b-130">同樣地，在回呼中取得的物件（例如，來自 [MESessionTopologyStatus](mesessiontopologystatus.md) 事件的拓撲）是在同進程中使用媒體基礎時的直接指標，而當使用媒體基礎的跨進程時，則是 MTA proxy。</span><span class="sxs-lookup"><span data-stu-id="ff36b-130">Similarly, objects obtained inside a callback — for example, a topology from the [MESessionTopologyStatus](mesessiontopologystatus.md) event — are direct pointers when Media Foundation is used in-process, but are MTA proxies when Media Foundation is used cross-process.</span></span>

> [!Note]  
> <span data-ttu-id="ff36b-131">使用媒體基礎跨進程的最常見案例是使用 [受保護的媒體路徑](protected-media-path.md) (PMP) 。</span><span class="sxs-lookup"><span data-stu-id="ff36b-131">The most common scenario for using Media Foundation cross-process is with the [Protected Media Path](protected-media-path.md) (PMP).</span></span> <span data-ttu-id="ff36b-132">不過，這些備註適用于透過 RPC 使用媒體基礎 Api 時的任何情況。</span><span class="sxs-lookup"><span data-stu-id="ff36b-132">However, these remarks apply to any situation when Media Foundation APIs are used through RPC.</span></span>

 

<span data-ttu-id="ff36b-133">[**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)的所有實施都應與 MTA 相容。</span><span class="sxs-lookup"><span data-stu-id="ff36b-133">All implementations of [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) should be MTA-compatible.</span></span> <span data-ttu-id="ff36b-134">這些物件完全不需要是 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="ff36b-134">These objects do not need to be COM objects at all.</span></span> <span data-ttu-id="ff36b-135">但如果是，則無法在 STA 中執行。</span><span class="sxs-lookup"><span data-stu-id="ff36b-135">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="ff36b-136">[**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)函式將會在 MTA workqueue 執行緒上叫用，而提供的 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)物件將會是直接物件指標或 MTA proxy。</span><span class="sxs-lookup"><span data-stu-id="ff36b-136">The [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) function will be invoked on an MTA workqueue thread, and the provided [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) object will be either a direct object pointer or an MTA proxy.</span></span>

## <a name="best-practices-for-media-foundation-components"></a><span data-ttu-id="ff36b-137">媒體基礎元件的最佳作法</span><span class="sxs-lookup"><span data-stu-id="ff36b-137">Best Practices for Media Foundation Components</span></span>

<span data-ttu-id="ff36b-138">有兩個類別的媒體基礎物件需要考慮 COM。</span><span class="sxs-lookup"><span data-stu-id="ff36b-138">There are two categories of Media Foundation objects that need to be concerned about COM.</span></span> <span data-ttu-id="ff36b-139">某些元件（例如轉換或位元組資料流程處理常式）是 CLSID 所建立的完整 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="ff36b-139">Some components, such as transforms or byte stream handlers, are full COM objects created by CLSID.</span></span> <span data-ttu-id="ff36b-140">這些物件必須遵循 COM 單元的規則，同時適用于同進程和跨進程的媒體基礎。</span><span class="sxs-lookup"><span data-stu-id="ff36b-140">These objects must follow the rules for COM apartments, for both in-process and cross-process Media Foundation.</span></span> <span data-ttu-id="ff36b-141">其他媒體基礎元件並非完整的 COM 物件，但需要 COM proxy 才能進行跨進程播放。</span><span class="sxs-lookup"><span data-stu-id="ff36b-141">Other Media Foundation components are not full COM objects, but do need COM proxies for cross-process playback.</span></span> <span data-ttu-id="ff36b-142">此類別中的物件包含媒體來源和啟用物件。</span><span class="sxs-lookup"><span data-stu-id="ff36b-142">Objects in this category include media sources and activation object.</span></span> <span data-ttu-id="ff36b-143">如果這些物件只會用於同進程媒體基礎，這些物件可能會忽略這些問題。</span><span class="sxs-lookup"><span data-stu-id="ff36b-143">These objects can ignore apartment issues if they will be used only for in-process Media Foundation.</span></span>

<span data-ttu-id="ff36b-144">雖然並非所有媒體基礎物件都是 COM 物件，但所有媒體基礎介面都是衍生自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)。</span><span class="sxs-lookup"><span data-stu-id="ff36b-144">Although not all Media Foundation objects are COM objects, all Media Foundation interfaces derive from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="ff36b-145">因此，所有媒體基礎物件都必須根據 COM 規格來執行 **IUnknown** ，包括參考計數和 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))的規則。</span><span class="sxs-lookup"><span data-stu-id="ff36b-145">Therefore, all Media Foundation objects must implement **IUnknown** according to COM specifications, including the rules for reference counting and [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="ff36b-146">所有參考計數的物件也應該確保在物件仍然存在時， [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) 不會允許卸載模組。</span><span class="sxs-lookup"><span data-stu-id="ff36b-146">All reference counted objects should also ensure that [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) will not allow the module to be unloaded while the objects still persist.</span></span>

<span data-ttu-id="ff36b-147">媒體基礎的元件不能是 STA 物件。</span><span class="sxs-lookup"><span data-stu-id="ff36b-147">Media Foundation components cannot be STA objects.</span></span> <span data-ttu-id="ff36b-148">許多媒體基礎物件都不需要是 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="ff36b-148">Many Media Foundation objects do not need to be COM objects at all.</span></span> <span data-ttu-id="ff36b-149">但如果是，則無法在 STA 中執行。</span><span class="sxs-lookup"><span data-stu-id="ff36b-149">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="ff36b-150">所有媒體基礎元件都必須是安全線程。</span><span class="sxs-lookup"><span data-stu-id="ff36b-150">All Media Foundation components must be thread-safe.</span></span> <span data-ttu-id="ff36b-151">某些媒體基礎的物件也必須是無限制執行緒或非中立的。</span><span class="sxs-lookup"><span data-stu-id="ff36b-151">Some Media Foundation objects must be free-threaded or apartment-neutral as well.</span></span> <span data-ttu-id="ff36b-152">下表指定自訂介面的需求：</span><span class="sxs-lookup"><span data-stu-id="ff36b-152">The following table specifies the requirements for custom interface implementations:</span></span>



| <span data-ttu-id="ff36b-153">介面</span><span class="sxs-lookup"><span data-stu-id="ff36b-153">Interface</span></span>                                                          | <span data-ttu-id="ff36b-154">類別</span><span class="sxs-lookup"><span data-stu-id="ff36b-154">Category</span></span>            | <span data-ttu-id="ff36b-155">必要的單元</span><span class="sxs-lookup"><span data-stu-id="ff36b-155">Required apartment</span></span>       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [<span data-ttu-id="ff36b-156">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="ff36b-156">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | <span data-ttu-id="ff36b-157">跨進程 proxy</span><span class="sxs-lookup"><span data-stu-id="ff36b-157">Cross-process proxy</span></span> | <span data-ttu-id="ff36b-158">無限制執行緒或中立</span><span class="sxs-lookup"><span data-stu-id="ff36b-158">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ff36b-159">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="ff36b-159">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | <span data-ttu-id="ff36b-160">COM 物件</span><span class="sxs-lookup"><span data-stu-id="ff36b-160">COM object</span></span>          | <span data-ttu-id="ff36b-161">MTA</span><span class="sxs-lookup"><span data-stu-id="ff36b-161">MTA</span></span>                      |
| [<span data-ttu-id="ff36b-162">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="ff36b-162">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | <span data-ttu-id="ff36b-163">跨進程 proxy</span><span class="sxs-lookup"><span data-stu-id="ff36b-163">Cross-process proxy</span></span> | <span data-ttu-id="ff36b-164">無限制執行緒或中立</span><span class="sxs-lookup"><span data-stu-id="ff36b-164">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ff36b-165">**IMFQualityManager**</span><span class="sxs-lookup"><span data-stu-id="ff36b-165">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | <span data-ttu-id="ff36b-166">COM 物件</span><span class="sxs-lookup"><span data-stu-id="ff36b-166">COM object</span></span>          | <span data-ttu-id="ff36b-167">無限制執行緒或中立</span><span class="sxs-lookup"><span data-stu-id="ff36b-167">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ff36b-168">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="ff36b-168">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | <span data-ttu-id="ff36b-169">跨進程 proxy</span><span class="sxs-lookup"><span data-stu-id="ff36b-169">Cross-process proxy</span></span> | <span data-ttu-id="ff36b-170">無限制執行緒或中立</span><span class="sxs-lookup"><span data-stu-id="ff36b-170">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ff36b-171">**IMFSchemeHandler**</span><span class="sxs-lookup"><span data-stu-id="ff36b-171">**IMFSchemeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | <span data-ttu-id="ff36b-172">COM 物件</span><span class="sxs-lookup"><span data-stu-id="ff36b-172">COM object</span></span>          | <span data-ttu-id="ff36b-173">MTA</span><span class="sxs-lookup"><span data-stu-id="ff36b-173">MTA</span></span>                      |
| [<span data-ttu-id="ff36b-174">**IMFTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="ff36b-174">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | <span data-ttu-id="ff36b-175">COM 物件</span><span class="sxs-lookup"><span data-stu-id="ff36b-175">COM object</span></span>          | <span data-ttu-id="ff36b-176">無限制執行緒或中立</span><span class="sxs-lookup"><span data-stu-id="ff36b-176">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ff36b-177">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="ff36b-177">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | <span data-ttu-id="ff36b-178">COM 物件</span><span class="sxs-lookup"><span data-stu-id="ff36b-178">COM object</span></span>          | <span data-ttu-id="ff36b-179">MTA</span><span class="sxs-lookup"><span data-stu-id="ff36b-179">MTA</span></span>                      |



 

<span data-ttu-id="ff36b-180">視執行而定，可能會有其他需求。</span><span class="sxs-lookup"><span data-stu-id="ff36b-180">There may be additional requirements depending upon the implementation.</span></span> <span data-ttu-id="ff36b-181">例如，如果媒體接收器所執行的另一個介面可讓應用程式對接收器進行直接函式呼叫，則接收器必須是無限制執行緒或中性，才能處理直接的跨進程呼叫。</span><span class="sxs-lookup"><span data-stu-id="ff36b-181">For example, if a media sink implements another interface that enables the application to make direct function calls to the sink, the sink would need to be free-threaded or neutral, so that it could handle direct cross-process calls.</span></span> <span data-ttu-id="ff36b-182">任何物件都可以自由執行緒;下表指定最低需求。</span><span class="sxs-lookup"><span data-stu-id="ff36b-182">Any object may be free-threaded; this table specifies the minimum requirements.</span></span>

<span data-ttu-id="ff36b-183">執行無限制執行緒或中性物件的建議方式，是藉由匯總無限制執行緒封送處理器。</span><span class="sxs-lookup"><span data-stu-id="ff36b-183">The recommended way to implement free-threaded or neutral objects is by aggregating the free-threaded marshaler.</span></span> <span data-ttu-id="ff36b-184">如需詳細資訊，請參閱 [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)上的 MSDN 檔。</span><span class="sxs-lookup"><span data-stu-id="ff36b-184">For more details, see the MSDN documentation on [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span></span> <span data-ttu-id="ff36b-185">根據不需要將 STA 物件或 proxy 傳遞給媒體基礎 Api 的需求，無限制執行緒的物件不需要擔心在自由執行緒元件中封送處理 STA 輸入指標。</span><span class="sxs-lookup"><span data-stu-id="ff36b-185">In accordance with the requirement not to pass STA objects or proxies to Media Foundation APIs, free-threaded objects do not need to worry about marshaling STA input pointers in free-threaded components.</span></span>

<span data-ttu-id="ff36b-186">使用長期函式工作佇列 (**MFASYNC \_ 回呼 \_ 佇列 \_ 長期 \_** 函式的元件) 必須更小心。</span><span class="sxs-lookup"><span data-stu-id="ff36b-186">Components that use the long-function work queue (**MFASYNC\_CALLBACK\_QUEUE\_LONG\_FUNCTION**) must exercise more care.</span></span> <span data-ttu-id="ff36b-187">Long 函數中的執行緒 workqueue 建立自己的 STA。</span><span class="sxs-lookup"><span data-stu-id="ff36b-187">Threads in the long function workqueue create their own STA.</span></span> <span data-ttu-id="ff36b-188">使用 long 函式 workqueue 回呼的元件應避免在這些執行緒上建立 COM 物件，並視需要小心將 proxy 封送處理至 STA。</span><span class="sxs-lookup"><span data-stu-id="ff36b-188">Components that use the long function workqueue for callbacks should avoid creating COM objects on these threads, and need to be careful to marshal proxies to the STA as necessary.</span></span>

## <a name="summary"></a><span data-ttu-id="ff36b-189">總結</span><span class="sxs-lookup"><span data-stu-id="ff36b-189">Summary</span></span>

<span data-ttu-id="ff36b-190">如果應用程式與來自 MTA 執行緒的媒體基礎互動，則應用程式會有更多的時間，但是使用來自 STA 執行緒的媒體基礎可能會有一些小心。</span><span class="sxs-lookup"><span data-stu-id="ff36b-190">Applications will have an easier time if they interact with Media Foundation from an MTA thread, but it is possible with some care to use Media Foundation from an STA thread.</span></span> <span data-ttu-id="ff36b-191">媒體基礎不會處理 STA 元件，而且應用程式應該小心不要將 STA 物件傳遞給媒體基礎 Api。</span><span class="sxs-lookup"><span data-stu-id="ff36b-191">Media Foundation does not handle STA components, and applications should be careful not to pass STA objects to Media Foundation APIs.</span></span> <span data-ttu-id="ff36b-192">有些物件有額外的需求，特別是在跨進程的情況下執行的物件。</span><span class="sxs-lookup"><span data-stu-id="ff36b-192">Some objects have additional requirements, especially objects that run in a cross-process situation.</span></span> <span data-ttu-id="ff36b-193">遵循這些指導方針將有助於避免發生 COM 錯誤、鎖死和非預期的媒體處理延遲。</span><span class="sxs-lookup"><span data-stu-id="ff36b-193">Following these guidelines will help avoid COM errors, deadlocks, and unexpected delays in media processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff36b-194">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff36b-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff36b-195">媒體基礎平臺 Api</span><span class="sxs-lookup"><span data-stu-id="ff36b-195">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> <dt>

[<span data-ttu-id="ff36b-196">媒體基礎架構</span><span class="sxs-lookup"><span data-stu-id="ff36b-196">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 
