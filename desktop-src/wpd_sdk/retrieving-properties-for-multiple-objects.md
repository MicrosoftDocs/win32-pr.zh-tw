---
description: 正在抓取多個物件的屬性
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: 正在抓取多個物件的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c069f6a28b923339f66f8423f211eff4704ef6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980637"
---
# <a name="retrieving-properties-for-multiple-objects"></a><span data-ttu-id="45222-103">正在抓取多個物件的屬性</span><span class="sxs-lookup"><span data-stu-id="45222-103">Retrieving Properties for Multiple Objects</span></span>

<span data-ttu-id="45222-104">某些設備磁碟機支援在單一函式呼叫中抓取多個物件的屬性;這稱為「大量抓取」。</span><span class="sxs-lookup"><span data-stu-id="45222-104">Some device drivers support the retrieval of properties for multiple objects in a single function call; this is referred to as a bulk retrieval.</span></span> <span data-ttu-id="45222-105">大量抓取作業有兩種類型：第一個型別會抓取物件清單的屬性，而第二個型別則會抓取特定格式之所有物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="45222-105">There are two types of bulk retrieval operations: the first type retrieves properties for a list of objects, and the second type retrieves properties for all objects of a given format.</span></span> <span data-ttu-id="45222-106">本節所述的範例會示範前者。</span><span class="sxs-lookup"><span data-stu-id="45222-106">The example described in this section demonstrates the former.</span></span>

<span data-ttu-id="45222-107">您的應用程式可以使用下表所述的介面來執行大量抓取。</span><span class="sxs-lookup"><span data-stu-id="45222-107">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="45222-108">介面</span><span class="sxs-lookup"><span data-stu-id="45222-108">Interface</span></span>                                                                                      | <span data-ttu-id="45222-109">描述</span><span class="sxs-lookup"><span data-stu-id="45222-109">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="45222-110">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="45222-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="45222-111">提供內容特定方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="45222-111">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="45222-112">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="45222-112">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="45222-113">用來識別要取出的屬性。</span><span class="sxs-lookup"><span data-stu-id="45222-113">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="45222-114">**IPortableDeviceProperties 介面**</span><span class="sxs-lookup"><span data-stu-id="45222-114">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="45222-115">用來判斷指定的驅動程式是否支援大量作業。</span><span class="sxs-lookup"><span data-stu-id="45222-115">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="45222-116">**IPortableDevicePropertiesBulk 介面**</span><span class="sxs-lookup"><span data-stu-id="45222-116">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="45222-117">支援大量抓取作業。</span><span class="sxs-lookup"><span data-stu-id="45222-117">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="45222-118">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="45222-118">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="45222-119">用來儲存大量作業的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="45222-119">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="45222-120">範例應用程式 ContentProperties .cpp 模組中的 ReadContentPropertiesBulk 函式會示範大量抓取作業。</span><span class="sxs-lookup"><span data-stu-id="45222-120">The ReadContentPropertiesBulk function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation.</span></span>

<span data-ttu-id="45222-121">在此範例中完成的第一項工作，是判斷指定的驅動程式是否支援大量作業。</span><span class="sxs-lookup"><span data-stu-id="45222-121">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="45222-122">這是藉由呼叫 IPortableDeviceProperties 介面上的 QueryInterface 並檢查 IPortableDevicePropertiesBulk 是否存在而完成。</span><span class="sxs-lookup"><span data-stu-id="45222-122">This is accomplished by calling QueryInterface on the IPortableDeviceProperties interface and checking for the existence of IPortableDevicePropertiesBulk.</span></span>


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



<span data-ttu-id="45222-123">如果驅動程式支援大量作業，下一步是建立 [**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md) 的實例，並指定對應到應用程式將抓取之屬性的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="45222-123">If the driver supports bulk operations, the next step is to create an instance of the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and to specify the keys that correspond to the properties that the application will retrieve.</span></span> <span data-ttu-id="45222-124">如需此程式的說明，請參閱「 [取得單一物件的屬性](retrieving-properties-for-a-single-object.md) 」主題。</span><span class="sxs-lookup"><span data-stu-id="45222-124">For a description of this process, see the [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md) topic.</span></span>

