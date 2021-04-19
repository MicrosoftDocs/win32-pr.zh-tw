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
# <a name="deleting-content-from-the-device"></a><span data-ttu-id="d1d08-103">正在從裝置刪除內容</span><span class="sxs-lookup"><span data-stu-id="d1d08-103">Deleting Content from the Device</span></span>

<span data-ttu-id="d1d08-104">WPD 應用程式所完成的另一項常見作業是從裝置上的位置刪除內容。</span><span class="sxs-lookup"><span data-stu-id="d1d08-104">Another common operation accomplished by a WPD application is the deletion of content from a location on the device.</span></span>

<span data-ttu-id="d1d08-105">您可以使用下表所述的介面來完成內容刪除作業。</span><span class="sxs-lookup"><span data-stu-id="d1d08-105">Content deletion operations are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="d1d08-106">介面</span><span class="sxs-lookup"><span data-stu-id="d1d08-106">Interface</span></span>                                                                                      | <span data-ttu-id="d1d08-107">描述</span><span class="sxs-lookup"><span data-stu-id="d1d08-107">Description</span></span>                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="d1d08-108">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="d1d08-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="d1d08-109">提供內容刪除方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="d1d08-109">Provides access to the content deletion methods.</span></span> |
| [<span data-ttu-id="d1d08-110">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="d1d08-110">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="d1d08-111">提供屬性特定方法的存取。</span><span class="sxs-lookup"><span data-stu-id="d1d08-111">Provides access to property-specific methods.</span></span>    |



 

<span data-ttu-id="d1d08-112">範例應用程式 ContentTransfer .cpp 模組中的 DeleteContentFromDevice 函式會示範應用程式如何刪除裝置上的內容。</span><span class="sxs-lookup"><span data-stu-id="d1d08-112">The DeleteContentFromDevice function in the sample application's ContentTransfer.cpp module demonstrates how an application could delete content on the device.</span></span> <span data-ttu-id="d1d08-113">內容刪除作業與內容傳輸作業非常類似。</span><span class="sxs-lookup"><span data-stu-id="d1d08-113">Content deletion operations are very similar to content-transfer operations.</span></span> <span data-ttu-id="d1d08-114">其中一個差異是在刪除期間，應用程式會呼叫 [**IPortableDeviceContent：:D elete**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-delete) ，而不是 [**IPortableDeviceContent：： Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move)。</span><span class="sxs-lookup"><span data-stu-id="d1d08-114">The one difference is that during a deletion, the application calls [**IPortableDeviceContent::Delete**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-delete) rather than [**IPortableDeviceContent::Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move).</span></span> <span data-ttu-id="d1d08-115"> (參閱 [裝置上的移動內容](moving-content-on-the-device.md) 主題，以取得在呼叫 Delete 方法時所需的工作描述。 ) </span><span class="sxs-lookup"><span data-stu-id="d1d08-115">(See the [Moving Content on the Device](moving-content-on-the-device.md) topic for a description of the tasks leading up to calling the Delete method.)</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d1d08-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="d1d08-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1d08-117">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="d1d08-117">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="d1d08-118">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="d1d08-118">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="d1d08-119">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="d1d08-119">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="d1d08-120">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="d1d08-120">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



