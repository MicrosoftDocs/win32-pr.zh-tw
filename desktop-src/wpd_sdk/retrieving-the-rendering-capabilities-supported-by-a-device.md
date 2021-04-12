---
description: 正在抓取裝置所支援的轉譯功能
ms.assetid: 2332e3cc-087c-49cf-bde9-7f86f65158e7
title: 正在抓取裝置所支援的轉譯功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523f1f9bbcaefe1c502c7c74252582fddcadad4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320712"
---
# <a name="retrieving-the-rendering-capabilities-supported-by-a-device"></a><span data-ttu-id="4cfea-103">正在抓取裝置所支援的轉譯功能</span><span class="sxs-lookup"><span data-stu-id="4cfea-103">Retrieving the Rendering Capabilities Supported by a Device</span></span>

<span data-ttu-id="4cfea-104">支援轉譯資訊功能類別目錄 (WPD 功能類別轉譯資訊的 Windows 可攜式裝置 \_ \_ \_ \_) 會在查詢時傳回轉譯資訊。</span><span class="sxs-lookup"><span data-stu-id="4cfea-104">Windows Portable Devices that support the rendering information functional category (WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION) will return rendering information when queried.</span></span> <span data-ttu-id="4cfea-105">轉譯資訊描述在嘗試將內容寫入至裝置的應用程式上所強加的需求和限制。</span><span class="sxs-lookup"><span data-stu-id="4cfea-105">The rendering information describes requirements and restrictions imposed on applications that attempt to write content to a device.</span></span>

<span data-ttu-id="4cfea-106">ListRenderingCapabilityInformation 函式、SupportsFunctionalCategory helper 函式和 DeviceCapabilities 中的 ReadProfileInformationProperties helper 函數會示範如何抓取所選裝置的轉譯功能。</span><span class="sxs-lookup"><span data-stu-id="4cfea-106">The ListRenderingCapabilityInformation function, the SupportsFunctionalCategory helper function, and the ReadProfileInformationProperties helper function in the DeviceCapabilities.cpp module demonstrate the retrieval of rendering capabilities for a selected device.</span></span>

