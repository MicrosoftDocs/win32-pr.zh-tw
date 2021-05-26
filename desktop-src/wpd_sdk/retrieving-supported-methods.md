---
description: 正在抓取支援的服務方法
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: 正在抓取支援的服務方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b021aa868ffaa95df23a729e94d62eae8a0c632e
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423798"
---
# <a name="retrieving-supported-service-methods"></a><span data-ttu-id="78c2a-103">正在抓取支援的服務方法</span><span class="sxs-lookup"><span data-stu-id="78c2a-103">Retrieving Supported Service Methods</span></span>

<span data-ttu-id="78c2a-104">服務方法會封裝每個服務定義和實行的功能。</span><span class="sxs-lookup"><span data-stu-id="78c2a-104">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="78c2a-105">它們是每種服務類型的特定類型，並以唯一的 GUID 表示。</span><span class="sxs-lookup"><span data-stu-id="78c2a-105">They are specific to each type of service type and are represented by a unique GUID.</span></span>

<span data-ttu-id="78c2a-106">例如，連絡人服務會定義 **BeginSync** 方法，讓應用程式呼叫以準備裝置來同步處理連絡人物件，並使用 **EndSync** 方法來通知裝置同步處理已完成。</span><span class="sxs-lookup"><span data-stu-id="78c2a-106">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span>

