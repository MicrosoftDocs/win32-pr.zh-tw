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
# <a name="retrieving-properties-for-a-single-object"></a><span data-ttu-id="53cc2-103">取得單一物件的屬性</span><span class="sxs-lookup"><span data-stu-id="53cc2-103">Retrieving Properties for a Single Object</span></span>

<span data-ttu-id="53cc2-104">在您的應用程式抓取物件識別碼之後 (查看指定物件的 [列舉內容](enumerating-content.md) 主題) ，它可以藉由呼叫 [**IPortableDeviceProperties 介面**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) 和 [**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md)中的方法，來取得該物件的描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="53cc2-104">After your application retrieves an object identifier (see the [Enumerating Content](enumerating-content.md) topic) for a given object, it can retrieve descriptive information about that object by calling methods in the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) and the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md).</span></span>

<span data-ttu-id="53cc2-105">[**IPortableDeviceProperties：： GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues)方法會取得指定物件的指定屬性清單。</span><span class="sxs-lookup"><span data-stu-id="53cc2-105">The [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method retrieves a list of specified properties for a given object.</span></span> <span data-ttu-id="53cc2-106"> (您的應用程式也可以呼叫 GetValues 方法，並為 pKeys 參數指定 **Null** 值，以抓取指定物件的所有屬性。不過，在抓取所有屬性時，此方法的效能可能會大幅降低。 ) </span><span class="sxs-lookup"><span data-stu-id="53cc2-106">(Your application could also call the GetValues method and specify a **NULL** value for the pKeys parameter to retrieve all properties for a given object; however, the performance of this method may be significantly slower when retrieving all properties.)</span></span>

<span data-ttu-id="53cc2-107">不過，在您的應用程式呼叫 GetValues 之前，它需要藉由在 [**IPortableDeviceKeyCollection 物件**](iportabledevicekeycollection.md)中設定對應的索引鍵來識別要抓取的屬性。</span><span class="sxs-lookup"><span data-stu-id="53cc2-107">Before your application calls GetValues, however, it needs to identify the properties to retrieve by setting corresponding keys in an [**IPortableDeviceKeyCollection object**](iportabledevicekeycollection.md).</span></span> <span data-ttu-id="53cc2-108">您的應用程式會藉由呼叫 [**IPortableDeviceKeyCollection：： Add**](iportabledevicekeycollection-add.md) 方法並提供 PROPERTYKEY 值來識別要抓取的每個屬性，來識別相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="53cc2-108">Your application will identify the properties of interest by calling the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method and supplying a PROPERTYKEY value that identifies each property that it will retrieve.</span></span>

<span data-ttu-id="53cc2-109">範例應用程式之 ContentProperties .cpp 模組中的 ReadContentProperties 函式會示範如何針對選取的物件抓取五個屬性。</span><span class="sxs-lookup"><span data-stu-id="53cc2-109">The ReadContentProperties function in the ContentProperties.cpp module of the sample application demonstrates how the five properties were retrieved for a selected object.</span></span> <span data-ttu-id="53cc2-110">下表描述每個屬性及其對應的 REFPROPERTYKEY 值。</span><span class="sxs-lookup"><span data-stu-id="53cc2-110">The following table describes each of these properties and their corresponding REFPROPERTYKEY value.</span></span>



| <span data-ttu-id="53cc2-111">屬性</span><span class="sxs-lookup"><span data-stu-id="53cc2-111">Property</span></span>                     | <span data-ttu-id="53cc2-112">描述</span><span class="sxs-lookup"><span data-stu-id="53cc2-112">Description</span></span>                                                                                                                                      | <span data-ttu-id="53cc2-113">PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="53cc2-113">PROPERTYKEY</span></span>                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="53cc2-114">父物件識別碼</span><span class="sxs-lookup"><span data-stu-id="53cc2-114">Parent-object identifier</span></span>     | <span data-ttu-id="53cc2-115">字串，指定指定物件之父系的識別碼。</span><span class="sxs-lookup"><span data-stu-id="53cc2-115">A string that specifies the identifier for the given object's parent.</span></span>                                                                            | <span data-ttu-id="53cc2-116">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="53cc2-116">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="53cc2-117">物件名稱</span><span class="sxs-lookup"><span data-stu-id="53cc2-117">Object name</span></span>                  | <span data-ttu-id="53cc2-118">指定指定物件名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="53cc2-118">A string that specifies the name of the given object.</span></span>                                                                                            | <span data-ttu-id="53cc2-119">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="53cc2-119">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="53cc2-120">持續性唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="53cc2-120">Persistent unique identifier</span></span> | <span data-ttu-id="53cc2-121">字串，指定指定物件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="53cc2-121">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="53cc2-122"> (此識別碼在會話之間是持續性的，與物件識別碼不同。 ) </span><span class="sxs-lookup"><span data-stu-id="53cc2-122">(This identifier is persistent across sessions, unlike the object identifier.)</span></span> | <span data-ttu-id="53cc2-123">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="53cc2-123">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="53cc2-124">物件格式</span><span class="sxs-lookup"><span data-stu-id="53cc2-124">Object format</span></span>                | <span data-ttu-id="53cc2-125"> (GUID) 的全域唯一識別碼，可指定對應于指定物件之檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="53cc2-125">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object.</span></span>                                       | <span data-ttu-id="53cc2-126">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="53cc2-126">WPD\_OBJECT\_FORMAT</span></span>                 |
| <span data-ttu-id="53cc2-127">物件內容類型</span><span class="sxs-lookup"><span data-stu-id="53cc2-127">Object content type</span></span>          | <span data-ttu-id="53cc2-128">GUID，指定與指定物件相關聯的內容類型。</span><span class="sxs-lookup"><span data-stu-id="53cc2-128">A GUID that specifies the type of content associated with a given object.</span></span>                                                                        | <span data-ttu-id="53cc2-129">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="53cc2-129">WPD\_OBJECT\_CONTENT\_TYPE</span></span>          |



 

<span data-ttu-id="53cc2-130">ReadContentProperties 函式的下列摘錄將示範範例應用程式如何使用 [**IPortableDeviceKeyCollection 介面**](iportabledevicekeycollection.md) 和 [**IPortableDeviceKeyCollection：： Add**](iportabledevicekeycollection-add.md) 方法來識別它所要抓取的屬性。</span><span class="sxs-lookup"><span data-stu-id="53cc2-130">The following excerpt from the ReadContentProperties function demonstrates how the sample application used the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method to identify the properties it would retrieve.</span></span>


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



<span data-ttu-id="53cc2-131">一旦範例應用程式設定適當的索引鍵，它就會呼叫 [**IPortableDeviceProperties：： GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) 方法，以取得指定物件的指定值。</span><span class="sxs-lookup"><span data-stu-id="53cc2-131">Once the sample application set the appropriate keys, it called the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method to retrieve the specified values for the given object.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="53cc2-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="53cc2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53cc2-133">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="53cc2-133">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="53cc2-134">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="53cc2-134">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="53cc2-135">**IPortableDeviceProperties 介面**</span><span class="sxs-lookup"><span data-stu-id="53cc2-135">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="53cc2-136">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="53cc2-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



