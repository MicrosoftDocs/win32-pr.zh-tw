---
description: 設定多個物件的屬性
ms.assetid: 0686ba54-4782-42a4-8fdb-2325fc8d8bc2
title: 設定多個物件的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14517e26843265d8273785657e98b691c155821c10f57b92d53e374c20d34ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842680"
---
# <a name="setting-properties-for-multiple-objects"></a>設定多個物件的屬性

有些設備磁碟機支援在單一函式呼叫中設定多個物件的屬性，這稱為「大量寫入」。 您的應用程式可以使用下表所述的介面來執行大量寫入。



| 介面                                                                                      | 描述                                                  |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | 提供內容特定方法的存取權。             |
| [**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | 提供屬性特定方法的存取。            |
| [**IPortableDevicePropertiesBulk 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | 支援大量寫入作業。                           |
| [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) | 用來儲存大量作業的物件識別碼。 |
| [**IPortableDeviceValuesCollection 介面**](iportabledevicevaluescollection.md)           | 用來識別要寫入的屬性。               |



 

`WriteContentPropertiesBulk`範例應用程式的 ContentProperties .cpp 模組中的函式會示範大量寫入操作。

在此範例中完成的第一項工作，是判斷指定的驅動程式是否支援大量作業。 這是藉由呼叫 **IPortableDeviceProperties** 物件上的 QueryInterface 並檢查 **IPortableDevicePropertiesBulk** 是否存在而完成。


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
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



下一項工作牽涉到建立 **IPortableDeviceValuesCollection** 物件。 這是包含範例將會寫入之屬性值的物件。


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDeviceValuesCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDeviceValuesCollection,
                          (VOID**) &pPropertiesToWrite);
    if (FAILED(hr))
    {
        printf("! Failed to CoCreate IPortableDeviceValuesCollection for bulk property values, hr = 0x%lx\n", hr);
    }
}
```



之後，此範例會建立 [**IPortableDevicePropertiesBulkCallback 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)的實例。 應用程式將會使用此介面中的方法來追蹤非同步大量寫入作業的進度。


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    pCallback = new CSetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CSetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



範例應用程式呼叫的下一個函式是 `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` helper 函數。 此函式會以遞迴方式列舉指定裝置上的所有物件，並傳回 [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) ，其中包含找到之每個物件的識別碼。 此函式定義于模組 ContentEnumeration 中。


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



**IPortableDevicePropVariantCollection** 物件會保存相同 VARTYPE 之索引 **PROPVARIANT** 值的集合。 在此情況下，這些值會包含在裝置上找到之每個物件的指定物件識別碼。

物件識別碼和其各自的名稱屬性會儲存在 [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) 物件中。 名稱屬性的組織方式是將 "NewName0" 的 name 屬性指派給第一個物件，第二個物件的名稱屬性為 "NewName1"，依此類推。

下列範例摘錄將示範如何使用物件識別碼和新名稱字串初始化 **IPortableDeviceValuesCollection** 物件。


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = pObjectIDs->GetCount(&cObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of objectIDs from IPortableDevicePropVariantCollection, hr = 0x%lx\n", hr);
    }
}


if (SUCCEEDED(hr))
{
    for(DWORD dwIndex = 0; (dwIndex < cObjectIDs) && (hr == S_OK); dwIndex++)
    {
        CComPtr<IPortableDeviceValues>  pValues;
        PROPVARIANT                     pv = {0};

        PropVariantInit(&pv);
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pValues);
        if (FAILED(hr))
        {
            printf("! Failed to CoCreate CLSID_PortableDeviceValues, hr = 0x%lx\n", hr);
        }

        // Get the Object ID whose properties we will set
        if (hr == S_OK)
        {
            hr = pObjectIDs->GetAt(dwIndex, &pv);
            if (FAILED(hr))
            {
                printf("! Failed to get next Object ID from list, hr = 0x%lx\n", hr);
            }
        }

        // Save them into the IPortableDeviceValues so the driver knows which object this proeprty set belongs to
        if (hr == S_OK)
        {
            hr = pValues->SetStringValue(WPD_OBJECT_ID, pv.pwszVal);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID, hr = 0x%lx\n", hr);
            }
        }

        // Set the new values.  In this sample, we attempt to set the name property.
        if (hr == S_OK)
        {
            CAtlStringW strValue;
            strValue.Format(L"NewName%d", dwIndex);

            hr = pValues->SetStringValue(WPD_OBJECT_NAME, strValue.GetString());
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_NAME, hr = 0x%lx\n", hr);
            }
        }

        // Add this property set to the collection
        if (hr == S_OK)
        {
            hr = pPropertiesToWrite->Add(pValues);
            if (FAILED(hr))
            {
                printf("! Failed to add values to collection, hr = 0x%lx\n", hr);
            }
        }
        PropVariantClear(&pv);
    }
}
```



一旦範例建立包含物件識別碼和名稱組的 **IPortableDeviceValuesCollection** 物件之後，就可以開始非同步作業。

當範例呼叫 [**IPortableDevicePropertiesBulk：： QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) 方法時，就會開始非同步寫入作業。 這個方法會通知驅動程式，大量作業即將開始。 之後，此範例會呼叫 [**IPortableDeviceBulk：： Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) 方法來開始實際寫入新的名稱值。


```C++
   HRESULT                                       hr                = S_OK;
   GUID                                          guidContext       = GUID_NULL;
   CSetBulkValuesCallback*                       pCallback         = NULL;
   CComPtr<IPortableDeviceProperties>            pProperties;
   CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
   CComPtr<IPortableDeviceValues>                pObjectProperties;
   CComPtr<IPortableDeviceContent>               pContent;
   CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
   CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
   DWORD                                         cObjectIDs        = 0;
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueSetValuesByObjectList(pPropertiesToWrite,
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
           printf("! QueueSetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



請注意，此範例會等待無限長的一段時間，讓作業完成。 如果這是實際執行的應用程式，則必須修改程式碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**IPortableDevicePropertiesBulk 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



