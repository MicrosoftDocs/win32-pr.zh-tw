---
description: 描述如何在應用程式中包含 WMI COM 提供者作為元件，而不是在內部處理 WMI。 所謂的低耦合提供者，這是建議的 WMI COM 提供者類型，可針對 Windows 2000 和更新版本的作業系統建立。
ms.assetid: a502f0dd-9add-4ebd-bc25-743a55eb78ac
ms.tgt_platform: multiple
title: 將提供者併入應用程式中
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb544cd3b04cc75cef026bb2e4d2e579b8dbf135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571141"
---
# <a name="incorporating-a-provider-in-an-application"></a>將提供者併入應用程式中

在建立要檢測的應用程式時，最佳作法是將提供者納入為應用程式本身內的元件。 這種作法可讓 Windows Management Instrumentation (WMI) 直接與服務提供者互動，而不是間接透過程式 API 來與服務提供者互動。 將提供者與 WMI 分離也會讓應用程式控制提供者存留期，而不是 WMI。 如需撰寫在 WMI 進程中執行的提供者的詳細資訊，請參閱 [撰寫提供者以將資料提供給 wmi](supplying-data-to-wmi-by-writing-a-provider.md)。 如需有關主控提供者之模型和安全性設定的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。

下圖說明 WMI、低耦合提供者和應用程式之間的關聯性。

![wmi、低耦合提供者和應用程式之間的關聯性](images/decoupledprov.png)

如需有關低耦合提供者方法的詳細資訊，請參閱 [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) 和 [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider)。

> [!Note]  
> 低耦合提供者支援實例、方法、事件提供者和事件取用者。 它不支援類別和屬性提供者。 如需詳細資訊，請參閱 [撰寫類別提供者](writing-a-class-provider.md) 和 [撰寫屬性提供者](writing-a-property-provider.md)。

 

本主題中的程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



下列程式會使用 c + + 程式碼範例，說明如何在應用程式中納入低耦合提供者。 應用程式的初始化方法會執行下列步驟，讓 WMI 僅與已註冊的低耦合提供者互動。

**在 c + + 應用程式中執行低耦合提供者**

1.  初始化 COM 程式庫以供呼叫執行緒使用。

    下列程式碼範例顯示如何初始化 COM 程式庫。

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  設定預設進程安全性層級。

    此層級會建立其他程式存取用戶端進程資訊所需的安全性層級。 驗證層級應為 RPC \_ C \_ 驗證 \_ 層級的 \_ 預設值。 如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。

    下列程式碼範例顯示如何設定預設的安全性層級。

    ```C++
    hr = CoInitializeSecurity (NULL, 
        -1, 
        NULL, 
        NULL,
        RPC_C_AUTHN_LEVEL_DEFAULT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, 
        EOAC_DYNAMIC_CLOAKING, 
        NULL);

    if (FAILED(hr))
    {
      CoUninitialize();
      cout << "Failed to initialize security. Error code = 0x"
           << hex << hr << endl;
      return;
    }
    ```

    

3.  註冊低耦合提供者註冊機構。

    下列程式碼範例顯示如何註冊低耦合提供者註冊機構。

    ```C++
    CLSID CLSID_WbemDecoupledRegistrar;
    IID IID_IWbemDecoupledRegistrar;
    IWbemDecoupledRegistrar *myRegistrar = NULL;

    hr = CoCreateInstance(CLSID_WbemDecoupledRegistrar,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledRegistrar,
                          (void**)&myRegistrar);
    if (SUCCEEDED(hr))
    {
        IUnknown *pIUnknown = NULL;
        // CMyProv is the class added for WMI instance / event provider
        HRESULT hr = CMyProv::CreateInstance(NULL,&pIUnknown);
        if ( SUCCEEDED(hr))
        {
            hr = myRegistrar->Register(0,
                NULL,
                NULL,
                NULL,
                L"root\\cimv2",
                L"DecoupledInstanceProvider",
                pIUnknown);

                pIUnknown->Release();
        }
    }

    if (FAILED (hr))
    {
        if ( myRegistrar )
        {
            myRegistrar->Release () ;
        }
    }
    ```

    

4.  註冊分離事件提供者。

    下列程式碼範例示範如何註冊分離事件提供者。

    ```C++
    IWbemDecoupledBasicEventProvider *myEvtRegistrar;

    // -- Create an instance of IWbemDecoupledEventProvider
    hr = CoCreateInstance(CLSID_WbemDecoupledBasicEventProvider,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledBasicEventProvider,
                          (void**)&myEvtRegistrar);

    if (SUCCEEDED(hr))
    {
       // -- Register the DecoupledEventProvider
       hr = myEvtRegistrar->Register(0,
                                     NULL,
                                     NULL,
                                     L"root\\cimv2",
                                     L"DecoupledEventProvider",
                                     NULL, NULL);
       if (SUCCEEDED(hr))
       {
          IWbemServices *pService = NULL;
          hr = myEvtRegistrar->GetService (0, NULL, &pService);
          if (SUCCEEDED(hr))
          {
             IWbemObjectSink *pSink = NULL;
             hr = myEvtRegistrar->GetSink ( 0, NULL, &pSink );
             if (SUCCEEDED(hr))
             {
                // Provide events
             }
          }
       } 
    }
    ```

    

5.  對提供者功能所需的 [WMI 進行呼叫](making-calls-to-wmi.md) 。 如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。 如需提供者服務腳本或應用程式的資料要求的詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。

在終止之前，應用程式必須先清除。 下列程式說明如何取消註冊低耦合提供者，讓 WMI 不會嘗試查詢資訊。

下列程式說明如何取消註冊低耦合提供者。

**取消註冊低耦合提供者**

1.  取消註冊並釋放註冊機構。

    下列程式碼範例示範如何取消註冊和釋放註冊機構。

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  取消註冊並釋放事件提供者。

    下列程式碼範例示範如何取消登錄和釋放事件提供者。

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  清除 COM 伺服器。

    下列程式碼範例示範如何將 COM 程式庫解除初始化。

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[保護您的提供者](securing-your-provider.md)
</dt> <dt>

[開發 WMI 提供者](developing-a-wmi-provider.md)
</dt> </dl>

 

 



