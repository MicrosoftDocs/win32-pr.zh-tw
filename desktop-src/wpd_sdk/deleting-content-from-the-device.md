---
description: 正在從裝置刪除內容
ms.assetid: 195f68d5-f139-456e-b000-86c91732a292
title: 正在從裝置刪除內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c7b8d266517933caaf770236e96110a3ef334c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966705"
---
# <a name="deleting-content-from-the-device"></a>正在從裝置刪除內容

WPD 應用程式所完成的另一項常見作業是從裝置上的位置刪除內容。

您可以使用下表所述的介面來完成內容刪除作業。



| 介面                                                                                      | 描述                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [**IPortableDeviceContent 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | 提供內容刪除方法的存取權。 |
| [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) | 提供屬性特定方法的存取。    |



 

範例應用程式 ContentTransfer .cpp 模組中的 DeleteContentFromDevice 函式會示範應用程式如何刪除裝置上的內容。 內容刪除作業與內容傳輸作業非常類似。 其中一個差異是在刪除期間，應用程式會呼叫 [**IPortableDeviceContent：:D elete**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-delete) ，而不是 [**IPortableDeviceContent：： Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move)。  (參閱 [裝置上的移動內容](moving-content-on-the-device.md) 主題，以取得在呼叫 Delete 方法時所需的工作描述。 ) 


```C++
void DeleteContentFromDevice(
    IPortableDevice* pDevice)
{
    HRESULT                                       hr               = S_OK;
    WCHAR                                         szSelection[81]  = {0};
    CComPtr<IPortableDeviceContent>               pContent;
    CComPtr<IPortableDevicePropVariantCollection> pObjectsToDelete;
    CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToDelete;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Prompt user to enter an object identifier on the device to delete.
    printf("Enter the identifer of the object you wish to delete.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
    if (FAILED(hr))
    {
        printf("An invalid object identifier was specified, aborting content deletion\n");
    }

    // 1) get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pDevice->Content(&pContent);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
        }
    }

    // 2) CoCreate an IPortableDevicePropVariantCollection interface to hold the object identifiers
    // to delete.
    //
    // NOTE: This is a collection interface so more than 1 object can be deleted at a time.
    //       This sample only deletes a single object.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pObjectsToDelete));
        if (SUCCEEDED(hr))
        {
            if (pObjectsToDelete != NULL)
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
                    hr = pObjectsToDelete->Add(&pv);
                    if (SUCCEEDED(hr))
                    {
                        // Attempt to delete the object from the device
                        hr = pContent->Delete(PORTABLE_DEVICE_DELETE_NO_RECURSION,  // Deleting with no recursion
                                              pObjectsToDelete,                     // Object(s) to delete
                                              NULL);                                // Object(s) that failed to delete (we are only deleting 1, so we can pass NULL here)
                        if (SUCCEEDED(hr))
                        {
                            // An S_OK return lets the caller know that the deletion was successful
                            if (hr == S_OK)
                            {
                                printf("The object '%ws' was deleted from the device.\n", szSelection);
                            }

                            // An S_FALSE return lets the caller know that the deletion failed.
                            // The caller should check the returned IPortableDevicePropVariantCollection
                            // for a list of object identifiers that failed to be deleted.
                            else
                            {
                                printf("The object '%ws' failed to be deleted from the device.\n", szSelection);
                            }
                        }
                        else
                        {
                            printf("! Failed to delete an object from the device, hr = 0x%lx\n",hr);
                        }
                    }
                    else
                    {
                        printf("! Failed to delete an object from the device because we could no add the object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    hr = E_OUTOFMEMORY;
                    printf("! Failed to delete an object from the device because we could no allocate memory for the object identifier string, hr = 0x%lx\n",hr);
                }

                // Free any allocated values in the PROPVARIANT before exiting
                PropVariantClear(&pv);
            }
            else
            {
                printf("! Failed to delete an object from the device because we were returned a NULL IPortableDevicePropVariantCollection interface pointer, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            printf("! Failed to CoCreateInstance CLSID_PortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
        }
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

 

 



