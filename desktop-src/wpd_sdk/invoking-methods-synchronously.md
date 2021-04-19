---
description: 叫用服務方法
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: 叫用服務方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b568ea169d0f3c6465d9879eb9eb01c0b46b526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996868"
---
# <a name="invoking-service-methods"></a><span data-ttu-id="aa4c7-103">叫用服務方法</span><span class="sxs-lookup"><span data-stu-id="aa4c7-103">Invoking Service Methods</span></span>

<span data-ttu-id="aa4c7-104">WpdServicesApiSample 應用程式包含的程式碼會示範應用程式如何以同步方式叫用指定連絡人服務所支援的方法。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-104">The WpdServicesApiSample application includes code that demonstrates how an application can invoke the methods supported by a given Contacts service synchronously..</span></span> <span data-ttu-id="aa4c7-105">此範例會使用下列介面</span><span class="sxs-lookup"><span data-stu-id="aa4c7-105">This sample uses the following interfaces</span></span>



|                                                                        |                                                                                                                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4c7-106">介面</span><span class="sxs-lookup"><span data-stu-id="aa4c7-106">Interface</span></span>                                                              | <span data-ttu-id="aa4c7-107">描述</span><span class="sxs-lookup"><span data-stu-id="aa4c7-107">Description</span></span>                                                                                                                                                             |
| [<span data-ttu-id="aa4c7-108">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="aa4c7-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="aa4c7-109">用來取出 **IPortableDeviceServiceMethods** 介面，以便在指定的服務上叫用方法。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="aa4c7-110">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="aa4c7-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | <span data-ttu-id="aa4c7-111">用來叫用服務方法。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="aa4c7-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="aa4c7-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="aa4c7-113">用來保存外寄方法參數和傳入方法的結果。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="aa4c7-114">如果方法不需要任何參數或傳回任何結果，這可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |



 

<span data-ttu-id="aa4c7-115">當使用者在命令列選擇選項 [9] 時，應用程式會叫用在 ServiceMethods .cpp 模組中找到的 **InvokeMethods** 方法。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-115">When the user chooses option "9" at the command line, the application invokes the **InvokeMethods** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="aa4c7-116">請注意，在叫用方法之前，範例應用程式會在連線的裝置上開啟連絡人服務。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-116">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="aa4c7-117">服務方法會封裝每個服務定義和實行的功能。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-117">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="aa4c7-118">它們對每種服務類型都是唯一的，並以 GUID 表示。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-118">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="aa4c7-119">例如，連絡人服務會定義 **BeginSync** 方法，讓應用程式呼叫以準備裝置來同步處理連絡人物件，並使用 **EndSync** 方法來通知裝置同步處理已完成。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-119">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="aa4c7-120">應用程式會藉由呼叫 [**IPortableDeviceServiceMethods：： Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)來執行方法。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-120">Applications execute a method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="aa4c7-121">服務方法不應與 WPD 命令混淆。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-121">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="aa4c7-122">WPD 命令是標準 WPD 設備磁碟機介面 (DDI) 的一部分，而且是 WPD 應用程式與驅動程式之間的通訊機制。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-122">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="aa4c7-123">命令是預先定義的，依類別分組（例如， **WPD \_ 類別 \_ 通用**），並以 **PROPERTYKEY** 結構表示。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-123">Commands are predefined, grouped by categories, for example, **WPD\_CATEGORY\_COMMON**, and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="aa4c7-124">應用程式會藉由呼叫 [**IPortableDeviceService：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)，將命令傳送至設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-124">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="aa4c7-125">如需詳細資訊，請參閱命令主題。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-125">For more information, see the Commands topic.</span></span>

<span data-ttu-id="aa4c7-126">**InvokeMethods** 方法會叫用 [**IPortableDeviceService：：**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) Method 方法來取出 [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)介面。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-126">The **InvokeMethods** method invokes the [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="aa4c7-127">使用這個介面，它會藉由呼叫 [**IPortableDeviceServiceMethods：： Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods)方法來叫用 **BeginSync** 和 **EndSync** 方法。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-127">Using this interface, it invokes the **BeginSync** and **EndSync** methods by calling the [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="aa4c7-128">每次呼叫 **Invoke** 時，應用程式會為叫用的方法提供 REFGUID。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-128">Each time it calls **Invoke**, the application supplies the REFGUID for the method that is invoked.</span></span>

<span data-ttu-id="aa4c7-129">下列程式碼會使用 **InvokeMethods** 方法。</span><span class="sxs-lookup"><span data-stu-id="aa4c7-129">The following code uses the **InvokeMethods** method.</span></span>


```C++
// Invoke methods on the Contacts Service.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethods(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke() the BeginSync method
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_BeginSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_EndSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        } 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="aa4c7-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa4c7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa4c7-131">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="aa4c7-131">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="aa4c7-132">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="aa4c7-132">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="aa4c7-133">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="aa4c7-133">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



