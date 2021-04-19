---
description: 移動裝置上的內容
ms.assetid: 5072d308-d376-4141-96df-dbef23fb9f9b
title: 移動裝置上的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb4a9638e656d5cab8437448d64b79947df337b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990304"
---
# <a name="moving-content-on-the-device"></a><span data-ttu-id="55dbb-103">移動裝置上的內容</span><span class="sxs-lookup"><span data-stu-id="55dbb-103">Moving Content on the Device</span></span>

<span data-ttu-id="55dbb-104">WPD 應用程式所完成的另一項常見的作業，是將內容從裝置上的一個位置傳送到另一個位置。</span><span class="sxs-lookup"><span data-stu-id="55dbb-104">Another common operation accomplished by a WPD application is the transfer of content from one location on the device to another.</span></span>

<span data-ttu-id="55dbb-105">您可以使用下表所述的介面來完成內容移動作業。</span><span class="sxs-lookup"><span data-stu-id="55dbb-105">Content move operations are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="55dbb-106">介面</span><span class="sxs-lookup"><span data-stu-id="55dbb-106">Interface</span></span>                                                                                      | <span data-ttu-id="55dbb-107">描述</span><span class="sxs-lookup"><span data-stu-id="55dbb-107">Description</span></span>                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="55dbb-108">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="55dbb-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="55dbb-109">提供內容特定方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="55dbb-109">Provides access to the content-specific methods.</span></span>  |
| [<span data-ttu-id="55dbb-110">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="55dbb-110">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="55dbb-111">提供屬性特定方法的存取。</span><span class="sxs-lookup"><span data-stu-id="55dbb-111">Provides access to the property-specific methods.</span></span> |



 

<span data-ttu-id="55dbb-112">範例應用程式的 ContentTransfer 中的 MoveContentAlreadyOnDevice 函式會示範應用程式如何將內容從某個位置移到另一個位置。</span><span class="sxs-lookup"><span data-stu-id="55dbb-112">The MoveContentAlreadyOnDevice function in the sample application's ContentTransfer.cpp module demonstrates how an application can move content from one location to another.</span></span>

<span data-ttu-id="55dbb-113">MoveContentAlreadyOnDevice 函式所完成的第一項工作是查詢設備磁碟機，以查看它是否支援內容移動。</span><span class="sxs-lookup"><span data-stu-id="55dbb-113">The first task accomplished by the MoveContentAlreadyOnDevice function is to query the device driver to see whether it supports content movement.</span></span> <span data-ttu-id="55dbb-114">這是藉由呼叫 SupportsCommand helper 函式，並傳遞 WPD \_ 命令 \_ 物件 \_ 管理 \_ 移動 \_ 物件做為第二個引數來完成。</span><span class="sxs-lookup"><span data-stu-id="55dbb-114">This is accomplished by calling the SupportsCommand helper function and passing WPD\_COMMAND\_OBJECT\_MANAGEMENT\_MOVE\_OBJECTS as the second argument.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SupportsCommand(pDevice, WPD_COMMAND_OBJECT_MANAGEMENT_MOVE_OBJECTS) == FALSE)
{
    printf("! This device does not support the move operation (i.e. The WPD_COMMAND_OBJECT_MANAGEMENT_MOVE_OBJECTS command)\n");
    return;
}
```



<span data-ttu-id="55dbb-115">下一個步驟需要提示使用者輸入兩個物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="55dbb-115">The next step entails prompting the user to enter two object identifiers.</span></span> <span data-ttu-id="55dbb-116">第一個是要移動之內容的識別碼。</span><span class="sxs-lookup"><span data-stu-id="55dbb-116">The first is the identifier for the content that will be moved.</span></span> <span data-ttu-id="55dbb-117">第二個是應用程式應該將此內容移至哪個位置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="55dbb-117">The second is the identifier for the location to which the application should move this content.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
printf("Enter the identifer of the object you wish to move.\n>");
hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content moving\n");
}

// Prompt user to enter an object identifier on the device to move.
printf("Enter the identifer of the object you wish to move '%ws' to.\n>", wszSelection);
hr = StringCbGetsW(wszDestinationFolderObjectID,sizeof(wszDestinationFolderObjectID));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content moving\n");
}
```



