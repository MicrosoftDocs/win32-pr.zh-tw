---
description: 設定多個物件的屬性
ms.assetid: 0686ba54-4782-42a4-8fdb-2325fc8d8bc2
title: 設定多個物件的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e951662d9920cb22db0a417f1af94f3eb7eb4d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985040"
---
# <a name="setting-properties-for-multiple-objects"></a><span data-ttu-id="6f5da-103">設定多個物件的屬性</span><span class="sxs-lookup"><span data-stu-id="6f5da-103">Setting Properties for Multiple Objects</span></span>

<span data-ttu-id="6f5da-104">有些設備磁碟機支援在單一函式呼叫中設定多個物件的屬性，這稱為「大量寫入」。</span><span class="sxs-lookup"><span data-stu-id="6f5da-104">Some device drivers support setting properties for multiple objects in a single function call—this is referred to as a bulk write.</span></span> <span data-ttu-id="6f5da-105">您的應用程式可以使用下表所述的介面來執行大量寫入。</span><span class="sxs-lookup"><span data-stu-id="6f5da-105">Your application can perform a bulk write using the interfaces described in the following table.</span></span>



| <span data-ttu-id="6f5da-106">介面</span><span class="sxs-lookup"><span data-stu-id="6f5da-106">Interface</span></span>                                                                                      | <span data-ttu-id="6f5da-107">描述</span><span class="sxs-lookup"><span data-stu-id="6f5da-107">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="6f5da-108">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="6f5da-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="6f5da-109">提供內容特定方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="6f5da-109">Provides access to the content-specific methods.</span></span>             |
| [<span data-ttu-id="6f5da-110">**IPortableDeviceProperties 介面**</span><span class="sxs-lookup"><span data-stu-id="6f5da-110">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="6f5da-111">提供屬性特定方法的存取。</span><span class="sxs-lookup"><span data-stu-id="6f5da-111">Provides access to the property-specific methods.</span></span>            |
| [<span data-ttu-id="6f5da-112">**IPortableDevicePropertiesBulk 介面**</span><span class="sxs-lookup"><span data-stu-id="6f5da-112">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="6f5da-113">支援大量寫入作業。</span><span class="sxs-lookup"><span data-stu-id="6f5da-113">Supports the bulk write operation.</span></span>                           |
| [<span data-ttu-id="6f5da-114">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="6f5da-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="6f5da-115">用來儲存大量作業的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f5da-115">Used to store the object identifiers for the bulk operation.</span></span> |
| [<span data-ttu-id="6f5da-116">**IPortableDeviceValuesCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="6f5da-116">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="6f5da-117">用來識別要寫入的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f5da-117">Used to identify the properties to be written.</span></span>               |



 

<span data-ttu-id="6f5da-118">`WriteContentPropertiesBulk`範例應用程式的 ContentProperties .cpp 模組中的函式會示範大量寫入操作。</span><span class="sxs-lookup"><span data-stu-id="6f5da-118">The `WriteContentPropertiesBulk` function in the sample application's ContentProperties.cpp module demonstrates a bulk write operation.</span></span>

<span data-ttu-id="6f5da-119">在此範例中完成的第一項工作，是判斷指定的驅動程式是否支援大量作業。</span><span class="sxs-lookup"><span data-stu-id="6f5da-119">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="6f5da-120">這是藉由呼叫 **IPortableDeviceProperties** 物件上的 QueryInterface 並檢查 **IPortableDevicePropertiesBulk** 是否存在而完成。</span><span class="sxs-lookup"><span data-stu-id="6f5da-120">This is accomplished by calling QueryInterface on an **IPortableDeviceProperties** object and checking for the existence of **IPortableDevicePropertiesBulk**.</span></span>


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



<span data-ttu-id="6f5da-121">下一項工作牽涉到建立 **IPortableDeviceValuesCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="6f5da-121">The next task entails creating an **IPortableDeviceValuesCollection** object.</span></span> <span data-ttu-id="6f5da-122">這是包含範例將會寫入之屬性值的物件。</span><span class="sxs-lookup"><span data-stu-id="6f5da-122">This is the object that contains the property values that the sample will write.</span></span>


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



<span data-ttu-id="6f5da-123">之後，此範例會建立 [**IPortableDevicePropertiesBulkCallback 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)的實例。</span><span class="sxs-lookup"><span data-stu-id="6f5da-123">After this, the sample creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="6f5da-124">應用程式將會使用此介面中的方法來追蹤非同步大量寫入作業的進度。</span><span class="sxs-lookup"><span data-stu-id="6f5da-124">The application will use the methods in this interface to track the progress of the asynchronous bulk-write operation.</span></span>


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



<span data-ttu-id="6f5da-125">範例應用程式呼叫的下一個函式是 `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` helper 函數。</span><span class="sxs-lookup"><span data-stu-id="6f5da-125">The next function that the sample application calls is the `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` helper function.</span></span> <span data-ttu-id="6f5da-126">此函式會以遞迴方式列舉指定裝置上的所有物件，並傳回 [**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md) ，其中包含找到之每個物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f5da-126">This function recursively enumerates all objects on a given device and returns an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="6f5da-127">此函式定義于模組 ContentEnumeration 中。</span><span class="sxs-lookup"><span data-stu-id="6f5da-127">This function is defined in the module ContentEnumeration.cpp.</span></span>


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



<span data-ttu-id="6f5da-128">**IPortableDevicePropVariantCollection** 物件會保存相同 VARTYPE 之索引 **PROPVARIANT** 值的集合。</span><span class="sxs-lookup"><span data-stu-id="6f5da-128">The **IPortableDevicePropVariantCollection** object holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="6f5da-129">在此情況下，這些值會包含在裝置上找到之每個物件的指定物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f5da-129">In this case, these values contain a given object identifier for each object found on the device.</span></span>

<span data-ttu-id="6f5da-130">物件識別碼和其各自的名稱屬性會儲存在 [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) 物件中。</span><span class="sxs-lookup"><span data-stu-id="6f5da-130">The object identifiers and their respective name properties are stored in an [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) object.</span></span> <span data-ttu-id="6f5da-131">名稱屬性的組織方式是將 "NewName0" 的 name 屬性指派給第一個物件，第二個物件的名稱屬性為 "NewName1"，依此類推。</span><span class="sxs-lookup"><span data-stu-id="6f5da-131">The name properties are organized so that the first object is assigned a name property of "NewName0", the second object is assigned a name property of "NewName1", and so on.</span></span>

<span data-ttu-id="6f5da-132">下列範例摘錄將示範如何使用物件識別碼和新名稱字串初始化 **IPortableDeviceValuesCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="6f5da-132">The following excerpt from the sample demonstrates how the **IPortableDeviceValuesCollection** object was initialized with object identifiers and new name strings.</span></span>


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



<span data-ttu-id="6f5da-133">一旦範例建立包含物件識別碼和名稱組的 **IPortableDeviceValuesCollection** 物件之後，就可以開始非同步作業。</span><span class="sxs-lookup"><span data-stu-id="6f5da-133">Once the sample creates the **IPortableDeviceValuesCollection** object that contains the object identifier and name pairs, it can begin the asynchronous operation.</span></span>

<span data-ttu-id="6f5da-134">當範例呼叫 [**IPortableDevicePropertiesBulk：： QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) 方法時，就會開始非同步寫入作業。</span><span class="sxs-lookup"><span data-stu-id="6f5da-134">The asynchronous write operation begins when the sample calls the [**IPortableDevicePropertiesBulk::QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) method.</span></span> <span data-ttu-id="6f5da-135">這個方法會通知驅動程式，大量作業即將開始。</span><span class="sxs-lookup"><span data-stu-id="6f5da-135">This method notifies the driver that a bulk operation is about to begin.</span></span> <span data-ttu-id="6f5da-136">之後，此範例會呼叫 [**IPortableDeviceBulk：： Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) 方法來開始實際寫入新的名稱值。</span><span class="sxs-lookup"><span data-stu-id="6f5da-136">After this, the sample calls the [**IPortableDeviceBulk::Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) method to begin actually writing the new name values.</span></span>


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



<span data-ttu-id="6f5da-137">請注意，此範例會等待無限長的一段時間，讓作業完成。</span><span class="sxs-lookup"><span data-stu-id="6f5da-137">Note that the sample waits an infinitely long period of time for the operation to complete.</span></span> <span data-ttu-id="6f5da-138">如果這是實際執行的應用程式，則必須修改程式碼。</span><span class="sxs-lookup"><span data-stu-id="6f5da-138">If this were a production application, the code would need to be modified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f5da-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="6f5da-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f5da-140">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="6f5da-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="6f5da-141">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="6f5da-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="6f5da-142">**IPortableDeviceProperties 介面**</span><span class="sxs-lookup"><span data-stu-id="6f5da-142">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="6f5da-143">**IPortableDevicePropertiesBulk 介面**</span><span class="sxs-lookup"><span data-stu-id="6f5da-143">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="6f5da-144">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="6f5da-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="6f5da-145">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="6f5da-145">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



