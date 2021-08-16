---
description: 連接到 WMI 的第一個步驟是設定 CoInitializeEx 和 CoInitializeSecurity 的 COM 呼叫。
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: 初始化 WMI 應用程式的 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723188602e440cd3ba49d78d8efb3c28ddae30f35dd0d4361a4fdb5ced026ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318572"
---
# <a name="initializing-com-for-a-wmi-application"></a>初始化 WMI 應用程式的 COM

連接到 WMI 的第一個步驟是設定 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的 COM 呼叫。

本主題中的程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



下列程式描述如何從用戶端應用程式初始化 COM。

**從用戶端應用程式初始化 COM**

1.  使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)的呼叫初始化 COM。

    呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 是設定 COM 介面的標準程式。 因此，在呼叫 **CoInitializeEx** 時，WMI 不需要您觀察任何額外的程式。 如需詳細資訊，請參閱 [COM](../com/component-object-model--com--portal.md)。

    下列程式碼範例說明如何呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)。

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 介面的呼叫來設定一般 COM 安全性層級。

    [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 是一種標準函式，您必須在設定進程的 COM 介面時呼叫此函數。 如果您想要針對整個進程設定驗證、模擬或驗證服務的預設安全性設定，請呼叫 **CoInitializeSecurity** 。 如需詳細資訊，請參閱 [設定用戶端應用程式處理安全性](setting-client-application-process-security.md)。 如果您想要設定或變更特定 proxy 的安全性，則必須呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)。 當您在無法控制驗證、模擬或驗證服務之預設安全性設定的另一個進程中執行時，每次必須設定或變更 COM 安全性時，請使用 **CoSetProxyBlanket** 。 如需詳細資訊，請參閱 [設定 WMI 連接的安全性層級](setting-the-security-levels-on-a-wmi-connection.md) 和 [設定 IWbemServices 和其他 proxy 的安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。

    當您設計 WMI 用戶端應用程式時，WMI 有幾個您應該注意的安全性問題。 如需詳細資訊，請參閱 [設定用戶端應用程式處理安全性](setting-client-application-process-security.md)。

    下列程式碼範例描述如何呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 來設定進程的 COM 安全性。

    ```C++
    hr =  CoInitializeSecurity(
        NULL,                        // Security descriptor    
        -1,                          // COM negotiates authentication service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication level for proxies
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation level for proxies
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities of the client or server
        NULL);                       // Reserved

    if (FAILED(hr))
    {
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       CoUninitialize();
       return hr;                  // Program has failed.
    }
    ```

    

在您初始化 COM 之後，下一步就是建立與 WMI 命名空間的連接。 如需詳細資訊，請參閱 [建立與 WMI 命名空間的連接](creating-a-connection-to-a-wmi-namespace.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 c + + 建立 WMI 應用程式](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[存取 WMI 命名空間](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