<span data-ttu-id="55dbb-118">接下來，此範例會抓取用來存取 [**IPortableDeviceContent：： Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move)方法的 [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)物件。</span><span class="sxs-lookup"><span data-stu-id="55dbb-118">Next, the sample retrieves an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object that is used to access the [**IPortableDeviceContent::Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move) method.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="55dbb-119">最後，會移動內容。</span><span class="sxs-lookup"><span data-stu-id="55dbb-119">Finally, the content is moved.</span></span> <span data-ttu-id="55dbb-120">此套裝程式含下列各項：</span><span class="sxs-lookup"><span data-stu-id="55dbb-120">This process involves the following:</span></span>

1.  <span data-ttu-id="55dbb-121">建立 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) 物件，以接收要移動之物件的 PROPVARIANT 結構。</span><span class="sxs-lookup"><span data-stu-id="55dbb-121">Creating an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that receives a PROPVARIANT structure for the object to be moved.</span></span>
2.  <span data-ttu-id="55dbb-122">將 PROPVARIANT 加入至 IPortableDevicePropVariantCollection 物件。</span><span class="sxs-lookup"><span data-stu-id="55dbb-122">Adding the PROPVARIANT to the IPortableDevicePropVariantCollection object.</span></span>
3.  <span data-ttu-id="55dbb-123">叫用 IPortableDeviceContent：： Move 方法。</span><span class="sxs-lookup"><span data-stu-id="55dbb-123">Invoking the IPortableDeviceContent::Move method.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDevicePropVariantCollection,
                          (VOID**) &pObjectsToMove);
    if (SUCCEEDED(hr))
    {
        if (pObjectsToMove != NULL)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);

            // Initialize a PROPVARIANT structure with the object identifier string
            // that the user selected above. Notice we are allocating memory for the
            // LPWSTR value.  This memory will be freed when PropVariantClear() is
            // called below.
            pv.vt      = VT_LPWSTR;
            pv.pwszVal = AtlAllocTaskWideString(wszSelection);
            if (pv.pwszVal != NULL)
            {
                // Add the object identifier to the objects-to-move list
                // (We are only moving 1 in this example)
                hr = pObjectsToMove->Add(&pv);
                if (SUCCEEDED(hr))
                {
                    // Attempt to move the object on the device
                    hr = pContent->Move(pObjectsToMove,               // Object(s) to move
                                        wszDestinationFolderObjectID, // Folder to move to
                                        NULL);                        // Object(s) that failed to delete (we are only moving 1, so we can pass NULL here)
                    if (SUCCEEDED(hr))
                    {
                        // An S_OK return lets the caller know that the deletion was successful
                        if (hr == S_OK)
                        {
                            printf("The object '%ws' was moved on the device.\n", wszSelection);
                        }

                        // An S_FALSE return lets the caller know that the move failed.
                        // The caller should check the returned IPortableDevicePropVariantCollection
                        // for a list of object identifiers that failed to be moved.
                        else
                        {
                            printf("The object '%ws' failed to be moved on the device.\n", wszSelection);
                        }
                    }
                    else
                    {
                        printf("! Failed to move an object on the device, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    printf("! Failed to move an object on the device because we could no add the object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
                printf("! Failed to move an object on the device because we could no allocate memory for the object identifier string, hr = 0x%lx\n",hr);
            }

            // Free any allocated values in the PROPVARIANT before exiting
            PropVariantClear(&pv);
        }
        else
        {
            printf("! Failed to move an object from the device because we were returned a NULL IPortableDevicePropVariantCollection interface pointer, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to CoCreateInstance CLSID_PortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="55dbb-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="55dbb-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55dbb-125">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="55dbb-125">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="55dbb-126">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="55dbb-126">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="55dbb-127">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="55dbb-127">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="55dbb-128">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="55dbb-128">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



