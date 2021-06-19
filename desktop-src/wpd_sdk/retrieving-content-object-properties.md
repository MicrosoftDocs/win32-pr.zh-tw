---
title: 正在抓取 WPD 物件屬性
description: WpdServiceApiSample 應用程式會示範應用程式如何取得指定連絡人服務所支援的內容物件屬性。
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e57258993d0a81f68042195db2caf338c97c53
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404311"
---
# <a name="retrieving-wpd-object-properties"></a><span data-ttu-id="0729f-103">正在抓取 WPD 物件屬性</span><span class="sxs-lookup"><span data-stu-id="0729f-103">Retrieving WPD object properties</span></span>

<span data-ttu-id="0729f-104">服務通常會包含屬於每個服務支援之其中一種格式的子物件。</span><span class="sxs-lookup"><span data-stu-id="0729f-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="0729f-105">例如，「連絡人」服務可能支援「抽象連絡人」格式的多個連絡人物件。</span><span class="sxs-lookup"><span data-stu-id="0729f-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="0729f-106">每個連絡人物件都是由相關屬性描述 (連絡人名稱、電話號碼、電子郵件地址等) 。</span><span class="sxs-lookup"><span data-stu-id="0729f-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="0729f-107">WpdServiceApiSample 應用程式所包含的程式碼會示範應用程式如何抓取指定連絡人服務所支援的內容物件屬性。</span><span class="sxs-lookup"><span data-stu-id="0729f-107">The WpdServiceApiSample application includes code that demonstrates how an application can retrieve the content-object properties supported by a given Contacts service.</span></span> <span data-ttu-id="0729f-108">此範例會使用下列介面。</span><span class="sxs-lookup"><span data-stu-id="0729f-108">This sample uses the following interfaces.</span></span>



