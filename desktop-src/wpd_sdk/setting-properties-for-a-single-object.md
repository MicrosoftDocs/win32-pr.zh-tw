---
description: 設定單一物件的屬性
ms.assetid: 1c003534-96b4-419b-94d1-73b5ffa2eba1
title: 設定單一物件的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5649d05ccadfeaef0dd8805abd7d556f7725f175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987394"
---
# <a name="setting-properties-for-a-single-object"></a><span data-ttu-id="5be76-103">設定單一物件的屬性</span><span class="sxs-lookup"><span data-stu-id="5be76-103">Setting Properties for a Single Object</span></span>

<span data-ttu-id="5be76-104">在您的應用程式抓取物件識別碼之後 (查看指定物件的 [列舉內容](enumerating-content.md) 主題) ，它可以藉由呼叫下表所述介面中的方法來設定該物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="5be76-104">After your application retrieves an object identifier (see the [Enumerating Content](enumerating-content.md) topic) for a given object, it can set properties for that object by calling methods in the interfaces described in the following table.</span></span>



| <span data-ttu-id="5be76-105">介面</span><span class="sxs-lookup"><span data-stu-id="5be76-105">Interface</span></span>                                                                | <span data-ttu-id="5be76-106">描述</span><span class="sxs-lookup"><span data-stu-id="5be76-106">Description</span></span>                                                                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5be76-107">**IPortableDeviceProperties 介面**</span><span class="sxs-lookup"><span data-stu-id="5be76-107">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="5be76-108">用來判斷是否可以寫入指定的屬性，並傳送寫入作業。</span><span class="sxs-lookup"><span data-stu-id="5be76-108">Used to determine whether a given property can be written and to send the write operation.</span></span>                                                                  |
| [<span data-ttu-id="5be76-109">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="5be76-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="5be76-110">提供內容特定方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="5be76-110">Provides access to the content-specific methods.</span></span>                                                                                                            |
| [<span data-ttu-id="5be76-111">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="5be76-111">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="5be76-112">用來保存要寫入的值、判斷寫入作業的結果，以及在決定寫入功能) 時， (抓取屬性的屬性。</span><span class="sxs-lookup"><span data-stu-id="5be76-112">Used to hold the values to be written, determine results of the write operation, and retrieve attributes of properties (when determining write capability).</span></span> |



 

<span data-ttu-id="5be76-113">應用程式會先建立屬性包（使用 [**IPortableDeviceValues 介面**](iportabledevicevalues.md)指定新值），藉以設定物件上的屬性。</span><span class="sxs-lookup"><span data-stu-id="5be76-113">Applications set properties on an object by first creating a property bag that specifies the new values using the [**IPortableDeviceValues interface**](iportabledevicevalues.md).</span></span> <span data-ttu-id="5be76-114">建立屬性包之後，應用程式會藉由呼叫 [**IPortableDeviceProperties：： SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) 方法來設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5be76-114">Once the property bag is created, an application sets those properties by calling the [**IPortableDeviceProperties::SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) method.</span></span>

<span data-ttu-id="5be76-115">`WriteContentProperties`範例應用程式的 ContentProperties .cpp 模組中的函式會示範應用程式如何為選取的物件設定新的物件名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="5be76-115">The `WriteContentProperties` function in the sample application's ContentProperties.cpp module demonstrates how an application could set a new object-name property for a selected object.</span></span>

<span data-ttu-id="5be76-116">函式所完成的第一項工作 `WriteContentProperties` 是提示使用者輸入物件的物件識別碼，應用程式將會為該物件撰寫新的名稱。</span><span class="sxs-lookup"><span data-stu-id="5be76-116">The first task accomplished by the `WriteContentProperties` function is to prompt the user to enter an object identifier for the object that the application will write the new name for.</span></span>


```C++
HRESULT                               hr                   = S_OK;
WCHAR                                 szSelection[81]      = {0};
WCHAR                                 szNewObjectName[81]  = {0};
CComPtr<IPortableDeviceProperties>    pProperties;
CComPtr<IPortableDeviceContent>       pContent;
CComPtr<IPortableDeviceValues>        pObjectPropertiesToWrite;
CComPtr<IPortableDeviceValues>        pPropertyWriteResults;
CComPtr<IPortableDeviceValues>        pAttributes;
BOOL                                  bCanWrite            = FALSE;

// Prompt user to enter an object identifier on the device to write properties on.
printf("Enter the identifer of the object you wish to write properties on.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting property reading\n");
}
```



<span data-ttu-id="5be76-117">之後，應用程式會抓取 WPD \_ 屬性 \_ 屬性， \_ \_ 以寫入 WPD \_ OBJECT NAME 屬性的值， \_ 以判斷是否可以寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="5be76-117">After this, the application retrieves the WPD\_PROPERTY\_ATTRIBUTE\_CAN\_WRITE value for the WPD\_OBJECT\_NAME property to determine whether the property can be written.</span></span> <span data-ttu-id="5be76-118"> (請注意，您的應用程式可以設定任何屬性，其中 WPD \_ 屬性 \_ 屬性 \_ 可以 \_ 寫入值為 true。 ) </span><span class="sxs-lookup"><span data-stu-id="5be76-118">(Note that your application could set any property for which the WPD\_PROPERTY\_ATTRIBUTE\_CAN\_WRITE value is true.)</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent interface
// to access the property-specific methods.
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 3) Check the property attributes to see if we can write/change the WPD_OBJECT_NAME property.
if (SUCCEEDED(hr))
{
    hr = pProperties->GetPropertyAttributes(szSelection,
                                            WPD_OBJECT_NAME,
                                            &pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
        if (SUCCEEDED(hr))
        {
            if (bCanWrite)
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports TRUE\nThis means that the property can be changed/updated\n\n");
            }
            else
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports FALSE\nThis means that the property cannot be changed/updated\n\n");
            }
        }
        else
        {
            printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value from WPD_OBJECT_NAME on object '%ws', hr = 0x%lx\n",szSelection, hr);
        }
    }
}
```



<span data-ttu-id="5be76-119">下一步是提示使用者輸入新的名稱字串。</span><span class="sxs-lookup"><span data-stu-id="5be76-119">The next step is to prompt the user for the new name string.</span></span> <span data-ttu-id="5be76-120"> (請注意， [**IPortableDeviceValues：： SetStringValue**](iportabledevicevalues-setstringvalue.md) 方法的呼叫只會建立屬性包;實際的屬性尚未寫入。 ) </span><span class="sxs-lookup"><span data-stu-id="5be76-120">(Note that the call to the [**IPortableDeviceValues::SetStringValue**](iportabledevicevalues-setstringvalue.md) method merely creates the property bag; the actual property has not been written yet.)</span></span>


```C++
if (bCanWrite)
{
    printf("Enter the new WPD_OBJECT_NAME for the object '%ws'.\n>",szSelection);
    hr = StringCbGetsW(szNewObjectName,sizeof(szNewObjectName));
    if (FAILED(hr))
    {
        printf("An invalid object name was specified, aborting property writing\n");
    }

    // 5) CoCreate an IPortableDeviceValues interface to hold the property values
    // we wish to write.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pObjectPropertiesToWrite));
        if (SUCCEEDED(hr))
        {
            if (pObjectPropertiesToWrite != NULL)
            {
                hr = pObjectPropertiesToWrite->SetStringValue(WPD_OBJECT_NAME, szNewObjectName);
                if (FAILED(hr))
                {
                    printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceValues, hr= 0x%lx\n", hr);
                }
            }
        }
    }
```



<span data-ttu-id="5be76-121">最後，使用者所指定的新值會套用至物件。</span><span class="sxs-lookup"><span data-stu-id="5be76-121">Finally, the new value, specified by the user, is applied to the object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->SetValues(szSelection,                // The object whose properties we are reading
                                pObjectPropertiesToWrite,   // The properties we want to read
                                &pPropertyWriteResults);    // Driver supplied property result values for the property read operation
    if (FAILED(hr))
    {
        printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
    else
    {
        printf("The WPD_OBJECT_NAME property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", szSelection);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="5be76-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="5be76-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5be76-123">**IPortableDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="5be76-123">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="5be76-124">**IPortableDeviceContent 介面**</span><span class="sxs-lookup"><span data-stu-id="5be76-124">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="5be76-125">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="5be76-125">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="5be76-126">**IPortableDeviceProperties 介面**</span><span class="sxs-lookup"><span data-stu-id="5be76-126">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="5be76-127">**IPortableDevicePropertiesBulk 介面**</span><span class="sxs-lookup"><span data-stu-id="5be76-127">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="5be76-128">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="5be76-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="5be76-129">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="5be76-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



