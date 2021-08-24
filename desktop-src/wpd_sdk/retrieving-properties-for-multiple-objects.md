---
description: 正在抓取多個物件的屬性
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: 正在抓取多個物件的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1ad9ec397daa90c149fe950c1fc4777c407e3f5f3a359f46cf8bef56e18b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083512"
---
# <a name="retrieving-properties-for-multiple-objects"></a>正在抓取多個物件的屬性

某些設備磁碟機支援在單一函式呼叫中抓取多個物件的屬性;這稱為「大量抓取」。 大量抓取作業有兩種類型：第一個型別會抓取物件清單的屬性，而第二個型別則會抓取特定格式之所有物件的屬性。 本節所述的範例會示範前者。

您的應用程式可以使用下表所述的介面來執行大量抓取。



| 介面                                                                                      | 描述                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | 提供內容特定方法的存取權。                   |
| [**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md)                 | 用來識別要取出的屬性。                   |
| [**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | 用來判斷指定的驅動程式是否支援大量作業。 |
| [**IPortableDevicePropertiesBulk 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | 支援大量抓取作業。                             |
| [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) | 用來儲存大量作業的物件識別碼。       |



 

範例應用程式 ContentProperties .cpp 模組中的 ReadContentPropertiesBulk 函式會示範大量抓取作業。

在此範例中完成的第一項工作，是判斷指定的驅動程式是否支援大量作業。 這是藉由呼叫 IPortableDeviceProperties 介面上的 QueryInterface 並檢查 IPortableDevicePropertiesBulk 是否存在而完成。


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CGetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceKeyCollection>         pPropertiesToRead;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;


if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pProperties->QueryInterface(IID_PPV_ARGS(&pPropertiesBulk));
    if (FAILED(hr))
    {
        printf("This driver does not support BULK property operations.\n");
    }
}
```



如果驅動程式支援大量作業，下一步是建立 [**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md) 的實例，並指定對應到應用程式將抓取之屬性的索引鍵。 如需此程式的說明，請參閱「 [取得單一物件的屬性](retrieving-properties-for-a-single-object.md) 」主題。

指定適當的索引鍵之後，範例應用程式會建立 [**IPortableDevicePropertiesBulkCallback 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)的實例。 應用程式將會使用此介面中的方法來追蹤非同步大量抓取作業的進度。


```C++
if (SUCCEEDED(hr))
{
    pCallback = new CGetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CGetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



範例應用程式呼叫的下一個函式是 CreateIPortableDevicePropVariantCollectionWithAllObjectIDs helper 函數。 此函式會建立所有可用物件識別碼的清單，例如用途。  (真實世界的應用程式，會將識別碼清單限制為一組特定物件。 例如，應用程式可能會針對目前在指定資料夾檢視中的所有物件建立識別碼清單。 ) 

如上面所述，helper 函式會以遞迴方式列舉指定裝置上的所有物件。 它會在 [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) 中傳回此清單，其中包含找到之每個物件的識別碼。 Helper 函數是在模組 ContentEnumeration 中定義。


```C++
// 7) Call our helper function CreateIPortableDevicePropVariantCollectionWithAllObjectIDs
// to enumerate and create an IPortableDevicePropVariantCollection with the object
// identifiers needed to perform the bulk operation on.
if (SUCCEEDED(hr))
{
    hr = CreateIPortableDevicePropVariantCollectionWithAllObjectIDs(pDevice,
                                                                    pContent,
                                                                    &pObjectIDs);
}
```



完成上述步驟之後，範例應用程式就會起始非同步屬性抓取。 做法是執行下列動作：

1.  呼叫 IPortableDevicePropertiesBulk：： QueueGetValuesByObjectList，以佇列大量屬性抓取的要求。  (請注意，雖然要求已排入佇列，但不會啟動。 ) 
2.  呼叫 IPortableDevicePropertiesBulk：： Start 以起始已排入佇列的要求。

這些步驟會在範例應用程式的下列程式碼摘錄中示範。


```C++
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueGetValuesByObjectList(pObjectIDs,
                                                        pPropertiesToRead,
                                                        pCallback,
                                                        &guidContext);


       if(SUCCEEDED(hr))
       {
           // Cleanup any previously created global event handles.
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               CloseHandle(g_hBulkPropertyOperationEvent);
               g_hBulkPropertyOperationEvent = NULL;
           }

           // In order to create a simpler to follow example we create and wait infinitly
           // for the bulk property operation to complete and ignore any errors.
           // Production code should be written in a more robust manner.
           // Create the global event handle to wait on for the bulk operation
           // to complete.
           g_hBulkPropertyOperationEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               // Call Start() to actually being the Asynchronous bulk operation.
               hr = pPropertiesBulk->Start(guidContext);
               if(FAILED(hr))
               {
                   printf("! Failed to start property operation, hr = 0x%lx\n", hr);
               }
           }
           else
           {
               printf("! Failed to create the global event handle to wait on for the bulk operation. Aborting operation.\n");
           }
       }
       else
       {
           printf("! QueueGetValuesByObjectList Failed, hr = 0x%lx\n", hr);
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

 

 