| <span data-ttu-id="0729f-109">介面</span><span class="sxs-lookup"><span data-stu-id="0729f-109">Interface</span></span> | <span data-ttu-id="0729f-110">描述</span><span class="sxs-lookup"><span data-stu-id="0729f-110">Description</span></span>    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0729f-111">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="0729f-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="0729f-112">抓取 **IPortableDeviceContent2** 介面以存取支援的服務方法。</span><span class="sxs-lookup"><span data-stu-id="0729f-112">Retrieves the **IPortableDeviceContent2** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="0729f-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="0729f-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="0729f-114">提供內容特定方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="0729f-114">Provides access to the content-specific methods.</span></span>                                             |
| [<span data-ttu-id="0729f-115">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="0729f-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | <span data-ttu-id="0729f-116">抓取物件屬性值。</span><span class="sxs-lookup"><span data-stu-id="0729f-116">Retrieves the object property values.</span></span>                                                        |
| [<span data-ttu-id="0729f-117">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="0729f-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)               | <span data-ttu-id="0729f-118">保存針對該物件所讀取的屬性值。</span><span class="sxs-lookup"><span data-stu-id="0729f-118">Holds the property values that were read for that object.</span></span>                                    |
| [<span data-ttu-id="0729f-119">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="0729f-119">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md) | <span data-ttu-id="0729f-120">包含指定方法的參數。</span><span class="sxs-lookup"><span data-stu-id="0729f-120">Contains the parameters for a given method.</span></span>                                                  |



 

<span data-ttu-id="0729f-121">當使用者在命令列選擇選項 "7" 時，應用程式會叫用在 ContentProperties .cpp 模組中找到的 **ReadContentProperties** 方法。</span><span class="sxs-lookup"><span data-stu-id="0729f-121">When the user chooses option "7" at the command line, the application invokes the **ReadContentProperties** method that is found in the ContentProperties.cpp module.</span></span>

<span data-ttu-id="0729f-122">這個方法會為指定的 contact 物件抓取下列四個屬性。</span><span class="sxs-lookup"><span data-stu-id="0729f-122">This method retrieves the following four properties for the specified contact object.</span></span>



| <span data-ttu-id="0729f-123">屬性</span><span class="sxs-lookup"><span data-stu-id="0729f-123">Property</span></span>                     | <span data-ttu-id="0729f-124">描述</span><span class="sxs-lookup"><span data-stu-id="0729f-124">Description</span></span>                                                                                                                                                                                                      | <span data-ttu-id="0729f-125">裝置服務 PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="0729f-125">Device Services PROPERTYKEY</span></span>     | <span data-ttu-id="0729f-126">對等的 WPD \_ PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="0729f-126">Equivalent WPD\_PROPERTYKEY</span></span>         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| <span data-ttu-id="0729f-127">父物件識別碼</span><span class="sxs-lookup"><span data-stu-id="0729f-127">Parent-object identifier</span></span>     | <span data-ttu-id="0729f-128">字串，指定指定物件之父系的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0729f-128">A string that specifies the identifier for the given object's parent.</span></span>                                                                                                                                            | <span data-ttu-id="0729f-129">PKEY \_ GenericObj \_ ParentID</span><span class="sxs-lookup"><span data-stu-id="0729f-129">PKEY\_GenericObj\_ParentID</span></span>      | <span data-ttu-id="0729f-130">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="0729f-130">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="0729f-131">物件名稱</span><span class="sxs-lookup"><span data-stu-id="0729f-131">Object name</span></span>                  | <span data-ttu-id="0729f-132">指定指定物件名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="0729f-132">A string that specifies the name of the given object</span></span>                                                                                                                                                             | <span data-ttu-id="0729f-133">PKEY \_ GenericObj \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="0729f-133">PKEY\_GenericObj\_Name</span></span>          | <span data-ttu-id="0729f-134">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="0729f-134">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="0729f-135">持續性唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="0729f-135">Persistent unique identifier</span></span> | <span data-ttu-id="0729f-136">字串，指定指定物件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="0729f-136">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="0729f-137">此識別碼在會話之間是持續性的，與物件識別碼不同。</span><span class="sxs-lookup"><span data-stu-id="0729f-137">This identifier is persistent across sessions, unlike the object identifier.</span></span> <span data-ttu-id="0729f-138">針對服務，這必須是 GUID 的字串標記法。</span><span class="sxs-lookup"><span data-stu-id="0729f-138">For services, this needs to be a string-representation of a GUID.</span></span> | <span data-ttu-id="0729f-139">PKEY \_ GenericObj \_ PersistentUID</span><span class="sxs-lookup"><span data-stu-id="0729f-139">PKEY\_GenericObj\_PersistentUID</span></span> | <span data-ttu-id="0729f-140">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="0729f-140">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="0729f-141">物件格式</span><span class="sxs-lookup"><span data-stu-id="0729f-141">Object format</span></span>                | <span data-ttu-id="0729f-142"> (GUID) 的全域唯一識別碼，可指定對應于指定物件之檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="0729f-142">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object</span></span>                                                                                                        | <span data-ttu-id="0729f-143">PKEY \_ GenericObj \_ ObjectFormat</span><span class="sxs-lookup"><span data-stu-id="0729f-143">PKEY\_GenericObj\_ObjectFormat</span></span>  | <span data-ttu-id="0729f-144">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="0729f-144">WPD\_OBJECT\_FORMAT</span></span>                 |



 

-   <span data-ttu-id="0729f-145">父識別碼</span><span class="sxs-lookup"><span data-stu-id="0729f-145">Parent ID</span></span>
-   <span data-ttu-id="0729f-146">Name</span><span class="sxs-lookup"><span data-stu-id="0729f-146">Name</span></span>
-   <span data-ttu-id="0729f-147">PersistentUID</span><span class="sxs-lookup"><span data-stu-id="0729f-147">PersistentUID</span></span>
-   <span data-ttu-id="0729f-148">格式</span><span class="sxs-lookup"><span data-stu-id="0729f-148">Format</span></span>

<span data-ttu-id="0729f-149">請注意，在抓取內容屬性之前，範例應用程式會在連線的裝置上開啟連絡人服務。</span><span class="sxs-lookup"><span data-stu-id="0729f-149">Note that prior to retrieving the content properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="0729f-150">下列 **ReadContentProperties** 方法的程式碼會示範應用程式如何使用 [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) 介面來取出 [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) 介面。</span><span class="sxs-lookup"><span data-stu-id="0729f-150">The following code for the **ReadContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="0729f-151">藉由將要求的屬性 PROPERTYKEYS 傳遞至 [**IPortableDeviceProperties：： GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) 方法， **ReadContentProperties** 會抓取要求的值，然後將其顯示在主控台視窗中。</span><span class="sxs-lookup"><span data-stu-id="0729f-151">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **ReadContentProperties** retrieves the requested values, and then displays them to the console window.</span></span>


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
    if (FAILED(hr))
    {
        printf("An invalid object identifier was specified, aborting property reading\n");
    }

    // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pService->Content(&pContent);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
        }
    }

    // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
    // to access the property-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pContent->Properties(&pProperties);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
        }
    }

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
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
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
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

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="0729f-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="0729f-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0729f-153">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="0729f-153">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="0729f-154">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="0729f-154">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="0729f-155">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="0729f-155">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



