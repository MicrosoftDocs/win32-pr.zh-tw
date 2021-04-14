---
description: 設定 COM 的標準呼叫之後，您必須透過呼叫 IWbemLocator：： ConnectServer 方法來連接到 WMI。
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: 建立與 WMI 命名空間的連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce0e1caeef15709742704570c008012feeaf8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469457"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a><span data-ttu-id="af2f3-103">建立與 WMI 命名空間的連接</span><span class="sxs-lookup"><span data-stu-id="af2f3-103">Creating a Connection to a WMI Namespace</span></span>

<span data-ttu-id="af2f3-104">設定 COM 的標準呼叫之後，您必須透過呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 方法來連接到 WMI。</span><span class="sxs-lookup"><span data-stu-id="af2f3-104">After you have set the standard calls to COM, you must then connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span> <span data-ttu-id="af2f3-105">**ConnectServer** 方法會傳回 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面的 proxy。</span><span class="sxs-lookup"><span data-stu-id="af2f3-105">The **ConnectServer** method returns a proxy of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span> <span data-ttu-id="af2f3-106">您可以透過 **IWbemServices** 存取 WMI 的不同功能。</span><span class="sxs-lookup"><span data-stu-id="af2f3-106">Through **IWbemServices**, you can access the different capabilities of WMI.</span></span>

<span data-ttu-id="af2f3-107">本主題中的程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="af2f3-107">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="af2f3-108">下列程式說明如何建立與 WMI 命名空間的連接。</span><span class="sxs-lookup"><span data-stu-id="af2f3-108">The following procedure describes how to create a connection to a WMI namespace.</span></span>

<span data-ttu-id="af2f3-109">**建立與 WMI 命名空間的連接**</span><span class="sxs-lookup"><span data-stu-id="af2f3-109">**To create a connection to a WMI namespace**</span></span>

-   <span data-ttu-id="af2f3-110">透過對 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的呼叫來初始化 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)介面。</span><span class="sxs-lookup"><span data-stu-id="af2f3-110">Initialize the [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) interface through a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="af2f3-111">WMI 不需要您在 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)上呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)時執行任何額外的程式。</span><span class="sxs-lookup"><span data-stu-id="af2f3-111">WMI does not require that you perform any additional procedures when calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

    <span data-ttu-id="af2f3-112">下列程式碼範例說明如何初始化 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)。</span><span class="sxs-lookup"><span data-stu-id="af2f3-112">The following code example describes how to initialize [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

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

    

    -   <span data-ttu-id="af2f3-113">透過呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 方法連接至 WMI。</span><span class="sxs-lookup"><span data-stu-id="af2f3-113">Connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span>

        <span data-ttu-id="af2f3-114">[**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)方法會將 proxy 傳回給 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面，這個介面是用來存取您對 **ConnectServer** 呼叫中指定的本機或遠端 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="af2f3-114">The [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method returns a proxy to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface that use to access the local or remote WMI namespace specified in your call to **ConnectServer**.</span></span>

        <span data-ttu-id="af2f3-115">下列程式碼範例說明如何呼叫 [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)。</span><span class="sxs-lookup"><span data-stu-id="af2f3-115">The following code example describes how to call [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

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

        

<span data-ttu-id="af2f3-116">當您收到 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy 的指標之後，您必須在 proxy 上設定安全性以存取 WMI。</span><span class="sxs-lookup"><span data-stu-id="af2f3-116">After you have received a pointer to the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI.</span></span> <span data-ttu-id="af2f3-117">如需詳細資訊，請參閱 [設定 WMI 連接的安全性層級](setting-the-security-levels-on-a-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="af2f3-117">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af2f3-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="af2f3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af2f3-119">使用 c + + 建立 WMI 應用程式</span><span class="sxs-lookup"><span data-stu-id="af2f3-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="af2f3-120">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="af2f3-120">IPv6 and IPv4 Support in WMI</span></span>](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
