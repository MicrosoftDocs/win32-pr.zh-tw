---
description: 正在載入 VDS
ms.assetid: 6b75fdb2-3d4c-4419-96e8-8677439e366b
title: 正在載入 VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec6a757b57c8e06e53862b3d36b9d54f291e4b07693dff008ecc2bbbb961c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125938"
---
# <a name="loading-vds"></a>正在載入 VDS

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代[虛擬磁碟服務](virtual-disk-service-portal.md)COM 介面。\]

**載入和初始化 VDS**

1.  釋放非 null 的介面。
2.  呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)、 [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)或 [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) 函數，以取得服務載入器物件的指標。

    **CLSCTX \_無法 \_** 在此呼叫中指定停用 AAA。 如果呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ，就不能在 *dwCapabilities* 參數中指定 **EOAC \_ DISABLE \_ AAA** 。

3.  呼叫 [**IVdsServiceLoader：： LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) 方法以載入 VDS。

    傳遞 **Null** 做為第一個參數，會在本機主機上載入並初始化 VDS。

4.  呼叫 [**IVdsService：： WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) 方法以等候 VDS 初始化完成。

下列程式碼範例會初始化服務，以傳回服務物件的指標。


```C++
#include "initguid.h"
#include "vds.h"
#include <stdio.h>

#pragma comment( lib, "ole32.lib" )

//
// Simple macro to release non-null interfaces.
//
#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

void __cdecl main(void) 
{
    HRESULT hResult;
    IVdsService *pService = NULL;
    IVdsServiceLoader *pLoader = NULL;

    // For this, you first get a pointer to the VDS Loader
    // Launch the VDS service. 
    //

    hResult = CoInitialize(NULL);

    if (SUCCEEDED(hResult)) 
    {
    
        hResult = CoCreateInstance(CLSID_VdsLoader,
            NULL,
            CLSCTX_LOCAL_SERVER,
            IID_IVdsServiceLoader,
            (void **) &pLoader);

        // 
        // And then load VDS on the local computer.
        //
        if (SUCCEEDED(hResult)) 
        {
            hResult = pLoader->LoadService(NULL, &pService);
        }

        //
        // You're done with the Loader interface at this point.
        //
        _SafeRelease(pLoader); 
        
        if (SUCCEEDED(hResult)) 
        {
            hResult = pService->WaitForServiceReady();
            if (SUCCEEDED(hResult)) 
            {
                //
                // You obtained an interface to the service: pService.
                // This interface can now be used to query for providers 
                // and perform other operations. 
                //
                printf("VDS Service Loaded");
            }

        } 
        else 
        {
            printf("VDS Service failed hr=%x\n",hResult);
        }
    }
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VDS](using-vds.md)
</dt> <dt>

[**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[安裝程式和服務物件](startup-and-service-objects.md)
</dt> </dl>

 

 
