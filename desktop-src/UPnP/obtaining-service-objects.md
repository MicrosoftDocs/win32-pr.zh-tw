---
title: 取得服務物件
description: 裝置物件會公開一個名為「服務」的屬性，此屬性會傳回服務物件的集合，其中包含裝置所匯出之每個服務的一個服務物件。
ms.assetid: 8ef12b6e-cb9b-4406-95be-002117b8fc3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf951c9c620c23c2d4919dc4a8bcf082159fa7a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842568"
---
# <a name="obtaining-service-objects"></a><span data-ttu-id="f374d-103">取得服務物件</span><span class="sxs-lookup"><span data-stu-id="f374d-103">Obtaining Service Objects</span></span>

<span data-ttu-id="f374d-104">裝置物件會公開一個名為「 [**服務**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) 」的屬性，此屬性會傳回服務物件的集合，其中包含裝置所匯出之每個服務的一個服務物件。</span><span class="sxs-lookup"><span data-stu-id="f374d-104">Device objects expose a property called [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) that returns a collection of Service objects that contains one service object for each service exported by the device.</span></span> <span data-ttu-id="f374d-105">應用程式能夠依序往返此集合，或使用服務識別碼來要求特定的服務。</span><span class="sxs-lookup"><span data-stu-id="f374d-105">Applications are able to traverse this collection sequentially, or request a particular service by using its service ID.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="f374d-106">VBScript 範例</span><span class="sxs-lookup"><span data-stu-id="f374d-106">VBScript Example</span></span>

<span data-ttu-id="f374d-107">下列範例是 VBScript 程式碼，它會將裝置所匯出的兩個服務的服務物件解壓縮。</span><span class="sxs-lookup"><span data-stu-id="f374d-107">The following example is VBScript code that extracts Service objects for two of the services exported by a device.</span></span>


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



<span data-ttu-id="f374d-108">第一行會藉由查詢 [**服務**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) 屬性，從裝置物件解壓縮服務集合。</span><span class="sxs-lookup"><span data-stu-id="f374d-108">The first line extracts the services collection from the Device object by querying the [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property.</span></span> <span data-ttu-id="f374d-109">接下來的兩行會藉由指定服務識別碼，從集合中取得兩個所需的服務物件。</span><span class="sxs-lookup"><span data-stu-id="f374d-109">The next two lines obtain the two desired Service objects from the collection by specifying their service IDs.</span></span> <span data-ttu-id="f374d-110">服務集合也可以使用 for each 來依序進行 **next** 迴圈。</span><span class="sxs-lookup"><span data-stu-id="f374d-110">The services collection can also be traversed sequentially by using a **for each … next** loop.</span></span>

## <a name="c-example"></a><span data-ttu-id="f374d-111">C + + 範例</span><span class="sxs-lookup"><span data-stu-id="f374d-111">C++ Example</span></span>

<span data-ttu-id="f374d-112">下列範例顯示從裝置取得服務物件所需的 c + + 程式碼。</span><span class="sxs-lookup"><span data-stu-id="f374d-112">The following example shows the C++ code required to obtain Service objects from a device.</span></span> <span data-ttu-id="f374d-113">首先，範例程式碼會查詢傳遞給函式之介面上的 [**IUPnPDevice：： Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) 屬性。</span><span class="sxs-lookup"><span data-stu-id="f374d-113">First, the sample code queries the [**IUPnPDevice::Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property on the interface that was passed to the function.</span></span> <span data-ttu-id="f374d-114">這會使用 [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) 介面傳回服務集合。</span><span class="sxs-lookup"><span data-stu-id="f374d-114">This returns a service collection using the [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) interface.</span></span> <span data-ttu-id="f374d-115">若要取得個別的服務物件，請使用 [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) 方法，並指定要求的服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="f374d-115">To obtain individual Service objects, use the [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) method, and specify the requested service IDs.</span></span> <span data-ttu-id="f374d-116">若要順序地遍歷集合，請使用 [**IEnumVARIANT：： Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset)、 [**IEnumVARIANT：： Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)和 [**IEnumVARIANT：： Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) 方法。</span><span class="sxs-lookup"><span data-stu-id="f374d-116">To traverse the collection sequentially, use the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next), and [**IEnumVARIANT::Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) methods.</span></span> <span data-ttu-id="f374d-117">這個範例類似于用來遍歷 [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) 集合的範例。</span><span class="sxs-lookup"><span data-stu-id="f374d-117">This example is similar to the example used to traverse the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) collection.</span></span>


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")


HRESULT ExtractServices(IUPnPDevice * pDevice)
{
    // Create a BSTR to hold the service name
    BSTR bstrServiceName = SysAllocString(L"urn:upnp-org:servicId:DVDVideo");
    if (NULL == bstrServiceName)
    {
        return E_OUTOFMEMORY;
    }
    // Get the list of services available on the device
    IUPnPServices * pServices = NULL;
    HRESULT hr = pDevice->get_Services(&pServices);
    if (SUCCEEDED(hr))
    {
        // Retrieve the service we are interested in
        IUPnPService * pAppService = NULL;
        hr = pServices->get_Item(bstrServiceName, &pAppService);
        if (SUCCEEDED(hr))
        {
            // Do something interesting with the service object
            pAppService->Release();
        }
        pServices->Release();
    }
    SysFreeString(bstrServiceName);
    return hr;
}
```



 

 