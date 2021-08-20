---
description: 開啟服務
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: 開啟服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 578dfee696fd17b0e360d6e344844670ca92ac6b48152242492a458a9a279f56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806718"
---
# <a name="opening-a-service"></a>開啟服務

在您的應用程式可以對服務執行作業之前（例如，列舉內容或取得支援事件或方法的描述），它必須開啟服務。 在 WpdServicesApiSample 應用程式中，會使用下表所述的介面，在 ServiceEnumeration .cpp 模組中示範這項工作。



| 介面                                                              | 描述                                        |
|------------------------------------------------------------------------|----------------------------------------------------|
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | 用來列舉裝置上的服務。        |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | 用來開啟裝置服務的連線。     |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | 用來保存應用程式的用戶端資訊。 |



 

開啟服務的方法是 [**IPortableDeviceService：： Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)。 這個方法會採用兩個引數：服務的隨插即用 (PnP) 識別碼，以及包含應用程式用戶端資訊的 [**IPortableDeviceValues**](iportabledevicevalues.md) 物件。

若要取得指定服務的 PnP 識別碼，您的應用程式會呼叫 [**IPortableDeviceServiceManager：： GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) 方法。 這個方法會抓取服務類別 GUID 服務的 PnP 識別碼陣列 (例如服務連絡人) 。

範例服務應用程式會在 ServiceEnumeration .cpp 模組的 **EnumerateContactsServices** 方法中，抓取連絡人服務的 PnP 識別碼。 下列程式碼範例取自這個方法。


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



當您的應用程式抓取服務的 PnP 識別碼之後，就可以設定用戶端資訊，並呼叫 [**IPortableDeviceService：： Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)。

在範例應用程式中，會在 ServiceEnumeration .cpp 模組的 **ChooseDeviceService** 內呼叫這個方法。

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) 支援兩個適用于 **CoCreateInstance** 的 clsid。 **CLSID \_PortableDeviceService** 會傳回未匯總無限制執行緒封送處理器的 **IPortableDeviceService** 指標; **CLSID \_PortableDeviceServiceFTM** 是新的 CLSID，會傳回匯總無限制執行緒封送處理器的 **IPortableDeviceService** 指標。 這兩個指標都支援相同的功能，否則為。

存留于單一執行緒單元中的應用程式應該使用 **CLSID \_ PortableDeviceServiceFTM** ，因為這樣可避免介面指標封送處理的額外負荷。 **CLSID \_** 繼承應用程式仍支援 PortableDeviceService。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDeviceService 介面**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceServiceManager 介面**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



