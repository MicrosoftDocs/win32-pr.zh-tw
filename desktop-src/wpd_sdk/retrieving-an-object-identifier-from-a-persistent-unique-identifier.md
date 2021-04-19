---
description: 從持續性唯一識別碼中取出物件識別碼
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: 從持續性的唯一識別碼中取出物件識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f997f0faf586a374e5a83c6f96b6508f02eb41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985265"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a><span data-ttu-id="b2f83-103">從持續性的唯一識別碼中取出物件識別碼</span><span class="sxs-lookup"><span data-stu-id="b2f83-103">Retrieving an Object Id from a Persistent Unique Id</span></span>

<span data-ttu-id="b2f83-104">針對指定的裝置會話，物件識別碼只保證是唯一的;如果使用者建立新的連接，則先前會話的識別碼可能不符合目前會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2f83-104">Object identifiers are only guaranteed to be unique for a given device session; if the user establishes a new connection, identifiers from a previous session may not match identifiers for the current session.</span></span> <span data-ttu-id="b2f83-105">為了解決此問題，WPD API 支援持續性的唯一識別碼 (Puid) ，其會跨裝置會話保存。</span><span class="sxs-lookup"><span data-stu-id="b2f83-105">To resolve this issue, the WPD API supports persistent unique identifiers (PUIDs), which persist across device sessions.</span></span>

<span data-ttu-id="b2f83-106">有些裝置會以原生方式儲存其 Puid 和指定的物件。</span><span class="sxs-lookup"><span data-stu-id="b2f83-106">Some devices store their PUIDs natively with a given object.</span></span> <span data-ttu-id="b2f83-107">其他可能會根據所選物件資料的雜湊來產生 PUID。</span><span class="sxs-lookup"><span data-stu-id="b2f83-107">Others may generate the PUID based on a hash of selected object data.</span></span> <span data-ttu-id="b2f83-108">其他人可能會將物件識別碼視為 Puid (，因為它們可以保證這些識別碼永遠不會變更) 。</span><span class="sxs-lookup"><span data-stu-id="b2f83-108">Others may treat object identifiers as PUIDs (because they can guarantee that these identifiers never change).</span></span>

<span data-ttu-id="b2f83-109">ContentProperties .cpp 模組中的 GetObjectIdentifierFromPersistentUniqueIdentifier 函式會示範如何抓取給定 PUID 的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2f83-109">The GetObjectIdentifierFromPersistentUniqueIdentifier function in the ContentProperties.cpp module demonstrates the retrieval of an object identifier for a given PUID.</span></span>

<span data-ttu-id="b2f83-110">您的應用程式可以使用下表所述的介面，來取得對應 PUID 的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2f83-110">Your application can retrieve an object identifier for a corresponding PUID using the interfaces described in the following table.</span></span>



| <span data-ttu-id="b2f83-111">介面</span><span class="sxs-lookup"><span data-stu-id="b2f83-111">Interface</span></span>                                                                                      | <span data-ttu-id="b2f83-112">描述</span><span class="sxs-lookup"><span data-stu-id="b2f83-112">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2f83-113">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="b2f83-113">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="b2f83-114">提供抓取方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="b2f83-114">Provides access to the retrieval method.</span></span>                                                            |
| [<span data-ttu-id="b2f83-115">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="b2f83-115">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="b2f83-116">用來將物件識別碼和對應的持續性唯一識別碼儲存 (PUID) 。</span><span class="sxs-lookup"><span data-stu-id="b2f83-116">Used to store both the object identifier and the corresponding persistent unique identifier (PUID).</span></span> |



 

<span data-ttu-id="b2f83-117">範例應用程式完成的第一項工作是從使用者取得 PUID。</span><span class="sxs-lookup"><span data-stu-id="b2f83-117">The first task that the sample application accomplishes is to obtain a PUID from the user.</span></span>


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



<span data-ttu-id="b2f83-118">在此之後，範例應用程式會抓取 [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) 物件，它會用來叫用 [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) 方法。</span><span class="sxs-lookup"><span data-stu-id="b2f83-118">After this, the sample application retrieves an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to invoke the [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span>


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



<span data-ttu-id="b2f83-119">接下來，它會建立 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) 物件，以保存使用者提供的 PUID。</span><span class="sxs-lookup"><span data-stu-id="b2f83-119">Next, it creates an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that will hold the PUID supplied by the user.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



<span data-ttu-id="b2f83-120">一旦採取上述三個步驟，範例就可以開始抓取符合使用者提供之 PUID 的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2f83-120">Once the previous three steps are taken, the sample is ready to retrieve the object identifier that matches the PUID supplied by the user.</span></span> <span data-ttu-id="b2f83-121">這是藉由呼叫 [**IPortableDeviceContent：： GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="b2f83-121">This is accomplished by calling the [**IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span> <span data-ttu-id="b2f83-122">在呼叫這個方法之前，範例會初始化 PROPVARIANT 結構、將使用者提供的 PUID 寫入此結構，並將它加入至 pPersistentUniqueIDs 點的 IPortableDevicePropVariantCollection 物件。</span><span class="sxs-lookup"><span data-stu-id="b2f83-122">Prior to calling this method, the sample initializes a PROPVARIANT structure, writes the PUID supplied by the user to this structure, and adds it to the IPortableDevicePropVariantCollection object at which pPersistentUniqueIDs points.</span></span> <span data-ttu-id="b2f83-123">這個指標會以第一個引數的形式傳遞至 GetObjectIDsFromPersistentUniqueIDs 方法。</span><span class="sxs-lookup"><span data-stu-id="b2f83-123">This pointer is passed as the first argument to the GetObjectIDsFromPersistentUniqueIDs method.</span></span> <span data-ttu-id="b2f83-124">GetObjectIDsFromPersistentUniqueIDs 的第二個引數是 IPortableDevicePropVariantCollection 物件，該物件會接收相符的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2f83-124">The second argument of GetObjectIDsFromPersistentUniqueIDs is an IPortableDevicePropVariantCollection object that receives the matching object identifier.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b2f83-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2f83-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2f83-126">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="b2f83-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="b2f83-127">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="b2f83-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="b2f83-128">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="b2f83-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="b2f83-129">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="b2f83-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



