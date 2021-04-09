---
description: 連接到 WMI 的第一個步驟是設定 CoInitializeEx 和 CoInitializeSecurity 的 COM 呼叫。
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: 初始化 WMI 應用程式的 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6c2e590ddb64914f5aab723a56dee2385a49bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945293"
---
# <a name="initializing-com-for-a-wmi-application"></a><span data-ttu-id="f2b3b-103">初始化 WMI 應用程式的 COM</span><span class="sxs-lookup"><span data-stu-id="f2b3b-103">Initializing COM for a WMI Application</span></span>

<span data-ttu-id="f2b3b-104">連接到 WMI 的第一個步驟是設定 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的 COM 呼叫。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-104">The first step in connecting to WMI is setting up the COM calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="f2b3b-105">本主題中的程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-105">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="f2b3b-106">下列程式描述如何從用戶端應用程式初始化 COM。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-106">The following procedure describes how to initialize COM from a client application.</span></span>

<span data-ttu-id="f2b3b-107">**從用戶端應用程式初始化 COM**</span><span class="sxs-lookup"><span data-stu-id="f2b3b-107">**To initialize COM from a client application**</span></span>

1.  <span data-ttu-id="f2b3b-108">使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)的呼叫初始化 COM。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-108">Initialize COM with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="f2b3b-109">呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 是設定 COM 介面的標準程式。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-109">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) is a standard procedure for setting up a COM interface.</span></span> <span data-ttu-id="f2b3b-110">因此，在呼叫 **CoInitializeEx** 時，WMI 不需要您觀察任何額外的程式。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-110">Therefore, WMI does not require that you observe any additional procedures when calling **CoInitializeEx**.</span></span> <span data-ttu-id="f2b3b-111">如需詳細資訊，請參閱 [COM](../com/component-object-model--com--portal.md)。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-111">For more information, see [COM](../com/component-object-model--com--portal.md).</span></span>

    <span data-ttu-id="f2b3b-112">下列程式碼範例說明如何呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-112">The following code example describes how to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  <span data-ttu-id="f2b3b-113">使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 介面的呼叫來設定一般 COM 安全性層級。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-113">Set the general COM security levels with a call to the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interface.</span></span>

    <span data-ttu-id="f2b3b-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 是一種標準函式，您必須在設定進程的 COM 介面時呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a standard function you must call when setting up a COM interface for a process.</span></span> <span data-ttu-id="f2b3b-115">如果您想要針對整個進程設定驗證、模擬或驗證服務的預設安全性設定，請呼叫 **CoInitializeSecurity** 。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-115">Call **CoInitializeSecurity** if you want to set the default security settings for authentication, impersonation, or authentication service for an entire process.</span></span> <span data-ttu-id="f2b3b-116">如需詳細資訊，請參閱 [設定用戶端應用程式處理安全性](setting-client-application-process-security.md)。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-116">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="f2b3b-117">如果您想要設定或變更特定 proxy 的安全性，則必須呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-117">If you want to set or change the security for a specific proxy, you must call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="f2b3b-118">當您在無法控制驗證、模擬或驗證服務之預設安全性設定的另一個進程中執行時，每次必須設定或變更 COM 安全性時，請使用 **CoSetProxyBlanket** 。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-118">Use **CoSetProxyBlanket** whenever you must set or change COM security when running inside another process where you cannot control the default security settings for authentication, impersonation, or authentication service.</span></span> <span data-ttu-id="f2b3b-119">如需詳細資訊，請參閱 [設定 WMI 連接的安全性層級](setting-the-security-levels-on-a-wmi-connection.md) 和 [設定 IWbemServices 和其他 proxy 的安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md) and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

    <span data-ttu-id="f2b3b-120">當您設計 WMI 用戶端應用程式時，WMI 有幾個您應該注意的安全性問題。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-120">WMI has several security issues you should be aware of when programming a WMI client application.</span></span> <span data-ttu-id="f2b3b-121">如需詳細資訊，請參閱 [設定用戶端應用程式處理安全性](setting-client-application-process-security.md)。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span>

    <span data-ttu-id="f2b3b-122">下列程式碼範例描述如何呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 來設定進程的 COM 安全性。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-122">The following code example describes how to call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set COM security on the process.</span></span>

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

    

<span data-ttu-id="f2b3b-123">在您初始化 COM 之後，下一步就是建立與 WMI 命名空間的連接。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-123">After you initialize COM, your next step is to create a connection to a WMI namespace.</span></span> <span data-ttu-id="f2b3b-124">如需詳細資訊，請參閱 [建立與 WMI 命名空間的連接](creating-a-connection-to-a-wmi-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="f2b3b-124">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2b3b-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2b3b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2b3b-126">使用 c + + 建立 WMI 應用程式</span><span class="sxs-lookup"><span data-stu-id="f2b3b-126">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="f2b3b-127">存取 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="f2b3b-127">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
