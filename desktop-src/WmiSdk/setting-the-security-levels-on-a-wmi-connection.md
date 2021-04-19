---
description: 取得 IWbemServices proxy 的指標之後，您必須將 proxy 上的安全性設定為透過 proxy 存取 WMI。
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: 設定 WMI 連接的安全性層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc58b4bbbe1a01d927d8f5977c21003cdae2e315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998336"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a><span data-ttu-id="edc9c-103">設定 WMI 連接的安全性層級</span><span class="sxs-lookup"><span data-stu-id="edc9c-103">Setting the Security Levels on a WMI Connection</span></span>

<span data-ttu-id="edc9c-104">取得 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy 的指標之後，您必須將 proxy 上的安全性設定為透過 PROXY 存取 WMI。</span><span class="sxs-lookup"><span data-stu-id="edc9c-104">After you retrieve a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI through the proxy.</span></span> <span data-ttu-id="edc9c-105">您必須設定安全性，因為 **IWbemServices** proxy 會授與跨進程物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="edc9c-105">You must set the security because the **IWbemServices** proxy grants access to an out-of-process object.</span></span> <span data-ttu-id="edc9c-106">一般而言，如果您未設定適當的安全性屬性，則 COM 安全性不允許一個進程存取另一個進程。</span><span class="sxs-lookup"><span data-stu-id="edc9c-106">In general, COM security does not allow one process to access another process if you do not set the proper security properties.</span></span> <span data-ttu-id="edc9c-107">如需詳細資訊，請參閱 [在 IWbemServices 和其他 proxy 上設定安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。</span><span class="sxs-lookup"><span data-stu-id="edc9c-107">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span> <span data-ttu-id="edc9c-108">連接不同的作業系統需要不同層級的驗證和模擬。</span><span class="sxs-lookup"><span data-stu-id="edc9c-108">Connections to different operating systems require varying levels of authentication and impersonation.</span></span> <span data-ttu-id="edc9c-109">如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="edc9c-109">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="edc9c-110">本主題中的程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="edc9c-110">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="edc9c-111">下列程式描述如何設定 WMI 連接的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="edc9c-111">The following procedure describes how to set the security levels on a WMI connection.</span></span>

<span data-ttu-id="edc9c-112">**設定 WMI 連接的安全性層級**</span><span class="sxs-lookup"><span data-stu-id="edc9c-112">**To set the security levels on a WMI connection**</span></span>

-   <span data-ttu-id="edc9c-113">使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)的呼叫，設定 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy 上的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="edc9c-113">Set the security levels on the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="edc9c-114">下列程式碼範例說明呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)的常見方式。</span><span class="sxs-lookup"><span data-stu-id="edc9c-114">The following code example describes a common way of calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

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

    

<span data-ttu-id="edc9c-115">設定 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標的安全性層級之後，您就可以存取 WMI 的各種功能。</span><span class="sxs-lookup"><span data-stu-id="edc9c-115">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="edc9c-116">使用 WMI 完成後，您必須關閉應用程式。</span><span class="sxs-lookup"><span data-stu-id="edc9c-116">After you finish using WMI, you must shut down your application.</span></span> <span data-ttu-id="edc9c-117">如需詳細資訊，請參閱 [清除和關閉 WMI 應用程式](cleaning-up-and-shutting-down-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="edc9c-117">For more information, see [Cleaning up and Shutting Down a WMI Application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

 

 
