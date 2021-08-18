---
title: 應用程式基本概念
description: 應用程式基本概念
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- Windows媒體格式 SDK，DRM 應用程式基本概念
- 數位版權管理 (DRM) ，應用程式基本概念
- DRM (數位版權管理) ，應用程式基本概念
- 數位版權管理 (DRM) ，WMDRMStartup 函式
- DRM (數位版權管理) ，WMDRMStartup 函式
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8356160565754764ac71cb152799a0fd9d1530e6e6969dc7a56e203b7504645d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086204"
---
# <a name="application-basics"></a>應用程式基本概念

使用 Windows 媒體 DRM 用戶端擴充 api 的任何應用程式，都必須執行一些額外的處理。 本主題說明簡單應用程式的需求。

首先，您必須藉由呼叫 [**WMDRMStartup**](wmdrmstartup.md)函式來初始化 Windows 媒體 DRM 用戶端擴充 api。 SDK 的物件是 COM 物件，但您不需要呼叫 **CoIntialize**，因為 **WMDRMStatup** 函數會為您初始化 com。

> [!Note]  
> Windows 媒體格式 SDK 只會使用 com 的子集，因此，如果您使用的 com 物件不是 Windows 媒體 DRM 用戶端擴充 API 中的物件，您仍然必須呼叫 **CoInitialize**。

 

Windows 媒體 DRM 用戶端擴充 api 的所有物件都是使用 helper 函式和方法建立的。 您永遠不需要呼叫 **CoCreateInstance** 來建立物件。 針對使用 SDK 的任何應用程式，要具現化的第一個介面是 [**IWMDRMProvider**](iwmdrmprovider.md)，您可以用它來具現化所有其他基底介面。 若要取得 **IWMDRMProvider** 的實例，您必須呼叫 [**WMDRMCreateProvider**](wmdrmcreateprovider.md) 或 [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md)。 這些函式之間的差異在於， **WMDRMCreateProvider** 會建立一個物件，而這個物件可以接著只建立不支援需要存根程式庫之方法的物件。

當您擁有 **IWMDRMProvider** 的實例之後，您可以藉由呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md)來建立您所需的其他物件。

當您準備好要結束應用程式時，您必須藉由呼叫 [**WMDRMShutdown**](wmdrmshutdown.md) 函式來釋出 DRM 子系統資源。 此函數也會為您關閉 COM。

下列程式碼範例示範如何初始化並結束使用 Windows 媒體 DRM 用戶端擴充 api 的應用程式。


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**開始使用**](drm-getting-started.md)
</dt> </dl>

 

 




