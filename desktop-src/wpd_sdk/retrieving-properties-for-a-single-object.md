---
description: 取得單一物件的屬性
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: 取得單一物件的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5851b31256659c2ca036bac504a53fa51a20ee14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985476"
---
# <a name="retrieving-properties-for-a-single-object"></a>取得單一物件的屬性

在您的應用程式抓取物件識別碼之後 (查看指定物件的 [列舉內容](enumerating-content.md) 主題) ，它可以藉由呼叫 [**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) 和 [**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md)中的方法，來取得該物件的描述性資訊。

[**IPortableDeviceProperties：： GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues)方法會取得指定物件的指定屬性清單。  (您的應用程式也可以呼叫 GetValues 方法，並為 pKeys 參數指定 **Null** 值，以抓取指定物件的所有屬性。不過，在抓取所有屬性時，此方法的效能可能會大幅降低。 ) 

不過，在您的應用程式呼叫 GetValues 之前，它需要藉由在 [**IPortableDeviceKeyCollection 物件**](iportabledevicekeycollection.md)中設定對應的索引鍵來識別要抓取的屬性。 您的應用程式會藉由呼叫 [**IPortableDeviceKeyCollection：： Add**](iportabledevicekeycollection-add.md) 方法並提供 PROPERTYKEY 值來識別要抓取的每個屬性，來識別相關的屬性。

範例應用程式之 ContentProperties .cpp 模組中的 ReadContentProperties 函式會示範如何針對選取的物件抓取五個屬性。 下表描述每個屬性及其對應的 REFPROPERTYKEY 值。



| 屬性                     | 描述                                                                                                                                      | PROPERTYKEY                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| 父物件識別碼     | 字串，指定指定物件之父系的識別碼。                                                                            | WPD \_ 物件 \_ 父 \_ 識別碼             |
| 物件名稱                  | 指定指定物件名稱的字串。                                                                                            | WPD \_ 物件 \_ 名稱                   |
| 持續性唯一識別碼 | 字串，指定指定物件的唯一識別碼。  (此識別碼在會話之間是持續性的，與物件識別碼不同。 )  | WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼 |
| 物件格式                |  (GUID) 的全域唯一識別碼，可指定對應于指定物件之檔案的格式。                                       | WPD \_ 物件 \_ 格式                 |
| 物件內容類型          | GUID，指定與指定物件相關聯的內容類型。                                                                        | WPD \_ 物件 \_ 內容 \_ 類型          |



 

ReadContentProperties 函式的下列摘錄將示範範例應用程式如何使用 [**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md) 和 [**IPortableDeviceKeyCollection：： Add**](iportabledevicekeycollection-add.md) 方法來識別它所要抓取的屬性。


```C++
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
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



一旦範例應用程式設定適當的索引鍵，它就會呼叫 [**IPortableDeviceProperties：： GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) 方法，以取得指定物件的指定值。


```C++
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
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