<span data-ttu-id="4cfea-107">您的應用程式可以使用下表所述的介面，來取得裝置所支援的轉譯功能。</span><span class="sxs-lookup"><span data-stu-id="4cfea-107">Your application can retrieve the rendering capabilities supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="4cfea-108">介面</span><span class="sxs-lookup"><span data-stu-id="4cfea-108">Interface</span></span>                                                                                      | <span data-ttu-id="4cfea-109">描述</span><span class="sxs-lookup"><span data-stu-id="4cfea-109">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="4cfea-110">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="4cfea-111">提供 IPortableDeviceProperties 介面的存取權。</span><span class="sxs-lookup"><span data-stu-id="4cfea-111">Provides access to the IPortableDeviceProperties interface.</span></span> |
| [<span data-ttu-id="4cfea-112">**IPortableDeviceProperties 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-112">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="4cfea-113">提供屬性特定方法的存取。</span><span class="sxs-lookup"><span data-stu-id="4cfea-113">Provides access to the property-specific methods.</span></span>           |
| [<span data-ttu-id="4cfea-114">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-114">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="4cfea-115">用來儲存指定設定檔的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4cfea-115">Used to store the property keys for the given profile.</span></span>      |
| [<span data-ttu-id="4cfea-116">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-116">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="4cfea-117">使用儲存指定設定檔的屬性值。</span><span class="sxs-lookup"><span data-stu-id="4cfea-117">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="4cfea-118">**IPortableDeviceCapabilities 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-118">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="4cfea-119">使用儲存指定設定檔的屬性值。</span><span class="sxs-lookup"><span data-stu-id="4cfea-119">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="4cfea-120">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-120">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="4cfea-121">使用儲存指定設定檔的屬性值。</span><span class="sxs-lookup"><span data-stu-id="4cfea-121">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="4cfea-122">**IPortableDeviceValuesCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-122">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="4cfea-123">使用儲存指定設定檔的屬性值。</span><span class="sxs-lookup"><span data-stu-id="4cfea-123">Used store the property values for the given profile.</span></span>       |



 

<span data-ttu-id="4cfea-124">範例應用程式所完成的第一項工作是判斷選取的裝置是否能夠列出轉譯功能。</span><span class="sxs-lookup"><span data-stu-id="4cfea-124">One of the first tasks accomplished by the sample application is to determine whether the selected device is capable of listing rendering capabilities.</span></span> <span data-ttu-id="4cfea-125">SupportsFunctionalCategory helper 函式會藉由呼叫 ListRenderingCapabilityInformation helper 函式，並 \_ 將 WPD 功能 \_ 類別轉譯資訊傳遞 \_ \_ 為第二個引數，來判斷是否為這種情況。</span><span class="sxs-lookup"><span data-stu-id="4cfea-125">The SupportsFunctionalCategory helper function determines whether this is the case by calling the ListRenderingCapabilityInformation helper function and passing WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION as the second argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SupportsFunctionalCategory(pDevice, WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION) == FALSE)
{
    printf("This device does not support device rendering information to display\n");
    return;
}
```



<span data-ttu-id="4cfea-126">如果裝置能夠列出轉譯功能，下一個步驟就需要抓取 [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) 物件，並叫用 [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) 方法來取得轉譯資訊物件的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="4cfea-126">If the device is capable of listing rendering capabilities, the next step entails retrieving an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object and invoking the [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method to retrieve an object identifier for the rendering-information object.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get the functional object identifier for the rendering information object
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalObjects(WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION, &pRenderingInfoObjects);
    if (FAILED(hr))
    {
        printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="4cfea-127">下一步是儲存剛剛在字串變數中取出的轉譯資訊物件識別碼 (strRenderingInfoObjectID) ，然後呼叫 ReadProfileInformationProperties helper 函數。</span><span class="sxs-lookup"><span data-stu-id="4cfea-127">The next step is to store the rendering-information object identifier that was just retrieved in a string variable (strRenderingInfoObjectID), and then to call the ReadProfileInformationProperties helper function.</span></span> <span data-ttu-id="4cfea-128"> (變數 strRenderingInfoObjectID 會以第二個引數的形式傳遞至 helper 函式。 ) </span><span class="sxs-lookup"><span data-stu-id="4cfea-128">(The variable, strRenderingInfoObjectID, is passed as the second argument to the helper function.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SUCCEEDED(hr))
{
    PROPVARIANT pv = {0};
    PropVariantInit(&pv);
    hr = pRenderingInfoObjects->GetAt(0, &pv);
    if ((SUCCEEDED(hr))    &&
        (pv.vt== VT_LPWSTR) )
    {
        strRenderingInfoObjectID = pv.pwszVal;
    }
    else
    {
        printf("! Failed to get first rendering object's identifier, hr = 0x%lx\n", hr);
    }

    PropVariantClear(&pv);
}

if (SUCCEEDED(hr))
{
    hr = ReadProfileInformationProperties(pDevice,
                                          strRenderingInfoObjectID,
                                          &pRenderingInfoProfiles);
    // Error output statements are performed by the helper function, so they
    // are omitted here.
}
```



<span data-ttu-id="4cfea-129">Helper 函式所完成的第一項工作之一，是取出 [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) 物件，它會用來存取內容特定的方法。</span><span class="sxs-lookup"><span data-stu-id="4cfea-129">One of the first tasks accomplished by the helper function is to retrieve an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to access the content-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="4cfea-130">接下來，helper 函式會抓取 [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) 物件，它會用來存取屬性特有的方法。</span><span class="sxs-lookup"><span data-stu-id="4cfea-130">Next, the helper function retrieves an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) object, which it will use to access the property-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="4cfea-131">下一步是建立 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) 物件，以在其中儲存轉譯資訊的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4cfea-131">The next step is to create an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object into which the property keys for the rendering information are stored.</span></span> <span data-ttu-id="4cfea-132">一旦建立物件之後，就會叫用 [**IPortableDeviceKeyCollection：： add**](iportabledevicekeycollection-add.md) 方法來新增必要的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4cfea-132">Once the object is created, the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method is invoked to add the necessary keys.</span></span> <span data-ttu-id="4cfea-133"> (需要新增這些金鑰，才能在後續步驟中取出對應的轉譯設定檔。 ) </span><span class="sxs-lookup"><span data-stu-id="4cfea-133">(It is necessary to add these keys so that the corresponding rendering profiles can be retrieved in the subsequent steps.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IPortableDeviceKeyCollection,
                      (VOID**) &pPropertiesToRead);
