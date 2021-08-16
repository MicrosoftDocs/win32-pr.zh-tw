---
description: 取得 IWbemServices proxy 的指標之後，您必須將 proxy 上的安全性設定為透過 proxy 存取 WMI。
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: 設定 WMI 連接的安全性層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c2c4a492d4b40410b42fd9a94f22d346617a84d3baaa0679db325452a69c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315322"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a>設定 WMI 連接的安全性層級

取得 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy 的指標之後，您必須將 proxy 上的安全性設定為透過 PROXY 存取 WMI。 您必須設定安全性，因為 **IWbemServices** proxy 會授與跨進程物件的存取權。 一般而言，如果您未設定適當的安全性屬性，則 COM 安全性不允許一個進程存取另一個進程。 如需詳細資訊，請參閱 [在 IWbemServices 和其他 proxy 上設定安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。 連接不同的作業系統需要不同層級的驗證和模擬。 如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。

本主題中的程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



下列程式描述如何設定 WMI 連接的安全性層級。

**設定 WMI 連接的安全性層級**

-   使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)的呼叫，設定 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy 上的安全性層級。

    下列程式碼範例說明呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)的常見方式。

    ```C++
        HRESULT hres;
        IWbemServices *pSvc = 0;
        IWbemLocator *pLoc = 0;

        // Set the proxy so that impersonation of the client occurs.
        hres = CoSetProxyBlanket(pSvc,
           RPC_C_AUTHN_WINNT,
           RPC_C_AUTHZ_NONE,
           NULL,
           RPC_C_AUTHN_LEVEL_CALL,
           RPC_C_IMP_LEVEL_IMPERSONATE,
           NULL,
           EOAC_NONE
        );

        if (FAILED(hres))
        {
            cout << "Could not set proxy blanket. Error code = 0x" 
                 << hex << hres << endl;
           pSvc->Release();
          pLoc->Release();     
            CoUninitialize();
            return hres;      // Program has failed.
        }
    ```

    

設定 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標的安全性層級之後，您就可以存取 WMI 的各種功能。 使用 WMI 完成後，您必須關閉應用程式。 如需詳細資訊，請參閱 [清除和關閉 WMI 應用程式](cleaning-up-and-shutting-down-a-wmi-application.md)。

 

 
