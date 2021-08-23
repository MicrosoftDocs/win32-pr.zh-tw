---
description: 正在抓取裝置所支援的轉譯功能
ms.assetid: 2332e3cc-087c-49cf-bde9-7f86f65158e7
title: 正在抓取裝置所支援的轉譯功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b5e4fd09417585954ae205fc28fc8cf0e78ab02fdd3add616859b35b4237ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546228"
---
# <a name="retrieving-the-rendering-capabilities-supported-by-a-device"></a>正在抓取裝置所支援的轉譯功能

Windows支援轉譯資訊功能類別目錄 (WPD 功能類別轉譯資訊的可攜式裝置 \_ \_ \_ \_) 會在查詢時傳回轉譯資訊。 轉譯資訊描述在嘗試將內容寫入至裝置的應用程式上所強加的需求和限制。

ListRenderingCapabilityInformation 函式、SupportsFunctionalCategory helper 函式和 DeviceCapabilities 中的 ReadProfileInformationProperties helper 函數會示範如何抓取所選裝置的轉譯功能。

您的應用程式可以使用下表所述的介面，來取得裝置所支援的轉譯功能。



| 介面                                                                                      | 描述                                                 |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | 提供 IPortableDeviceProperties 介面的存取權。 |
| [**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | 提供屬性特定方法的存取。           |
| [**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md)                 | 用來儲存指定設定檔的屬性索引鍵。      |
| [**IPortableDeviceValues 介面**](iportabledevicevalues.md)                               | 使用儲存指定設定檔的屬性值。       |
| [**IPortableDeviceCapabilities 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | 使用儲存指定設定檔的屬性值。       |
| [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) | 使用儲存指定設定檔的屬性值。       |
| [**IPortableDeviceValuesCollection 介面**](iportabledevicevaluescollection.md)           | 使用儲存指定設定檔的屬性值。       |



 

範例應用程式所完成的第一項工作是判斷選取的裝置是否能夠列出轉譯功能。 SupportsFunctionalCategory helper 函式會藉由呼叫 ListRenderingCapabilityInformation helper 函式，並 \_ 將 WPD 功能 \_ 類別轉譯資訊傳遞 \_ \_ 為第二個引數，來判斷是否為這種情況。


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



如果裝置能夠列出轉譯功能，下一個步驟就需要抓取 [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) 物件，並叫用 [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) 方法來取得轉譯資訊物件的物件識別碼。


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



下一步是儲存剛剛在字串變數中取出的轉譯資訊物件識別碼 (strRenderingInfoObjectID) ，然後呼叫 ReadProfileInformationProperties helper 函數。  (變數 strRenderingInfoObjectID 會以第二個引數的形式傳遞至 helper 函式。 ) 


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



Helper 函式所完成的第一項工作之一，是取出 [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) 物件，它會用來存取內容特定的方法。


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



接下來，helper 函式會抓取 [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) 物件，它會用來存取屬性特有的方法。


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



下一步是建立 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) 物件，以在其中儲存轉譯資訊的屬性索引鍵。 一旦建立物件之後，就會叫用 [**IPortableDeviceKeyCollection：： add**](iportabledevicekeycollection-add.md) 方法來新增必要的索引鍵。  (需要新增這些金鑰，才能在後續步驟中取出對應的轉譯設定檔。 ) 


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



下一步是藉由呼叫 [**IPortableDeviceProperties：： GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) 方法，從設備磁碟機取出屬性值。


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



下一個步驟會取出轉譯資訊設定檔，並將它儲存在 ppRenderingInfoProfiles 引數中。


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



Helper 函式讀取 WPD 轉譯 \_ \_ 資訊 \_ 配置檔案屬性之後，就會顯示轉譯設定檔。 DisplayRenderingProfile helper 函數會顯示這些設定檔。


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



請注意，由於轉譯設定檔是靜態的，因此您的應用程式可能會選擇讀取設定檔，並將它們儲存在本機 (而不是每次需要資料時都存取裝置) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceCapabilities 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**IPortableDeviceValuesCollection 介面**](iportabledevicevaluescollection.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



