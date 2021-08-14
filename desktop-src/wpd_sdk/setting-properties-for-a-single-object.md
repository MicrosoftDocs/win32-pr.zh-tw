---
description: 設定單一物件的屬性
ms.assetid: 1c003534-96b4-419b-94d1-73b5ffa2eba1
title: 設定單一物件的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a38964282b4ff6a51ee104bafc596f40f6107a87ae8069eba84a25386e7842
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704278"
---
# <a name="setting-properties-for-a-single-object"></a>設定單一物件的屬性

在您的應用程式抓取物件識別碼之後 (查看指定物件的 [列舉內容](enumerating-content.md) 主題) ，它可以藉由呼叫下表所述介面中的方法來設定該物件的屬性。



| 介面                                                                | 描述                                                                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | 用來判斷是否可以寫入指定的屬性，並傳送寫入作業。                                                                  |
| [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | 提供內容特定方法的存取權。                                                                                                            |
| [**IPortableDeviceValues 介面**](iportabledevicevalues.md)         | 用來保存要寫入的值、判斷寫入作業的結果，以及在決定寫入功能) 時， (抓取屬性的屬性。 |



 

應用程式會先建立屬性包（使用 [**IPortableDeviceValues 介面**](iportabledevicevalues.md)指定新值），藉以設定物件上的屬性。 建立屬性包之後，應用程式會藉由呼叫 [**IPortableDeviceProperties：： SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) 方法來設定這些屬性。

`WriteContentProperties`範例應用程式的 ContentProperties .cpp 模組中的函式會示範應用程式如何為選取的物件設定新的物件名稱屬性。

函式所完成的第一項工作 `WriteContentProperties` 是提示使用者輸入物件的物件識別碼，應用程式將會為該物件撰寫新的名稱。


```C++
HRESULT                               hr                   = S_OK;
WCHAR                                 szSelection[81]      = {0};
WCHAR                                 szNewObjectName[81]  = {0};
CComPtr<IPortableDeviceProperties>    pProperties;
CComPtr<IPortableDeviceContent>       pContent;
CComPtr<IPortableDeviceValues>        pObjectPropertiesToWrite;
CComPtr<IPortableDeviceValues>        pPropertyWriteResults;
CComPtr<IPortableDeviceValues>        pAttributes;
BOOL                                  bCanWrite            = FALSE;

// Prompt user to enter an object identifier on the device to write properties on.
printf("Enter the identifer of the object you wish to write properties on.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting property reading\n");
}
```



之後，應用程式會抓取 WPD \_ 屬性 \_ 屬性， \_ \_ 以寫入 WPD \_ OBJECT NAME 屬性的值， \_ 以判斷是否可以寫入屬性。  (請注意，您的應用程式可以設定任何屬性，其中 WPD \_ 屬性 \_ 屬性 \_ 可以 \_ 寫入值為 true。 ) 


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent interface
// to access the property-specific methods.
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 3) Check the property attributes to see if we can write/change the WPD_OBJECT_NAME property.
if (SUCCEEDED(hr))
{
    hr = pProperties->GetPropertyAttributes(szSelection,
                                            WPD_OBJECT_NAME,
                                            &pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
        if (SUCCEEDED(hr))
        {
            if (bCanWrite)
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports TRUE\nThis means that the property can be changed/updated\n\n");
            }
            else
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports FALSE\nThis means that the property cannot be changed/updated\n\n");
            }
        }
        else
        {
            printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value from WPD_OBJECT_NAME on object '%ws', hr = 0x%lx\n",szSelection, hr);
        }
    }
}
```



下一步是提示使用者輸入新的名稱字串。  (請注意， [**IPortableDeviceValues：： SetStringValue**](iportabledevicevalues-setstringvalue.md) 方法的呼叫只會建立屬性包;實際的屬性尚未寫入。 ) 


```C++
if (bCanWrite)
{
    printf("Enter the new WPD_OBJECT_NAME for the object '%ws'.\n>",szSelection);
    hr = StringCbGetsW(szNewObjectName,sizeof(szNewObjectName));
    if (FAILED(hr))
    {
        printf("An invalid object name was specified, aborting property writing\n");
    }

    // 5) CoCreate an IPortableDeviceValues interface to hold the property values
    // we wish to write.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pObjectPropertiesToWrite));
        if (SUCCEEDED(hr))
        {
            if (pObjectPropertiesToWrite != NULL)
            {
                hr = pObjectPropertiesToWrite->SetStringValue(WPD_OBJECT_NAME, szNewObjectName);
                if (FAILED(hr))
                {
                    printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceValues, hr= 0x%lx\n", hr);
                }
            }
        }
    }
```



最後，使用者所指定的新值會套用至物件。


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->SetValues(szSelection,                // The object whose properties we are reading
                                pObjectPropertiesToWrite,   // The properties we want to read
                                &pPropertyWriteResults);    // Driver supplied property result values for the property read operation
    if (FAILED(hr))
    {
        printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
    else
    {
        printf("The WPD_OBJECT_NAME property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", szSelection);
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**IPortableDevicePropertiesBulk 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