<span data-ttu-id="78c2a-107">應用程式可以使用 [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) 介面，以程式設計方式查詢支援的方法，並存取這些方法及其屬性。</span><span class="sxs-lookup"><span data-stu-id="78c2a-107">Applications can programmatically query the supported methods and access these methods and their attributes by using the [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span>

<span data-ttu-id="78c2a-108">服務方法不應與 WPD 命令混淆。</span><span class="sxs-lookup"><span data-stu-id="78c2a-108">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="78c2a-109">WPD 命令是標準 WPD 設備磁碟機介面 (DDI) 的一部分，而且是 WPD 應用程式與驅動程式之間的通訊機制。</span><span class="sxs-lookup"><span data-stu-id="78c2a-109">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="78c2a-110">命令是預先定義的，依類別分組（例如，WPD \_ 類別 \_ 通用），並以 PROPERTYKEY 結構表示。</span><span class="sxs-lookup"><span data-stu-id="78c2a-110">Commands are predefined, grouped by categories, for example, WPD\_CATEGORY\_COMMON, and are represented by a PROPERTYKEY structure.</span></span> <span data-ttu-id="78c2a-111">如需詳細資訊，請參閱 [**命令**](commands.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="78c2a-111">For more information, see the [**Commands**](commands.md) topic.</span></span>

<span data-ttu-id="78c2a-112">WpdServicesApiSample 應用程式包含的程式碼會示範應用程式如何使用下表中的介面，來取得指定連絡人服務所支援的方法。</span><span class="sxs-lookup"><span data-stu-id="78c2a-112">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the methods supported by a given Contacts service by using the interfaces in the following table.</span></span>



| <span data-ttu-id="78c2a-113">介面</span><span class="sxs-lookup"><span data-stu-id="78c2a-113">Interface</span></span>      | <span data-ttu-id="78c2a-114">描述</span><span class="sxs-lookup"><span data-stu-id="78c2a-114">Description</span></span>         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78c2a-115">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="78c2a-115">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="78c2a-116">用來取出 **IPortableDeviceServiceCapabilities** 介面，以存取支援的服務方法。</span><span class="sxs-lookup"><span data-stu-id="78c2a-116">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="78c2a-117">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="78c2a-117">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="78c2a-118">提供支援的方法、方法屬性和方法參數的存取權。</span><span class="sxs-lookup"><span data-stu-id="78c2a-118">Provides access to the supported methods, method attributes and method parameters.</span></span>                             |
| [<span data-ttu-id="78c2a-119">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="78c2a-119">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="78c2a-120">包含支援的方法清單。</span><span class="sxs-lookup"><span data-stu-id="78c2a-120">Contains the list of supported methods.</span></span>                                                                        |
| [<span data-ttu-id="78c2a-121">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="78c2a-121">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="78c2a-122">包含方法和指定方法之參數的屬性。</span><span class="sxs-lookup"><span data-stu-id="78c2a-122">Contains the attributes for a method and for a given method's parameters.</span></span>                                      |
| [<span data-ttu-id="78c2a-123">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="78c2a-123">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="78c2a-124">包含指定方法的參數。</span><span class="sxs-lookup"><span data-stu-id="78c2a-124">Contains the parameters for a given method.</span></span>                                                                    |



 

<span data-ttu-id="78c2a-125">當使用者在命令列選擇選項 "5" 時，應用程式會叫用在 ServiceMethods .cpp 模組中找到的 **ListSupportedMethods** 方法。</span><span class="sxs-lookup"><span data-stu-id="78c2a-125">When the user chooses option "5" at the command line, the application invokes the **ListSupportedMethods** method that is found in the ServiceMethods.cpp module.</span></span>

<span data-ttu-id="78c2a-126">請注意，在抓取事件清單之前，範例應用程式會在連線的裝置上開啟連絡人服務。</span><span class="sxs-lookup"><span data-stu-id="78c2a-126">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="78c2a-127">在 WPD 中，方法的名稱、存取權限、參數和相關資料會加以描述。</span><span class="sxs-lookup"><span data-stu-id="78c2a-127">In WPD, a method is described by its name, access rights, parameters, and related data.</span></span> <span data-ttu-id="78c2a-128">範例應用程式會顯示使用者易記名稱，例如 "CustomMethod" 或 GUID。</span><span class="sxs-lookup"><span data-stu-id="78c2a-128">The sample application displays a user-friendly name, for example, "CustomMethod", or a GUID.</span></span> <span data-ttu-id="78c2a-129">方法名稱或 GUID 後面接著存取資料 ( 「讀取/寫入」 ) 、任何相關格式的名稱，以及參數資料。</span><span class="sxs-lookup"><span data-stu-id="78c2a-129">The method name or GUID is followed by access data ("Read/Write"), the name of any associated format, and the parameter data.</span></span> <span data-ttu-id="78c2a-130">此資料包含參數名稱、使用方式、VARTYPE 和表單。</span><span class="sxs-lookup"><span data-stu-id="78c2a-130">This data includes the parameter name, usage, VARTYPE, and form.</span></span>

<span data-ttu-id="78c2a-131">ServiceMethods .cpp 模組中的五個方法支援對指定連絡人服務的方法 (和相關資料) 的抓取： **ListSupportedMethods**、 **DisplayMethod**、 **DisplayMethodAccess**、 **DisplayFormat** 和 **DisplayMethodParameters**。</span><span class="sxs-lookup"><span data-stu-id="78c2a-131">Five methods in the ServiceMethods.cpp module support the retrieval of methods (and related data) for the given Contacts service: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters**.</span></span> <span data-ttu-id="78c2a-132">**ListSupportedMethods** 方法會抓取支援的方法計數和每個方法的 GUID 識別碼;然後，它會呼叫 **DisplayMethod** 方法。</span><span class="sxs-lookup"><span data-stu-id="78c2a-132">The **ListSupportedMethods** method retrieves a count of supported methods and the GUID identifier for each; it then calls the **DisplayMethod** method.</span></span> <span data-ttu-id="78c2a-133">**DisplayMethod** 方法會呼叫 [**IPortableDeviceServiceCapapbilities：： GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes)方法，以取得指定方法的選項、參數等等。</span><span class="sxs-lookup"><span data-stu-id="78c2a-133">The **DisplayMethod** method calls the [**IPortableDeviceServiceCapapbilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve the given method's options, parameters, and so on.</span></span> <span data-ttu-id="78c2a-134">在 **DisplayMethod** 抓取方法資料之後，它會轉譯名稱 (或 GUID) 、存取限制、相關聯的格式 (如果有任何) 和參數描述。</span><span class="sxs-lookup"><span data-stu-id="78c2a-134">After the **DisplayMethod** retrieves the method data, it renders the name (or GUID), the access restrictions, the associated format (if any), and the parameter descriptions.</span></span> <span data-ttu-id="78c2a-135">**DisplayMethodAccess**、 **DisplayFormat** 和 **DisplayMethodParameters** 是可轉譯其各自資料欄位的 helper 函式。</span><span class="sxs-lookup"><span data-stu-id="78c2a-135">The **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** are helper functions that render their respective fields of data.</span></span>

<span data-ttu-id="78c2a-136">**ListSupportedMethods** 方法會叫用 [**IPortableDeviceService：：功能**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities)方法來取出 [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)介面。</span><span class="sxs-lookup"><span data-stu-id="78c2a-136">The **ListSupportedMethods** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="78c2a-137">使用這個介面，它會藉由呼叫 [**IPortableDeviceServiceCapabilities：： GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) 方法來抓取支援的方法。</span><span class="sxs-lookup"><span data-stu-id="78c2a-137">Using this interface, it retrieves the supported methods by calling the [**IPortableDeviceServiceCapabilities::GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="78c2a-138">**GetSupportedMethods** 方法會抓取服務所支援之每個方法的 guid，並將該 guid 複製到 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)物件中。</span><span class="sxs-lookup"><span data-stu-id="78c2a-138">The **GetSupportedMethods** method retrieves the GUIDs for each method supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="78c2a-139">下列程式碼會使用 **ListSupportedMethods** 方法。</span><span class="sxs-lookup"><span data-stu-id="78c2a-139">The following code uses the **ListSupportedMethods** method.</span></span>


```C++
// List all supported methods on the service
void ListSupportedMethods(IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumMethods    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all methods supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedMethods(&pMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get supported methods from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported methods found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pMethods->GetCount(&dwNumMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported methods, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Methods Found on the service\n\n", dwNumMethods);

    // Loop through each method and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumMethods; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pMethods->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a method.  It is assumed that
                // methods are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayMethod(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }    
}
```



<span data-ttu-id="78c2a-140">在 **ListSupportedMethods** 方法為指定服務所支援的每個事件取得 GUID 之後，它會叫用 **DisplayMethod** 方法來抓取方法特定屬性。</span><span class="sxs-lookup"><span data-stu-id="78c2a-140">After the **ListSupportedMethods** method retrieves the GUID for each event supported by the given service, it invokes the **DisplayMethod** method to retrieve the method-specific attributes.</span></span> <span data-ttu-id="78c2a-141">這些屬性包括：方法的腳本易記名稱、必要的存取限制、任何相關的格式和參數清單。</span><span class="sxs-lookup"><span data-stu-id="78c2a-141">These attributes include: the method's script-friendly name , required access restrictions, any associated format, and list of parameters.</span></span>

<span data-ttu-id="78c2a-142">**DisplayMethod** 方法會叫用 [**IPortableDeviceServiceCapabilities：： GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes)方法，以取得指定方法的屬性集合。</span><span class="sxs-lookup"><span data-stu-id="78c2a-142">The **DisplayMethod** method invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve a collection of attributes for the given method.</span></span> <span data-ttu-id="78c2a-143">然後，它會呼叫 [**IPortableDeviceValues：： GetStringValue**](iportabledevicevalues-getstringvalue.md) 方法，以取得方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="78c2a-143">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method to retrieve the method's name.</span></span> <span data-ttu-id="78c2a-144">**DisplayMethod** 會呼叫 [**IPortableDeviceValues：： GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)以取得存取 restrctions。</span><span class="sxs-lookup"><span data-stu-id="78c2a-144">The **DisplayMethod** calls the [**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) to retrieve the access restrctions.</span></span> <span data-ttu-id="78c2a-145">之後，它會呼叫 [**IPortableDeviceValues：： GetGuidValue**](iportabledevicevalues-getguidvalue.md) 來取得任何相關聯的格式。</span><span class="sxs-lookup"><span data-stu-id="78c2a-145">After this, it calls [**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md) to retrieve any associated format.</span></span> <span data-ttu-id="78c2a-146">最後， **DisplayMethod** 會呼叫 [**IPortableDeviceValues：： GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) 來取出參數資料。</span><span class="sxs-lookup"><span data-stu-id="78c2a-146">And, finally, the **DisplayMethod** calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the parameter data.</span></span> <span data-ttu-id="78c2a-147">它會將這些方法所傳回的資料傳遞至 **DisplayMethodAccess**、 **DisplayFormat** 和 **DisplayMethodParameters** helper 函式，以轉譯指定方法的資訊。</span><span class="sxs-lookup"><span data-stu-id="78c2a-147">It passes the data returned by these methods to the **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** helper functions, which render the information for the given method.</span></span>

<span data-ttu-id="78c2a-148">下列程式碼會使用 **DisplayMethod** 方法。</span><span class="sxs-lookup"><span data-stu-id="78c2a-148">The following code uses the **DisplayMethod** method.</span></span>


```C++
// Display basic information about a method
void DisplayMethod(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the method attributes which describe the method
    HRESULT hr = pCapabilities->GetMethodAttributes(Method, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the method attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR   pszMethodName  = NULL;
        DWORD   dwMethodAccess = WPD_COMMAND_ACCESS_READ;
        GUID    guidFormat     = GUID_NULL;

        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the method if available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_METHOD_ATTRIBUTE_NAME, &pszMethodName);
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszMethodName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Method));
        }       

        // Display the method access if available, otherwise default to WPD_COMMAND_ACCESS_READ access
        hr = pAttributes->GetUnsignedIntegerValue(WPD_METHOD_ATTRIBUTE_ACCESS, &dwMethodAccess);
        if (FAILED(hr))
        {
            dwMethodAccess = WPD_COMMAND_ACCESS_READ;
            hr = S_OK;
        }
        printf("\n\tAccess: ");
        DisplayMethodAccess(dwMethodAccess);

        // Display the associated format if specified.
        // Methods that have an associated format may only be supported for that format.
        // Methods that don't have associated formats generally apply to the entire service.
        hr = pAttributes->GetGuidValue(WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("\n\tAssociated Format: ");
            DisplayFormat(pCapabilities, guidFormat);
        }

        // Display the method parameters, if available
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_METHOD_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayMethodParameters(pCapabilities, Method, pParameters);
        }
        
        CoTaskMemFree(pszMethodName);
        pszMethodName = NULL;

    }
}
```



<span data-ttu-id="78c2a-149">**DisplayMethodAccess** helper 函式會接收包含方法存取選項的 DWORD 值。</span><span class="sxs-lookup"><span data-stu-id="78c2a-149">The **DisplayMethodAccess** helper function receives a DWORD value that contains the method's access options.</span></span> <span data-ttu-id="78c2a-150">它會將此值與 WPD \_ 命令 \_ 存取 \_ READ 和 WPD \_ 命令存取 READWRITE 進行比較， \_ \_ 以判斷方法的存取權限。</span><span class="sxs-lookup"><span data-stu-id="78c2a-150">It compares this value to WPD\_COMMAND\_ACCESS\_READ and WPD\_COMMAND\_ACCESS\_READWRITE to determine the method's access privilege.</span></span> <span data-ttu-id="78c2a-151">它會使用結果來呈現字串，指出指定方法的存取限制。</span><span class="sxs-lookup"><span data-stu-id="78c2a-151">Using the result, it renders a string indicating the access restriction for the given method.</span></span>

<span data-ttu-id="78c2a-152">下列程式碼會使用 **DisplayMethodAccess** helper 函數。</span><span class="sxs-lookup"><span data-stu-id="78c2a-152">The following code uses the **DisplayMethodAccess** helper function.</span></span>


```C++
void DisplayMethodAccess(
    DWORD   dwAccess)
{
    switch(static_cast<WPD_COMMAND_ACCESS_TYPES>(dwAccess))
    {
        case WPD_COMMAND_ACCESS_READ:
            printf("Read");
            break;
            
        case WPD_COMMAND_ACCESS_READWRITE:
            printf("Read/Write");
            break;

        default:
            printf("Unknown Access");
            break;
    }
}
```



<span data-ttu-id="78c2a-153">**DisplayMethod** helper 函式會接收 [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)物件和方法的 GUID 做為參數。</span><span class="sxs-lookup"><span data-stu-id="78c2a-153">The **DisplayMethod** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object and the method's GUID as parameters.</span></span> <span data-ttu-id="78c2a-154">使用 **IPortableDeviceServiceCapabilities** 物件，它會叫用 [**IPortableDeviceServiceCapabilities：： GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) 方法，以抓取方法屬性並在應用程式的主控台視窗中轉譯它們。</span><span class="sxs-lookup"><span data-stu-id="78c2a-154">Using the **IPortableDeviceServiceCapabilities** object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method to retrieve the method attributes and render them in the application's console window.</span></span>

<span data-ttu-id="78c2a-155">**DisplayMethodParameters** helper 函式會接收 [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)物件、方法的 GUID，以及包含方法參數的 IPortableDeviceKeyCollection 物件。</span><span class="sxs-lookup"><span data-stu-id="78c2a-155">The **DisplayMethodParameters** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object, the method's GUID, and an IPortableDeviceKeyCollection object containing the method parameters.</span></span> <span data-ttu-id="78c2a-156">使用 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) 物件，它會叫用 [**IPortableDeviceServiceCapabilities：： GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) 方法來取出參數的名稱、使用方式、VARTYPE 和表單。</span><span class="sxs-lookup"><span data-stu-id="78c2a-156">Using the [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) method to retrieve the parameter's name, usage, VARTYPE, and form.</span></span> <span data-ttu-id="78c2a-157">它會在應用程式的主控台視窗中呈現此資訊。</span><span class="sxs-lookup"><span data-stu-id="78c2a-157">It renders this information in the application's console window.</span></span>

<span data-ttu-id="78c2a-158">下列程式碼會使用 **DisplayMethodParameters** helper 函數。</span><span class="sxs-lookup"><span data-stu-id="78c2a-158">The following code uses the **DisplayMethodParameters** helper function.</span></span>


```C++
// Display the method parameters.
void DisplayMethodParameters(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method,
    IPortableDeviceKeyCollection*       pParameters)
{
    DWORD   dwNumParameters = 0;

    // Get the number of parameters for this event.
    HRESULT hr = pParameters->GetCount(&dwNumParameters);
    if (FAILED(hr))
    {
        printf("! Failed to get number of parameters, hr = 0x%lx\n",hr);
    }

    printf("\n\t%d Method Parameters:\n", dwNumParameters);

    // Loop through each parameter and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumParameters; dwIndex++)
        {
            PROPERTYKEY parameter;
            hr = pParameters->GetAt(dwIndex, &parameter);

            if (SUCCEEDED(hr))
            {
                CComPtr<IPortableDeviceValues> pAttributes;

                // Display the parameter's Name, Usage, Vartype, and Form
                hr = pCapabilities->GetMethodParameterAttributes(Method, parameter, &pAttributes);
                if (FAILED(hr))
                {
                    printf("! Failed to get the method parameter attributes, hr = 0x%lx\n",hr);
                }

                if (SUCCEEDED(hr))
                {
                    PWSTR   pszParameterName    = NULL;
                    DWORD   dwAttributeVarType  = 0;
                    DWORD   dwAttributeForm     = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                    DWORD   dwAttributeUsage    = (DWORD)-1;

                    hr = pAttributes->GetStringValue(WPD_PARAMETER_ATTRIBUTE_NAME, &pszParameterName);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tName: %ws\n", pszParameterName);
                    }
                    else
                    {
                        printf("! Failed to get the method parameter name, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_USAGE value, if specified. 
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_USAGE, &dwAttributeUsage);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tUsage: ");
                        DisplayParameterUsage(dwAttributeUsage);
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter usage, hr = 0x%lx\n",hr);
                    }

                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_VARTYPE, &dwAttributeVarType);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tVARTYPE: ");
                        DisplayVarType(static_cast<VARTYPE>(dwAttributeVarType));
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter VARTYPE, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_FORM value.
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_FORM, &dwAttributeForm);
                    if (FAILED(hr))
                    {
                        // If the read fails, assume WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED
                        dwAttributeForm = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                        hr = S_OK;
                    }

                    printf("\t\tForm: ");
                    DisplayParameterForm(dwAttributeForm);
                    printf("\n");

                    CoTaskMemFree(pszParameterName);
                    pszParameterName = NULL;
                }
                
                printf("\n");
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="78c2a-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="78c2a-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78c2a-160">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="78c2a-160">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="78c2a-161">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="78c2a-161">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="78c2a-162">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="78c2a-162">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="78c2a-163">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="78c2a-163">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="78c2a-164">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="78c2a-164">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



