---
description: 依物件格式抓取多個物件的屬性
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: 依物件格式抓取多個物件的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469316"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a><span data-ttu-id="55615-103">依物件格式抓取多個物件的屬性</span><span class="sxs-lookup"><span data-stu-id="55615-103">Retrieving Properties for Multiple Objects by Object Format</span></span>

<span data-ttu-id="55615-104">除了大量抓取物件識別碼集合的屬性之外，應用程式也可以針對特定類型的所有物件，執行屬性的大量抓取。</span><span class="sxs-lookup"><span data-stu-id="55615-104">In addition to a bulk retrieval of properties for a collection of object identifiers, an application can also perform a bulk retrieval of properties for all objects of a particular type.</span></span> <span data-ttu-id="55615-105">如先前的範例所示，針對特定類型進行大量抓取需要設備磁碟機支援大量檢索。</span><span class="sxs-lookup"><span data-stu-id="55615-105">As in the previous example, bulk retrieval for a given type requires that the device driver support bulk retrievals.</span></span>

<span data-ttu-id="55615-106">您的應用程式可以使用下表所述的介面來執行大量抓取。</span><span class="sxs-lookup"><span data-stu-id="55615-106">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="55615-107">介面</span><span class="sxs-lookup"><span data-stu-id="55615-107">Interface</span></span>                                                                                      | <span data-ttu-id="55615-108">描述</span><span class="sxs-lookup"><span data-stu-id="55615-108">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="55615-109">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="55615-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="55615-110">提供內容特定方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="55615-110">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="55615-111">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="55615-111">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="55615-112">用來識別要取出的屬性。</span><span class="sxs-lookup"><span data-stu-id="55615-112">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="55615-113">**IPortableDeviceProperties 介面**</span><span class="sxs-lookup"><span data-stu-id="55615-113">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="55615-114">用來判斷指定的驅動程式是否支援大量作業。</span><span class="sxs-lookup"><span data-stu-id="55615-114">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="55615-115">**IPortableDevicePropertiesBulk 介面**</span><span class="sxs-lookup"><span data-stu-id="55615-115">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="55615-116">支援大量抓取作業。</span><span class="sxs-lookup"><span data-stu-id="55615-116">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="55615-117">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="55615-117">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="55615-118">用來儲存大量作業的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="55615-118">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="55615-119">範例應用程式 ContentProperties .cpp 模組中的 ReadContentPropertiesBulkFilteringFormat 函式會示範特定類型或格式之物件的大量抓取作業。</span><span class="sxs-lookup"><span data-stu-id="55615-119">The ReadContentPropertiesBulkFilteringFormat function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation for objects of a particular type or format.</span></span>

<span data-ttu-id="55615-120">在 ReadContentPropertiesBulkFilteringFormat 函式中找到的程式碼與在 ReadContentPropertiesBulk 函數中找到的程式碼幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="55615-120">The code found in the ReadContentPropertiesBulkFilteringFormat function is almost identical to the code found in the ReadContentPropertiesBulk function.</span></span> <span data-ttu-id="55615-121">如需此函式的完整描述， (參閱為 [多個物件取得屬性](retrieving-properties-for-multiple-objects.md) 。 ) </span><span class="sxs-lookup"><span data-stu-id="55615-121">(See the [Retrieving Properties for Multiple Objects](retrieving-properties-for-multiple-objects.md) topic for a complete description of this function.)</span></span>

<span data-ttu-id="55615-122">當作業排入佇列時，會發生主要的差異。</span><span class="sxs-lookup"><span data-stu-id="55615-122">The one primary difference occurs when the operation is queued.</span></span> <span data-ttu-id="55615-123">依類型或格式篩選時，會呼叫 [**IPortableDevicePropertiesBulk：： QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) 方法，而不是 [**IPortableDevicePropertiesBulk：： QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) 方法。</span><span class="sxs-lookup"><span data-stu-id="55615-123">When filtering by type or format, the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) method is called instead of the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) method.</span></span>


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a><span data-ttu-id="55615-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="55615-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55615-125">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="55615-125">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="55615-126">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="55615-126">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="55615-127">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="55615-127">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="55615-128">**IPortableDeviceProperties 介面**</span><span class="sxs-lookup"><span data-stu-id="55615-128">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="55615-129">**IPortableDevicePropertiesBulk 介面**</span><span class="sxs-lookup"><span data-stu-id="55615-129">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="55615-130">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="55615-130">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="55615-131">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="55615-131">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



