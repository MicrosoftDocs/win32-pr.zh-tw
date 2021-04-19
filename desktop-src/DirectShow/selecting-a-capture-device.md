---
description: 選取捕獲裝置
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: 選取捕獲裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b599728c6bd2d98b89285b6008923aa4fb2a3aef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970885"
---
# <a name="selecting-a-capture-device"></a><span data-ttu-id="01371-103">選取捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="01371-103">Selecting a Capture Device</span></span>

<span data-ttu-id="01371-104">若要選取音訊或影片捕獲裝置，請使用 [系統裝置列舉](system-device-enumerator.md)值，如 [使用系統裝置列舉](using-the-system-device-enumerator.md)值的主題所述。</span><span class="sxs-lookup"><span data-stu-id="01371-104">To select an audio or video capture device, use the [System Device Enumerator](system-device-enumerator.md), described in the topic [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="01371-105">系統裝置列舉值會傳回裝置類別目錄的集合，該集合是由裝置類別所選取。</span><span class="sxs-lookup"><span data-stu-id="01371-105">The System Device Enumerator returns a collection of device monikers, selected by device category.</span></span> <span data-ttu-id="01371-106">*標記* 是包含另一個物件相關資訊的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="01371-106">A *moniker* is a COM object that contains information about another object.</span></span> <span data-ttu-id="01371-107">標記可讓應用程式取得物件的相關資訊，而不需要實際建立物件。</span><span class="sxs-lookup"><span data-stu-id="01371-107">Monikers enable the application to get information about an object without actually creating the object.</span></span> <span data-ttu-id="01371-108">之後，應用程式可以使用此標記來建立物件。</span><span class="sxs-lookup"><span data-stu-id="01371-108">Later, the application can use the moniker to create the object.</span></span> <span data-ttu-id="01371-109">如需有關別名的詳細資訊，請參閱 [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)的檔。</span><span class="sxs-lookup"><span data-stu-id="01371-109">For more information about monikers, see the documentation for [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span></span>

<span data-ttu-id="01371-110">若要使用系統裝置列舉值，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="01371-110">To use the System Device Enumerator, perform the following steps.</span></span>

1.  <span data-ttu-id="01371-111">呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立系統裝置列舉值的實例。</span><span class="sxs-lookup"><span data-stu-id="01371-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create an instance of the System Device Enumerator.</span></span>
2.  <span data-ttu-id="01371-112">呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) ，並將裝置類別指定為 GUID。</span><span class="sxs-lookup"><span data-stu-id="01371-112">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) and specify the device category as a GUID.</span></span> <span data-ttu-id="01371-113">針對 capture 裝置，下列類別是相關的。</span><span class="sxs-lookup"><span data-stu-id="01371-113">For capture devices, the following categories are relevant.</span></span> 

    | <span data-ttu-id="01371-114">類別 GUID</span><span class="sxs-lookup"><span data-stu-id="01371-114">Category GUID</span></span>                       | <span data-ttu-id="01371-115">Description</span><span class="sxs-lookup"><span data-stu-id="01371-115">Description</span></span>           |
    |-------------------------------------|-----------------------|
    | <span data-ttu-id="01371-116">**CLSID \_ AudioInputDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="01371-116">**CLSID\_AudioInputDeviceCategory**</span></span> | <span data-ttu-id="01371-117">音訊捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="01371-117">Audio capture devices</span></span> |
    | <span data-ttu-id="01371-118">**CLSID \_ VideoInputDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="01371-118">**CLSID\_VideoInputDeviceCategory**</span></span> | <span data-ttu-id="01371-119">影片捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="01371-119">Video capture devices</span></span> |

    

     

    <span data-ttu-id="01371-120">如果攝影機有整合式麥克風，則會同時出現在這兩個類別中。</span><span class="sxs-lookup"><span data-stu-id="01371-120">If a video camera has an integrated microphone, it appears in both categories.</span></span> <span data-ttu-id="01371-121">不過，系統會將相機和麥克風視為個別的裝置，以供列舉、裝置建立和資料串流之用。</span><span class="sxs-lookup"><span data-stu-id="01371-121">However, the camera and microphone are treated as separate devices by the system, for purposes of enumeration, device creation, and data streaming.</span></span>

