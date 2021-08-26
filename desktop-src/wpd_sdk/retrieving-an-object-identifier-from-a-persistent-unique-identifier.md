---
description: 從持續性唯一識別碼中取出物件識別碼
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: 從持續性的唯一識別碼中取出物件識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d4f08d496c7c03101602c945e6c27e7a2624fe84957eda932ead806f964d3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054768"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a>從持續性的唯一識別碼中取出物件識別碼

針對指定的裝置會話，物件識別碼只保證是唯一的;如果使用者建立新的連接，則先前會話的識別碼可能不符合目前會話的識別碼。 為了解決此問題，WPD API 支援持續性的唯一識別碼 (Puid) ，其會跨裝置會話保存。

有些裝置會以原生方式儲存其 Puid 和指定的物件。 其他可能會根據所選物件資料的雜湊來產生 PUID。 其他人可能會將物件識別碼視為 Puid (，因為它們可以保證這些識別碼永遠不會變更) 。

ContentProperties .cpp 模組中的 GetObjectIdentifierFromPersistentUniqueIdentifier 函式會示範如何抓取給定 PUID 的物件識別碼。

您的應用程式可以使用下表所述的介面，來取得對應 PUID 的物件識別碼。



| 介面                                                                                      | 描述                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | 提供抓取方法的存取權。                                                            |
| [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) | 用來將物件識別碼和對應的持續性唯一識別碼儲存 (PUID) 。 |



 

範例應用程式完成的第一項工作是從使用者取得 PUID。


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



在此之後，範例應用程式會抓取 [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) 物件，它會用來叫用 [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) 方法。


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



接下來，它會建立 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) 物件，以保存使用者提供的 PUID。


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



一旦採取上述三個步驟，範例就可以開始抓取符合使用者提供之 PUID 的物件識別碼。 這是藉由呼叫 [**IPortableDeviceContent：： GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) 方法來完成。 在呼叫這個方法之前，範例會初始化 PROPVARIANT 結構、將使用者提供的 PUID 寫入此結構，並將它加入至 pPersistentUniqueIDs 點的 IPortableDevicePropVariantCollection 物件。 這個指標會以第一個引數的形式傳遞至 GetObjectIDsFromPersistentUniqueIDs 方法。 GetObjectIDsFromPersistentUniqueIDs 的第二個引數是 IPortableDevicePropVariantCollection 物件，該物件會接收相符的物件識別碼。


```C++
if (SUCCEEDED(hr))
{
    if (pPersistentUniqueIDs != NULL)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);

        // Initialize a PROPVARIANT structure with the object identifier string
        // that the user selected above. Notice we are allocating memory for the
        // PWSTR value.  This memory will be freed when PropVariantClear() is
        // called below.
        pv.vt      = VT_LPWSTR;
        pv.pwszVal = AtlAllocTaskWideString(szSelection);
        if (pv.pwszVal != NULL)
        {
            // Add the object identifier to the objects-to-delete list
            // (We are only deleting 1 in this example)
            hr = pPersistentUniqueIDs->Add(&pv);
            if (SUCCEEDED(hr))
            {
                // 3) Attempt to get the unique idenifier for the object from the device
                hr = pContent->GetObjectIDsFromPersistentUniqueIDs(pPersistentUniqueIDs,
                                                                   &pObjectIDs);
                if (SUCCEEDED(hr))
                {
                    PROPVARIANT pvId = {0};
                    hr = pObjectIDs->GetAt(0, &pvId);
                    if (SUCCEEDED(hr))
                    {
                        printf("The persistent unique identifier '%ws' relates to object identifier '%ws' on the device.\n", szSelection, pvId.pwszVal);
                    }
                    else
                    {
                        printf("! Failed to get the object identifier for '%ws' from the IPortableDevicePropVariantCollection, hr = 0x%lx\n",szSelection, hr);
                    }

                    // Free the returned allocated string from the GetAt() call
                    PropVariantClear(&pvId);
                }
                else
                {
                    printf("! Failed to get the object identifier from persistent object idenifier '%ws', hr = 0x%lx\n",szSelection, hr);
                }
            }
            else
            {
                printf("! Failed to get the object identifier from persistent object idenifier because we could no add the persistent object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
            printf("! Failed to get the object identifier because we could no allocate memory for the persistent object identifier string, hr = 0x%lx\n",hr);
        }

        // Free any allocated values in the PROPVARIANT before exiting
        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDevice 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



