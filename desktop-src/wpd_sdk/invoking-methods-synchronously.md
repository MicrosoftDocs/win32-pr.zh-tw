---
description: 叫用服務方法
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: 叫用服務方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0553e1490a6f8d0903756767397c30c2e1137a16a80609ed3a22da69188f799e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843105"
---
# <a name="invoking-service-methods"></a>叫用服務方法

WpdServicesApiSample 應用程式包含的程式碼會示範應用程式如何以同步方式叫用指定連絡人服務所支援的方法。 此範例會使用下列介面



| 介面    | 描述    |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | 用來取出 **IPortableDeviceServiceMethods** 介面，以便在指定的服務上叫用方法。                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | 用來叫用服務方法。                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | 用來保存外寄方法參數和傳入方法的結果。 如果方法不需要任何參數或傳回任何結果，這可以是 **Null** 。 |



 

當使用者在命令列選擇選項 [9] 時，應用程式會叫用在 ServiceMethods .cpp 模組中找到的 **InvokeMethods** 方法。 請注意，在叫用方法之前，範例應用程式會在連線的裝置上開啟連絡人服務。

服務方法會封裝每個服務定義和實行的功能。 它們對每種服務類型都是唯一的，並以 GUID 表示。 例如，連絡人服務會定義 **BeginSync** 方法，讓應用程式呼叫以準備裝置來同步處理連絡人物件，並使用 **EndSync** 方法來通知裝置同步處理已完成。 應用程式會藉由呼叫 [**IPortableDeviceServiceMethods：： Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)來執行方法。

服務方法不應與 WPD 命令混淆。 WPD 命令是標準 WPD 設備磁碟機介面 (DDI) 的一部分，而且是 WPD 應用程式與驅動程式之間的通訊機制。 命令是預先定義的，依類別分組（例如， **WPD \_ 類別 \_ 通用**），並以 **PROPERTYKEY** 結構表示。 應用程式會藉由呼叫 [**IPortableDeviceService：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)，將命令傳送至設備磁碟機。 如需詳細資訊，請參閱命令主題。

**InvokeMethods** 方法會叫用 [**IPortableDeviceService：：**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) Method 方法來取出 [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)介面。 使用這個介面，它會藉由呼叫 [**IPortableDeviceServiceMethods：： Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods)方法來叫用 **BeginSync** 和 **EndSync** 方法。 每次呼叫 **Invoke** 時，應用程式會為叫用的方法提供 REFGUID。

下列程式碼會使用 **InvokeMethods** 方法。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



