---
title: 連接到 BITS 服務
description: 若要連接到 BITS 服務，請建立 BackgroundCopyManager 物件的實例，如下列範例所示。
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8146fa0def8c9c7dfd976784a930f35f20c965eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092842"
---
# <a name="connecting-to-the-bits-service"></a>連接到 BITS 服務

若要連接到 BITS 系統服務，請建立 BackgroundCopyManager 物件的實例，如下列範例所示。 BITS 系統服務是在用戶端電腦上執行的 Windows 系統服務，該服務會在執行背景傳輸功能的用戶端電腦上執行。


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>

//Global variable that several of the code examples in this document reference.
IBackgroundCopyManager* g_pbcm = NULL;  
HRESULT hr;

//Specify the appropriate COM threading model for your application.
hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
  hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                        CLSCTX_LOCAL_SERVER,
                        __uuidof(IBackgroundCopyManager),
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //Use g_pbcm to create, enumerate, or retrieve jobs from the queue.
  }
}
```



若要測試特定版本的位，請根據您想要檢查的版本，使用 BackgroundCopyManager 的符號類別識別碼。 例如，若要測試 BITS 10.2，請使用 CLSID \_ BackgroundCopyManager10 \_ 2。

下列範例顯示如何使用其中一個符號類別識別碼。


```C++
  hr = CoCreateInstance(CLSID_BackgroundCopyManager5_0, NULL,
                        CLSCTX_LOCAL_SERVER,
                        IID_IBackgroundCopyManager,
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //BITS 5.0 is installed.
  }
```



使用 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) 介面的方法來 [建立傳送作業](creating-a-job.md)、列舉佇列中的 [作業](enumerating-jobs-in-the-transfer-queue.md) ，以及抓取 [工作](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob)。



BITS 要求用戶端的介面 proxy 必須使用識別或模擬層級的模擬。 如果應用程式未呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)，COM 會依預設使用 [識別]。 如果未設定正確的模擬等級，則 BITS 會失敗，並出現 E \_ ACCESSDENIED。 如果您提供的程式庫會演練 BITS 介面，而呼叫您程式庫的應用程式會設定以下的模擬層級，則您必須呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 來為您呼叫的每個 BITS 介面設定正確的模擬層級。

在您的應用程式結束之前，請釋放 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) 介面指標的複本，如下列範例所示。


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[從 .net 和 c #](/windows/desktop/Bits/bits-dot-net) 對 bits 進行 Bits 的呼叫
</dt> </dl>

 

 