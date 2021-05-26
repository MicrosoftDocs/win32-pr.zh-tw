---
description: 開啟服務
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: 開啟服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b273b8709a4d750085f14075d605f88ed0faa6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423918"
---
# <a name="opening-a-service"></a><span data-ttu-id="45e70-103">開啟服務</span><span class="sxs-lookup"><span data-stu-id="45e70-103">Opening a Service</span></span>

<span data-ttu-id="45e70-104">在您的應用程式可以對服務執行作業之前（例如，列舉內容或取得支援事件或方法的描述），它必須開啟服務。</span><span class="sxs-lookup"><span data-stu-id="45e70-104">Before your application can perform operations on a service, for example, enumerating content or retrieving descriptions of supported events or methods, it must open the service.</span></span> <span data-ttu-id="45e70-105">在 WpdServicesApiSample 應用程式中，會使用下表所述的介面，在 ServiceEnumeration .cpp 模組中示範這項工作。</span><span class="sxs-lookup"><span data-stu-id="45e70-105">In the WpdServicesApiSample application, this task is demonstrated in the ServiceEnumeration.cpp module using the interfaces described in the following table.</span></span>



| <span data-ttu-id="45e70-106">介面</span><span class="sxs-lookup"><span data-stu-id="45e70-106">Interface</span></span>                                                              | <span data-ttu-id="45e70-107">描述</span><span class="sxs-lookup"><span data-stu-id="45e70-107">Description</span></span>                                        |
|------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="45e70-108">**IPortableDeviceServiceManager**</span><span class="sxs-lookup"><span data-stu-id="45e70-108">**IPortableDeviceServiceManager**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | <span data-ttu-id="45e70-109">用來列舉裝置上的服務。</span><span class="sxs-lookup"><span data-stu-id="45e70-109">Used to enumerate the services on a device.</span></span>        |
| [<span data-ttu-id="45e70-110">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="45e70-110">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="45e70-111">用來開啟裝置服務的連線。</span><span class="sxs-lookup"><span data-stu-id="45e70-111">Used to open a connection to a device service.</span></span>     |
| [<span data-ttu-id="45e70-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="45e70-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="45e70-113">用來保存應用程式的用戶端資訊。</span><span class="sxs-lookup"><span data-stu-id="45e70-113">Used to hold the application's client information.</span></span> |



 

<span data-ttu-id="45e70-114">開啟服務的方法是 [**IPortableDeviceService：： Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)。</span><span class="sxs-lookup"><span data-stu-id="45e70-114">The method that opens a service is [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span> <span data-ttu-id="45e70-115">這個方法會採用兩個引數：服務的隨插即用 (PnP) 識別碼，以及包含應用程式用戶端資訊的 [**IPortableDeviceValues**](iportabledevicevalues.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="45e70-115">This method takes two arguments: a Plug-and-Play (PnP) identifier for the service and an [**IPortableDeviceValues**](iportabledevicevalues.md) object that contains the application's client information.</span></span>

<span data-ttu-id="45e70-116">若要取得指定服務的 PnP 識別碼，您的應用程式會呼叫 [**IPortableDeviceServiceManager：： GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) 方法。</span><span class="sxs-lookup"><span data-stu-id="45e70-116">To obtain a PnP identifier for a given service, your application calls the [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) method.</span></span> <span data-ttu-id="45e70-117">這個方法會抓取服務類別 GUID 服務的 PnP 識別碼陣列 (例如服務連絡人) 。</span><span class="sxs-lookup"><span data-stu-id="45e70-117">This method retrieves an array of PnP identifiers for services of a service category GUID (for example SERVICE Contacts).</span></span>

<span data-ttu-id="45e70-118">範例服務應用程式會在 ServiceEnumeration .cpp 模組的 **EnumerateContactsServices** 方法中，抓取連絡人服務的 PnP 識別碼。</span><span class="sxs-lookup"><span data-stu-id="45e70-118">The sample Service application retrieves a PnP identifier for Contacts services within the **EnumerateContactsServices** method in the ServiceEnumeration.cpp module.</span></span> <span data-ttu-id="45e70-119">下列程式碼範例取自這個方法。</span><span class="sxs-lookup"><span data-stu-id="45e70-119">The following code sample is taken from this method.</span></span>


```C++
// For each device found, find the contacts service
for (dwIndex = 0; dwIndex < cPnpDeviceIDs; dwIndex++)
{
    DWORD   cPnpServiceIDs = 0;
    PWSTR   pPnpServiceID  = NULL;

    // First, pass NULL as the PWSTR array pointer to get the total number
    // of contacts services (SERVICE_Contacts) found on the device.
    // To find the total number of all services on the device, use GUID_DEVINTERFACE_WPD_SERVICE.
    hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, NULL, &cPnpServiceIDs);
    
    if (SUCCEEDED(hr) && (cPnpServiceIDs > 0))
    {                               
        // For simplicity, we are only using the first contacts service on each device
        cPnpServiceIDs = 1;
        hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, &pPnpServiceID, &cPnpServiceIDs);

        if (SUCCEEDED(hr))
        {
            // We've found the service, display it and save its PnP Identifier
            ContactsServicePnpIDs.Add(pPnpServiceID);

            printf("[%d] ", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()-1));

            // Display information about the device that contains this service.
            DisplayDeviceInformation(pServiceManager, pPnpServiceID);

            // ContactsServicePnpIDs now owns the memory for this string
            pPnpServiceID = NULL;
        }
        else
        {
            printf("! Failed to get the first contacts service from '%ws, hr = 0x%lx\n",pPnpDeviceIDs[dwIndex],hr);
        }
    }
}
```



<span data-ttu-id="45e70-120">當您的應用程式抓取服務的 PnP 識別碼之後，就可以設定用戶端資訊，並呼叫 [**IPortableDeviceService：： Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)。</span><span class="sxs-lookup"><span data-stu-id="45e70-120">After your application retrieves the PnP identifier for the service, it can set up the client information and call [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span>

<span data-ttu-id="45e70-121">在範例應用程式中，會在 ServiceEnumeration .cpp 模組的 **ChooseDeviceService** 內呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="45e70-121">In the sample application, this method is called within **ChooseDeviceService** in the ServiceEnumeration.cpp module.</span></span>

<span data-ttu-id="45e70-122">[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) 支援兩個適用于 **CoCreateInstance** 的 clsid。</span><span class="sxs-lookup"><span data-stu-id="45e70-122">[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="45e70-123">**CLSID \_PortableDeviceService** 會傳回未匯總無限制執行緒封送處理器的 **IPortableDeviceService** 指標; **CLSID \_PortableDeviceServiceFTM** 是新的 CLSID，會傳回匯總無限制執行緒封送處理器的 **IPortableDeviceService** 指標。</span><span class="sxs-lookup"><span data-stu-id="45e70-123">**CLSID\_PortableDeviceService** returns an **IPortableDeviceService** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceServiceFTM** is a new CLSID that returns an **IPortableDeviceService** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="45e70-124">這兩個指標都支援相同的功能，否則為。</span><span class="sxs-lookup"><span data-stu-id="45e70-124">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="45e70-125">存留于單一執行緒單元中的應用程式應該使用 **CLSID \_ PortableDeviceServiceFTM** ，因為這樣可避免介面指標封送處理的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="45e70-125">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceServiceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="45e70-126">**CLSID \_** 繼承應用程式仍支援 PortableDeviceService。</span><span class="sxs-lookup"><span data-stu-id="45e70-126">**CLSID\_PortableDeviceService** is still supported for legacy applications.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDeviceServiceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pService));
if (SUCCEEDED(hr))
{
    hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the service for Read Write access, will open it for Read-only access instead\n");

            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);

            hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);

            if (FAILED(hr))
            {
                printf("! Failed to Open the service for Read access, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            printf("! Failed to Open the service, hr = 0x%lx\n",hr);
        }
    }
```



## <a name="related-topics"></a><span data-ttu-id="45e70-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="45e70-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45e70-128">**IPortableDeviceService 介面**</span><span class="sxs-lookup"><span data-stu-id="45e70-128">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="45e70-129">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="45e70-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="45e70-130">**IPortableDeviceServiceManager 介面**</span><span class="sxs-lookup"><span data-stu-id="45e70-130">**IPortableDeviceServiceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[<span data-ttu-id="45e70-131">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="45e70-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



