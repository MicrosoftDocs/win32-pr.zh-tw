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
# <a name="obtaining-service-objects"></a>取得服務物件

裝置物件會公開一個名為「 [**服務**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) 」的屬性，此屬性會傳回服務物件的集合，其中包含裝置所匯出之每個服務的一個服務物件。 應用程式能夠依序往返此集合，或使用服務識別碼來要求特定的服務。

## <a name="vbscript-example"></a>VBScript 範例

下列範例是 VBScript 程式碼，它會將裝置所匯出的兩個服務的服務物件解壓縮。


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



第一行會藉由查詢 [**服務**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) 屬性，從裝置物件解壓縮服務集合。 接下來的兩行會藉由指定服務識別碼，從集合中取得兩個所需的服務物件。 服務集合也可以使用 for each 來依序進行 **next** 迴圈。

## <a name="c-example"></a>C + + 範例

下列範例顯示從裝置取得服務物件所需的 c + + 程式碼。 首先，範例程式碼會查詢傳遞給函式之介面上的 [**IUPnPDevice：： Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) 屬性。 這會使用 [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) 介面傳回服務集合。 若要取得個別的服務物件，請使用 [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) 方法，並指定要求的服務識別碼。 若要順序地遍歷集合，請使用 [**IEnumVARIANT：： Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset)、 [**IEnumVARIANT：： Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)和 [**IEnumVARIANT：： Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) 方法。 這個範例類似于用來遍歷 [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) 集合的範例。


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



 

 