3.  <span data-ttu-id="01371-122">[**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator)方法會傳回 [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="01371-122">The [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method returns a pointer to the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="01371-123">若要列舉名字，請呼叫 [**IEnumMoniker：： Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next)。</span><span class="sxs-lookup"><span data-stu-id="01371-123">To enumerate the monikers, call [**IEnumMoniker::Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span></span>

<span data-ttu-id="01371-124">下列程式碼會建立指定裝置類別的列舉值。</span><span class="sxs-lookup"><span data-stu-id="01371-124">The following code creates an enumerator for a specified device category.</span></span>


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



<span data-ttu-id="01371-125">[**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker)介面會列舉 [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)介面的清單，每個介面都代表一個裝置的標記。</span><span class="sxs-lookup"><span data-stu-id="01371-125">The [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface enumerates a list of [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interfaces, each of which represents a device moniker.</span></span> <span data-ttu-id="01371-126">應用程式可以從標記讀取屬性，或使用此標記來建立裝置的 DirectShow 捕獲篩選。</span><span class="sxs-lookup"><span data-stu-id="01371-126">The application can read properties from the moniker, or use the moniker to create a DirectShow capture filter for the device.</span></span> <span data-ttu-id="01371-127">會以 **變異** 值的形式傳回「標記」屬性。</span><span class="sxs-lookup"><span data-stu-id="01371-127">Moniker properties are returned as **VARIANT** values.</span></span> <span data-ttu-id="01371-128">裝置的名字標記支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="01371-128">The following properties are supported by device monikers.</span></span>



| <span data-ttu-id="01371-129">屬性</span><span class="sxs-lookup"><span data-stu-id="01371-129">Property</span></span>       | <span data-ttu-id="01371-130">描述</span><span class="sxs-lookup"><span data-stu-id="01371-130">Description</span></span>                                                               | <span data-ttu-id="01371-131">VARIANT 型別</span><span class="sxs-lookup"><span data-stu-id="01371-131">VARIANT Type</span></span> |
|----------------|---------------------------------------------------------------------------|--------------|
| <span data-ttu-id="01371-132">友好</span><span class="sxs-lookup"><span data-stu-id="01371-132">"FriendlyName"</span></span> | <span data-ttu-id="01371-133">裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="01371-133">The name of the device.</span></span>                                                   | <span data-ttu-id="01371-134">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="01371-134">**VT\_BSTR**</span></span> |
| <span data-ttu-id="01371-135">產品介紹</span><span class="sxs-lookup"><span data-stu-id="01371-135">"Description"</span></span>  | <span data-ttu-id="01371-136">裝置的描述。</span><span class="sxs-lookup"><span data-stu-id="01371-136">A description of the device.</span></span>                                              | <span data-ttu-id="01371-137">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="01371-137">**VT\_BSTR**</span></span> |
| <span data-ttu-id="01371-138">DevicePath</span><span class="sxs-lookup"><span data-stu-id="01371-138">"DevicePath"</span></span>   | <span data-ttu-id="01371-139">識別裝置的唯一字串。</span><span class="sxs-lookup"><span data-stu-id="01371-139">A unique string that identifies the device.</span></span> <span data-ttu-id="01371-140">僅 (影片捕獲裝置。 ) </span><span class="sxs-lookup"><span data-stu-id="01371-140">(Video capture devices only.)</span></span> | <span data-ttu-id="01371-141">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="01371-141">**VT\_BSTR**</span></span> |
| <span data-ttu-id="01371-142">"WaveInID"</span><span class="sxs-lookup"><span data-stu-id="01371-142">"WaveInID"</span></span>     | <span data-ttu-id="01371-143">音訊捕獲裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="01371-143">The identifier for an audio capture device.</span></span> <span data-ttu-id="01371-144">僅 (音訊捕獲裝置。 ) </span><span class="sxs-lookup"><span data-stu-id="01371-144">(Audio capture devices only.)</span></span> | <span data-ttu-id="01371-145">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="01371-145">**VT\_I4**</span></span>   |



 

<span data-ttu-id="01371-146">"FriendlyName" 和 "Description" 屬性適用于在 UI 中顯示。</span><span class="sxs-lookup"><span data-stu-id="01371-146">The "FriendlyName" and "Description" properties are suitable for displaying in a UI.</span></span>

-   <span data-ttu-id="01371-147">每個裝置都可以使用「FriendlyName」屬性。</span><span class="sxs-lookup"><span data-stu-id="01371-147">The "FriendlyName" property is available for every device.</span></span> <span data-ttu-id="01371-148">它包含人們看得懂的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="01371-148">It contains a human-readable name for the device.</span></span>
-   <span data-ttu-id="01371-149">[描述] 屬性僅適用于 DV 和 D VHS/MPEG 攝像機裝置。</span><span class="sxs-lookup"><span data-stu-id="01371-149">The "Description" property is available only for DV and D-VHS/MPEG camcorder devices.</span></span> <span data-ttu-id="01371-150">如需詳細資訊，請參閱 [MSDV 驅動程式](msdv-driver.md) 和 [MSTape 驅動程式](mstape-driver.md)。</span><span class="sxs-lookup"><span data-stu-id="01371-150">For more information, see [MSDV Driver](msdv-driver.md) and [MSTape Driver](mstape-driver.md).</span></span> <span data-ttu-id="01371-151">如果有的話，它會包含裝置的描述，而該裝置的描述比 "FriendlyName" 屬性更明確。</span><span class="sxs-lookup"><span data-stu-id="01371-151">If available, it contains a description of the device which is more specific than the "FriendlyName" property.</span></span> <span data-ttu-id="01371-152">通常會包含廠商名稱。</span><span class="sxs-lookup"><span data-stu-id="01371-152">Typically it includes the vendor name.</span></span>
-   <span data-ttu-id="01371-153">"DevicePath" 屬性不是人們可讀取的字串，但在系統上的每個影片捕獲裝置保證都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="01371-153">The "DevicePath" property is not a human-readable string, but is guaranteed to be unique for each video capture device on the system.</span></span> <span data-ttu-id="01371-154">您可以使用這個屬性來區別相同裝置模型的兩個或多個實例。</span><span class="sxs-lookup"><span data-stu-id="01371-154">You can use this property to distinguish between two or more instances of the same model of device.</span></span>
-   <span data-ttu-id="01371-155">如果出現 "WaveInID" 屬性，則表示 DirectShow 捕獲篩選器會在內部使用 [波形音訊](../multimedia/waveform-audio.md) api 來與裝置通訊。</span><span class="sxs-lookup"><span data-stu-id="01371-155">If the "WaveInID" property is present, it means the DirectShow capture filter uses the [Waveform Audio](../multimedia/waveform-audio.md) APIs internally to communicate with the device.</span></span> <span data-ttu-id="01371-156">"WaveInID" 屬性的值會對應到 \**waveIn \** _ 函式所使用的識別碼，例如 [_ *waveInOpen* \*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)。</span><span class="sxs-lookup"><span data-stu-id="01371-156">The value of the "WaveInID" property corresponds to the identifier used by the \**waveIn\** _ functions, such as [_ *waveInOpen*\*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span></span>

<span data-ttu-id="01371-157">若要從標記讀取屬性，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="01371-157">To read properties from the moniker, perform the following steps.</span></span>

1.  <span data-ttu-id="01371-158">呼叫 [**IMoniker：： BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) 來取得 [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="01371-158">Call [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) to get a pointer to the [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) interface.</span></span>
2.  <span data-ttu-id="01371-159">呼叫 **IPropertyBag：： read** 以讀取屬性。</span><span class="sxs-lookup"><span data-stu-id="01371-159">Call **IPropertyBag::Read** to read the property.</span></span>

<span data-ttu-id="01371-160">下列程式碼範例示範如何列舉裝置名字標記的清單並取得屬性。</span><span class="sxs-lookup"><span data-stu-id="01371-160">The following code example shows how to enumerate a list of device monikers and get the properties.</span></span>


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



<span data-ttu-id="01371-161">若要建立裝置的 DirectShow 捕獲篩選器，請呼叫 [**IMoniker：： BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) 方法來取得 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 指標。</span><span class="sxs-lookup"><span data-stu-id="01371-161">To create a DirectShow capture filter for the device, call the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to get an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="01371-162">然後呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) ，將篩選新增至篩選圖形：</span><span class="sxs-lookup"><span data-stu-id="01371-162">Then call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph:</span></span>


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a><span data-ttu-id="01371-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="01371-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01371-164">音訊捕獲</span><span class="sxs-lookup"><span data-stu-id="01371-164">Audio Capture</span></span>](audio-capture.md)
</dt> <dt>

[<span data-ttu-id="01371-165">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="01371-165">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