<span data-ttu-id="45222-125">指定適當的索引鍵之後，範例應用程式會建立 [**IPortableDevicePropertiesBulkCallback 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)的實例。</span><span class="sxs-lookup"><span data-stu-id="45222-125">After the appropriate keys are specified, the sample application creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="45222-126">應用程式將會使用此介面中的方法來追蹤非同步大量抓取作業的進度。</span><span class="sxs-lookup"><span data-stu-id="45222-126">The application will use the methods in this interface to track the progress of the asynchronous bulk-retrieval operation.</span></span>


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



<span data-ttu-id="45222-127">範例應用程式呼叫的下一個函式是 CreateIPortableDevicePropVariantCollectionWithAllObjectIDs helper 函數。</span><span class="sxs-lookup"><span data-stu-id="45222-127">The next function that the sample application calls is the CreateIPortableDevicePropVariantCollectionWithAllObjectIDs helper function.</span></span> <span data-ttu-id="45222-128">此函式會建立所有可用物件識別碼的清單，例如用途。</span><span class="sxs-lookup"><span data-stu-id="45222-128">This function creates a list of all available object identifiers for example purposes.</span></span> <span data-ttu-id="45222-129"> (真實世界的應用程式，會將識別碼清單限制為一組特定物件。</span><span class="sxs-lookup"><span data-stu-id="45222-129">(A real-world application would limit the list of identifiers to a particular set of objects.</span></span> <span data-ttu-id="45222-130">例如，應用程式可能會針對目前在指定資料夾檢視中的所有物件建立識別碼清單。 ) </span><span class="sxs-lookup"><span data-stu-id="45222-130">For instance, an application may create a list of identifiers for all of the objects currently in a given folder view.)</span></span>

<span data-ttu-id="45222-131">如上面所述，helper 函式會以遞迴方式列舉指定裝置上的所有物件。</span><span class="sxs-lookup"><span data-stu-id="45222-131">As noted above, the helper function recursively enumerates all objects on a given device.</span></span> <span data-ttu-id="45222-132">它會在 [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) 中傳回此清單，其中包含找到之每個物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="45222-132">It returns this list in an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="45222-133">Helper 函數是在模組 ContentEnumeration 中定義。</span><span class="sxs-lookup"><span data-stu-id="45222-133">The helper function is defined in the module ContentEnumeration.cpp.</span></span>


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



<span data-ttu-id="45222-134">完成上述步驟之後，範例應用程式就會起始非同步屬性抓取。</span><span class="sxs-lookup"><span data-stu-id="45222-134">Once the previous steps are accomplished, the sample application initiates the asynchronous property retrieval.</span></span> <span data-ttu-id="45222-135">做法是執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="45222-135">This is accomplished by doing the following:</span></span>

1.  <span data-ttu-id="45222-136">呼叫 IPortableDevicePropertiesBulk：： QueueGetValuesByObjectList，以佇列大量屬性抓取的要求。</span><span class="sxs-lookup"><span data-stu-id="45222-136">Calling IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, which queues a request for the bulk property retrieval.</span></span> <span data-ttu-id="45222-137"> (請注意，雖然要求已排入佇列，但不會啟動。 ) </span><span class="sxs-lookup"><span data-stu-id="45222-137">(Note that although the request is queued, it is not started.)</span></span>
2.  <span data-ttu-id="45222-138">呼叫 IPortableDevicePropertiesBulk：： Start 以起始已排入佇列的要求。</span><span class="sxs-lookup"><span data-stu-id="45222-138">Calling IPortableDevicePropertiesBulk::Start to initiate the queued request.</span></span>

<span data-ttu-id="45222-139">這些步驟會在範例應用程式的下列程式碼摘錄中示範。</span><span class="sxs-lookup"><span data-stu-id="45222-139">These steps are demonstrated in the following code excerpt from the sample application.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="45222-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="45222-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45222-141">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="45222-141">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="45222-142">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="45222-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="45222-143">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="45222-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="45222-144">**IPortableDeviceProperties 介面**</span><span class="sxs-lookup"><span data-stu-id="45222-144">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="45222-145">**IPortableDevicePropertiesBulk 介面**</span><span class="sxs-lookup"><span data-stu-id="45222-145">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="45222-146">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="45222-146">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="45222-147">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="45222-147">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



