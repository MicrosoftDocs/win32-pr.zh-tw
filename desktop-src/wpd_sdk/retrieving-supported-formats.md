---
description: 正在抓取支援的服務格式
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: 正在抓取支援的服務格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccbaa5678d12e4393f377bb0ae0a399634b247ceb9bd54e1d815d4e9f7e5a763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806668"
---
# <a name="retrieving-supported-service-formats"></a>正在抓取支援的服務格式

WpdServicesApiSample 應用程式所包含的程式碼會示範應用程式如何藉由呼叫下表中的介面方法，來取得指定連絡人服務所支援的格式。



| 介面 | 描述   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | 用來取出 **IPortableDeviceServiceCapabilities** 介面，以存取支援的事件。 |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | 提供支援的事件和事件屬性的存取權。                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | 包含支援的格式清單。                                                               |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | 包含給定格式的屬性。                                                           |



 

當使用者在命令列選擇選項 "3" 時，應用程式會叫用在 ServiceCapabilities .cpp 模組中找到的 **ListSupportedFormats** 方法。

請注意，在抓取事件清單之前，範例應用程式會在連線的裝置上開啟連絡人服務。

在 WPD 中，格式是由指定名稱的屬性描述， (選擇性地) 指定格式的 MIME 類型。 這些屬性是在 thePortableDevice 標頭檔中定義。 如需支援屬性的說明，請參閱 [屬性](attributes.md) 主題。

在範例應用程式的案例中，如果 WpdServiceSampleDriver 是唯一安裝的裝置，驅動程式會針對其 Contact service 傳回兩種支援的格式： "AbstractContactFormat" 和 "VCard2Format"。 這些格式對應于 **WPD \_ 物件格式的「 \_ \_ 抽象 \_ 連絡人** 」和「 **WPD \_ 物件格式」 \_ \_ VCARD2** 在 PortableDevice 中找到的屬性。

ServiceCapabilities .cpp 模組中的兩個方法支援將連絡人服務的支援格式抓取： **ListSupportedFormats** 和 **DisplayFormat**。 前者會針對每個支援的格式抓取 GUID 識別碼。 後者會將此 GUID 轉換為使用者易記字串。

**ListSupportedFormats** 方法會叫用 [**IPortableDeviceService：：功能**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities)方法來取出 [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)介面。 使用這個介面，它會藉由呼叫 [**IPortableDeviceServiceCapabilities：： GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) 方法來抓取支援的格式。 **GetSupportedFormats** 方法會針對服務所支援的每種格式抓取 guid，並將該 guid 複製到 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)物件中。

下列程式碼會使用 **ListSupportedFormats** 方法。


```C++
// List all supported formats on the service
void ListSupportedFormats(
    IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumFormats    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pFormats;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all formats supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedFormats(&pFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get supported formats from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported formats found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pFormats->GetCount(&dwNumFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported formats, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Formats Found on the service\n\n", dwNumFormats);

    // Loop through each format and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumFormats; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pFormats->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a format.  It is assumed that
                // formats are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayFormat(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



在 **ListSupportedFormats** 方法為指定服務所支援的每種格式取得 GUID 之後，它會叫用 **DisplayFormat** 方法，以顯示每個格式的腳本易記名稱;例如，"VCard2"。

**DisplayFormat** 方法會叫用 [**IPortableDeviceServiceCapabilities：： GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes)方法，以取得指定之格式 GUID 的屬性集合。 然後，它會呼叫 [**IPortableDeviceValues：： GetStringValue**](iportabledevicevalues-getstringvalue.md) 方法，並要求驅動程式針對指定的格式傳回腳本易記的名稱。

下列程式碼會使用 **DisplayFormat** 方法。


```C++
// Display basic information about a format
void DisplayFormat(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Format)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    HRESULT hr = pCapabilities->GetFormatAttributes(Format, &pAttributes);

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        hr = pAttributes->GetStringValue(WPD_FORMAT_ATTRIBUTE_NAME, &pszFormatName);

        // Display the name of the format if it is available, otherwise fall back to displaying the GUID.
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszFormatName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Format));
        }       

        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



