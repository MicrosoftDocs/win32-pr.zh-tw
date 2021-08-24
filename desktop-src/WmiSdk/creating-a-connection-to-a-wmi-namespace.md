---
description: 設定 COM 的標準呼叫之後，您必須透過呼叫 IWbemLocator：： ConnectServer 方法來連接到 WMI。
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: 建立與 WMI 命名空間的連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2587024d7f581cd28a8fdaf339db9567b17c509599c01aca0599b701186fb786
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412138"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a>建立與 WMI 命名空間的連接

設定 COM 的標準呼叫之後，您必須透過呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 方法來連接到 WMI。 **ConnectServer** 方法會傳回 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面的 proxy。 您可以透過 **IWbemServices** 存取 WMI 的不同功能。

本主題中的程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



下列程式說明如何建立與 WMI 命名空間的連接。

**建立與 WMI 命名空間的連接**

-   透過對 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的呼叫來初始化 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)介面。

    WMI 不需要您在 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)上呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)時執行任何額外的程式。

    下列程式碼範例說明如何初始化 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)。

    ```C++
        IWbemLocator *pLoc = 0;
        HRESULT hr;

        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
            CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
     
        if (FAILED(hr))
        {
            cout << "Failed to create IWbemLocator object. Err code = 0x"
                 << hex << hr << endl;
            CoUninitialize();
            return hr;     // Program has failed.
        }
    ```

    

    -   透過呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)方法連線至 WMI。

        [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)方法會將 proxy 傳回給 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面，這個介面是用來存取您對 **ConnectServer** 呼叫中指定的本機或遠端 WMI 命名空間。

        下列程式碼範例說明如何呼叫 [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)。

        ```C++
        IWbemServices *pSvc = 0;

            // Connect to the root\default namespace with the current user.
            hr = pLoc->ConnectServer(
                    BSTR(L"ROOT\\DEFAULT"),  //namespace
                    NULL,       // User name 
                    NULL,       // User password
                    0,         // Locale 
                    NULL,     // Security flags
                    0,         // Authority 
                    0,        // Context object 
                    &pSvc);   // IWbemServices proxy


            if (FAILED(hr))
            {
                cout << "Could not connect. Error code = 0x" 
                     << hex << hr << endl;
                pLoc->Release();
                CoUninitialize();
                return hr;      // Program has failed.
            }

            cout << "Connected to WMI" << endl;
        ```

        

當您收到 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy 的指標之後，您必須在 proxy 上設定安全性以存取 WMI。 如需詳細資訊，請參閱 [設定 WMI 連接的安全性層級](setting-the-security-levels-on-a-wmi-connection.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 c + + 建立 WMI 應用程式](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[WMI 中的 IPv6 和 IPv4 支援](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
