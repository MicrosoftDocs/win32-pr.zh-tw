---
title: 正在抓取 WPD 物件屬性
description: WpdServiceApiSample 應用程式會示範應用程式如何取得指定連絡人服務所支援的內容物件屬性。
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56b164980249911ce267050143611dc599520fc841e33157bd6ac84718c1728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806688"
---
# <a name="retrieving-wpd-object-properties"></a>正在抓取 WPD 物件屬性

服務通常會包含屬於每個服務支援之其中一種格式的子物件。 例如，「連絡人」服務可能支援「抽象連絡人」格式的多個連絡人物件。 每個連絡人物件都是由相關屬性描述 (連絡人名稱、電話號碼、電子郵件地址等) 。

WpdServiceApiSample 應用程式所包含的程式碼會示範應用程式如何抓取指定連絡人服務所支援的內容物件屬性。 此範例會使用下列介面。



| 介面 | 描述    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | 抓取 **IPortableDeviceContent2** 介面以存取支援的服務方法。 |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | 提供內容特定方法的存取權。                                             |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | 抓取物件屬性值。                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)               | 保存針對該物件所讀取的屬性值。                                    |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) | 包含指定方法的參數。                                                  |



 

當使用者在命令列選擇選項 "7" 時，應用程式會叫用在 ContentProperties .cpp 模組中找到的 **ReadContentProperties** 方法。

這個方法會為指定的 contact 物件抓取下列四個屬性。



| 屬性                     | 描述                                                                                                                                                                                                      | 裝置服務 PROPERTYKEY     | 對等的 WPD \_ PROPERTYKEY         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| 父物件識別碼     | 字串，指定指定物件之父系的識別碼。                                                                                                                                            | PKEY \_ GenericObj \_ ParentID      | WPD \_ 物件 \_ 父 \_ 識別碼             |
| 物件名稱                  | 指定指定物件名稱的字串。                                                                                                                                                             | PKEY \_ GenericObj \_ 名稱          | WPD \_ 物件 \_ 名稱                   |
| 持續性唯一識別碼 | 字串，指定指定物件的唯一識別碼。 此識別碼在會話之間是持續性的，與物件識別碼不同。 針對服務，這必須是 GUID 的字串標記法。 | PKEY \_ GenericObj \_ PersistentUID | WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼 |
| 物件格式                |  (GUID) 的全域唯一識別碼，可指定對應于指定物件之檔案的格式。                                                                                                        | PKEY \_ GenericObj \_ ObjectFormat  | WPD \_ 物件 \_ 格式                 |



 

-   父識別碼
-   名稱
-   PersistentUID
-   格式

請注意，在抓取內容屬性之前，範例應用程式會在連線的裝置上開啟連絡人服務。

下列 **ReadContentProperties** 方法的程式碼會示範應用程式如何使用 [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) 介面來取出 [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) 介面。 藉由將要求的屬性 PROPERTYKEYS 傳遞至 [**IPortableDeviceProperties：： GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) 方法， **ReadContentProperties** 會抓取要求的值，然後將其顯示在主控台視窗中。


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
    if (FAILED(hr))
    {
        printf("An invalid object identifier was specified, aborting property reading\n");
    }

    // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pService->Content(&pContent);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
        }
    }

    // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
    // to access the property-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pContent->Properties(&pProperties);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
        }
    }

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pPropertiesToRead));
    if (SUCCEEDED(hr))
    {
        // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
        // NOTE: We are not handling any special error cases here so we can proceed with
        // adding as many of the target properties as we can.
        if (pPropertiesToRead != NULL)
        {
            HRESULT hrTemp = S_OK;
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
    if (SUCCEEDED(hr))
    {
        hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                    pPropertiesToRead,   // The properties we want to read
                                    &pObjectProperties); // Driver supplied property values for the specified object
        if (FAILED(hr))
        {
            printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
        }
    }

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



