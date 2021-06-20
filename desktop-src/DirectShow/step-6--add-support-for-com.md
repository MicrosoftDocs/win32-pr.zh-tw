---
description: 在寫入轉換篩選時，加入對 COM 的支援。 這是本教學課程中的最後一個步驟。
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: 步驟 6. 新增對 COM 的支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097d51fa440812311edde9ce448916c66721a507
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406771"
---
# <a name="step-6-add-support-for-com"></a><span data-ttu-id="24174-105">步驟 6.</span><span class="sxs-lookup"><span data-stu-id="24174-105">Step 6.</span></span> <span data-ttu-id="24174-106">新增對 COM 的支援</span><span class="sxs-lookup"><span data-stu-id="24174-106">Add Support for COM</span></span>

<span data-ttu-id="24174-107">這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟6。</span><span class="sxs-lookup"><span data-stu-id="24174-107">This is step 6 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="24174-108">最後一個步驟是新增對 COM 的支援。</span><span class="sxs-lookup"><span data-stu-id="24174-108">The final step is to add support for COM.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="24174-109">參考計數</span><span class="sxs-lookup"><span data-stu-id="24174-109">Reference Counting</span></span>

<span data-ttu-id="24174-110">您不需要執行 [**IUnknown：： AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 或 [**Iunknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。</span><span class="sxs-lookup"><span data-stu-id="24174-110">You do not have to implement [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) or [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="24174-111">所有的篩選和釘選類別都是衍生自 [**CUnknown**](cunknown.md)，它會處理參考計數。</span><span class="sxs-lookup"><span data-stu-id="24174-111">All of the filter and pin classes derive from [**CUnknown**](cunknown.md), which handles reference counting.</span></span>

## <a name="queryinterface"></a><span data-ttu-id="24174-112">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="24174-112">QueryInterface</span></span>

<span data-ttu-id="24174-113">所有的篩選和釘選類別都會針對它們所繼承的任何 COM 介面，執行 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="24174-113">All of the filter and pin classes implement [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for any COM interfaces they inherit.</span></span> <span data-ttu-id="24174-114">例如， [**CTransformFilter**](ctransformfilter.md)會透過 [**CBaseFilter**](cbasefilter.md)) 繼承 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (。</span><span class="sxs-lookup"><span data-stu-id="24174-114">For example, [**CTransformFilter**](ctransformfilter.md) inherits [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (through [**CBaseFilter**](cbasefilter.md)).</span></span> <span data-ttu-id="24174-115">如果您的篩選不會公開任何額外的介面，則不需要執行任何其他動作。</span><span class="sxs-lookup"><span data-stu-id="24174-115">If your filter does not expose any additional interfaces, you do not have to do anything else.</span></span>

<span data-ttu-id="24174-116">若要公開其他介面，請覆寫 [**CUnknown：： NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="24174-116">To expose additional interfaces, override the [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method.</span></span> <span data-ttu-id="24174-117">例如，假設您的篩選器會執行名為 IMyCustomInterface 的自訂介面。</span><span class="sxs-lookup"><span data-stu-id="24174-117">For example, suppose your filter implements a custom interface named IMyCustomInterface.</span></span> <span data-ttu-id="24174-118">若要將此介面公開給用戶端，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="24174-118">To expose this interface to clients, do the following:</span></span>

-   <span data-ttu-id="24174-119">從該介面衍生您的篩選類別。</span><span class="sxs-lookup"><span data-stu-id="24174-119">Derive your filter class from that interface.</span></span>
-   <span data-ttu-id="24174-120">將 [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) 宏放在公用宣告區段中。</span><span class="sxs-lookup"><span data-stu-id="24174-120">Put the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section.</span></span>
-   <span data-ttu-id="24174-121">覆寫 [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) 以檢查介面的 IID，並將指標傳回至篩選準則。</span><span class="sxs-lookup"><span data-stu-id="24174-121">Override [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IID of your interface and return a pointer to your filter.</span></span>

<span data-ttu-id="24174-122">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="24174-122">The following code shows these steps:</span></span>


```C++
CMyFilter : public CBaseFilter, public IMyCustomInterface
{
public:
    DECLARE_IUNKNOWN
    STDMETHODIMP NonDelegatingQueryInterface(REFIID iid, void **ppv);
};
STDMETHODIMP CMyFilter::NonDelegatingQueryInterface(REFIID iid, void **ppv)
{
    if (riid == IID_IMyCustomInterface) {
        return GetInterface(static_cast<IMyCustomInterface*>(this), ppv);
    }
    return CBaseFilter::NonDelegatingQueryInterface(riid,ppv);
}
```



<span data-ttu-id="24174-123">如需詳細資訊，請參閱 [如何執行 IUnknown](how-to-implement-iunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="24174-123">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="object-creation"></a><span data-ttu-id="24174-124">建立物件</span><span class="sxs-lookup"><span data-stu-id="24174-124">Object Creation</span></span>

<span data-ttu-id="24174-125">如果您打算將篩選封裝到 DLL 中，並將它提供給其他用戶端使用，您必須支援 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 和其他相關的 COM 函數。</span><span class="sxs-lookup"><span data-stu-id="24174-125">If you plan to package your filter in a DLL and make it available to other clients, you must support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and other related COM functions.</span></span> <span data-ttu-id="24174-126">基類庫會執行大部分的，您只需要提供一些關於篩選的資訊。</span><span class="sxs-lookup"><span data-stu-id="24174-126">The base class library implements most of this; you just need to provide some information about your filter.</span></span> <span data-ttu-id="24174-127">本節將簡短介紹該怎麼做。</span><span class="sxs-lookup"><span data-stu-id="24174-127">This section gives a brief overview of what to do.</span></span> <span data-ttu-id="24174-128">如需詳細資訊，請參閱 [如何建立 DirectShow 篩選 DLL](how-to-create-a-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="24174-128">For details, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="24174-129">首先，撰寫會傳回新的篩選準則實例的靜態類別方法。</span><span class="sxs-lookup"><span data-stu-id="24174-129">First, write a static class method that returns a new instance of your filter.</span></span> <span data-ttu-id="24174-130">您可以將此方法命名為任何您喜歡的名稱，但簽章必須符合下列範例中所示的內容：</span><span class="sxs-lookup"><span data-stu-id="24174-130">You can name this method anything you like, but the signature must match the one shown in the following example:</span></span>


```C++
CUnknown * WINAPI CRleFilter::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr)
{
    CRleFilter *pFilter = new CRleFilter();
    if (pFilter== NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pFilter;
}
```



<span data-ttu-id="24174-131">接下來，宣告名為 *g \_ Templates* 的 [**CFactoryTemplate**](cfactorytemplate.md)類別實例的全域陣列。</span><span class="sxs-lookup"><span data-stu-id="24174-131">Next, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) class instances, named *g\_Templates*.</span></span> <span data-ttu-id="24174-132">每個 **CFactoryTemplate** 類別都包含一個篩選準則的登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="24174-132">Each **CFactoryTemplate** class contains registry information for one filter.</span></span> <span data-ttu-id="24174-133">有幾個篩選可以位於單一 DLL 中;只包含其他 **CFactoryTemplate** 專案。</span><span class="sxs-lookup"><span data-stu-id="24174-133">Several filters can reside in a single DLL; simply include additional **CFactoryTemplate** entries.</span></span> <span data-ttu-id="24174-134">您也可以宣告其他 COM 物件，例如屬性頁。</span><span class="sxs-lookup"><span data-stu-id="24174-134">You can also declare other COM objects, such as property pages.</span></span>


```C++
static WCHAR g_wszName[] = L"My RLE Encoder";
CFactoryTemplate g_Templates[] = 
{
  { 
    g_wszName,
    &CLSID_RLEFilter,
    CRleFilter::CreateInstance,
    NULL,
    NULL
  }
};
```



<span data-ttu-id="24174-135">定義名為 *g \_ cTemplates* 的全域整數，其值等於 *g \_ 範本* 陣列的長度：</span><span class="sxs-lookup"><span data-stu-id="24174-135">Define a global integer named *g\_cTemplates* whose value equals the length of the *g\_Templates* array:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



<span data-ttu-id="24174-136">最後，請執行 DLL 註冊函式。</span><span class="sxs-lookup"><span data-stu-id="24174-136">Finally, implement the DLL registration functions.</span></span> <span data-ttu-id="24174-137">下列範例會顯示這些函式的最基本執行：</span><span class="sxs-lookup"><span data-stu-id="24174-137">The following example shows the minimal implementation for these functions:</span></span>


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}
STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



## <a name="filter-registry-entries"></a><span data-ttu-id="24174-138">篩選登錄專案</span><span class="sxs-lookup"><span data-stu-id="24174-138">Filter Registry Entries</span></span>

<span data-ttu-id="24174-139">先前的範例示範如何註冊 COM 的篩選器 CLSID。</span><span class="sxs-lookup"><span data-stu-id="24174-139">The previous examples show how to register a filter's CLSID for COM.</span></span> <span data-ttu-id="24174-140">針對許多篩選準則，這就夠了。</span><span class="sxs-lookup"><span data-stu-id="24174-140">For many filters, this is sufficient.</span></span> <span data-ttu-id="24174-141">接著，用戶端應該使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 建立篩選，並藉由呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter)將它新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="24174-141">The client is then expected to create the filter using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and add it to the filter graph by calling [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span></span> <span data-ttu-id="24174-142">不過，在某些情況下，您可能會想要在登錄中提供篩選的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="24174-142">In some cases, however, you might want to provide additional information about the filter in the registry.</span></span> <span data-ttu-id="24174-143">這項資訊會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="24174-143">This information does the following:</span></span>

-   <span data-ttu-id="24174-144">可讓用戶端使用 [篩選器](filter-mapper.md) 對應程式或 [系統裝置列舉](system-device-enumerator.md)值來探索篩選。</span><span class="sxs-lookup"><span data-stu-id="24174-144">Enables clients to discover the filter using the [Filter Mapper](filter-mapper.md) or the [System Device Enumerator](system-device-enumerator.md).</span></span>
-   <span data-ttu-id="24174-145">讓篩選圖形管理員在自動圖形建立期間探索篩選。</span><span class="sxs-lookup"><span data-stu-id="24174-145">Enables the Filter Graph Manager to discover the filter during automatic graph building.</span></span>

<span data-ttu-id="24174-146">下列範例會在影片壓縮程式類別目錄中註冊 RLE 編碼器篩選器。</span><span class="sxs-lookup"><span data-stu-id="24174-146">The following example registers the RLE encoder filter in the video compressor category.</span></span> <span data-ttu-id="24174-147">如需詳細資訊，請參閱 [如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="24174-147">For details, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="24174-148">請務必閱讀註冊篩選準則的章節 [指導方針](guidelines-for-registering-filters.md)，其中描述了篩選註冊的建議作法。</span><span class="sxs-lookup"><span data-stu-id="24174-148">Be sure to read the section [Guidelines for Registering Filters](guidelines-for-registering-filters.md), which describes the recommended practices for filter registration.</span></span>


```C++
// Declare media type information.
FOURCCMap fccMap = FCC('MRLE'); 
REGPINTYPES sudInputTypes = { &MEDIATYPE_Video, &GUID_NULL };
REGPINTYPES sudOutputTypes = { &MEDIATYPE_Video, (GUID*)&fccMap };

// Declare pin information.
REGFILTERPINS sudPinReg[] = {
    // Input pin.
    { 0, FALSE, // Rendered?
         FALSE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudInputTypes  // Media types.
    },
    // Output pin.
    { 0, FALSE, // Rendered?
         TRUE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudOutputTypes      // Media types.
    }
};
 
// Declare filter information.
REGFILTER2 rf2FilterReg = {
    1,                // Version number.
    MERIT_DO_NOT_USE, // Merit.
    2,                // Number of pins.
    sudPinReg         // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->RegisterFilter(
            CLSID_RLEFilter,                // Filter CLSID. 
            g_wszName,                       // Filter name.
            NULL,                            // Device moniker. 
            &CLSID_VideoCompressorCategory,  // Video compressor category.
            g_wszName,                       // Instance data.
            &rf2FilterReg                    // Filter information.
            );
        pFM2->Release();
    }
    return hr;
}

STDAPI DllUnregisterServer()
{
    HRESULT hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_RLEFilter);
        pFM2->Release();
    }
    return hr;
}
```



<span data-ttu-id="24174-149">此外，篩選不需要封裝在 Dll 內。</span><span class="sxs-lookup"><span data-stu-id="24174-149">Also, filters do not have to be packaged inside DLLs.</span></span> <span data-ttu-id="24174-150">在某些情況下，您可能會撰寫僅針對特定應用程式所設計的特殊篩選。</span><span class="sxs-lookup"><span data-stu-id="24174-150">In some cases, you might write a specialized filter that is designed only for a specific application.</span></span> <span data-ttu-id="24174-151">在這種情況下，您可以直接在應用程式中編譯篩選類別，並使用運算子來建立它 `new` ，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="24174-151">In that case, you can compile the filter class directly in your application, and create it with the `new` operator, as shown in the following example:</span></span>


```C++
#include "MyFilter.h"  // Header file that declares the filter class.
// Compile and link MyFilter.cpp.
int main()
{
    IBaseFilter *pFilter = 0;
    {
        // Scope to hide pF.
        CMyFilter* pF = new MyFilter();
        if (!pF)
        {
            printf("Could not create MyFilter.\n");
            return 1;
        }
        pF->QueryInterface(IID_IBaseFilter, 
            reinterpret_cast<void**>(&pFilter));
    }
    
    /* Now use pFilter as normal. */
    
    pFilter->Release();  // Deletes the filter.
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="24174-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="24174-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24174-153">智慧型連接</span><span class="sxs-lookup"><span data-stu-id="24174-153">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="24174-154">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="24174-154">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="24174-155">寫入轉換篩選</span><span class="sxs-lookup"><span data-stu-id="24174-155">Writing Transform Filters</span></span>](writing-transform-filters.md)
</dt> </dl>

 

 