if (SUCCEEDED(hr))
{
    // Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_RENDERING_INFORMATION_PROFILES);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_RENDERING_INFORMATION_PROFILES to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="4cfea-134">下一步是藉由呼叫 [**IPortableDeviceProperties：： GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) 方法，從設備磁碟機取出屬性值。</span><span class="sxs-lookup"><span data-stu-id="4cfea-134">The next step is to retrieve the property values from the device driver by calling the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(wszFunctionalObjectID, // The object whose properties we are reading
                                pPropertiesToRead,     // The properties we want to read
                                &pObjectProperties);   // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", wszFunctionalObjectID, hr);
    }
}
```



<span data-ttu-id="4cfea-135">下一個步驟會取出轉譯資訊設定檔，並將它儲存在 ppRenderingInfoProfiles 引數中。</span><span class="sxs-lookup"><span data-stu-id="4cfea-135">The next step retrieves the rendering-information profile and stores it in the ppRenderingInfoProfiles argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pObjectProperties->GetIPortableDeviceValuesCollectionValue(WPD_RENDERING_INFORMATION_PROFILES,
                                                                    &pRenderingInfoProfiles);
    if (FAILED(hr))
    {
        printf("! Failed to get WPD_RENDERING_INFORMATION_PROFILES from rendering information, hr= 0x%lx\n",  hr);
    }
}

// QueryInterface the interface into the out-going parameters.
if (SUCCEEDED(hr))
{
    hr = pRenderingInfoProfiles->QueryInterface(IID_PPV_ARGS(ppRenderingInfoProfiles));
    if (FAILED(hr))
    {
        printf("! Failed to QueryInterface for IPortableDeviceValuesCollection (Rendering information profiles), hr= 0x%lx\n",  hr);
    }
}
```



<span data-ttu-id="4cfea-136">Helper 函式讀取 WPD 轉譯 \_ \_ 資訊 \_ 配置檔案屬性之後，就會顯示轉譯設定檔。</span><span class="sxs-lookup"><span data-stu-id="4cfea-136">After the helper function reads the WPD\_RENDERING\_INFORMATION\_PROFILES properties, the rendering profiles are displayed.</span></span> <span data-ttu-id="4cfea-137">DisplayRenderingProfile helper 函數會顯示這些設定檔。</span><span class="sxs-lookup"><span data-stu-id="4cfea-137">These profiles are displayed by the DisplayRenderingProfile helper function.</span></span>


```C++
void DisplayRenderingProfile(
    IPortableDeviceValues* pProfile)
{
    HRESULT hr = S_OK;
    if (pProfile == NULL)
    {
        return;
    }

    if (SUCCEEDED(hr))
    {
        DWORD dwTotalBitrate    = 0;
        DWORD dwChannelCount    = 0;
        DWORD dwAudioFormatCode = 0;
        GUID  guidFormat        = WPD_OBJECT_FORMAT_UNSPECIFIED;

        // Display WPD_MEDIA_TOTAL_BITRATE
        hr = pProfile->GetUnsignedIntegerValue(WPD_MEDIA_TOTAL_BITRATE, &dwTotalBitrate);
        if (SUCCEEDED(hr))
        {
            printf("Total Bitrate: %d\n", dwTotalBitrate);
        }

        // If we fail to read the total bitrate as a single value, then it must be
        // a valid value set.  (i.e. returning IPortableDeviceValues as the value which
        // contains properties describing the valid values for this property.)
        if (hr == DISP_E_TYPEMISMATCH)
        {
            CComPtr<IPortableDeviceValues> pExpectedValues;
            hr = pProfile->GetIPortableDeviceValuesValue(WPD_MEDIA_TOTAL_BITRATE, &pExpectedValues);
            if (SUCCEEDED(hr))
            {
                printf("Total Bitrate: ");
                DisplayExpectedValues(pExpectedValues);
            }
        }

        // If we are still a failure here, report the error
        if (FAILED(hr))
        {

            printf("! Failed to get WPD_MEDIA_TOTAL_BITRATE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_CHANNEL_COUNT
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_CHANNEL_COUNT, &dwChannelCount);
        if (SUCCEEDED(hr))
        {
            printf("Channel Count: %d\n", dwChannelCount);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_CHANNEL_COUNT from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_FORMAT_CODE
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_FORMAT_CODE,   &dwAudioFormatCode);
        if (SUCCEEDED(hr))
        {
            printf("Audio Format Code: %d\n", dwAudioFormatCode);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_FORMAT_CODE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_OBJECT_FORMAT
        hr = pProfile->GetGuidValue(WPD_OBJECT_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("Object Format: %ws\n", (LPWSTR)CComBSTR(guidFormat));
        }
        else
        {
            printf("! Failed to get WPD_OBJECT_FORMAT from rendering profile, hr = 0x%lx\n",hr);
        }
    }
}
```



<span data-ttu-id="4cfea-138">請注意，由於轉譯設定檔是靜態的，因此您的應用程式可能會選擇讀取設定檔，並將它們儲存在本機 (而不是每次需要資料時都存取裝置) 。</span><span class="sxs-lookup"><span data-stu-id="4cfea-138">Note that since the rendering profiles are static, your application may choose to read the profiles and store them locally (instead of accessing the device each time the data is needed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cfea-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="4cfea-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cfea-140">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="4cfea-141">**IPortableDeviceCapabilities 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-141">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="4cfea-142">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="4cfea-143">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="4cfea-144">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="4cfea-145">**IPortableDeviceValuesCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="4cfea-145">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> <dt>

[<span data-ttu-id="4cfea-146">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="4cfea-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



