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
# <a name="connecting-to-the-bits-service"></a><span data-ttu-id="b57f7-103">連接到 BITS 服務</span><span class="sxs-lookup"><span data-stu-id="b57f7-103">Connecting to the BITS Service</span></span>

<span data-ttu-id="b57f7-104">若要連接到 BITS 系統服務，請建立 BackgroundCopyManager 物件的實例，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="b57f7-104">To connect to the BITS system service, create an instance of the BackgroundCopyManager object as shown in the following example.</span></span> <span data-ttu-id="b57f7-105">BITS 系統服務是在用戶端電腦上執行的 Windows 系統服務，該服務會在執行背景傳輸功能的用戶端電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="b57f7-105">The BITS system service is the Windows system service running on the client computer that implements the background transfer capability.</span></span>


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



<span data-ttu-id="b57f7-106">若要測試特定版本的位，請根據您想要檢查的版本，使用 BackgroundCopyManager 的符號類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="b57f7-106">To test for a specific version of BITS, use a symbolic class identifier for the BackgroundCopyManager based on the version you want to check.</span></span> <span data-ttu-id="b57f7-107">例如，若要測試 BITS 10.2，請使用 CLSID \_ BackgroundCopyManager10 \_ 2。</span><span class="sxs-lookup"><span data-stu-id="b57f7-107">For example, to test for BITS 10.2, use CLSID\_BackgroundCopyManager10\_2.</span></span>

<span data-ttu-id="b57f7-108">下列範例顯示如何使用其中一個符號類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="b57f7-108">The following example shows how to use one of the symbolic class identifiers.</span></span>


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



<span data-ttu-id="b57f7-109">使用 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) 介面的方法來 [建立傳送作業](creating-a-job.md)、列舉佇列中的 [作業](enumerating-jobs-in-the-transfer-queue.md) ，以及抓取 [工作](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob)。</span><span class="sxs-lookup"><span data-stu-id="b57f7-109">Use the methods of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to [create transfer jobs](creating-a-job.md), [enumerate jobs](enumerating-jobs-in-the-transfer-queue.md) in the queue, and [retrieve jobs](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span>



<span data-ttu-id="b57f7-110">BITS 要求用戶端的介面 proxy 必須使用識別或模擬層級的模擬。</span><span class="sxs-lookup"><span data-stu-id="b57f7-110">BITS requires that the client's interface proxies use either the IDENTIFY or IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="b57f7-111">如果應用程式未呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)，COM 會依預設使用 [識別]。</span><span class="sxs-lookup"><span data-stu-id="b57f7-111">If the application does not call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), COM uses IDENTIFY by default.</span></span> <span data-ttu-id="b57f7-112">如果未設定正確的模擬等級，則 BITS 會失敗，並出現 E \_ ACCESSDENIED。</span><span class="sxs-lookup"><span data-stu-id="b57f7-112">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span> <span data-ttu-id="b57f7-113">如果您提供的程式庫會演練 BITS 介面，而呼叫您程式庫的應用程式會設定以下的模擬層級，則您必須呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 來為您呼叫的每個 BITS 介面設定正確的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="b57f7-113">If you provide a library that exercises the BITS interfaces, and an application that calls your library sets the impersonation level below IDENTIFY, then you will need to call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to set the correct impersonation level for each BITS interface that you call.</span></span>

<span data-ttu-id="b57f7-114">在您的應用程式結束之前，請釋放 [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) 介面指標的複本，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="b57f7-114">Before your application exits, release your copy of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer, as shown in the following example.</span></span>


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a><span data-ttu-id="b57f7-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="b57f7-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b57f7-116">[從 .net 和 c #](/windows/desktop/Bits/bits-dot-net) 對 bits 進行 Bits 的呼叫</span><span class="sxs-lookup"><span data-stu-id="b57f7-116">[Calling into BITS from .NET and C#](/windows/desktop/Bits/bits-dot-net) for BITS</span></span>
</dt> </dl>

 

 