---
description: 設定 IWbemServices 指標的安全性層級之後，您就可以存取 WMI 的各種功能。 使用 WMI 完成後，您必須關閉應用程式。
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: 清除和關閉 WMI 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7758cbdba81e018ff3362cec86aa5096838dc9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944719"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a><span data-ttu-id="d87bb-104">清除和關閉 WMI 應用程式</span><span class="sxs-lookup"><span data-stu-id="d87bb-104">Cleaning up and Shutting Down a WMI Application</span></span>

<span data-ttu-id="d87bb-105">設定 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標的安全性層級之後，您就可以存取 WMI 的各種功能。</span><span class="sxs-lookup"><span data-stu-id="d87bb-105">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="d87bb-106">使用 WMI 完成後，您必須關閉應用程式。</span><span class="sxs-lookup"><span data-stu-id="d87bb-106">After you finish using WMI, you must shut down your application.</span></span>

<span data-ttu-id="d87bb-107">下列程式說明如何清除和關閉 WMI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d87bb-107">The following procedure describes how to clean up and shut down a WMI application.</span></span>

<span data-ttu-id="d87bb-108">**清除和關閉 WMI 應用程式**</span><span class="sxs-lookup"><span data-stu-id="d87bb-108">**To clean up and shut down a WMI application**</span></span>

1.  <span data-ttu-id="d87bb-109">釋放任何開啟的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="d87bb-109">Release any open COM interfaces.</span></span>

    <span data-ttu-id="d87bb-110">您必須記得發行的兩個主要介面是 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 和 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)。</span><span class="sxs-lookup"><span data-stu-id="d87bb-110">The two primary interfaces you must remember to release are [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) and [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

2.  <span data-ttu-id="d87bb-111">呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)。</span><span class="sxs-lookup"><span data-stu-id="d87bb-111">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

    <span data-ttu-id="d87bb-112">和所有 COM 應用程式一樣，您必須在應用程式結束時呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 。</span><span class="sxs-lookup"><span data-stu-id="d87bb-112">As with all COM applications, you must call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) at the end of your application.</span></span>

3.  <span data-ttu-id="d87bb-113">結束您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d87bb-113">Exit your application.</span></span>

    <span data-ttu-id="d87bb-114">下列程式碼範例顯示如何結束 WMI 用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="d87bb-114">The following code example shows how to exit a WMI client application.</span></span>

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > <span data-ttu-id="d87bb-115">`pSvc`變數的類型是 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* ，qps-ploc 變數的類型為 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* 。</span><span class="sxs-lookup"><span data-stu-id="d87bb-115">The `pSvc` variable is of type [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)\*, and the pLoc variable is of type [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)\*.</span></span>

     

<span data-ttu-id="d87bb-116">您現在已成功初始化 COM、存取 WMI，並結束您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d87bb-116">You have now successfully initialized COM, accessed WMI, and exited your application.</span></span> <span data-ttu-id="d87bb-117">如需詳細資訊，請參閱 [範例：建立 WMI 應用程式](example-creating-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="d87bb-117">For more information, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d87bb-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="d87bb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d87bb-119">使用 c + + 建立 WMI 應用程式</span><span class="sxs-lookup"><span data-stu-id="d87bb-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
